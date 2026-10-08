# Workflow library

54 proven Phantom chains from the PhantomBuster Phantom Workflow Database,
captured on 9 October 2026. This file is self-contained: you do not need any
other source to use it.

## How to use this file

- **Coach check (Part 2 of SKILL.md):** find the chain closest to the user's
  plan. If a chain reaches the same outcome with a warmer audience, fewer
  steps or an all-in-one Phantom, say so and propose it.
- **Recommend (Part 4):** pick chains by the user's job to be done
  (Extraction, Enrichment, Engagement, or full cycle), then by temperature
  (Warm before Lukewarm before Cold), then by level (start new users on
  Beginner chains). Offer at most 3, each with why it fits.
- **Chain (Part 7):** every arrow is a handoff. For each one, set the data
  handoff (Leads list, upstream results file, or Google Sheet) and, separately,
  the trigger. Never call a chain done when only the trigger is set.
- **Before you recommend a chain, check every step in
  `references/phantom-catalog.md` (or the live Phantom Database).** Use the
  catalog name and link. Steps marked † are not in the current catalog of
  Released and Beta Phantoms: tell the user, and replace the step with a
  catalog Phantom that does the same job, or leave it as a manual step.
- Engagement chains must respect the rate limits in Part 9 for the whole
  account, not per Phantom.

## Legend

- `A → B`: B runs on A's results (a handoff).
- `A + B`: run both, then merge and deduplicate (for example in one Leads
  list).
- `A / B`: either one.
- *Italics*: an input the user provides, not a Phantom.
- †: not a Released or Beta Phantom in the 9 October 2026 catalog.
- **Temperature**: how warm the audience is. Warm (they know you or engaged
  with you), Lukewarm (they engaged with a topic or competitor), Cold (a
  search).
- **Level**: Beginner, Intermediate or Advanced setup effort.

## Extraction (build a list): 13 chains

| Workflow | Outcome | Chain | Temperature | Level |
|---|---|---|---|---|
| Company Follower Warm Pool | Start outbound from a warm audience: people who already follow your company page. | LinkedIn Company Follower Collector → LinkedIn Profile Scraper → AI LinkedIn Profile Enricher | Lukewarm | Beginner |
| Competitor Audience Harvest | Capture the engaged audience of a competitor's popular post. | LinkedIn Post Commenters Export + LinkedIn Post Likers Export → LinkedIn Profile Scraper | Lukewarm | Beginner |
| Community Mining | Extract niche community members and score them by recent activity. | LinkedIn Group Members Export → LinkedIn Profile Scraper → LinkedIn Activity Extractor | Lukewarm | Intermediate |
| Event Lead Engine | Capture an event's attendee list and prepare highly personalized outreach. | LinkedIn Event Guests Export → LinkedIn Profile Scraper → LinkedIn Activity Extractor | Lukewarm | Intermediate |
| Hiring Signal Hunter | Find companies actively hiring (a strong buying signal), then map the decision-makers around the role. | LinkedIn Job Scraper → LinkedIn Company Scraper → LinkedIn Company Employees Export → AI LinkedIn Profile Enricher | Lukewarm | Intermediate |
| Intent Signal Monitor | Track buying-intent keywords on X and build a daily lukewarm list. | Twitter Search Export → Twitter Profile Scraper | Lukewarm | Advanced |
| Competitive Intel from Extension Reviews | Mine competitor user pain from their Chrome extension reviews, for content, positioning and product. | Chrome Extension Review Extractor → Advanced AI Enricher (theme and pain extraction) | Cold | Beginner |
| Creator Discovery | Identify creators in a niche and qualify them before outreach. | Instagram Hashtag Search Export + TikTok hashtag search † → Instagram Profile Scraper / Twitter Profile Scraper | Cold | Beginner |
| ICP Discovery Engine | Turn a refined Sales Navigator search into a clean, qualified lead list ready for enrichment. | Sales Navigator Search Export → LinkedIn Profile Scraper | Cold | Beginner |
| Local Business Finder | Build a local outbound list with website and tech context in one pass. | Google Maps Search Export → Company Website Scraper † | Cold | Beginner |
| ABM Account Map | Map every relevant buyer inside your list of target accounts. | Sales Navigator List Export (account list) → LinkedIn Company Employees Export → LinkedIn Profile Scraper | Cold | Intermediate |
| Creator Interest Graph | Map a creator's or prospect's interests across platforms for highly personalized outreach. | Instagram Following Collector + Twitter Following Collector → Instagram Profile Scraper → AI LinkedIn Profile Enricher | Cold | Advanced |
| Daily Watcher ABM Feed | Daily sync: every new hire or signal inside a target account lands in HubSpot, enriched and ready for outreach. | Sales Navigator List Export (account list, watcher mode) → LinkedIn Company Employees Export → LinkedIn Profile Scraper → Professional Email Finder → HubSpot Contact Sender | Cold | Advanced |

