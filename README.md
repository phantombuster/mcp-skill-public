# PhantomBuster MCP Assistant: a Claude skill

A skill that turns Claude into a PhantomBuster operator. You describe a goal in
plain language ("reach the CTOs who commented on my competitor's post"), and
the skill takes Claude from that goal to a correctly configured, safely
launched Phantom or chain of Phantoms, through the PhantomBuster MCP.

It coaches as it goes: it flags plans that are risky, wasteful or unlikely to
convert, and proposes the better way. It never launches without your go-ahead.

## What it does

Every conversation starts with a short introduction. If you have not described
your ideal customer yet, Claude asks one batch of questions to lock your ICP and
context: industry, company size, buyer persona, geography, job to be done
(extract, enrich, engage, or full cycle), your position, and the tone of voice
for any message it writes. Quick requests, like "what's running right now?",
are answered straight away.

Then it walks every request through 11 stages, each with a clear "done when"
check:

1. **Intake**: platform, the input you already have, outcome, ICP, account
   type and weekly volume goal. Claude reads any sheet or link you give it, and
   matches your request to a real use case so it can tell you up front what
   works today.
2. **Coach check**: compares your plan with proven chains and catches about 40
   common mistakes (cold lists when a warm source exists, messaging people who
   are not connections, notes over 200 characters, a chain with a trigger but
   no data handoff, and more).
3. **Recommend**: the right Phantom or workflow, from the Phantom Database and
   the workflow library.
4. **Install**: creates the Phantom from the store and checks it worked.
5. **Identity**: confirms which LinkedIn (or other) account the Phantom runs as.
6. **Input and lists**: sets the input, and builds lead lists from a filter,
   with a dry run and a member count.
7. **Chain**: connects steps with both a data handoff and a trigger, and keeps
   later steps manual until you approve them.
8. **Interview**: schedule, volume worked back from your weekly goal, behavior
   and output settings, and message copy, all from the Phantom's real settings.
9. **Name**: offers to rename every Phantom.
10. **Confirm and launch**: shows the full setup, then launches one step at a
    time, each with its own yes.
11. **Report**: reports from a fresh read of your workspace, plus the metrics
    to watch.

## Install

You need:

- **Claude** with skills enabled.
- **The PhantomBuster MCP connected** in Claude, as a connector with the URL
  `https://mcp.phantombuster.com`. The skill gives Claude the know-how; the MCP
  gives it the tools. Without the MCP, the skill cannot act on your workspace.

Then:

1. Download `phantombuster-mcp-assistant.zip` from this repository (or zip the
   `phantombuster-mcp-assistant` folder yourself).
2. In Claude, open **Settings**, go to the skills section (Settings, then
   Customize, then Skills, depending on your app), and **upload** the zip.
3. Start a new chat and describe what you want to do.

If Claude says it has no PhantomBuster tools right after you connect, refresh
the connector and start a new chat.

## Folder layout

```
phantombuster-mcp-assistant/
  SKILL.md                          the skill
  references/
    use-cases.md                    23 real use cases and their MCP status
    workflow-library.md             54 proven Phantom chains
    phantom-catalog.md              snapshot of the Phantom Database (145 Phantoms)
    golden-prompts.md               19 test cases
    changelog.md                    what changed in each version
```

Everything the skill needs is inside this folder. It does not depend on any
private page.

## Knowledge sources

- **The Phantom Database**: every Released and Beta Phantom, what it does, its
  input and its link. Claude reads the live public database first:
  https://thephantomcompany.notion.site/d22ab00a50994f078509e07b416c356a?v=f1c1b6f00fe6430aa4204ffee45b8bdc
  and falls back to the bundled snapshot (`references/phantom-catalog.md`,
  145 Phantoms, 9 October 2026).
- **The workflow library (54 chains)**: proven Phantom chains, each with its
  outcome, the audience temperature (warm, lukewarm, cold) and the setup level.
  Used by the coach check, the recommendations and the chaining stage.
- **Real use cases (23)**: requests PhantomBuster users raised in live MCP
  sessions, each with what the MCP supports today. Used at intake so Claude
  never promises more than the MCP can do.
- **PhantomBuster playbooks (14 chains)**: the proven plays published at
  https://phantombuster.com/playbooks/, each linked from the skill.
- **The PhantomBuster blog**: safe limits, connection notes, follow-up
  sequences, warm-up and enrichment. Each post used is linked from the skill.
- **The PhantomBuster Help Center**: rate limits by platform and Phantom,
  scheduling, watcher mode, inputs, results files, duplicates, placeholder tags
  and error fixes. Each article used is linked from the skill.

Rate limits follow the Help Center's per-platform, per-account-type ceilings,
counted per account across all Phantoms. When two sources give different
numbers, the most conservative one wins. Above 20 connection requests or
messages a day, Claude stops and asks for a second, explicit confirmation.

## Test it with the golden prompts

`references/golden-prompts.md` holds 19 tests, each drawn from a real failure.
Each test gives the exact prompt to type, any setup needed, what Claude must
do, and what it must not do.

1. Install the skill and connect the PhantomBuster MCP. Use a test workspace
   or test account where you can.
2. Open a new chat for each test and type the prompt exactly as written.
3. When Claude asks to save or launch something, check its behavior, then
   answer no unless you want the action to happen.
4. A test passes only when every "Must" happens and no "Must not" happens.
   Note the result of each test.
5. If a failure comes from the MCP server itself (a tool error or a missing
   tool), report it to PhantomBuster support.

Run all 19 again whenever you change the skill, and compare the results.

## Feedback

Questions, bugs or ideas: contact PhantomBuster support from your
PhantomBuster account.
