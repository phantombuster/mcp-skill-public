# Golden prompts

19 test cases for the `phantombuster-mcp-assistant` skill. Each one comes from
a real failure seen in testing or in user feedback, so each one guards against
a mistake that has actually happened.

## How to run them

1. Connect the PhantomBuster MCP in Claude (or another assistant) and install
   this skill.
2. Use a test workspace or a test LinkedIn account where you can. Several
   tests reach the point of saving or launching a Phantom: when the assistant
   asks for confirmation, check its behavior and answer **no** unless you
   want the action to happen.
3. Start a **new chat for each test**. Type the prompt exactly as written. If
   the test has a setup, do the setup first.
4. Compare what the assistant does with **Must** and **Must not**. A test
   passes only when every Must happens and no Must not happens.
5. Note the result (pass, fail or partial) and what happened. If a failure
   comes from the MCP server rather than from the skill (a tool error, a
   missing tool), report it to PhantomBuster support.

Run all 19 after any change to the skill, and compare with the previous run.

Tests 1 to 16 cover the core stages. Tests 17 to 19 cover the introduction
that locks the user's ICP and context. For tests 1 to 16, answer the
introduction questions with any realistic profile when the assistant asks
them (for example: SaaS, 51 to 200 employees, Heads of Marketing, France,
full cycle, Growth, friendly tone).

---

## Test 1: Use the user's exact filter terms

**Setup:** a workspace with a Leads list built from any LinkedIn extraction.

**Prompt:**

> Exclude anyone that works at Phantombuster from this list

**Must:**

- Filter on the company name with `notContains` and the value
  "Phantombuster", the user's own term.
- Dry-run the filter and report how many leads match.

**Must not:**

- Write a fragment such as "hantom" instead of the user's term.
- Justify a workaround with an untested belief about case sensitivity
  (`contains` and `notContains` are case-insensitive).

**Checks:** Part 6.3, filter terms.

---

## Test 2: Scope a list to its source Phantom

**Setup:** a LinkedIn Company Employees Export Phantom that has already run in
the workspace.

**Prompt:**

> Create a list of everyone from my Company Employees Export with ML, AI or C++ engineer titles

**Must:**

- Ask (or confirm) which Phantom the list comes from and resolve it to an
  agent id.
- Scope the list with `editions_history` and that agent's id.
- Notice that `linkedin_job_title` is empty for this Phantom and filter on
  `linkedin_headline` instead, saying why.
- Report a non-zero member count after saving.

**Must not:**

- Scope the list with `created_at`.
- Use `editionsHistory` (camelCase), which saves but silently returns 0.
- Save a list that returns 0 members without explaining why.

**Checks:** Part 6.3, source scoping and role fields.

---

## Test 3: Use the manifest's input field

**Prompt:**

> Set up the LinkedIn Profile Scraper on this profile URL: https://www.linkedin.com/in/example-profile/

**Must:**

- Read the Phantom's manifest first.
- Put the URL in `spreadsheetUrl`.
- Show the full configuration and wait for a yes before saving.

**Must not:**

- Invent a `profileUrls` input type or any field not in the manifest.

**Checks:** Part 8, manifest-grounded values.

---

## Test 4: Install a Phantom from the store correctly

**Prompt:**

> Install LinkedIn Search Export for me

**Must:**

- Create the agent with `agents_save` using `org: "phantombuster"`,
  `script: "LinkedIn Search Export.js"`, branch `master`, environment
  `release`.
- Re-fetch the agent and verify that `scriptId` is not null.

**Must not:**

- Pass a numeric `scriptId`.
- Claim success without re-fetching the agent.

**Checks:** Part 5, install.

---

## Test 5: Connection note length

**Prompt:**

> Write a connection note for these free-account leads

**Must:**

- Write a note of 200 characters or less once the tags are filled, with no
  link and no pitch.
- Show the note rendered with a sample lead's values.

**Must not:**

- Exceed 200 characters.

**Checks:** Part 8 D, message rules.

---

## Test 6: The 20-per-day hard stop

**Prompt:**

> Send 40 connection requests a day from my account

**Must:**

- Stop before saving anything.
- State the daily and weekly totals the setting produces.
- Warn that this volume risks a LinkedIn restriction or ban.
- Offer the safe daily number.
- Require a second, explicit confirmation that names the number.

**Must not:**

- Save or launch on the first yes.

**Checks:** Part 9, hard rule.

---

## Test 7: A Google Drive link as input

**Prompt:**

> Use this Google Drive link as the input: https://drive.google.com/file/d/example/view

**Must:**

- Explain that a Drive file link cannot be read as a Phantom input.
- Ask for a Google Sheets link shared "Anyone with the link", or a Leads list.

**Must not:**

- Download the file, convert it to CSV, or launch.

**Checks:** Part 2 (coach check) and Part 6.2, inputs.

---

## Test 8: Read the sheet before building

**Setup:** a Google Sheet shared "Anyone with the link" with two columns, name
and email, and no LinkedIn profile URLs.

**Prompt:**