## Enrichment (complete the data): 12 chains

| Workflow | Outcome | Chain | Temperature | Level |
|---|---|---|---|---|
| Job-Change Alert Stack | Daily feed of buyers who changed jobs in the last 90 days, synced into HubSpot with AI scoring. | Sales Navigator Search Export (job-change filter) → LinkedIn Profile Scraper → Advanced AI Enricher → HubSpot CRM Enricher | Lukewarm | Advanced |
| ABM Firmographic Pack | Build a rich firmographic dataset for scoring and routing. | *Account list* → LinkedIn Company Scraper + Company Website Scraper † | Cold | Beginner |
| Cold Email Ready | Turn any LinkedIn list into a deliverable, sales-ready email file. The Professional Email Finder returns only deliverable emails. | LinkedIn Profile Scraper → Professional Email Finder | Cold | Beginner |
| AI-Ranked ICP List | Sort any prospect list by AI-generated ICP-fit score before outreach, so effort goes to the top 20%. | LinkedIn Search Export → LinkedIn Profile Scraper → AI LinkedIn Profile Enricher (ICP scorer) | Cold | Intermediate |
| CRM Hygiene Flow | Clean and refresh stale CRM records with current LinkedIn and email data. | *CRM export* → LinkedIn Profile URL Finder → LinkedIn Profile Scraper → Professional Email Finder | Cold | Intermediate |
| Company Data Stack | Enrich accounts with LinkedIn firmographics and website or tech-stack data. | LinkedIn Company URL Finder → LinkedIn Company Scraper → Company Website Scraper † | Cold | Intermediate |
| Local Business Multichannel Enrichment | Turn a Google Maps category search into a multichannel-ready local business list with LinkedIn and Facebook handles. | Google Maps Search To Contact Data → Facebook Profile URL Finder + LinkedIn Company URL Finder → Professional Email Finder | Cold | Intermediate |
| Multi-CRM Enrichment Hub | One enrichment pipeline that feeds whichever CRM you use: HubSpot, Salesforce or Pipedrive. | LinkedIn Profile Scraper → Advanced AI Enricher → HubSpot CRM Enricher / Salesforce CRM Enricher / Pipedrive CRM Enricher | Cold | Intermediate |
| Reverse Lookup Stack | Recover LinkedIn profiles from a raw email list for a LinkedIn campaign. | *Email list* → LinkedIn Profile URL Finder → LinkedIn Profile Scraper | Cold | Intermediate |
| AI-Qualified Lead to CRM | Turn a raw LinkedIn search into AI-scored contacts already in HubSpot. Maximum-output top of funnel. | LinkedIn Search to Lead Connection → LinkedIn Profile Scraper → Advanced AI Enricher → HubSpot Contact Sender | Cold | Advanced |
| Full CRM Refresh Cycle | Monthly hygiene cycle: every stale HubSpot record is refreshed with current LinkedIn and verified email data. | HubSpot Contact Data Enricher + LinkedIn Profile URL Finder → LinkedIn Profile Scraper → Professional Email Finder → HubSpot CRM Enricher | Cold | Advanced |
| Full Persona Build | Deliver a complete multichannel contact record for every lead. | LinkedIn Profile Scraper → Professional Email Finder → Phone Number Finder † | Cold | Advanced |

## Engagement (act on the list): 29 chains

