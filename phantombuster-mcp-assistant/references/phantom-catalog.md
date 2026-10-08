# Phantom catalog

Offline snapshot of the public PhantomBuster Phantom Database, taken on
**9 October 2026**: every Phantom whose status is Released or Beta (145).

Live source (public): https://thephantomcompany.notion.site/d22ab00a50994f078509e07b416c356a?v=f1c1b6f00fe6430aa4204ffee45b8bdc

Use the live database first. Use this file when it cannot be read, and say
that you are using a snapshot dated 9 October 2026.

Columns:

- **Goal**: Scrape (build a list), Enrich (complete the data), Engage (act on
  the list).
- **Input**: what the Phantom reads. "None (your own account)" means it works
  on the connected account and needs no input list.
- **Watcher**: "Yes" means it supports watcher mode (only new results on each
  launch).
- **Link**: the public store page. Where no public link exists, look the
  Phantom up by name in the PhantomBuster store or ask the user.

Always confirm field names and accepted inputs in the Phantom's manifest
(Part 8 of SKILL.md) before configuring it.

## LinkedIn

| Phantom | Status | Goal | What it does | Input | Watcher | Link |
|---|---|---|---|---|---|---|
| AI LinkedIn Message Writer | Released | Engage | Write a personalized LinkedIn message from profile data | Leads list or spreadsheet with scraped LinkedIn profile data | No | https://phantombuster.com/phantombuster/3614446764718424/ai-linkedin-message-writer |
| AI LinkedIn Post Responder | Released | Engage | Write comments for your leads' most impactful posts of the last month | Leads list | No | https://phantombuster.com/phantombuster/5825898517687124/ai-linkedin-post-responder |
| AI LinkedIn Profile Enricher | Released | Enrich | Structure and enrich LinkedIn lead data with AI | Leads list or spreadsheet with scraped LinkedIn profile data | No | https://phantombuster.com/automations/ai/1333223865797404/ai-linkedin-profile-enricher |
| LinkedIn Activity Extractor | Released | Scrape | Scrape the posts and likes of profiles or company pages | LinkedIn profile or company page URLs | Yes | https://phantombuster.com/automations/linkedin/9136/linkedin-activity-extractor |
| LinkedIn Auto Commenter | Released | Engage | Comment on posts and articles | LinkedIn post URLs and the comment | No | https://phantombuster.com/api-store/16226/linkedin-auto-commenter |
| LinkedIn Auto Connect | Released | Engage | Send connection requests with a note | Profile URLs | No | https://phantombuster.com/automations/linkedin/2818/linkedin-auto-connect |
| LinkedIn Auto Connection Remover | Released | Engage | Remove connections | LinkedIn profile URLs | No | https://phantombuster.com/automations/linkedin/7132580939722323/linkedin-auto-connection-remover |
| LinkedIn Auto Endorser | Released | Engage | Endorse skills | LinkedIn profile URLs | No | https://phantombuster.com/automations/linkedin/3611/linkedin-auto-endorser |
| LinkedIn Auto Follow | Released | Engage | Follow or unfollow profiles | LinkedIn profile URLs | No | https://phantombuster.com/api-store/6874/linkedin-auto-follow |
| LinkedIn Auto Invitation Accepter | Released | Engage | Accept incoming invitations | None (your own account) | No | https://phantombuster.com/automations/linkedin/2885/linkedin-auto-invitation-accepter |
| LinkedIn Auto Invitation Withdrawer | Released | Engage | Withdraw pending invitations | None (your own account) | No | https://phantombuster.com/automations/linkedin/3672/linkedin-auto-invitation-withdrawer |
| LinkedIn Auto Liker | Released | Engage | Like posts or articles | LinkedIn profile or post URLs | Yes | https://phantombuster.com/api-store/16227/linkedin-auto-liker |
| LinkedIn Auto Poster | Released | Engage | Schedule and publish pre-written posts | List of posts | No | https://phantombuster.com/automations/linkedin/7415410842242185/linkedin-auto-poster |
| LinkedIn Auto Unfollow | Released | Engage | Unfollow profiles | LinkedIn profile URLs | No | https://phantombuster.com/phantombuster/1942869543072163/linkedin-auto-unfollow |
| LinkedIn Company Employees Export | Released | Scrape | Scrape a company's employee list | Company URLs | No | https://phantombuster.com/automations/linkedin/3295/linkedin-company-employees-export |
| LinkedIn Company Follow Inviter | Released | Engage | Invite your connections to follow your company page | LinkedIn profile URLs or names from the official export | No | https://phantombuster.com/automations/linkedin/1298207880720700/linkedin-compay-follow-inviter |
| LinkedIn Company Follower Collector | Released | Scrape | Scrape your company page's followers | Company URL | No | https://phantombuster.com/automations/linkedin/6609751279582074/linkedin-company-follower-collector |
| LinkedIn Company Follower Collector to Outreach | Released | Engage | Extract your company page's followers, then connect and follow up | Your company page (admin access) and message templates | No | https://phantombuster.com/automations/linkedin/7972540039693475/linkedin-company-follower-collector-to-outreach |
| LinkedIn Company Page Inviter | Released | Engage | Invite 1st-degree connections to follow your company page | Spreadsheet, Leads list or previous results with profile URLs, plus your company page URL | No | https://phantombuster.com/automations/linkedin/8522029843786898/linkedin-company-page-inviter |
| LinkedIn Company Post Commenter and Liker Scraper | Released | Scrape | Extract leads who commented on or liked a company's posts | LinkedIn company page URLs | No | https://phantombuster.com/automations/linkedin/5251160215300729/linkedin-post-commenter-and-liker-scraper |
| LinkedIn Company Scraper | Released | Enrich | Scrape company profiles | Company URLs or names | No | https://phantombuster.com/automations/linkedin/3296/linkedin-company-scraper |
| LinkedIn Company URL Finder | Released | Scrape | Find LinkedIn company page URLs | Company names or website URLs | No | https://phantombuster.com/api-store/4372/linkedin-company-url-finder |
| LinkedIn Connections Export | Released | Scrape | Export your connections | None (your own account) or the official contacts export | No | https://phantombuster.com/automations/linkedin/12670/linkedin-connections-export |
| LinkedIn Connections to Emails | Released | Scrape | Extract your connections and find their emails | None (your own account) | No | https://phantombuster.com/automations/linkedin/2220776630920718/linkedin-connections-to-emails |
| LinkedIn Event Guests Export | Released | Scrape | Extract the attendees of an event you attend | LinkedIn event URLs (you must attend) | No | https://phantombuster.com/automations/linkedin/5447892918325546/linkedin-event-guests-export |
| LinkedIn Event Inviter | Released | Engage | Send event invitations and export guests | Connections' profile URLs (a list, not a single URL) | No | https://phantombuster.com/phantombuster/2814528681070599/linkedin-event-inviter |
| LinkedIn Group Member Message Sender | Beta | Engage | Message group members (no connection needed) | Group URLs | No | https://phantombuster.com/phantombuster/511865799449120/linkedin-group-member-message-sender |
| LinkedIn Group Members Export | Released | Scrape | Scrape group member lists | Group URLs | Yes | https://phantombuster.com/automations/linkedin/2852/linkedin-group-members-export |
| LinkedIn Group Members to Emails | Released | Scrape | Extract group members and find their emails | Group URLs | No | https://phantombuster.com/automations/linkedin/1960014583069690/linkedin-group-members-to-emails |
| LinkedIn Group Members to Outreach | Released | Engage | Extract group members, then connect and follow up | Group URL and message templates | No | https://phantombuster.com/automations/linkedin/2246643678897122/linkedin-group-members-to-outreach |
| LinkedIn Inbox Scraper | Released | Scrape | Scrape your inbox threads | None (your own account) | No | https://phantombuster.com/automations/linkedin/532696507966746/linkedin-inbox-scraper |
| LinkedIn Job Scraper | Released | Scrape | Scrape job ads | Job ad URLs | No | https://phantombuster.com/phantombuster/6772788738377011/linkedin-job-scraper |
| LinkedIn Join Group Inviter | Released | Engage | Invite your connections to join a group | Group URL plus profile URLs or names from the official export | No | https://phantombuster.com/automations/linkedin/7381354215467141/linkedin-join-group-inviter |
| LinkedIn Message Sender | Released | Engage | Send messages to 1st-degree connections | Profile URLs and the message | No | https://phantombuster.com/api-store/9227/linkedin-message-sender |
| LinkedIn Message Thread Scraper | Released | Scrape | Scrape one-to-one chat conversations | Chat thread or profile URLs | No | https://phantombuster.com/automations/linkedin/9387/linkedin-message-thread-scraper |
| LinkedIn New Connection Welcome Message | Released | Engage | Message new connections | Welcome message template (#firstName# supported) | No | https://phantombuster.com/automations/linkedin/7572144804575918/linkedin-new-connection-welcome-message |
| LinkedIn Outreach | Released | Engage | Connect with a list of profiles and follow up with those who accept | LinkedIn profile URLs or Sales Navigator search URLs | No | https://phantombuster.com/automations/linkedin/4545709793535249/linkedin-outreach |
| LinkedIn Personal Email Extractor | Released | Enrich | Scrape your connections' personal emails | Official contacts export | No | https://phantombuster.com/automations/linkedin/18231/linkedin-personal-email-extractor |
| LinkedIn Poll Voters Export | Released | Scrape | Scrape the voters of a poll | LinkedIn poll URL | Yes | https://phantombuster.com/automations/linkedin/4648700649184588/linkedin-poll-voters-export |
| LinkedIn Post Commenters Export | Released | Scrape | Scrape commenters and comments on posts | Post URLs | Yes | https://phantombuster.com/automations/linkedin/2823/linkedin-post-commenters-export |
| LinkedIn Post Commenters to Emails | Released | Enrich | Extract a post's commenters and find their emails | LinkedIn post URLs | Yes | https://phantombuster.com/automations/linkedin/2238207930449780/linkedin-post-commenters-to-emails |
| LinkedIn Post Engagers to Lead Outreach | Released | Engage | Scrape a post's commenters and likers, filter with AI, then connect and follow up | LinkedIn post URLs and message templates | No | https://phantombuster.com/automations/linkedin/811469274539266/linkedin-post-engagers-to-lead-outreach |
| LinkedIn Post Likers Export | Released | Scrape | Scrape the likers of posts | Post URLs | Yes | https://phantombuster.com/phantombuster/2880/linkedin-post-likers |
| LinkedIn Profile Follower Collector | Released | Scrape | Scrape your followers | None (your own account) | No | https://phantombuster.com/automations/linkedin/3750/linkedin-profile-follower-collector |
| LinkedIn Profile Post Commenter and Liker Scraper | Released | Scrape | Extract leads who commented on or liked a profile's posts | LinkedIn profile URLs | No | https://phantombuster.com/automations/linkedin/5251160215300729/linkedin-post-commenter-and-liker-scraper |
| LinkedIn Profile Scraper | Released | Enrich | Scrape profiles | Profile URLs (single URL or Sheet via spreadsheetUrl) | No | https://phantombuster.com/automations/linkedin/5589386912058181/linkedin-profile-scraper |
| LinkedIn Profile URL Finder | Released | Enrich | Find profile URLs from name and company | Full names and company names | No | https://phantombuster.com/api-store/4015/linkedin-profile-url-finder |
| LinkedIn Profile Visitor | Released | Scrape | Visit profiles (and scrape them) | Profile URLs | No | https://phantombuster.com/automations/linkedin/3112/linkedin-profile-visitor |
| LinkedIn Profiles to lemlist Campaign | Released | Engage | Send LinkedIn profile data to a lemlist campaign | LinkedIn profile URLs and a lemlist API key | No | https://phantombuster.com/automations/linkedin/1069439181217466/linkedin-profiles-to-lemlist-campaign |
| LinkedIn Recruiter Profile Scraper | Released | Enrich | Scrape LinkedIn Recruiter profiles | Profile URLs | No | https://phantombuster.com/automations/linkedin/4274640725828784/linkedin-recruiter-profile-scraper |
| LinkedIn Search Export | Released | Scrape | Export search results | LinkedIn search URLs or search terms | Yes | https://phantombuster.com/api-store/3149/linkedin-search-export |
| LinkedIn Search To Emails | Released | Scrape | Extract people search results and find their emails | LinkedIn people search URLs | No | https://phantombuster.com/automations/linkedin/6546459929405349/linkedin-search-to-emails |
| LinkedIn Search to Lead Connection | Released | Engage | Extract a search or group, connect, and track who accepts | LinkedIn search, Sales Navigator search or group URL | No | https://phantombuster.com/automations/linkedin/2350589230697394/linkedin-search-to-lead-connection |
| LinkedIn Search to Lead Outreach | Released | Engage | Extract a search, connect, and follow up with those who accept | LinkedIn people search URLs | No | https://phantombuster.com/automations/linkedin/6276867532496207/linkedin-search-to-lead-outreach |
| LinkedIn Search to Outreach | Released | Engage | Extract a LinkedIn or Sales Navigator search, then connect and follow up | Search URLs | No | https://phantombuster.com/phantombuster/8154936279314174/linkedin-search-to-outreach |
| LinkedIn Search to Profile Data | Released | Scrape | Scrape the profiles and company profiles of search results | LinkedIn search URLs or search terms | No | https://phantombuster.com/automations/linkedin/25772/linkedin-search-to-profile-data |
| LinkedIn Search to lemlist Campaign | Released | Engage | Send search results to a lemlist email campaign | LinkedIn search URLs or search terms | No | https://phantombuster.com/automations/toolbox/4201331544314519/linkedin-search-to-lemlist-campaign |
| LinkedIn Sent Request Extractor | Released | Scrape | Extract all sent invitations | None (your own account) | No | https://phantombuster.com/automations/linkedin/2625694299992413/linkedin-sent-request-extracto |

## Sales Navigator

| Phantom | Status | Goal | What it does | Input | Watcher | Link |
|---|---|---|---|---|---|---|
| Sales Navigator Account Employees Export | Released | Scrape | Extract the employees of a Sales Navigator account | LinkedIn company URLs | Yes | https://phantombuster.com/automations/sales-navigator/4200612184013755/sales-navigator-account-employees-export |
| Sales Navigator Account Scraper | Released | Enrich | Extract company information | Sales Navigator account URL | No | https://phantombuster.com/automations/linkedin/1229523726637056/linkedin-sales-navigator-account-scraper |
| Sales Navigator Alert Extractor | Released | Enrich | Scrape alerts from a Sales Navigator account | Alert type (account connected) | No | https://phantombuster.com/phantombuster/8380235547652117/sales-navigator-alert-extractor |
| Sales Navigator Auto Connect | Released | Engage | Send connection requests with a note | Sales Navigator profile URLs | No | https://phantombuster.com/automations/sales-navigator/29582/sales-navigator-auto-connect |
| Sales Navigator Inbox Scraper | Released | Scrape | Scrape your Sales Navigator inbox threads | None (your own account) | No | https://phantombuster.com/automations/sales-navigator/2449319061041483/sales-navigator-inbox-scraper |
| Sales Navigator Lead Sender | Released | Enrich | Send Sales Navigator leads to your Leads page and enrich them | Sales Navigator profile URLs | No | https://phantombuster.com/phantombuster/2157800763358807/sales-navigator-lead-sender |
| Sales Navigator List Export | Released | Scrape | Export the leads and accounts of a Sales Navigator list | List URL | Yes | https://phantombuster.com/automations/linkedin/2316536293241490/linkedin-sales-navigator-list-export |
| Sales Navigator Message Sender | Released | Engage | Send messages or InMails on Sales Navigator | Sales Navigator profile URLs, message and subject | No | https://phantombuster.com/automations/linkedin/6318432035741982/sales-navigator-message-sender |
| Sales Navigator Profile Scraper | Released | Enrich | Scrape Sales Navigator profiles | Sales Navigator profile URLs | No | https://phantombuster.com/api-store/11108/linkedin-sales-navigator-profile-scraper |
| Sales Navigator Profile Viewers Export | Released | Scrape | Scrape your profile viewers | None (your own account) | No | https://phantombuster.com/automations/sales-navigator/7495268271828736/sales-navigator-profile-viewers-export |
| Sales Navigator Search Export | Released | Scrape | Export the results of a Sales Navigator search (up to 2,500 per search) | Sales Navigator search URLs or search terms | Yes | https://phantombuster.com/api-store/6988/linkedin-sales-navigator-search-export |
| Sales Navigator Search To Emails | Released | Scrape | Extract Sales Navigator search results and find their emails | Sales Navigator lead search URLs | No | https://phantombuster.com/automations/sales-navigator/3345210151302862/sales-navigator-search-to-emails |
| Sales Navigator Search to Lead Outreach | Released | Engage | Extract a Sales Navigator search, connect, and follow up | Sales Navigator lead search URLs or list URL | No | https://phantombuster.com/automations/sales-navigator/990186133186253/sales-navigator-search-to-lead-outreach |
| Sales Navigator URL Converter | Released | Enrich | Convert Sales Navigator profile URLs into regular LinkedIn URLs | Sales Navigator profile URLs | No | https://phantombuster.com/api-store/9068/linkedin-sales-navigator-url-converter |

## CRM

| Phantom | Status | Goal | What it does | Input | Watcher | Link |
|---|---|---|---|---|---|---|
| HubSpot CRM Enricher | Released | Enrich | Fill HubSpot with contact data from PhantomBuster or elsewhere | Email, first name, last name, company name | No | https://phantombuster.com/automations/hubspot/276741128276076/hubspot-crm-enricher |
| HubSpot Contact Career Tracker | Released | Enrich | Track job changes of HubSpot contacts on LinkedIn | HubSpot contact list with LinkedIn profile URLs | No | https://phantombuster.com/automations/hubspot/2152744569299391/hubspot-contact-career-tracker |
| HubSpot Contact Data Enricher | Released | Enrich | Fill HubSpot with contact data scraped from LinkedIn | LinkedIn profile URLs | No | https://phantombuster.com/automations/hubspot/7401331807175971/hubspot-contact-data-enricher |
| HubSpot Contact Data Refresher | Released | Enrich | Refresh HubSpot contacts from their LinkedIn profiles | HubSpot contact list with LinkedIn profile URLs | No | https://phantombuster.com/automations/hubspot/8591269450646814/hubspot-contact-data-refresher |
| HubSpot Contact LinkedIn Outreach | Released | Engage | Run a LinkedIn outreach campaign on a HubSpot contact list | HubSpot contact list with LinkedIn profile URLs | No | https://phantombuster.com/automations/hubspot/5426528541103641/hubspot-contact-linkedin-outreach |
| HubSpot Contact LinkedIn URL Finder | Released | Enrich | Find LinkedIn profiles from full name and company | HubSpot contact list (full names) | No | https://phantombuster.com/automations/hubspot/5512064239143016/hubspot-contact-linkedin-url-finder |
| HubSpot Contact Sender | Released | Enrich | Send leads from PhantomBuster to HubSpot | HubSpot connection; LinkedIn profile URLs or PhantomBuster leads | No | https://phantombuster.com/phantombuster/1386033999114383/hubspot-contact-sender |
| Pipedrive CRM Enricher | Released | Enrich | Fill Pipedrive with contact data from PhantomBuster or elsewhere | Pipedrive connection and lead data | No | https://phantombuster.com/automations/pipedrive/789401822848446/pipedrive-crm-enricher |
| Salesforce CRM Enricher | Released | Enrich | Fill Salesforce with contact data from PhantomBuster or elsewhere | Salesforce connection and lead data | No | https://phantombuster.com/automations/salesforce/2264953542925362/salesforce-integration |

## Instagram

| Phantom | Status | Goal | What it does | Input | Watcher | Link |
|---|---|---|---|---|---|---|
| Instagram Auto Commenter | Released | Engage | Comment on posts | Post URLs | No | https://phantombuster.com/api-store/14303/instagram-auto-commenter |
| Instagram Auto Follow | Released | Engage | Follow profiles | Profile URLs | No | https://phantombuster.com/api-store/10274/instagram-auto-follow |
| Instagram Auto Liker | Released | Engage | Like posts | Profile URLs or post URLs | No | https://phantombuster.com/api-store/10506/instagram-auto-liker |
| Instagram Auto Unfollow | Released | Engage | Unfollow profiles | Profile URLs | No | https://phantombuster.com/automations/instagram/8175445863495364/instagram-auto-unfollow |
| Instagram Follower Collector | Released | Scrape | Scrape the followers of profiles | Profile URLs | Yes | https://phantombuster.com/api-store/7175/instagram-follower-collector |
| Instagram Followers Auto Follow | Released | Engage | Follow the followers of a profile | One Instagram profile URL | No | https://phantombuster.com/phantombuster/2439619339195827/instagram-followers-auto-follow |
| Instagram Following Collector | Released | Scrape | Scrape the profiles a user follows | Profile URLs | No | https://phantombuster.com/api-store/7195/instagram-following-collector |
| Instagram Hashtag Search Export | Released | Scrape | Scrape posts tagged with a hashtag | Hashtags or locations | No | https://phantombuster.com/automations/instagram/5391/instagram-hashtag-search-export |
| Instagram Hashtag Search To Post Engagement | Released | Engage | Comment daily on top posts for chosen hashtags | Hashtags and comments to post | No | https://phantombuster.com/automations/instagram/1310092046585771/engage-with-instagram-hashtags |
| Instagram Multiple Hashtag Collector | Released | Scrape | Scrape posts tagged with a hashtag combination | Hashtags or locations | No | https://phantombuster.com/automations/instagram/5952/instagram-multiple-hashtag-collector |
| Instagram Notification Extractor | Released | Scrape | Export your notifications and the users behind them | None (your own account) | No | https://phantombuster.com/automations/instagram/3146421772946574/instagram-notification-extractor |
| Instagram Photo Likers | Released | Engage | Scrape the profiles who liked photos | Post URLs | No | https://phantombuster.com/api-store/10253/instagram-photo-likers |
| Instagram Post Commenters Export | Released | Scrape | Scrape commenters and comments on posts | Post URLs | No | https://phantombuster.com/automations/instagram/13788/instagram-post-commenters-export |
| Instagram Post Scraper | Released | Scrape | Scrape post information | Post URLs | No | https://phantombuster.com/automations/instagram/10152/instagram-post-scraper |
| Instagram Profile Post Extractor | Released | Scrape | Scrape and export a profile's posts | Profile URLs | Yes | https://phantombuster.com/automations/instagram/12766/instagram-profile-post-extractor |
| Instagram Profile Scraper | Released | Enrich | Scrape profiles | Profile URLs | No | https://phantombuster.com/api-store/7085/instagram-profile-scraper |
| Instagram Profile URL Finder | Released | Enrich | Find profile URLs from names | Names | No | https://phantombuster.com/api-store/4487/instagram-profile-url-finder |
| Instagram Story Auto Watcher | Released | Engage | Watch stories with your account | Profile URLs | No | https://phantombuster.com/automations/instagram/22794/instagram-story-auto-watcher |
| Instagram Story Extractor | Released | Scrape | Scrape stories | Profile URLs | No | https://phantombuster.com/automations/instagram/22487/instagram-story-extractor |
| Instagram Story Viewers Export | Released | Scrape | Scrape the viewers of your own stories | None (your own account) | No | https://phantombuster.com/automations/instagram/22807/instagram-story-viewers-export |
| Instagram Tagged Post Extractor | Released | Scrape | Scrape posts a user is tagged in | Profile URLs | No | https://phantombuster.com/automations/instagram/21841/instagram-tagged-post-extractor |

## X (Twitter)

| Phantom | Status | Goal | What it does | Input | Watcher | Link |
|---|---|---|---|---|---|---|
| Twitter Auto Follow | Released | Engage | Follow a list of profiles | Profile URLs | No | https://phantombuster.com/phantombuster/4127/twitter-auto-follow |
| Twitter Auto Liker | Released | Engage | Like a list of tweets | Profile URLs | No | https://phantombuster.com/phantombuster/5770/twitter-auto-liker |
| Twitter Auto Poster | Released | Engage | Schedule and publish pre-written tweets | Tweet content | No | https://phantombuster.com/automations/twitter/6367798890597108/twitter-auto-poster |
| Twitter Auto Retweeter | Released | Engage | Retweet tweets | Tweet or profile URLs | Yes | https://phantombuster.com/phantombuster/11057/twitter-auto-retweeter |
| Twitter Auto Unfollow | Released | Engage | Unfollow a list of profiles | Profile URLs | No | https://phantombuster.com/automations/twitter/1312398357250675/twitter-auto-unfollow |
| Twitter Follower Collector | Released | Scrape | Scrape a profile's followers | Profile URL | Yes | https://phantombuster.com/phantombuster/4130/twitter-follower-collector |
| Twitter Following Collector | Released | Scrape | Scrape the profiles someone follows | Profile URL | Yes | https://phantombuster.com/phantombuster/4457/twitter-following-collector |
| Twitter Hashtag Search Export | Released | Scrape | Find tweets for a hashtag | Hashtags | No | https://phantombuster.com/automations/twitter/10622/twitter-hashtag-search-export |
| Twitter Media Extractor | Released | Scrape | Scrape a profile's media posts | Profile URL | No | https://phantombuster.com/phantombuster/8835/twitter-media-extractor |
| Twitter Message Sender | Released | Engage | Send direct messages | Profile URLs | No | https://phantombuster.com/phantombuster/10678/twitter-message-sender |
| Twitter Profile Likes Extractor | Released | Scrape | Scrape the tweets a profile liked | Profile URL | No | https://phantombuster.com/automations/twitter/9807/twitter-profile-likes-extractor |
| Twitter Profile Scraper | Released | Enrich | Scrape profile information | Profile URLs | No | https://phantombuster.com/phantombuster/9375/twitter-profile-scraper |
| Twitter Profile URL Finder | Released | Enrich | Find profile URLs from names | Full names | No | https://phantombuster.com/phantombuster/4485/twitter-profile-url-finder |
| Twitter Search Export | Released | Scrape | Scrape search results | Search or tweet URLs | Yes | https://phantombuster.com/phantombuster/7263448483654601/twitter-search-export |
| Twitter Tweet Extractor | Released | Scrape | Scrape a profile's tweets | Profile URL | No | https://phantombuster.com/automations/twitter/30442/twitter-tweet-extractor |
| Twitter Tweet Likers Export | Released | Scrape | Scrape a tweet's likers | Tweet URL | Yes | https://phantombuster.com/automations/twitter/8886/twitter-likes-export |

## Facebook

| Phantom | Status | Goal | What it does | Input | Watcher | Link |
|---|---|---|---|---|---|---|
| Facebook Group Members Export | Released | Scrape | Scrape the members of a Facebook group | Facebook group URL | Yes | https://phantombuster.com/automations/facebook/6987/facebook-group-members-export |
| Facebook Profile Scraper | Released | Enrich | Scrape every available data point from a profile | Facebook profile URLs | No | https://phantombuster.com/phantombuster/8369/facebook-profile-scraper |
| Facebook Profile URL Finder | Released | Enrich | Find Facebook profiles from full names | Names | No | https://phantombuster.com/phantombuster/4371/facebook-profile-url-finder |

## Google Maps and directories

| Phantom | Status | Goal | What it does | Input | Watcher | Link |
|---|---|---|---|---|---|---|
| Google Maps Search Export | Released | Scrape | Scrape all places and their data from a Google Maps search | Google Maps search URL | No | https://phantombuster.com/automations/google-maps/23412/google-maps-search-export |
| Google Maps Search To Contact Data | Released | Scrape | Extract emails, phone numbers and social profiles from Google Maps results | Google Maps search URLs | No | https://phantombuster.com/automations/google-maps/3164769743055708/generate-leads-with-google-maps |
| Pages Jaunes Business Scraper | Released | Scrape | Scrape a business from the Pages Jaunes directory (France) | Pages Jaunes URL | No | https://phantombuster.com/automations/pages-jaunes/8382506532665958/pages-jaunes-business-scraper |
| Pages Jaunes Search Export | Released | Scrape | Export Pages Jaunes search results | Pages Jaunes URL | No | https://phantombuster.com/automations/pages-jaunes/8088768334781496/pages-jaunes-search-export |
| Yellow Pages Business Scraper | Released | Enrich | Scrape a business from Yellow Pages (USA) | Yellow Pages URL | No | https://phantombuster.com/automations/yellow-pages/7789470996120613/yellow-pages-business-scraper |
| Yellow Pages Search Export | Released | Scrape | Export Yellow Pages search results (USA) | Yellow Pages URL | No | https://phantombuster.com/automations/yellow-pages/7991936744428339/yellow-pages-search-export |

## Web and toolbox

| Phantom | Status | Goal | What it does | Input | Watcher | Link |
|---|---|---|---|---|---|---|
| Chrome Extension Review Extractor | Released | Scrape | Scrape the reviews of Chrome Web Store extensions | Chrome Web Store extension URLs | No | https://phantombuster.com/automations/toolbox/6817/chrome-extension-review-extractor |
| Data Scraping Crawler | Released | Enrich | Visit a website's pages and scrape data | Website URLs and the data to scrape | No | No public link: search the store by name |
| Domain Name Finder | Released | Enrich | Turn business names into domain names | Company or business names | No | https://phantombuster.com/automations/toolbox/3171/domain-name-finder |
| Email Extractor | Released | Enrich | Extract email addresses from a website | Domain names | No | https://phantombuster.com/automations/toolbox/6774/email-extractor |
| Professional Email Finder | Released | Enrich | Find a professional email from full name and company | Full name and company name or website | No | https://phantombuster.com/automations/toolbox/18998/professional-email-finder |
| Web Element Extractor | Released | Scrape | Extract web elements with CSS selectors | Website URLs and CSS selectors | No | https://phantombuster.com/automations/toolbox/6776/web-element-extractor |

## AI

| Phantom | Status | Goal | What it does | Input | Watcher | Link |
|---|---|---|---|---|---|---|
| Advanced AI Enricher | Released | Enrich | Enhance your data with GPT | Any data | No | https://phantombuster.com/automations/ai/147200841883363/advanced-ai-enricher |

## GitHub

| Phantom | Status | Goal | What it does | Input | Watcher | Link |
|---|---|---|---|---|---|---|
| GitHub Contributors Export | Released | Scrape | Scrape the contributors of a GitHub repository | Repository URL | No | https://phantombuster.com/automations/github/13243/github-contributors-export |
| GitHub Profile Scraper | Released | Enrich | Scrape GitHub profiles | Profile URLs (GitHub account connected) | No | https://phantombuster.com/automations/github/12016/github-profile-scraper |
| GitHub Stargazers Export | Released | Scrape | Scrape developers who starred a repository you own or collaborate on | Repository URL | No | https://phantombuster.com/automations/github/11695/github-stargazers-export |
| GitHub User Search Export | Released | Scrape | Scrape GitHub user search results (developers and emails) | GitHub search (account connected) | No | https://phantombuster.com/automations/github/19487/github-user-search-export |

## Slack

| Phantom | Status | Goal | What it does | Input | Watcher | Link |
|---|---|---|---|---|---|---|
| Slack Channel User Extractor | Released | Scrape | Scrape names and emails from a Slack workspace | Workspace URL (account connected) | No | https://phantombuster.com/automations/slack/12190/slack-channel-user-extractor |
| Slack Message Sender | Released | Engage | Send Slack messages | Workspace URL and user IDs (account connected) | No | https://phantombuster.com/automations/slack/12420/slack-message-sender |
| Slack Search Export | Released | Scrape | Export Slack searches | Workspace URL (account connected) | No | https://phantombuster.com/automations/slack/5994628008869727/slack-search-export |

## YouTube

| Phantom | Status | Goal | What it does | Input | Watcher | Link |
|---|---|---|---|---|---|---|
| YouTube Channel Scraper | Released | Scrape | Extract data from YouTube channels | CSV URL or channel URL | No | https://phantombuster.com/automations/youtube/11479/youtube-channel-scraper |
| YouTube Channel Video Extractor | Released | Scrape | Extract video data from YouTube channels | CSV URL or channel URL | Yes | https://phantombuster.com/automations/youtube/11494/youtube-channel-video-extractor |
| YouTube Video Scraper | Released | Enrich | Scrape video content, metrics and related URLs | Video URL or CSV URL | No | https://phantombuster.com/automations/youtube/2932599717283203/youtube-video-scraper |

## Reddit

| Phantom | Status | Goal | What it does | Input | Watcher | Link |
|---|---|---|---|---|---|---|
| Reddit Profile Scraper | Released | Scrape | Collect the information of Reddit profiles | Reddit profile URLs | No | No public link: search the store by name |
