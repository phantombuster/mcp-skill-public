# Changelog

## 2.2 (9 October 2026)

- **Fallback account when LinkedIn disconnects** (Part 6.1, error table).
  When a run fails because the account is disconnected, the skill stops, lists
  the other accounts connected to the workspace and always asks the user to
  switch to one of them (or reconnect). It never switches on its own, and it
  re-checks the safety limits for the new account before relaunching.
- **Scoring preview before scaling** (Part 10). AI scoring runs first on 10
  leads; the skill shows the scored leads in the chat once (score, reason and
  a summary), waits for the user to validate or adjust, then scores every lead
  in the list.

## 2.1, public edition (9 October 2026)

First public release of the skill, for every PhantomBuster user.

- **Self-contained.** Everything the skill relies on now ships inside its
  folder, so it works without access to any private page:
  - `references/use-cases.md`: 23 real user requests with their MCP status,
    read at Intake and before promising anything.
  - `references/workflow-library.md`: 54 proven Phantom chains with outcome,
    temperature and level, read at the coach check, Recommend and Chain stages.
  - `references/phantom-catalog.md`: refreshed snapshot of the public Phantom
    Database (145 Released and Beta Phantoms), the fallback when the live
    database cannot be read.
  - `references/golden-prompts.md`: all 19 test cases written out in full
    (prompt, setup, what must and must not happen) so anyone can run them.
- Rate limits: when sources disagree, the most conservative number wins.
- Same behavior as 2.1: introduction and ICP lock, 11 stages, coach check,
  launch interview, rate limits and every 2.0 fix.

## 2.1 (8 October 2026)

- **Introduction and ICP lock** (stage 0): a short introduction, then one batch
  of questions to lock industry, company size, buyer persona, geo, job to be
  done, the user's position and tone of voice. The answers are played back for
  confirmation and reused in intake, recommendations, list filters and
  messages. Quick requests (status, results, errors, connection problems) are
  not blocked.
- Messages are written in the locked tone of voice and from the user's
  position.
- Every source is public and cited page by page: the Phantom Database, each
  PhantomBuster playbook, and the specific Help Center articles and blog posts.

## 2.0 (8 October 2026)

**Lists and filters**
- Ask which Phantom a list is based on and scope it with `editions_history` +
  `mainAgentId`; never use `created_at` as a source marker. `editionsHistory`
  (camelCase) saves and silently returns 0.
- Use the user's exact terms in filters and flag any change first;
  `contains` / `notContains` are case-insensitive.
- Role filters fall back to `linkedin_headline` when the source Phantom does not
  fill `linkedin_job_title`.

**Foundations**
- Scope section: one workspace per session, and what the MCP cannot do (another
  Phantom as input, CSV input, live follow, output schemas, non-primary
  identities).
- Refer to Phantoms by id and ask when names clash or a deleted Phantom matches;
  verify tool behavior before explaining it; saving is not launching; no
  polling loops.
- Connection problems table.

**Coach check, inputs, recommend**
- New red flags: lists built by date, bulk delete, Excel export.
- LinkedIn Outreach fallback (Auto Connect + Message Sender on one Leads list).
- Sheets the model creates are made public before use.
- Sales Navigator batching recipe above 2,500 results.
- Enum values and output columns come from the manifest or a real result.

**Launch, report, cleanup**
- "Saved, not launched" after every edit.
- Cleanup procedure for deleting several Phantoms or lists.
- A successful run can be empty: check results before reporting.
- Extended error table.

## 1.0 (September 2026)

The 11-stage flow, the coach check, the playbooks, chaining and results
handoff, the list filter cookbook, Help Center rate limits and the error
table.