| Workflow | Outcome | Chain | Temperature | Level |
|---|---|---|---|---|
| Hottest Viewer Outreach | The highest-intent audience available: people who viewed your profile. Fully automated follow-up. | Sales Navigator Profile Viewers Export → LinkedIn Profile Scraper → AI LinkedIn Message Writer → Sales Navigator Auto Connect → Sales Navigator Message Sender | Warm | Beginner |
| Network Activation Play | Re-engage your existing 1st-degree network with AI-personalized messages. No new connection requests needed. | LinkedIn Connections Export → Advanced AI Enricher → AI LinkedIn Message Writer → LinkedIn Message Sender | Warm | Beginner |
| Event Magnet Workflow | Fill your webinar from your own network, then auto-follow up with every attendee and interested user. | LinkedIn Connections Export → LinkedIn Event Inviter → LinkedIn Event Guests Export → AI LinkedIn Message Writer → LinkedIn Auto Connect | Warm | Intermediate |
| Inbound Accelerator | Welcome every new connection with a personalized message and a reciprocity endorsement. | LinkedIn Auto Invitation Accepter → LinkedIn Auto Endorser → AI LinkedIn Message Writer → LinkedIn Message Sender | Warm | Intermediate |
| Post-Engagement Lead Magnet | Turn every commenter on your own posts into a multichannel lead and send the promised resource automatically. | LinkedIn Post Commenters Export (your own post) → LinkedIn Profile Scraper → Professional Email Finder → AI LinkedIn Message Writer → LinkedIn Message Sender + Email Sender † | Warm | Intermediate |
| AI Social Selling Machine | Comment intelligently on ICPs' posts first, then message them warm. AI handles both layers of personalization. | Sales Navigator Search Export → LinkedIn Activity Extractor → AI LinkedIn Post Responder → AI LinkedIn Message Writer → LinkedIn Message Sender | Warm | Advanced |
| Inbox Reply Mining | Understand why leads reply or don't, and turn the patterns into team guidance. | LinkedIn Inbox Scraper + Sales Navigator Inbox Scraper → Advanced AI Enricher (sentiment and objection tagging) | Warm | Advanced |
| Social Selling at Scale | Stay visible in target accounts' feeds to nurture buying committees. | LinkedIn Profile Scraper → LinkedIn Auto Commenter + LinkedIn Auto Liker | Warm | Advanced |
| Creator Outreach | Run creator and influencer outreach at scale on Instagram. | Instagram Hashtag Search Export → Instagram Profile Scraper → Instagram DM Sender † | Lukewarm | Beginner |
| HubSpot Re-engagement | Revive dormant HubSpot records with fresh LinkedIn touches, no export needed. | *HubSpot stale contacts* → HubSpot Contact LinkedIn Outreach → AI LinkedIn Message Writer → LinkedIn Message Sender | Lukewarm | Beginner |
| Post-Engagement Outreach | Convert engaged commenters on a relevant post into booked meetings. | LinkedIn Post Commenters Export / LinkedIn Post Likers Export → LinkedIn Profile Scraper → LinkedIn Auto Connect → LinkedIn Message Sender | Lukewarm | Beginner |
| Event Follow-Up | Turn an event attendee list into a full post-event outreach motion. | LinkedIn Event Guests Export → LinkedIn Profile Scraper → LinkedIn Auto Connect → LinkedIn Message Sender + Email Sender † | Lukewarm | Intermediate |
| Group-Message Bypass Play | Message niche ICPs without using a connection slot, through shared-group messaging rights. | LinkedIn Group Members Export → Advanced AI Enricher (ICP filter) → AI LinkedIn Message Writer → LinkedIn Group Member Message Sender | Lukewarm | Intermediate |
| Job-Change Signal Play | Reach decision-makers in their first 90 days in a new job. | Sales Navigator Search Export (changed jobs in the past 90 days) → LinkedIn Profile Scraper → AI LinkedIn Message Writer → LinkedIn Auto Connect | Lukewarm | Intermediate |
| X Audience Growth Flywheel | Algorithm-friendly X growth: engage with relevant content, then message the highest-signal accounts. | Twitter Search Export → Twitter Auto Liker → Twitter Auto Retweeter → Twitter Profile Scraper → Twitter Message Sender | Lukewarm | Intermediate |
| X Community Growth | Grow presence and open conversations on X with engaged accounts. | Twitter Search Export / Twitter Follower Collector → Twitter Auto Liker → Twitter Message Sender | Lukewarm | Intermediate |
| Competitor Intent Harvester | Pull the engaged audience of a competitor, AI-qualify for ICP fit, auto-write a context-aware opener, connect and message. Highest-intent cold play. | LinkedIn Post Commenters Export + LinkedIn Post Likers Export (on competitor posts) → LinkedIn Profile Scraper → Advanced AI Enricher → AI LinkedIn Message Writer → LinkedIn Auto Connect → LinkedIn Message Sender | Lukewarm | Advanced |
| Instagram Creator Outreach Stack | Safe, multi-touch creator outreach: warm up on stories and posts before messaging. Stays inside Instagram limits. | Instagram Multiple Hashtag Collector → Instagram Profile Scraper → Instagram Story Auto Watcher → Instagram Auto Liker → Instagram DM Sender † | Lukewarm | Advanced |
| LinkedIn Ad Engager Conversion | Recover the conversion signal from paid LinkedIn Ads: reach every engager with a personalized opener. | LinkedIn Post Likers Export / LinkedIn Post Commenters Export (ad post) → LinkedIn Profile Scraper → Advanced AI Enricher → AI LinkedIn Message Writer → LinkedIn Auto Connect | Lukewarm | Advanced |
| Promoted-Buyer Play | Newly promoted buyers tend to be more open to new solutions. AI tailors the message to their new scope. | Sales Navigator Search Export (recently promoted) → LinkedIn Profile Scraper → Advanced AI Enricher → AI LinkedIn Message Writer → Sales Navigator Auto Connect | Lukewarm | Advanced |
| Safe LinkedIn Outbound | Warm up profiles before connecting to improve acceptance and reply rates. | LinkedIn Profile Visitor → LinkedIn Auto Connect → LinkedIn Message Sender | Cold | Beginner |
| InMail Executive Play | Reach out-of-network executives directly with personalized InMails. | Sales Navigator Search Export → Sales Navigator Profile Scraper → Sales Navigator Message Sender (InMail) | Cold | Intermediate |
| Multichannel Sequence | Run a coordinated LinkedIn and email sequence from one lead file. | LinkedIn Auto Connect → LinkedIn Message Sender → Email Sender † | Cold | Intermediate |
| Recruiter-to-Candidate Outreach | Talent acquisition: sourced candidates get multichannel personalized outreach from day one. | LinkedIn Recruiter Profile Scraper → Professional Email Finder → AI LinkedIn Message Writer → LinkedIn Auto Connect + Email Sender † | Cold | Intermediate |
| lemlist Multichannel Machine | LinkedIn and email in lockstep from one search URL: lemlist handles email, PhantomBuster handles LinkedIn. | LinkedIn Search to lemlist Campaign + LinkedIn Auto Connect + LinkedIn Message Sender | Cold | Intermediate |
| AI-Personalized Outbound at Scale | Every connection request and follow-up is a custom-written GPT message based on the lead's profile and activity. Highest reply-rate play in the stack. | Sales Navigator Search Export → LinkedIn Profile Scraper → AI LinkedIn Message Writer → Sales Navigator Auto Connect → LinkedIn Message Sender | Cold | Advanced |
| Connection-Slot Reclaim | Full connection-capacity hygiene cycle: clear out dead weight, refill with active ICPs, start messaging. | LinkedIn Auto Invitation Withdrawer (stale pending) → LinkedIn Auto Connection Remover (stale 1st-degree) → LinkedIn Network Booster † → AI LinkedIn Message Writer → LinkedIn Message Sender | Cold | Advanced |
| Content-Led Warm-Up Ritual | Multi-touch social warm-up that produces 2 to 3x higher acceptance rates than cold connects. | Sales Navigator Search Export → LinkedIn Auto Liker → LinkedIn Auto Commenter (wait 3 to 7 days) → LinkedIn Profile Visitor → LinkedIn Auto Connect → LinkedIn Message Sender | Cold | Advanced |
| Network Hygiene Flywheel | Keep your 30,000-connection cap stocked with active ICPs by rotating out stale contacts and adding new ones. | LinkedIn Auto Connection Remover (stale) → LinkedIn Network Booster (new ICPs) † → AI LinkedIn Message Writer → LinkedIn Message Sender | Cold | Advanced |
