# WIREFRAMES

# CANONICAL PRODUCT TRUTH (NO-DRIFT)
The system is THREE-LAYER.

1) LAYER 1 (AI Navigator) provides CLARITY with zero risk.
2) LAYER 2 (Community Bridge) provides IMMEDIACY with low risk.
3) LAYER 3 (Continuity Reserve) is LAST RESORT with tight control.
4) COMMUNITY CREDIT is the GLUE (private score, never public).

If any document or wireframe conflicts with this model, it is WRONG and must be rewritten to match.

# EXECUTABLE STRUCTURAL WIREFRAMES (ESW)
Wireframe standard:
- Explicit, column-based ASCII schematics with vertical rails.
- Every wireframe includes: HEADER line, LAYER indicator (LAYER 1/2/3), 2-3 columns where relevant.
- Required symbols: [ ] pending, [x] confirmed, [>] active, [?] suggested.
- Every wireframe answers: Which layer? What moves the user forward?

## Route Catalog
| Route | Layer | Purpose | Key actions | State transitions |
| --- | --- | --- | --- | --- |
| /navigator | LAYER 1 | AI conversation | Ask questions, match programs | Conversation -> Programs |
| /request | LAYER 2 | Submit need | Fill form, submit | Request -> Matching |
| /request/:id | LAYER 2 | Track match | View status, confirm receipt | Matching -> Fulfilled |
| /reserve | LAYER 3 | Apply for reserve | Fill application | Reserve -> Active |
| /reserve/:id | LAYER 3 | Track reserve | View status, resolve | Active -> Resolved |
| /community-credit | CREDIT | View score | See history, unlocked benefits | N/A |
| /helper-preferences | LAYER 2 | Set capacity | Configure helping | Inactive -> Active helper |

