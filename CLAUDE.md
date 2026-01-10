# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**Opportunity Navigator** is a three-layer support system combining AI guidance, community bridge, and micro-credit safety net to help people navigate help systems with dignity.

**Tagline:** Clarity. Community. Continuity.

**Core Concept:** Three-layer system - AI Navigator (clarity) → Community Bridge (immediacy) → Continuity Reserve (safety net). Each layer addresses a different failure mode of traditional help systems.

## Primary Documentation

**Start here:** [docs/MASTER_PLAN.md](./docs/MASTER_PLAN.md) - Complete project plan with architecture, features, wireframes, and implementation roadmap.

## Technology Stack

| Component | Technology |
|-----------|------------|
| **Frontend** | React + TypeScript + Next.js 14 (App Router) |
| **UI** | Tailwind CSS + shadcn/ui |
| **State** | Zustand |
| **Forms** | React Hook Form + Zod |
| **Backend** | Python + FastAPI |
| **Database** | PostgreSQL + Redis |
| **Auth** | JWT + bcrypt |
| **AI** | OpenAI API / Claude for conversational navigator |
| **Payments** | Stripe (for optional fees, reserve system) |

## MVP Philosophy

**Full feature set at launch.** No deferred features. Everything ships in MVP:
- AI Opportunity Navigator (conversational UI)
- Community Bridge (helper matching)
- Continuity Reserve (micro-credit safety net)
- Community Credit system (dual-track scoring)
- Request/Helper matching algorithm
- Privacy-first design

## Documentation Structure

```
/docs/
├── MASTER_PLAN.md           ← Start here (comprehensive)
├── planning/
│   ├── MVP_SPEC.md
│   └── ROADMAP.md
├── architecture/
│   └── ARCHITECTURE.md
├── ux/
│   └── WIREFRAMES.md
└── research/
    ├── FEATURES.md
    ├── MARKET_ANALYSIS.md
    └── RISK_MANAGEMENT.md
```

## Route Structure

**Marketing:** `/`, `/how-it-works`, `/features`, `/privacy`, `/terms`

**Auth:** `/login`, `/signup`, `/onboarding`

**App:** `/navigator`, `/request`, `/reserve`, `/helper-preferences`, `/community-credit`, `/settings`

**Core Flows:**
- Layer 1: AI conversational navigator → program matching
- Layer 2: Request form → helper matching → fulfillment
- Layer 3: Continuity reserve (last resort)

## Core Data Models

- **Users** - Account + helper preferences
- **Requests** - User needs ($10-$25, 48-72h windows)
- **Helpers** - Community members + capacity + visibility choices
- **CommunityCredit** - Dual-dimensional score (capacity + reliability)
- **Reserv**es - Micro-credit safety net allocations
- **Programs** - AI-matched resources (timelines, eligibility)

See [docs/MASTER_PLAN.md](./docs/MASTER_PLAN.md) for full schema.

## Key Components

| Component | Purpose |
|-----------|---------|
| `ai-navigator-chat` | Conversational UI for program discovery |
| `request-form` | Helper request submission |
| `helper-matching-engine` | Algorithm matching requests to helpers |
| `community-credit-display` | Private trust score visualization |
| `reserve-request` | Continuity reserve application |

## MVP Rules (Non-Negotiables)

- Help exists but takes weeks (benefits, programs, resources have long processing times)
- Small gaps spiral into crises ($10-$25 can prevent collapse)
- **Layer 1** (AI Navigator) = Zero risk, clarity only
- **Layer 2** (Community Bridge) = Low risk, community-sized
- **Layer 3** (Continuity Reserve) = Tightly controlled, last resort
- Community Credit is PRIVATE (no public scores, leaderboards, or flexing)
- No predatory fees, no public shaming, no hidden terms
- Dignity-first design (no aggressive collection, no selling data)
- Reserve amounts: $10-$25 max, 48-72h windows, one active at a time

## Legal & Ethical Design

**Non-negotiable constraints:**
- No predatory fees
- No public shaming
- No hidden terms
- No aggressive collection
- No selling data

**Core principle:** Dignity-first design. Help people, don't exploit them.

See [docs/research/RISK_MANAGEMENT.md](./docs/research/RISK_MANAGEMENT.md) for full risk analysis.

## When Modifying Scope

Update these files on every scope change:
- `docs/MASTER_PLAN.md`
- `docs/ux/WIREFRAMES.md`
- `docs/architecture/ARCHITECTURE.md`
