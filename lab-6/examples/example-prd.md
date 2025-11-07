# Product Requirements Document (PRD)
# StudySpot: Real-Time Study Room Finder

**Product:** StudySpot MVP v1.0  
**Team:** Team Discovery Engine  
**Document Owner:** Lekso Tevdorashvili (Product Lead)  
**Contributors:** Dato (Engineering), Murman (Research), Ana (Design)  
**Status:** Approved for Development  
**Last Updated:** October 28, 2025  
**Target Release:** December 15, 2025 (Week 15)

---

## Table of Contents

1. [Executive Summary](#executive-summary)
2. [Problem Statement](#problem-statement)
3. [Goals & Success Metrics](#goals--success-metrics)
4. [User Personas](#user-personas)
5. [User Stories & Prioritization](#user-stories--prioritization)
6. [Feature Requirements](#feature-requirements)
7. [Out of Scope (Explicitly)](#out-of-scope-explicitly)
8. [Technical Considerations](#technical-considerations)
9. [Design Requirements](#design-requirements)
10. [Analytics & Instrumentation](#analytics--instrumentation)
11. [Launch Plan](#launch-plan)
12. [Risks & Mitigations](#risks--mitigations)
13. [Open Questions](#open-questions)
14. [Appendix](#appendix)

---

## Executive Summary

**What are we building?**  
A mobile-first web app that shows KIU students real-time occupancy of study rooms across campus, helping them find available study spaces quickly without walking to multiple buildings.

**Why are we building it?**  
Our research (10 student interviews, 15 observational sessions) shows that KIU commuter students waste 12-20 minutes per day (avg: 15.3 minutes) searching for available study spots during peak hours (10 AM - 2 PM). This translates to 75+ minutes per week and causes:
- Missed assignment deadlines (4/10 students)
- High stress levels (8/10 students)
- Reduced study time during critical gaps between classes

**Who is it for?**  
Primary: KIU commuter students (Years 2-4) with 1-3 hour gaps between classes  
Secondary: All KIU students looking for study spaces

**What's the MVP scope?**  
- Real-time occupancy for 4 study locations (K-Building Library, H-Building Study Hall, Cafeteria Quiet Zone, Computer Lab 2)
- Mobile-responsive web app (no native app for MVP)
- Manual occupancy updates by student "spotters" (automated sensors in v2)
- Basic search and filter by building

**Success Criteria:**
- 50+ weekly active users by Week 2 of launch
- Average decision time <30 seconds (measured via app analytics)
- 70%+ of users report "time saved" in post-use survey

---

## Problem Statement

### The Validated Problem

**Problem:**  
KIU commuter students with 1-3 hour gaps between classes waste 12-20 minutes per day (3-4 times per week) searching for available quiet study spaces because they lack real-time occupancy information, resulting in wasted study time, increased stress, and occasionally missed deadlines.

**Evidence:**
- **Interviews:** 10 in-depth interviews with commuter students (Years 2-4)
- **Observation:** 15 hours of shadowing students during peak hours
- **Survey:** 43 students confirmed experiencing this problem 2+ times per week
- **Quantified Impact:**
  - Time wasted: 12-20 min per occurrence (avg: 15.3 min)
  - Frequency: 3-4 times per week
  - Total: ~60 minutes per student per week
  - Emotional impact: "Frustrating" (8/10), "Stressful" (6/10)

### Current User Behavior (Workarounds)

**What students do today:**
1. **Check Library First (70% of students):**  
   Walk to K-Building Library (closest to most classes). If full, proceed to step 2.

2. **Sequential Building Checks (60%):**  
   Walk to 2-3 buildings in order of proximity: H-Building → Cafeteria → Computer Labs

3. **Ask Friends via WhatsApp (40%):**  
   Message 3-5 friends "Is library full?" - unreliable, responses in 5-30 min

4. **Give Up & Study in Loud Areas (30%):**  
   Study in cafeteria or hallway despite noise if all quiet spots full

5. **Go Home Early (15%):**  
   Leave campus if can't find quiet spot, losing entire study session

**Gaps in Current Solutions:**
- No real-time occupancy data
- Friends don't always respond quickly
- Walking time wasted (5-7 min per building × 2-3 buildings = 15-20 min)
- Information is stale by the time you arrive

---

## Goals & Success Metrics

### Product Goals

**Primary Goal:**  
Reduce time wasted searching for study spaces from 15 minutes to <3 minutes for 50+ KIU students.

**Secondary Goals:**
- Increase study time utilization during class gaps
- Reduce student stress around finding study spaces
- Create a foundation for campus space optimization (data for facilities management)

### Success Metrics (MVP - First 4 Weeks)

#### Primary Metrics (Must Achieve)

| Metric | Target | Measurement Method |
|--------|--------|-------------------|
| Weekly Active Users | 50+ | Google Analytics - unique users per week |
| Time to Decision | <30 seconds | Analytics - homepage load to building selection |
| User Retention (Week 2) | 40%+ | Users active in Week 1 who return in Week 2 |
| Time Saved (Self-Reported) | 70%+ report saving time | Post-use survey (n=30) |

#### Secondary Metrics (Good to Achieve)

| Metric | Target | Measurement Method |
|--------|--------|-------------------|
| Data Freshness | 90%+ updates <5 min old | Backend tracking of update timestamps |
| Mobile Usage | 80%+ | Device type tracking |
| Peak Hour Usage | 60%+ sessions 10 AM-2 PM | Time-based analytics |
| NPS (Net Promoter Score) | 40+ | Survey: "How likely to recommend?" (0-10 scale) |

#### Learning Metrics (Inform v2)

| Metric | Purpose |
|--------|---------|
| Most-checked buildings | Prioritize sensor installation for v2 |
| Search filter usage | Determine which filters to add |
| Average session duration | Understand user behavior patterns |
| Drop-off points | Identify UX friction |

### Leading vs Lagging Indicators

**Leading Indicators (Early Warning Signs):**
- Daily active spotters (need 8+ to maintain freshness)
- Update frequency per location (target: every 5-10 min)
- Homepage bounce rate (<40% good, >60% problem)

**Lagging Indicators (Success Confirmation):**
- Week-over-week retention
- Survey responses about time saved
- Word-of-mouth growth (referral tracking)

---

## User Personas

### Primary Persona: Dato the Commuter Engineer

**Demographics:**
- Year: 3rd year Computer Science
- Age: 21
- Lives: 30 minutes from campus (public transport)
- Schedule: 8 AM - 6 PM, 3-4 classes per day with 1-2 hour gaps

**Goals:**
- Maximize study time during gaps between classes
- Avoid wasting time walking between buildings
- Find quiet spaces for focused work (coding assignments)

**Frustrations:**
- "I have a 2-hour gap between Database and Algorithms. By the time I find a quiet spot, I have 45 minutes left."
- "The library looks empty from outside but it's full inside. I wish I knew before walking up 3 flights of stairs."
- "I ask friends on WhatsApp but they respond too late."

**Tech Savvy:** High - daily GitHub user, comfortable with web apps

**Key Quote:** *"If I could see room status from my phone, I'd save at least 20 minutes every Tuesday and Thursday."* - Interview #3

---

### Secondary Persona: Mariam the Group Project Coordinator

**Demographics:**
- Year: 2nd year Business Administration  
- Age: 20
- Lives: On-campus dorms
- Schedule: Lighter class load but coordinates 2 group projects

**Goals:**
- Find study rooms for team meetings (4-6 people)
- Book spaces that won't be noisy
- Coordinate last-minute meeting location changes

**Frustrations:**
- "We plan to meet at the library, everyone walks there, and it's full. Then we scramble to find backup."
- "I wish I could check capacity - we need a room for 6 people, not a 2-person desk."
- "Sometimes we give up and meet in the loud cafeteria."

**Tech Savvy:** Medium - uses Instagram, WhatsApp; less comfortable with new apps

**Key Quote:** *"My team wastes 30 minutes every Wednesday just figuring out where to meet."* - Interview #7

---

### Tertiary Persona: Nika the First-Year Commuter

**Demographics:**
- Year: 1st year Economics
- Age: 19
- Lives: 45 minutes from campus (bus + metro)
- Schedule: New to campus, doesn't know building layouts well

**Goals:**
- Discover available study spaces on campus
- Learn which buildings are quieter
- Build better study habits in new environment

**Frustrations:**
- "I don't know where to study. I try the library but it's always full."
- "I'm too shy to ask upperclassmen where to go."
- "Sometimes I just go home because I can't find a spot."

**Tech Savvy:** Medium-Low - uses social media but hesitant with new apps

**Key Quote:** *"I need something that just tells me: go here, there are seats."* - Interview #9

---

## User Stories & Prioritization

### Priority Framework: MoSCoW Method

- **Must Have (P0):** Required for MVP launch; without this, product fails
- **Should Have (P1):** Important but can be added in v1.1 (2 weeks post-launch)
- **Could Have (P2):** Nice to have; v2.0+ (next semester)
- **Won't Have (P3):** Explicitly out of scope for foreseeable future

---

### Must Have (P0) - MVP Launch

#### US-001: View Current Room Occupancy [P0]
```
As a commuter student checking study room options on my phone,
I want to see which buildings have available seats RIGHT NOW,
So that I can decide where to walk without wasting time checking multiple buildings.

Evidence: 10/10 interviews; primary use case
Effort: M (Medium - 3-5 days)
```

**Acceptance Criteria:**
- [ ] Homepage shows list of 4 study locations
- [ ] Each location displays: building name, current occupancy (e.g., "12/50 seats"), status indicator (green/yellow/red)
- [ ] Data updates every 30 seconds automatically (no manual refresh required)
- [ ] Occupancy data is <5 minutes old (freshness indicator shown)
- [ ] Works on mobile browsers (iOS Safari, Android Chrome)
- [ ] Page loads in <3 seconds on 4G connection

---

#### US-002: See Individual Room Details [P0]
```
As a student who wants more information before walking across campus,
I want to tap a building and see detailed room breakdown,
So that I know exactly which floor/room to go to.

Evidence: 7/10 interviews mentioned wanting room-level detail
Effort: S (Small - 1-2 days)
```

**Acceptance Criteria:**
- [ ] Tapping a building opens detail view
- [ ] Detail view shows: list of rooms (e.g., "K-201", "K-203"), occupancy per room, floor number
- [ ] Visual indicator (green/yellow/red) for each room
- [ ] "Back" button returns to main list
- [ ] Transitions are smooth (<500ms)

---

#### US-003: Mobile-First Design [P0]
```
As a student checking availability while walking between classes,
I want the app to work perfectly on my phone without downloading anything,
So that I can make quick decisions on the go.

Evidence: 10/10 interviews mentioned mobile-first use; 8/10 won't download app
Effort: M (Medium - built into design)
```

**Acceptance Criteria:**
- [ ] Responsive design works on screens 320px - 430px wide
- [ ] Touch targets are 44px+ (Apple HIG compliant)
- [ ] No horizontal scrolling required
- [ ] Text is readable without zooming (16px+ font size)
- [ ] Works without app install (progressive web app OK)

---

#### US-004: Data Freshness Indicator [P0]
```
As a user making a decision based on occupancy data,
I want to know how recent the information is,
So that I don't walk to a room that filled up 20 minutes ago.

Evidence: 6/10 interviews mentioned trust/staleness concern
Effort: XS (Extra Small - <1 day)
```

**Acceptance Criteria:**
- [ ] Each location shows timestamp: "Updated 3 minutes ago"
- [ ] If data is >5 minutes old, show warning: "⚠️ Data may be outdated"
- [ ] If data is >15 minutes old, show error: "❌ Unable to get current status"
- [ ] Timestamp updates every 30 seconds

---

### Should Have (P1) - v1.1 (Week 2 Post-Launch)

#### US-005: Filter by Building [P1]
```
As a student near a specific building with limited time,
I want to filter to show only rooms in my current building,
So that I see relevant options first.

Evidence: 5/10 interviews; especially relevant for quick decisions
Effort: S (Small - 1-2 days)
```

**Acceptance Criteria:**
- [ ] Filter dropdown at top: "All Buildings" (default), "K-Building", "H-Building", etc.
- [ ] Selecting filter updates list within 1 second
- [ ] Filter choice persists during session
- [ ] "Clear filter" option visible when active

---

#### US-006: Favorite Locations [P1]
```
As a student who prefers 2-3 specific study spots,
I want to mark them as favorites and see them first,
So that I don't scroll through all options every time.

Evidence: 4/10 interviews mentioned having "regular spots"
Effort: S (Small - 2 days)
```

**Acceptance Criteria:**
- [ ] Star icon next to each location to toggle favorite
- [ ] Favorites appear at top of list (with divider)
- [ ] Favorites persist across sessions (localStorage)
- [ ] Max 3 favorites (prevent list clutter)

---

### Could Have (P2) - v2.0 (Next Semester)

#### US-007: Capacity Filter [P2]
```
As a team lead coordinating group study sessions,
I want to filter rooms by capacity (showing 4-6 person rooms),
So that I don't waste time checking rooms that are too small.

Evidence: 3/10 interviews (secondary persona: group coordinators)
Effort: M (Medium - 3 days)
```

---

#### US-008: Quiet Level Indicator [P2]
```
As a student sensitive to noise when studying,
I want to see noise level for each location,
So that I can choose appropriately quiet spaces.

Evidence: 6/10 interviews mentioned noise as important factor
Effort: L (Large - requires additional data collection)
```

---

### Won't Have (P3) - Explicitly Out of Scope

#### US-009: Room Reservations [P3]
**Why not:**
- Requires authentication system (adds 2-3 weeks development)
- Requires admin approval/policies (outside team control)
- Interview data shows "finding" is higher pain point than "reserving"
- Can validate need after MVP proves value

#### US-010: Push Notifications [P3]
**Why not:**
- Requires native app or PWA setup (complex for MVP)
- Battery drain concerns (mentioned in 2 interviews)
- Email/SMS alternatives not yet validated
- v2.0 feature after we understand user retention

#### US-011: Historical Patterns / Predictions [P3]
**Why not:**
- Need 4-8 weeks of data before patterns are meaningful
- Complex ML/analytics beyond MVP scope
- Interview data doesn't strongly support predictive need yet
- Could be v3.0 feature if data supports it

---

## Feature Requirements

### Feature 1: Real-Time Occupancy Display

**Description:**  
Display current seat occupancy for 4 key study locations with visual indicators and auto-refresh.

**Functional Requirements:**

**FR-1.1:** Homepage displays a card-based list of study locations  
- Each card contains: Location name, Building name, Current occupancy (X/Y format), Visual indicator (color-coded), Last updated timestamp

**FR-1.2:** Visual occupancy indicators follow traffic light pattern
- **Green (Available):** 0-60% capacity - "Mostly Empty" or "Some Seats Available"
- **Yellow (Filling Up):** 61-85% capacity - "Filling Up" or "Limited Seats"
- **Red (Full):** 86-100% capacity - "Nearly Full" or "Full"

**FR-1.3:** Auto-refresh mechanism
- Page refreshes occupancy data every 30 seconds automatically
- No user action required
- Loading state shown during refresh (subtle, non-disruptive)

**FR-1.4:** Manual refresh option
- Pull-to-refresh gesture on mobile
- Refresh button on desktop
- Visual feedback on refresh action

**Non-Functional Requirements:**

**NFR-1.1:** Performance
- Initial page load <3 seconds on 4G
- Data refresh <1 second
- Lightweight payload <100 KB per request

**NFR-1.2:** Reliability
- 95%+ uptime during peak hours (10 AM - 4 PM)
- Graceful degradation if data unavailable (show last known state with warning)

**NFR-1.3:** Accessibility
- WCAG 2.1 AA compliant
- Screen reader compatible
- Color-blind friendly (not relying on color alone)

---

### Feature 2: Study Location Details

**Description:**  
Detailed view for each study location showing room-by-room breakdown.

**Functional Requirements:**

**FR-2.1:** Tap/click any location card to open detail view

**FR-2.2:** Detail view displays:
- Location header (building, floor)
- List of individual rooms within location
- Occupancy per room (X/Y seats format)
- Visual indicators per room
- Amenities icons (power outlets, whiteboard, quiet zone, group-friendly)

**FR-2.3:** Detail view navigation
- Back button to return to main list
- Smooth transition animation (<500ms)
- Browser back button support

**Non-Functional Requirements:**

**NFR-2.1:** Detail view loads instantly (data pre-fetched on homepage)  
**NFR-2.2:** Detail view URL is shareable (deep linking)

---

### Feature 3: Data Collection System (Spotter Dashboard)

**Description:**  
Separate web interface for student "spotters" to manually update room occupancy.

**Functional Requirements:**

**FR-3.1:** Spotter Login
- Simple PIN-based authentication (4-digit PIN)
- No full user management system (MVP simplification)

**FR-3.2:** Spotter Dashboard
- List of assigned locations
- Quick update interface: tap room → see current count → +/- buttons to adjust
- Submit button to push update

**FR-3.3:** Update Validation
- Cannot set occupancy > max capacity
- Requires confirmation if change is >50% from previous value (prevent errors)

**FR-3.4:** Spotter Incentive Tracking
- Simple point system (1 point per update)
- Leaderboard visible to spotters
- Points reset weekly

**Non-Functional Requirements:**

**NFR-3.1:** Mobile-optimized (spotters use phones while in location)  
**NFR-3.2:** Update submission <2 seconds  
**NFR-3.3:** Works offline with queue (sync when connection restored)

---

## Out of Scope (Explicitly)

This section is critical to prevent scope creep. These are features we explicitly will NOT build in MVP.

### Authentication & User Accounts
- **Not building:** Login, user profiles, saved preferences (beyond localStorage)
- **Rationale:** Adds 2-3 weeks development; not required for core value proposition
- **Future:** v2.0 if retention justifies investment

### Room Reservations
- **Not building:** Ability to book/reserve a study room
- **Rationale:** Requires policies, admin approval, conflicts with university systems
- **Future:** Partner with university facilities if MVP proves demand

### Push Notifications
- **Not building:** Alerts when favorite room becomes available
- **Rationale:** Requires PWA setup or native app; battery concerns; unvalidated need
- **Future:** v2.0 after understanding user retention patterns

### Automated Sensors
- **Not building:** Automated occupancy detection (cameras, weight sensors, etc.)
- **Rationale:** Requires hardware budget, installation permissions, privacy concerns
- **Future:** Pitch to university facilities with MVP data as proof of concept

### Historical Data & Predictions
- **Not building:** "Library is usually full at 2 PM on Tuesdays" predictions
- **Rationale:** Need 4-8 weeks of data; ML complexity; unvalidated need
- **Future:** v3.0 if data supports patterns

### Multi-Campus Support
- **Not building:** Support for multiple universities
- **Rationale:** MVP is KIU-specific; expansion after local success
- **Future:** v4.0+ (different product trajectory)

### Social Features
- **Not building:** Check-ins, reviews, study buddy matching
- **Rationale:** Feature creep; unvalidated; dilutes core value
- **Future:** Unlikely - stay focused on occupancy data

---

## Technical Considerations

### Tech Stack (Recommended)

**Frontend:**
- **Framework:** React (familiarity, component reusability)
- **Styling:** Tailwind CSS (rapid prototyping, mobile-first utilities)
- **State Management:** React Context (simple, no Redux needed for MVP)
- **Build Tool:** Vite (fast dev server, optimized builds)

**Backend:**
- **Runtime:** Node.js + Express
- **Database:** PostgreSQL (structured data, relationships)
- **Hosting:** Vercel (frontend) + Railway (backend + DB) - free tier adequate
- **API Design:** RESTful endpoints (simpler than GraphQL for MVP)

**Data Storage:**
```
Tables:
- locations (id, name, building, floor, max_capacity, amenities)
- rooms (id, location_id, room_number, max_capacity)
- occupancy_updates (id, room_id, occupancy_count, timestamp, spotter_id)
- spotters (id, name, pin_hash, points)
```

**APIs:**
```
GET /api/locations - Get all locations with current occupancy
GET /api/locations/:id - Get specific location with room details
POST /api/occupancy - Submit occupancy update (spotter auth required)
GET /api/spotters/:id/stats - Get spotter points and history
```

### Performance Requirements

**Page Load:**
- First Contentful Paint: <1.5 seconds
- Time to Interactive: <3 seconds
- Lighthouse Performance Score: >85

**API Response Times:**
- GET requests: <500ms p95
- POST requests: <1 second p95

**Data Freshness:**
- Target: 90%+ of occupancy data <5 minutes old
- Acceptable: 80%+ of data <10 minutes old
- Alert: If >50% of data >15 minutes old (indicates spotter dropout)

### Scalability Considerations

**MVP Expectations:**
- 100-200 users per day
- 50 concurrent users at peak
- 4 locations × 10 rooms = 40 data points

**Bottlenecks to Monitor:**
- Database queries (index on location_id, timestamp)
- API rate limiting (implement after 500+ daily users)
- Frontend re-renders (optimize React components if sluggish)

**Cost Projections:**
- Vercel: Free tier (adequate for <100 GB bandwidth)
- Railway: Free tier → $5/mo if usage exceeds (likely Week 3-4)
- Domain: $12/year (optional; can use .vercel.app subdomain)
- **Total:** $0-10/month for MVP

---

## Design Requirements

### Visual Design Principles

**1. Mobile-First:**
- Design for 375px width (iPhone SE) as baseline
- Scale up for tablets/desktop (not down from desktop)

**2. Clarity Over Aesthetics:**
- Information hierarchy: occupancy data is always most prominent
- Minimal decoration; functional design
- High contrast for outdoor visibility (students check while walking)

**3. Speed & Simplicity:**
- Max 2 taps to any information
- No unnecessary animations (except feedback/transitions)
- Large touch targets (44px minimum)

### Design Specifications

**Color Palette:**
```
Primary: #2563EB (Blue - trustworthy, tech)
Success: #10B981 (Green - available)
Warning: #F59E0B (Yellow - filling up)
Danger: #EF4444 (Red - full/unavailable)
Neutral: #6B7280 (Gray - text/borders)
Background: #F9FAFB (Light gray - easy on eyes)
```

**Typography:**
```
Primary Font: Inter (clean, readable, optimized for screens)
Headings: 20-24px, Semi-bold
Body: 16px, Regular (mobile) / 18px (desktop)
Labels: 14px, Medium
Timestamps: 12px, Regular, Gray
```

**Component Library:**
- Use shadcn/ui for consistent components (buttons, cards, modals)
- Maintain KIU brand colors where appropriate (blue as primary aligns with KIU)

### Key Screens (Wireframe References)

**Screen 1: Homepage (Location List)**
```
┌─────────────────────────┐
│ 🏫 StudySpot            │ ← Header
│ Find your study space   │
├─────────────────────────┤
│                         │
│ ┌─────────────────────┐ │
│ │ K-Building Library  │ │ ← Location Card
│ │ 🟢 Mostly Empty     │ │
│ │ 12/50 seats         │ │
│ │ Updated 2 min ago   │ │
│ └─────────────────────┘ │
│                         │
│ ┌─────────────────────┐ │
│ │ H-Building Study    │ │
│ │ 🟡 Filling Up       │ │
│ │ 34/40 seats         │ │
│ │ Updated 4 min ago   │ │
│ └─────────────────────┘ │
│                         │
│ ┌─────────────────────┐ │
│ │ Cafeteria Quiet     │ │
│ │ 🔴 Full             │ │
│ │ 28/30 seats         │ │
│ │ Updated 1 min ago   │ │
│ └─────────────────────┘ │
│                         │
│ ┌─────────────────────┐ │
│ │ Computer Lab 2      │ │
│ │ 🟢 Available        │ │
│ │ 8/25 seats          │ │
│ │ Updated 6 min ago   │ │
│ └─────────────────────┘ │
│                         │
│ 🔄 Auto-refresh: 30s    │ ← Footer status
└─────────────────────────┘
```

**Screen 2: Location Detail**
```
┌─────────────────────────┐
│ ← K-Building Library    │ ← Header with back
├─────────────────────────┤
│ Floor 2                 │
│ ┌─────────────────────┐ │
│ │ Room K-201          │ │
│ │ 🟢 3/20 seats       │ │
│ │ 🔌 💡 🤫 (quiet)   │ │ ← Amenity icons
│ └─────────────────────┘ │
│                         │
│ ┌─────────────────────┐ │
│ │ Room K-203          │ │
│ │ 🟡 14/20 seats      │ │
│ │ 🔌 💡             │ │
│ └─────────────────────┘ │
│                         │
│ Floor 3                 │
│ ┌─────────────────────┐ │
│ │ Room K-301          │ │
│ │ 🔴 18/20 seats      │ │
│ │ 🔌 📊 (group-ok)   │ │
│ └─────────────────────┘ │
│                         │
│ Updated 3 minutes ago   │
└─────────────────────────┘
```

### Accessibility Requirements

- **WCAG 2.1 Level AA** compliance minimum
- **Color contrast:** 4.5:1 for normal text, 3:1 for large text
- **Keyboard navigation:** Tab order logical, focus indicators visible
- **Screen readers:** Semantic HTML, ARIA labels where needed
- **Touch targets:** 44×44px minimum (Apple HIG standard)
- **Alternative text:** All icons have text labels or aria-labels

---

## Analytics & Instrumentation

### Events to Track

**Page Views:**
- `page_view_home` - Homepage loaded
- `page_view_location_detail` - Specific location detail viewed

**User Actions:**
- `location_card_clicked` - User tapped location (track which building)
- `manual_refresh_triggered` - User manually refreshed data
- `filter_applied` - User applied building filter (track filter value)
- `favorite_toggled` - User favorited/unfavorited location

**Performance Metrics:**
- `page_load_time` - Time from request to interactive
- `api_response_time` - Time for API calls to complete
- `data_staleness` - Age of occupancy data when viewed

**Spotter Activity:**
- `occupancy_update_submitted` - Spotter submitted update
- `spotter_login` - Spotter logged in
- `update_validation_failed` - Update exceeded capacity or looked suspicious

### Analytics Stack

**Tool:** Google Analytics 4 (free, easy setup)

**Custom Dimensions:**
- Device type (mobile vs desktop)
- Time of day (morning/midday/afternoon/evening)
- Day of week
- Building selected
- User agent (browser)

**Sample Event Implementation:**
```javascript
// Location card clicked
gtag('event', 'location_card_clicked', {
  'building_name': 'K-Building Library',
  'occupancy_status': 'mostly_empty',
  'device_type': 'mobile',
  'time_of_day': 'midday'
});
```

### Dashboard for Team

**Weekly Review Metrics:**
- Daily active users (DAU)
- Most viewed locations
- Peak usage times
- Average session duration
- Data freshness (% of updates <5 min old)
- Spotter activity (updates per spotter per day)

---

## Launch Plan

### Pre-Launch (Weeks 12-13)

**Week 12: Development Sprint**
- Mon-Wed: Core features (location list, occupancy display)
- Thu-Fri: Spotter dashboard, data entry
- Weekend: Testing, bug fixes

**Week 13: Testing & Refinement**
- Mon-Tue: Internal team testing (all 4 members)
- Wed: Usability test with 5 external students
- Thu: Bug fixes based on feedback
- Fri: Final QA, deploy to staging

### Launch Week (Week 14)

**Soft Launch (Mon-Wed):**
- Recruit 8 spotters (2 per location)
- Train spotters on data entry
- Invite 20 beta testers (recruited from interviews)
- Monitor closely for bugs

**Public Launch (Thu):**
- Post in KIU CS WhatsApp group
- Post in KIU Student WhatsApp group
- Flyers in K-Building and H-Building (QR codes)
- Instagram story (team members share)
- In-class announcement (request 2 min from friendly professors)

**Launch Day Monitoring:**
- Team on standby 10 AM - 4 PM (peak hours)
- Rapid bug fixes if critical issues
- Respond to user feedback within 2 hours

### Post-Launch (Week 15)

**Daily Monitoring (Days 1-7):**
- Check analytics every morning
- Ping spotters if data goes stale
- Fix bugs within 24 hours
- Collect user feedback (in-app survey link)

**Week 2 Review:**
- Analyze metrics vs targets
- Survey 30 users for qualitative feedback
- Decide on v1.1 features (from P1 backlog)
- Plan next sprint

---

## Risks & Mitigations

### Risk 1: Spotter Dropout (HIGH LIKELIHOOD, HIGH IMPACT)

**Risk:**  
Student spotters lose motivation after Week 1, data becomes stale, users lose trust and abandon app.

**Likelihood:** High (70%) - Volunteer fatigue is common  
**Impact:** High - Stale data = unusable product  

**Mitigation Strategies:**
1. **Incentive System:**
   - Points + leaderboard (gamification)
   - Weekly prize for top spotter (5,000 GEL gift card - budget: 20,000 GEL for 4 weeks)
   - Social recognition (shout-outs in group chat)

2. **Low Effort Updates:**
   - Mobile-optimized dashboard (2 taps to update)
   - Push notifications to remind spotters
   - Target: <30 seconds per update

3. **Backup Plan:**
   - Recruit 3 backup spotters per location (train but hold in reserve)
   - Team members become spotters if dropouts occur
   - Automate with sensors in v2 (pitch to university with MVP data)

**Success Criteria:** 80%+ of updates happening within 10 minutes of target time

---

### Risk 2: Low User Adoption (MEDIUM LIKELIHOOD, HIGH IMPACT)

**Risk:**  
Students don't discover the app or don't see the value; <20 weekly active users.

**Likelihood:** Medium (40%) - Marketing to students is challenging  
**Impact:** High - Can't validate product-market fit  

**Mitigation Strategies:**
1. **Grassroots Marketing:**
   - Personal invitations to interview participants (10 people likely to adopt)
   - Word-of-mouth incentive (share with friend → both get priority feature access)
   - QR codes in high-traffic areas (library entrance, cafeteria)

2. **Reduce Friction:**
   - No login required (remove barrier)
   - Mobile-first (students have phones, not always laptops)
   - <3 second load time (impatient users)

3. **Viral Loop:**
   - Shareable links ("Room K-201 is empty right now!" → link in WhatsApp)
   - Social proof (show "47 students used this today")

**Success Criteria:** 50+ WAU by end of Week 2

---

### Risk 3: Technical Failure During Peak Hours (LOW LIKELIHOOD, MEDIUM IMPACT)

**Risk:**  
Server crashes or API becomes slow during 12-2 PM peak when students need it most.

**Likelihood:** Low (20%) - Simple stack, low traffic expected  
**Impact:** Medium - Bad first impression, but recoverable  

**Mitigation Strategies:**
1. **Stress Testing:**
   - Simulate 100 concurrent users before launch
   - Load test API endpoints

2. **Monitoring & Alerts:**
   - Uptime monitoring (UptimeRobot free tier)
   - Slack alerts if API response time >3 seconds
   - Team member on standby during peak hours Week 1

3. **Graceful Degradation:**
   - Cache last known occupancy data
   - Show "⚠️ Data may be outdated" warning
   - Static message if server fully down: "Check back in 5 minutes"

**Success Criteria:** 95%+ uptime during peak hours (10 AM - 2 PM)

---

### Risk 4: Privacy Concerns (LOW LIKELIHOOD, LOW IMPACT)

**Risk:**  
Students worry about being tracked or data being shared.

**Likelihood:** Low (15%) - No personal data collected  
**Impact:** Low - Can address with clear communication  

**Mitigation Strategies:**
1. **Transparency:**
   - Privacy policy (simple, 1-page)
   - "No personal data collected" badge on homepage
   - Anonymous analytics only

2. **No Authentication:**
   - Users don't create accounts (no email, no phone numbers)
   - Spotters use PIN (not tied to identity)

3. **GDPR-Aligned:**
   - Even though not required (Georgia), follow best practices
   - Users can't be identified from analytics

**Success Criteria:** <5 privacy-related complaints in first month

---

## Open Questions

These are unresolved questions that will be answered during development or early post-launch.

### Question 1: Spotter Compensation
**Question:** Should we offer paid compensation instead of prizes?  
**Options:**
- A) Points + prizes (current plan)
- B) Hourly payment (10 GEL per hour of spotting)
- C) Course credit (negotiate with department)

**Decision Maker:** Team Lead  
**Deadline:** Before spotter recruitment (Week 13)  
**Impact:** Budget, spotter motivation

---

### Question 2: Data Refresh Rate
**Question:** Is 30-second auto-refresh too frequent or not frequent enough?  
**Options:**
- A) 15 seconds (more real-time, higher server load)
- B) 30 seconds (current plan)
- C) 60 seconds (less load, slightly staler data)

**Decision Maker:** Engineering + User Testing  
**Deadline:** During Week 12 development  
**Impact:** User experience, server costs

---

### Question 3: Anonymous vs Authenticated
**Question:** Should we add optional user accounts for favorites/personalization?  
**Tradeoff:**
- Pro: Better personalization, retention tracking
- Con: Adds 2 weeks development, friction for new users

**Decision Maker:** Product Lead after Week 1 analytics  
**Deadline:** Post-launch (informs v1.1 decision)  
**Impact:** v1.1 roadmap

---

### Question 4: University Partnership
**Question:** Should we approach university facilities before or after MVP launch?  
**Options:**
- A) Before launch (ask permission, risk getting blocked)
- B) After launch (show traction, easier to get buy-in)

**Decision Maker:** Team consensus  
**Deadline:** Week 14 (launch week decision point)  
**Impact:** Long-term viability, sensor automation path

---

## Appendix

### Appendix A: Interview Summary

**Total Interviews:** 10  
**Duration:** 20-30 minutes each  
**Method:** In-person, semi-structured, Mom Test approach  

**Key Insights:**
1. **Frequency:** 10/10 students experience problem 2+ times per week
2. **Time Wasted:** Average 15.3 minutes per occurrence (range: 10-25 min)
3. **Peak Hours:** 10 AM - 2 PM (between morning and afternoon classes)
4. **Primary Pain:** Walking to multiple buildings to find space
5. **Current Solutions:** Ask friends (unreliable), sequential building checks (time-consuming)
6. **Mobile-First:** 10/10 would use on phone, 8/10 would NOT download native app
7. **Key Features:** Real-time occupancy (10/10), room-level detail (7/10), capacity filter for groups (3/10)

**See full interview logs:** `/01-discovery/interview-logs/`

---

### Appendix B: Competitive Analysis

**Competitor 1: LibCal (Library Calendar System)**
- Used by US universities for room booking
- Pros: Mature, feature-rich
- Cons: Requires authentication, complex UI, not real-time occupancy
- **Takeaway:** We're simpler, real-time, no auth required

**Competitor 2: SpaceOS**
- Workspace management for coworking spaces
- Pros: Real-time occupancy, sensor integration
- Cons: Enterprise-focused, expensive, overkill for students
- **Takeaway:** We're student-focused, free, mobile-first

**Competitor 3: WhatsApp Groups (Current Solution)**
- Students ask "Is library full?" in group chats
- Pros: Free, familiar, no new app
- Cons: Unreliable, slow responses, no structure
- **Takeaway:** We're structured, reliable, faster

**Conclusion:** No direct competitor for student-focused, real-time, mobile-first study room finder at KIU. Market gap confirmed.

---

### Appendix C: Research Artifacts

**1. Interview Logs:** `/01-discovery/interview-logs/interview-001.md` to `interview-010.md`  
**2. Synthesis Docs:** `/01-discovery/synthesis/patterns-analysis.md`  
**3. ICP v2:** `/01-discovery/synthesis/icp-v2.md`  
**4. Problem Statement:** `/00-foundation/validated-problem-statement.md`  
**5. Usability Test Plan:** `/04-validation/usability-test-plan.md` (for Week 13)

---

### Appendix D: Technical Architecture Diagram

```
┌─────────────────────────────────────────────────────┐
│                   USER DEVICES                      │
│  (Mobile browsers: iOS Safari, Android Chrome)      │
└─────────────────┬───────────────────────────────────┘
                  │
                  │ HTTPS
                  │
┌─────────────────▼───────────────────────────────────┐
│               VERCEL (Frontend Host)                │
│  - React app (Vite build)                          │
│  - Static assets (images, CSS)                     │
│  - CDN distribution                                │
└─────────────────┬───────────────────────────────────┘
                  │
                  │ API Requests
                  │
┌─────────────────▼───────────────────────────────────┐
│            RAILWAY (Backend Host)                   │
│  ┌────────────────────────────────────────────┐    │
│  │  Node.js + Express API                     │    │
│  │  - GET /api/locations                      │    │
│  │  - GET /api/locations/:id                  │    │
│  │  - POST /api/occupancy (auth required)     │    │
│  └────────────┬───────────────────────────────┘    │
│               │                                      │
│  ┌────────────▼───────────────────────────────┐    │
│  │  PostgreSQL Database                       │    │
│  │  - locations table                         │    │
│  │  - rooms table                             │    │
│  │  - occupancy_updates table                 │    │
│  │  - spotters table                          │    │
│  └────────────────────────────────────────────┘    │
└─────────────────────────────────────────────────────┘
```

---

### Appendix E: Glossary

**Spotter:** Student volunteer who manually updates room occupancy data via spotter dashboard

**Freshness:** How recent occupancy data is (e.g., "updated 3 minutes ago")

**Staleness:** When data is too old to be useful (e.g., >10 minutes without update)

**MVP (Minimum Viable Product):** First version with minimum features needed to test value hypothesis

**P0/P1/P2:** Priority levels (P0 = must have, P1 = should have, P2 = nice to have)

**MoSCoW:** Prioritization method (Must have, Should have, Could have, Won't have)

**INVEST:** User story quality criteria (Independent, Negotiable, Valuable, Estimable, Small, Testable)

---

## Document Change Log

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 0.1 | Oct 20, 2025 | Lekso | Initial draft after synthesis |
| 0.2 | Oct 23, 2025 | Dato | Added technical architecture |
| 0.3 | Oct 25, 2025 | Murman | Added user personas, refined priorities |
| 1.0 | Oct 28, 2025 | Lekso | Final review, approved for development |

---

## Approval

**Approved by:**  
✅ Lekso Tevdorashvili (Product Lead) - Oct 28, 2025  
✅ Dato Grigalashvili (Engineering Lead) - Oct 28, 2025  
✅ Murman Kakhiani (Research Lead) - Oct 28, 2025  
✅ Ana Beridze (Design Lead) - Oct 28, 2025  

**Instructor Review:**  
✅ Zeshan Ahmad - Oct 28, 2025  
Feedback: "Excellent scope management. Watch spotter dropout risk closely. Consider university partnership earlier than planned."

---

**This PRD is a living document.** As we learn from users post-launch, we'll update priorities, metrics, and scope for v1.1 and beyond.
