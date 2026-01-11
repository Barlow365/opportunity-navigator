# Opportunity Navigator

| Repo Map | Purpose | Authority |
| --- | --- | --- |
| [docs/PRODUCT_MAP.md](docs/PRODUCT_MAP.md) | Canonical product model (three-layer system) | Source of truth |
| [docs/MASTER_PLAN.md](docs/MASTER_PLAN.md) | End-to-end behavior and execution | Source of truth |
| [docs/ux/WIREFRAMES.md](docs/ux/WIREFRAMES.md) | ESW wireframes for all routes | Derived |
| [docs/ux/SITEMAP.md](docs/ux/SITEMAP.md) | Route map tied to PRODUCT_MAP | Derived |
| [docs/planning/MVP_SPEC.md](docs/planning/MVP_SPEC.md) | MVP definition and success criteria | Derived |
| [docs/architecture/ARCHITECTURE.md](docs/architecture/ARCHITECTURE.md) | Data model + API contracts | Architecture-only |

| System Entities | Description | Persisted? | User-facing label |
| --- | --- | --- | --- |
| User | Account + helper preferences | Yes | Your Account |
| Request | Community help need ($10-$25, 48-72h) | Yes | Request |
| Helper | Community member offering capacity | Yes | Helper |
| Match | Request-Helper pairing | Yes | Match |
| CommunityCredit | Dual-dimensional score (capacity + reliability) | Yes | Community Credit |
| Reserve | Continuity Reserve allocation ($10-$25) | Yes | Reserve |
| Program | AI-matched resource (timelines, eligibility) | No (external) | Program |
| Conversation | AI Navigator chat history | Yes | Conversation |

| Routes Index | Mode | Writes | Reads | Wireframe location |
| --- | --- | --- | --- | --- |
| / | PUBLIC | None | None | [WIREFRAMES.md](docs/ux/WIREFRAMES.md) (Home) |
| /navigator | LAYER 1 | Conversation | Programs | [WIREFRAMES.md](docs/ux/WIREFRAMES.md) (AI Navigator) |
| /request | LAYER 2 | Request | Request status | [WIREFRAMES.md](docs/ux/WIREFRAMES.md) (Request Form) |
| /request/:requestId | LAYER 2 | Match confirmation | Request, Match | [WIREFRAMES.md](docs/ux/WIREFRAMES.md) (Request Status) |
| /helper-preferences | LAYER 2 | Helper capacity, preferences | Helper profile | [WIREFRAMES.md](docs/ux/WIREFRAMES.md) (Helper Preferences) |
| /reserve | LAYER 3 | Reserve application | Reserve status | [WIREFRAMES.md](docs/ux/WIREFRAMES.md) (Reserve Application) |
| /reserve/:reserveId | LAYER 3 | Reserve resolution | Reserve tracking | [WIREFRAMES.md](docs/ux/WIREFRAMES.md) (Reserve Status) |
| /community-credit | CREDIT | None | Credit score, history | [WIREFRAMES.md](docs/ux/WIREFRAMES.md) (Credit Dashboard) |
| /settings | SETTINGS | Account, location, privacy | User profile | [WIREFRAMES.md](docs/ux/WIREFRAMES.md) (Settings) |

# CANONICAL PRODUCT TRUTH (NO-DRIFT)
The system is THREE-LAYER.

1) LAYER 1 (AI Navigator) provides CLARITY with zero risk.
   - Conversational UI helps users find resources.
   - Max 5 clarifying questions, honest timelines (2-6 weeks typical).
   - Identifies gaps and opens door to Layer 2.

2) LAYER 2 (Community Bridge) provides IMMEDIACY with low risk.
   - Request form for short-term needs ($10-$25, 48-72h).
   - Helper matching algorithm (geography + capacity).
   - Four forms of help: Time, Items, Cash, Access.
   - Helper agency: form, visibility, expectation.

3) LAYER 3 (Continuity Reserve) is LAST RESORT with tight control.
   - Very small amounts ($10-$25 max).
   - One active use at a time.
   - Only when community matching fails (24h elapsed).
   - No interest, no fees.

4) COMMUNITY CREDIT is the GLUE.
   - Private score tracking capacity extended + reliability demonstrated.
   - Unlocks priority matching, longer windows, fewer cooldowns.
   - Never public, never leaderboards, never flexing.

Terminology rules:
- Internal system term: Three-Layer Funnel (architecture only).
- User-facing term: AI Navigator / Community Bridge / Continuity Reserve.
- Community Credit is PRIVATE (no public scores).
- Helpers have AGENCY (choose form, visibility, expectation).
- No predatory fees, no public shaming, no hidden terms.

## Gut Check (Yes/No)
- Is this a loan? NO (Continuity Reserve is a micro-credit safety net)
- Is Layer 1 required? NO (users can skip to Layer 2)
- Can helpers see personal info? ONLY IF you choose "Visible"
- Is Community Credit public? NO (always private)
- What happens if reserve isn't repaid? Access pauses (no aggressive collection)
- Do helpers get paid? NO (voluntary community support)

## Core Innovation
**Three-layer system sits between crisis and collapse:**

**Layer 1 (Clarity):**
- Purpose: Understand what help exists
- Risk: Zero
- Outcome: Program matching + honest timelines

**Layer 2 (Immediacy):**
- Purpose: Bridge short-term gaps with community support
- Risk: Low (community-sized)
- Outcome: Helper matching (time, items, cash, access)

**Layer 3 (Safety Net):**
- Purpose: Prevent failure when peers can't help
- Risk: Tightly controlled (last resort)
- Outcome: Micro-credit safety net ($10-$25)

## Key Principle
**Most crises are TIMING problems, not money problems.**

Continuity matters more than cash. This system:
- Helps people understand their options (Layer 1)
- Bridges short-term gaps through community (Layer 2)
- Protects continuity when needed (Layer 3)
- Rewards reliability with Community Credit (all layers)

---

**Tagline:** Clarity. Community. Continuity.

**Documentation:** See [docs/PRODUCT_MAP.md](./docs/PRODUCT_MAP.md) for complete feature specifications.

**Technology Stack:** React + TypeScript + Next.js 14 | Python + FastAPI | PostgreSQL + Redis | OpenAI API

**Status:** Ready for Development
