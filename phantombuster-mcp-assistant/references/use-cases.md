# Use cases

23 real requests from PhantomBuster users, raised in PhantomBuster's live
MCP sessions, each with what the MCP supports today. Captured on 9 October
2026. Self-contained: you do not need any other source to use this file.

## How to use this file

- **At Intake (Part 3 of SKILL.md):** match the user's request to the closest
  use case below. If one matches, use its Phantom and notes as the starting
  point.
- **Before promising anything:** check the use case's MCP status and say what
  to expect. Never promise more than the status allows.
- If nothing matches, say so and continue with the normal stages; do not
  claim the request is supported until you have checked the tools and the
  Phantom's manifest.

## What each MCP status means for you

| MCP status | What to do |
|---|---|
| Works today | Do it. Follow the normal stages. |
| Works with skill | Do it, following this skill's procedure for it (named in the notes). |
| Work in progress | Say up front that it may not work reliably yet, use the workaround in the notes, and verify the result before reporting success. |
| Not supported via MCP | Say it is not possible through the MCP, offer the workaround (often doing it in the PhantomBuster app), and do not attempt it. |

None of the 23 is currently "Not supported via MCP"; the status is listed so
you know how to handle one if the user asks for something the MCP cannot do
(for example using another Phantom as input, a CSV file as input, or another
workspace: see Scope in Part 1).

## Extraction