--------------------------------------------------------------------------------
AI NAVIGATOR (CONVERSATIONAL) | MODE: LAYER 1
--------------------------------------------------------------------------------
/navigator
+--------------------------------------------------------------------------------------+
| HEADER: AI Navigator | Clarity | Zero Risk                                         |
+--------------------------------------------------------------------------------------+
| DATA LOCATION: CONVERSATION HISTORY        ||| ACTION: Ask questions, match programs      |
| AI: What do you need help with?            |||                                        |
| USER: I'm behind on rent, worried about    ||| CONVERSATION FLOW:                         |
|       eviction                             ||| AI asks up to 5 clarifying questions       |
|                                            ||| Then surfaces 3-5 programs                 |
| AI: How much are you behind? (1/5)         |||                                        |
| USER: About $800                           ||| PROGRAM MATCHING: ---->                    |
|                                            ||| +--------------------------------------+ |
| AI: Are you currently working? (2/5)       ||| | 1. Emergency Rental Assistance (ERAP)| |
| USER: Yes, part-time                       ||| |    Timeline: 4-6 weeks typical       | |
|                                            ||| |    Amount: Up to 12 months rent      | |
| AI: Based on what you've told me:          ||| |    [Apply Link]                      | |
| - ERAP (4-6 weeks)                         ||| +--------------------------------------+ |
| - Community Action Agency (2-3 weeks)      ||| | 2. Community Action Agency           | |
| - United Way 211                           ||| |    Timeline: 2-3 weeks               | |
|                                            ||| |    Amount: $200-$500                 | |
| AI: These programs take 2-6 weeks.         ||| |    [Schedule Appointment]            | |
|     That doesn't solve today.              ||| +--------------------------------------+ |
|     Would you like community help?         |||                                        |
|                                            ||| GAP DETECTED: ---->                        |
| ACTION: [Yes, Show Community Options] ->   ||| [Yes] -> /request (Layer 2)                |
|         Opens Layer 2                      ||| [No, I'm Good] -> Export results           |
+--------------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
REQUEST FORM (COMMUNITY BRIDGE) | MODE: LAYER 2
--------------------------------------------------------------------------------
/request
+--------------------------------------------------------------------------------------+
| HEADER: Community Bridge Request | Immediacy | Low Risk                            |
+--------------------------------------------------------------------------------------+
| DATA LOCATION: REQUEST FORM                ||| ACTION: Submit request                     |
| WHAT DO YOU NEED?                          |||                                        |
| Describe your need:                        ||| MATCHING CRITERIA:                         |
| [Need $25 for gas to get to work_____]     ||| - Amount: $10-$25 max                      |
| [interviews this week_________________]     ||| - Timeframe: 48-72h                        |
|                                            ||| - Geographic: City                         |
| Amount: [$__25___] (Max $25)               ||| - Category: Cash                           |
| Timeframe: ● 48 hours  ○ 72 hours          |||                                        |
|                                            ||| HELPER MATCHING:                           |
| CATEGORY:                                  ||| Algorithm matches based on:                |
| ○ Time (rides, errands)                    ||| 1. Geography + capacity                    |
| ● Cash ($10-$25)                           ||| 2. Helper preferences                      |
| ○ Items (tools, goods)                     ||| 3. Community Credit                        |
| ○ Access (intros, know-how)                |||                                        |
|                                            ||| IF NO MATCH IN 24H: ---->                  |
| VISIBILITY:                                ||| Eligible for Layer 3 (Reserve)             |
| ● Anonymous  ○ Visible                     |||                                        |
|                                            |||                                        |
| EXPECTATION:                               |||                                        |
| ○ Gift  ● Repay when stable  ○ Pay forward |||                                        |
|                                            |||                                        |
| ACTION: [Submit Request] -> /request/:id   |||                                        |
+--------------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
REQUEST STATUS (WAITING FOR MATCH) | MODE: LAYER 2
--------------------------------------------------------------------------------
/request/:requestId
+--------------------------------------------------------------------------------------+
| HEADER: Request Status | Waiting for Match | Posted 2 hours ago                    |
+--------------------------------------------------------------------------------------+
| DATA LOCATION: REQUEST TRACKING            ||| ACTION: Wait or cancel                     |
| YOUR REQUEST IS ACTIVE:                    |||                                        |
| Status: [>] Waiting for helper match       ||| MATCHING PROGRESS:                         |
| Expires: In 22 hours (if no match)         ||| ████████░░░░░░░░ Searching...              |
|                                            ||| 8 helpers notified                         |
| What you requested:                        |||                                        |
| "$25 for gas for work interviews"          ||| Typically matches within 12 hours          |
|                                            |||                                        |
| WHAT HAPPENS NEXT:                         ||| STATE TRANSITIONS:                         |
| ✓ If matched: Connect with helper          ||| Waiting ---> Matched ---> Fulfilled        |
| ✓ If no match (24h): Layer 3 eligible      ||| Waiting ---> No Match ---> Reserve         |
|                                            |||                                        |
| ACTION: [Cancel Request]                   |||                                        |
+--------------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
REQUEST STATUS (MATCHED) | MODE: LAYER 2
--------------------------------------------------------------------------------
/request/:requestId (matched)
+--------------------------------------------------------------------------------------+
| HEADER: Request Matched! | Helper Found | Jordan M.                                |
+--------------------------------------------------------------------------------------+
| DATA LOCATION: MATCH RECORD                ||| ACTION: Confirm receipt                    |
| MATCHED!                                   |||                                        |
| Helper: Jordan M. (High Community Credit)  ||| HELPER DETAILS:                            |
| Offering: $25 cash                         ||| Capacity Extended: $120 (3 helps)          |
| Visibility: Anonymous (shared name)        ||| Reliability: 100% (all resolved)           |
| Expectation: Gift                          |||                                        |
|                                            ||| PAYMENT FLOW: ---->                        |
| Jordan says: "I've been there. Hope this   ||| Jordan sends payment via Venmo/CashApp     |
| helps with the interviews!"                ||| You confirm receipt                        |
|                                            ||| Jordan earns +$25 Community Credit         |
| NEXT STEPS:                                |||                                        |
| - Jordan will send payment via Venmo       |||                                        |
| - Check messages for details               |||                                        |
| - Confirm receipt when you get it          |||                                        |
|                                            |||                                        |
| ACTION: [Message Jordan] [Confirm Receipt] ||| [Confirm] -> Jordan earns credit           |
+--------------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
HELPER PREFERENCES | MODE: LAYER 2
--------------------------------------------------------------------------------
/helper-preferences
+--------------------------------------------------------------------------------------+
| HEADER: Helper Preferences | Become a Helper | Set Capacity                        |
+--------------------------------------------------------------------------------------+
| DATA LOCATION: HELPER PROFILE              ||| ACTION: Configure helping                  |
| YOUR COMMUNITY CREDIT: 145 points (High)   |||                                        |
| - Capacity Extended: $120 (3 helps)        ||| MONTHLY CAPACITY:                          |
| - Reliability: 100% (all resolved)         ||| Cash: [$___50___] (Rec: $25-$100)          |
|                                            ||| Time: [___5___] hours/month                |
| FORMS OF HELP (select all):                |||                                        |
| [x] Time (rides, errands, childcare)       ||| Used this month: $25 cash | 2 hours        |
| [x] Cash ($10-$25)                         ||| Remaining: $25 cash | 3 hours              |
| [x] Items (tools, supplies, goods)         |||                                        |
| [ ] Access (introductions, know-how)       ||| MATCHING PREFERENCES:                      |
|                                            ||| Geographic: ● City  ○ County  ○ State      |
| VISIBILITY:                                ||| Visibility: ● Visible  ○ Anonymous         |
| ● Visible (share name)  ○ Anonymous        ||| Expectation: ● Gift  ○ Repay  ○ Pay fwd    |
|                                            |||                                        |
| EXPECTATION DEFAULT:                       ||| NOTIFICATIONS:                             |
| ● Gift  ○ Repay when stable  ○ Pay forward ||| ● Daily digest  ○ Immediate  ○ Weekly      |
|                                            |||                                        |
| ACTION: [Save Preferences] [Activate]      |||                                        |
+--------------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
CONTINUITY RESERVE APPLICATION | MODE: LAYER 3
--------------------------------------------------------------------------------
/reserve
+--------------------------------------------------------------------------------------+
| HEADER: Continuity Reserve | Last Resort | Tightly Controlled                      |
+--------------------------------------------------------------------------------------+
| DATA LOCATION: RESERVE APPLICATION         ||| ACTION: Apply for reserve                  |
| REQUIREMENTS:                              |||                                        |
| ✓ Community match failed (24h elapsed)     ||| RESERVE CHARACTERISTICS:                   |
| ✓ No active reserve use                    ||| - Amount: $10-$25 max                      |
| ✓ Urgent need confirmed                    ||| - Window: 48-72 hours                      |
| ✓ Community Credit > 50 (you have 145)     ||| - One active use at a time                 |
|                                            ||| - No interest, no fees                     |
| YOUR REQUEST:                              ||| - Last resort only                         |
| "$25 for gas for work interviews"          |||                                        |
| Status: No community match after 24h       ||| STATE FLOW: ---->                          |
|                                            ||| Apply -> Pending -> Active -> Resolved     |
| RESERVE AMOUNT: [$__25___] (Max $25)       |||                                        |
|                                            ||| IF NOT RESOLVED:                           |
| WHY IS THIS URGENT?                        ||| - Access pauses (no personal chase)        |
| [I have 3 job interviews this week____]    ||| - Limits tighten quietly                   |
| [Without gas, I can't get there_______]    ||| - No aggressive collection                 |
|                                            |||                                        |
| EXPECTED RESOLUTION:                       |||                                        |
| ● Paycheck on Friday (3 days)              |||                                        |
| ○ Benefit payment (5-7 days)               |||                                        |
| ○ Other: [_____________________]           |||                                        |
|                                            |||                                        |
| ACTION: [Submit Application] -> /reserve/:id|||                                       |
+--------------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
RESERVE STATUS (ACTIVE) | MODE: LAYER 3
--------------------------------------------------------------------------------
/reserve/:reserveId
+--------------------------------------------------------------------------------------+
| HEADER: Reserve Active | $25 | Window: 72 hours | Expires in 71h                   |
+--------------------------------------------------------------------------------------+
| DATA LOCATION: RESERVE TRACKING            ||| ACTION: Mark resolved or request extension |
| ACTIVE RESERVE:                            |||                                        |
| Amount: $25                                ||| PROGRESS TRACKER:                          |
| Received: Today                            ||| Day 1: ●●●●●●●●●●●● (You are here)        |
| Window: 72 hours (expires in 71h)          ||| Day 2: ○○○○○○○○○○○○                        |
| Expected resolution: Paycheck (2 days)     ||| Day 3: ○○○○○○○○○○○○ (Paycheck)             |
|                                            |||                                        |
| RESOLUTION OPTIONS:                        ||| EARLY RESOLUTION BONUS:                    |
| [Mark as Resolved]                         ||| Resolve early: +25 Community Credit        |
| [Voluntary Repayment]                      ||| Resolve on time: +10 Community Credit      |
| [Need Extension]                           ||| Extension: No credit                       |
|                                            |||                                        |
| ACTION: [Mark as Resolved] -> /community-credit (earn bonus)                        |
+--------------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
COMMUNITY CREDIT DASHBOARD | MODE: COMMUNITY CREDIT
--------------------------------------------------------------------------------
/community-credit
+--------------------------------------------------------------------------------------+
| HEADER: Community Credit | Private Score | Never Public                            |
+--------------------------------------------------------------------------------------+
| DATA LOCATION: CREDIT HISTORY              ||| ACTION: View history, unlocked benefits    |
| YOUR SCORE: 145 points (High)              |||                                        |
| Capacity Extended: 120 pts ████████░       ||| HOW YOU EARNED IT:                         |
| Reliability:        25 pts ███░░░░░░       ||| CAPACITY EXTENDED:                         |
|                                            ||| [x] Helped Jordan ($25 gas) - 2d ago       |
| WHAT IT UNLOCKS:                           ||| [x] Gave ride to Sarah - 1w ago            |
| ✓ Priority matching (matched first)        ||| [x] Loaned tools to Alex - 2w ago          |
| ✓ Longer reserve windows (72h vs 48h)      |||                                        |
| ✓ Fewer cooldowns (request again sooner)   ||| RELIABILITY DEMONSTRATED:                  |
| ✓ Access to nonprofit grants (Phase 2)     ||| [x] All 3 helps resolved cleanly (+50)     |
|                                            ||| [x] Repaid reserve early 2d ahead (+25)    |
| KEEP BUILDING:                             |||                                        |
| - Help community members (capacity)        ||| PRIVATE SCORE:                             |
| - Resolve requests cleanly (reliability)   ||| No public scores, leaderboards, or flexing |
| - Repay reserves early (reliability bonus) |||                                        |
| - Pay forward (help after being helped)    |||                                        |
+--------------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
SETTINGS | MODE: SETTINGS
--------------------------------------------------------------------------------
/settings
+--------------------------------------------------------------------------------------+
| HEADER: Settings | Account | Location | Privacy | Notifications                    |
+--------------------------------------------------------------------------------------+
| DATA LOCATION: USER SETTINGS               ||| ACTION: Update account, privacy            |
| ACCOUNT:                                   |||                                        |
| Name:  [Jordan Smith______________]        ||| LOCATION (for helper matching):            |
| Email: [jordan@example.com________]        ||| City: [Los Angeles________________]        |
| Phone: [(555) 123-4567____________]        ||| State: [California________________]        |
| Password: [••••••••] [Change]              ||| ZIP: [90001_______________________]        |
|                                            |||                                        |
| PRIVACY:                                   ||| NOTIFICATIONS:                             |
| Profile Visibility: ● Private              ||| [x] Request matched                        |
| Community Credit: ● Private (never public) ||| [x] Reserve approved/denied                |
| [ ] Share credit with helpers              ||| [x] Community Credit milestones            |
|                                            ||| [ ] Weekly summary                         |
| ACTION: [Save Changes]                     |||                                        |
|                                            ||| DANGER ZONE:                               |
|                                            ||| [Deactivate Account]                       |
|                                            ||| (Credit preserved 6 months)                |
+--------------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
MOBILE RESPONSIVE NOTES
--------------------------------------------------------------------------------
All layouts stack vertically on mobile:
- Single column (||| separators become stacked sections)
- Bottom navigation: Navigator | Requests | Credit | Settings
- Conversational UI optimized for mobile chat
- Touch-friendly tap targets (44x44px min)

--------------------------------------------------------------------------------
ANIMATION SPECIFICATIONS
--------------------------------------------------------------------------------
AI NAVIGATOR TYPING:
1. User sends message
2. AI typing indicator (3 bouncing dots)
3. Message slides in from left
4. Scroll to bottom smoothly

REQUEST MATCHING:
1. Request submitted
2. "Searching..." spinner with progress bar
3. Helper match notification slides down
4. Success confetti (subtle)

COMMUNITY CREDIT UPDATE:
1. Action completed (help given, reserve repaid)
2. "+25 points" badge floats up from action
3. Merges with credit score
4. Score counts up with easing
5. Progress bars fill smoothly

--------------------------------------------------------------------------------
ACCESSIBILITY NOTES
--------------------------------------------------------------------------------
- All images have alt text
- Color contrast 4.5:1 min (WCAG AA)
- Keyboard nav (Tab, Enter, Arrow keys)
- Screen reader announcements for AI responses, request status, credit changes
- Focus indicators on all interactive elements
- ARIA labels on all icon buttons
- Live regions for chat updates