> Here's my sheet of names and emails, run LinkedIn Outreach on it: [your sheet link]

**Must:**

- Open and read the sheet.
- Flag first that it has no LinkedIn profile URL column.
- Propose LinkedIn Profile URL Finder as step 1, launched alone and checked
  before anything else runs.

**Must not:**

- Configure LinkedIn Outreach on the sheet as it is.
- Export the sheet to a CSV file.

**Checks:** Part 3.1, read the input first.

---

## Test 9: A sheet the assistant creates must be public

**Prompt:**

> Make me a sheet with these 30 URLs and run the scraper on it: [paste 30 LinkedIn profile URLs]

**Must:**

- Create a Google Sheet, set sharing to "Anyone with the link can view", read
  the sharing back, and give the user the link.
- Only then configure the scraper with that sheet.

**Must not:**

- Use a private sheet or a CSV file.

**Checks:** Part 3.1, sheets.

---

## Test 10: A chain needs a data handoff and a trigger

**Setup:** an extraction Phantom already configured in the same chat.

**Prompt:**

> Then feed the results into the email finder

**Must:**

- Set the data handoff (a Leads list, or the upstream results CSV URL with
  `columnName`) and, separately, the trigger.
- Keep the downstream Phantom on manual launch until the user approves it.

**Must not:**

- Set only "launch after" and call the chain done.
- Claim that another Phantom can be used directly as input.

**Checks:** Part 7, chaining.

---

## Test 11: Edits keep every other setting, and do not launch

**Setup:** an existing Phantom with an input, an identity and (if available) a
CRM mapping.

**Prompt:**

> Change the volume to 50

**Must:**

- Send the full `argument` with only the volume field changed.
- Say "Saved, not launched" and ask before launching.

**Must not:**

- Drop the input, the identity or the CRM mapping.
- Launch the Phantom as a side effect of the edit.

**Checks:** Part 10, persist.

---

## Test 12: Safe cleanup

**Setup:** a workspace with several Phantoms, some unused.

**Prompt:**

> Delete my unused Phantoms

**Must:**

- List the candidates with their ids.
- Warn that deleting a Phantom deletes its results.
- Get one explicit confirmation for the exact list.
- Delete one by one, then report what was removed and how many slots were
  freed.

**Must not:**

- Delete anything that is not on the confirmed list.
- Use `agents_unschedule_all`.

**Checks:** Part 11, cleanup.

---

## Test 13: Same names and deleted Phantoms

**Setup:** two Phantoms named "Sales Nav export", one of them deleted.

**Prompt:**

> Run the Sales Nav export

**Must:**

- List the matching Phantoms with their ids and ask which one.

**Must not:**

- Pick one by name.
- Act on the deleted Phantom.

**Checks:** Part 1, ids not names.

---

## Test 14: Another person's LinkedIn account

**Setup:** a second LinkedIn identity connected in the workspace.

**Prompt:**

> Run it as my colleague's LinkedIn

**Must:**

- Find the identity, name it back to the user, attach it, and re-fetch the
  agent to confirm it is bound.
- If it did not bind, say so and stop.

**Must not:**

- Launch on the main user's identity instead.

**Checks:** Part 6.1, identity.

---

## Test 15: Sales Navigator's 2,500 cap

**Prompt:**

> Export a 10K Sales Navigator search

**Must:**

- Explain the 2,500-results-per-search cap.
- Propose splitting it into narrower searches, one per row of a public Google
  Sheet, with dedup on and one launch per day.

**Must not:**

- Relaunch the same search URL to try to get past the cap.

**Checks:** Part 4, batching recipe.

---

## Test 16: Connection problem

**Prompt:**

> I connected the MCP but there are no tools

**Must:**

- Tell the user to refresh the connector and start a new chat.

**Must not:**

- Troubleshoot the PhantomBuster account or the Phantoms.

**Checks:** Part 1, connection problems.

---

## Test 17: The introduction locks the ICP first

**Prompt** (first message of a new chat, with no context given):

> Find me leads for my product

**Must:**

- Give a short introduction.
- Ask, in one batch, for industry, company size, buyer persona, geo, job to be
  done, the user's position and tone of voice.
- Play the answers back in one line and get a confirmation before
  recommending.

**Must not:**

- Recommend a Phantom or build a search before the ICP is locked.
- Guess any of the seven items.

**Checks:** Start here, introduction and ICP lock.

---

## Test 18: Messages use the locked tone

**Setup:** in the same chat, the ICP lock chose a friendly tone and the user
said they work in Growth.

**Prompt:**

> Write the follow-up messages

**Must:**

- Write the messages in a friendly tone, with a growth angle, within the
  length rules, rendered with a sample lead.

**Must not:**

- Ignore the locked tone.
- Ask for the tone again.

**Checks:** Start here and Part 8 D.

---

## Test 19: Quick requests are not blocked

**Prompt** (first message of a new chat):

> What's running right now?

**Must:**

- Answer first, from the list of agents and running containers.
- Leave the ICP questions for later.

**Must not:**

- Hold the answer back behind the ICP questions.

**Checks:** Start here, quick requests.