| Use case | Platform | Phantom | MCP status | Notes |
|---|---|---|---|---|
| Build a lead list from a LinkedIn search prompted in chat | LinkedIn | [LinkedIn Search Export](https://phantombuster.com/phantombuster/3149/linkedin-search-export) | Works today | The assistant can run the search in the browser (for example with Claude in Chrome), take the search URL, then set the daily schedule, volume and watcher mode in the launch interview. |
| Extract everyone who commented on a LinkedIn post | LinkedIn | [LinkedIn Post Commenters Export](https://phantombuster.com/phantombuster/2823/linkedin-post-commenters-export) | Works today | The comment text doubles as a personalization hook for later messages. |
| Extract everyone who liked a LinkedIn post | LinkedIn | [LinkedIn Post Likers Export](https://phantombuster.com/phantombuster/2880/linkedin-post-likers-export) | Works today | Warm lead source. Recommended for posts with many reactions. |
| Trigger a Sales Navigator search export from chat | Sales Navigator | [Sales Navigator Search Export](https://phantombuster.com/phantombuster/6988/sales-navigator-search-export) | Works today | Ask the assistant to search Sales Navigator rather than LinkedIn. |
| Watch target accounts for LinkedIn activity signals | LinkedIn | [LinkedIn Activity Extractor](https://phantombuster.com/phantombuster/9136/linkedin-activity-extractor) | Works today | Used alongside search exports to spot posts and activity from target accounts. |
| Split a 10K Sales Navigator list into sub-2,500 batches | Sales Navigator | [Sales Navigator Search Export](https://phantombuster.com/phantombuster/6988/sales-navigator-search-export) | Work in progress | CSV upload is not available through the MCP. Workaround: split the search into narrower searches, one per row of a public Google Sheet used as input (the batching recipe in Part 4), or spread the volume across several connected accounts. |

## Enrichment

| Use case | Platform | Phantom | MCP status | Notes |
|---|---|---|---|---|
| Enrich extracted leads with full profile data | LinkedIn | [LinkedIn Profile Scraper](https://phantombuster.com/phantombuster/5589386912058181/linkedin-profile-scraper) | Works today | The standard enrichment step after an extraction. |
| Scrape profiles in bulk from a spreadsheet | LinkedIn | [LinkedIn Profile Scraper](https://phantombuster.com/phantombuster/5589386912058181/linkedin-profile-scraper) | Works today | Use a public Google Sheet URL ("Anyone with the link") as the input. |
| Find professional emails for leads not active on LinkedIn | Email | [Professional Email Finder](https://phantombuster.com/phantombuster/18998/professional-email-finder) | Works today | Keep leads who are active on LinkedIn on LinkedIn, and route the rest to email. |

## Engagement

| Use case | Platform | Phantom | MCP status | Notes |
|---|---|---|---|---|
| Auto-like posts from a target list of profiles | LinkedIn | [LinkedIn Auto Liker](https://phantombuster.com/phantombuster/16227/linkedin-auto-liker) | Works today | Engagement Phantoms can be run from chat like any other. |
| Auto-comment under posts of specific profiles | LinkedIn | [LinkedIn Auto Commenter](https://phantombuster.com/phantombuster/16226/linkedin-auto-commenter) | Works today | Often combined with auto-liking the same list of profiles. |
| Send connection requests with notes written by the assistant | LinkedIn | [LinkedIn Auto Connect](https://phantombuster.com/phantombuster/2818/linkedin-auto-connect) | Works today | The assistant writes the note; Auto Connect sends it. The two-slot LinkedIn Outreach Phantom is not always configurable through the MCP: run Auto Connect as a single-slot Phantom instead. |
| Write a custom personalized message for each follow-up | LinkedIn | [AI LinkedIn Message Writer](https://phantombuster.com/phantombuster/3614446764718424/ai-linkedin-message-writer) | Works with skill | Personalization follows this skill's message rules (Part 8 D). |
| Send DMs triggered by a prospect's posts or comments | LinkedIn | [LinkedIn Message Sender](https://phantombuster.com/phantombuster/9227/linkedin-message-sender) | Works with skill | Automated, relevant messages based on what the prospect posted or commented. |

## List management

| Use case | Platform | Phantom | MCP status | Notes |
|---|---|---|---|---|
| Add leads processed by a Phantom to a specific leads list | LinkedIn | [LinkedIn Profile Scraper](https://phantombuster.com/phantombuster/5589386912058181/linkedin-profile-scraper) | Work in progress | Works by scoping the list to its source Phantom (Part 6.3), but can be unreliable when two Phantoms share a name or one was deleted: always refer to Phantoms by id, and verify the member count. |
| Switch a Phantom's input from a search URL to a leads-list segment | LinkedIn | [LinkedIn Profile Scraper](https://phantombuster.com/phantombuster/5589386912058181/linkedin-profile-scraper) | Works today | Example: input swapped to a sales-managers list, volume lowered from 500 to 100, frequency set to once. Saving does not launch: say whether to run it after the edit. |

## Reporting

| Use case | Platform | Phantom | MCP status | Notes |
|---|---|---|---|---|
| Build reports from raw leads-list data | Any | Any Phantom | Works today | The in-app Phantom report does not export with the list. The assistant can build custom reports across Phantoms from the raw run data. |
| Export a Phantom's scraped results to Excel | Any | Any Phantom | Works with skill | Works when the assistant has a spreadsheet (xlsx) skill or tool. |
| Pick up watcher-Phantom output files, deduplicate, and email the results | LinkedIn | [LinkedIn Search Export](https://phantombuster.com/phantombuster/3149/linkedin-search-export) | Works today | Works with an assistant that can also read files and send email: it collects the results of watcher Phantoms, removes duplicates and emails the result. |

## Account management

| Use case | Platform | Phantom | MCP status | Notes |
|---|---|---|---|---|
| Delete unused Phantoms to free up slots | Any | Any Phantom | Works today | List the Phantoms, then delete the ones taking up slots (cleanup procedure, Part 11). Lists filtered on a deleted Phantom still work and show it as deleted. |
| Set Phantom options not exposed in the app | Any | Any Phantom | Works today | Example: a limit on posts scraped in watcher mode. The MCP can set manifest fields the app does not show; read them from the manifest first. |
| Stop a Phantom mid-run from chat | Any | Any Phantom | Works today | The fix for a Phantom launched by mistake. MCP actions apply in the app immediately. |

## Safety

| Use case | Platform | Phantom | MCP status | Notes |
|---|---|---|---|---|
| Enforce safe LinkedIn volumes | LinkedIn | [LinkedIn Auto Connect](https://phantombuster.com/phantombuster/2818/linkedin-auto-connect) | Works with skill | This skill sets safe defaults (Part 9). Benchmarks: about 100 connection requests per week; start at 5 to 10 requests or messages per day for two weeks, then ramp gradually. |
