# Opportunity Navigator: Research & Implementation Plan

## Executive Summary

Build a **three-layer support system** that provides:
1. **AI Opportunity Navigator (Layer 1)** - Clarity and honest guidance
2. **Community Bridge (Layer 2)** - Immediate peer support
3. **Continuity Reserve (Layer 3)** - Safety net when community can't help
4. **Community Credit System** - Private trust metric threading through all layers
5. **Dignity-first design** - Help without humiliation

**Measurable Win**: Crisis prevention rate - % of users who avoid financial collapse
- Track: requests made → community match rate → reserve usage → outcome resolution
- Target: 70%+ of urgent needs resolved without reserve, 90%+ overall resolution

**Target**: Budget-constrained individuals, crisis-facing households, community helpers who want to give back with clear boundaries.

**Architecture**: React/Next.js frontend + Python/FastAPI backend + PostgreSQL + Redis

**Platform**: Web-first (responsive PWA) with full feature set at launch

**MVP Includes Everything**: AI navigator, community matching, continuity reserve, community credit system, privacy controls - all in MVP. No deferred features.

---

## Table of Contents

1. [Executive Summary](#executive-summary)
2. [The Problem](#the-problem)
3. [Three-Layer Solution](#three-layer-solution)
4. [Architecture Design](#architecture-design)
5. [Community Credit System](#community-credit-system)
6. [Implementation Roadmap](#implementation-roadmap)
7. [Database Schema](#database-schema)
8. [Legal & Ethical Design](#legal--ethical-design)

---

## The Problem

Most people don't fail because they're irresponsible. They fail because:

- **Help exists but takes weeks** - Benefits, programs have 2-6 week processing times
- **Small gaps spiral** - $25 shortage cascades into late fees, overdrafts, job loss
- **Asking feels humiliating** - Public call-outs create shame
- **Financial tools punish** - Payday loans (400% APR), overdraft fees ($35 each)
- **Systems fragment** - Food banks, rent assistance, job programs don't coordinate

**The Reality:** Most crises are **timing problems**, not money problems.

---

## Three-Layer Solution

### Layer 1: AI Opportunity Navigator
**Purpose:** Clarity | **Risk:** Zero

Conversational interface helps users understand what help exists.

### Layer 2: Community Bridge  
**Purpose:** Immediacy | **Risk:** Low (community-sized)

Peer-to-peer support with helper agency and privacy controls.

### Layer 3: Continuity Reserve
**Purpose:** Last resort | **Risk:** Tightly controlled

Micro-credit ($10-$25) safety net with automatic protections.

---

## Architecture Design

### Technology Stack

| Component | Technology |
|-----------|------------|
| **Frontend** | React + TypeScript + Next.js 14 |
| **Backend** | Python + FastAPI |
| **Database** | PostgreSQL + Redis |
| **AI** | OpenAI API / Claude |
| **Payments** | Stripe |

---

## Community Credit System

**Two Dimensions:**
1. **Capacity Extended** - Help given
2. **Reliability Demonstrated** - Follow-through

**Private Only** - No public scores, leaderboards, or flexing.

---

## Implementation Roadmap

### Phase 1: AI Navigator
Build conversational UI + program matching

### Phase 2: Community Bridge
Helper matching + request fulfillment

### Phase 3: Continuity Reserve
Micro-credit safety net

### Phase 4: Community Credit
Trust scoring system

### Phase 5: Polish & Launch
Marketing + help pages

---

## Database Schema

### Users, Requests, Helpers, CommunityCredit, Reserves

See full schema in ARCHITECTURE.md

---

## Legal & Ethical Design

**Non-negotiables:**
- No predatory fees
- No public shaming
- Dignity-first
- Privacy-first
- No data selling

---

**Clarity. Community. Continuity.**
