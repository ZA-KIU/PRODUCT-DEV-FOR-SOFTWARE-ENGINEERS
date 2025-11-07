# Sprint Plan: StudySpot MVP
# 8-Week Development Timeline

**Team:** Discovery Engine  
**Sprint Duration:** 2 weeks per sprint  
**Total Sprints:** 4 sprints (8 weeks)  
**Target Launch:** Week 15 (December 15, 2025)  
**Planning Date:** October 28, 2025

---

## Table of Contents

1. [Sprint Planning Overview](#sprint-planning-overview)
2. [Team Capacity & Velocity](#team-capacity--velocity)
3. [Sprint 1: Foundation (Weeks 8-9)](#sprint-1-foundation-weeks-8-9)
4. [Sprint 2: Core Features (Weeks 10-11)](#sprint-2-core-features-weeks-10-11)
5. [Sprint 3: Polish & Testing (Weeks 12-13)](#sprint-3-polish--testing-weeks-12-13)
6. [Sprint 4: Launch Prep (Week 14)](#sprint-4-launch-prep-week-14)
7. [Daily Standup Template](#daily-standup-template)
8. [Risk Management](#risk-management)
9. [Definition of Done](#definition-of-done)

---

## Sprint Planning Overview

### What is a Sprint?

**Sprint:** A fixed time period (1-2 weeks) where a team commits to completing specific features and delivering shippable code.

**Key Principles:**
- Fixed duration (we're using 2-week sprints)
- Clear goals defined at start
- Daily progress tracking
- Demo at end of each sprint
- Retrospective to improve process

---

### Our Sprint Structure

```
Sprint Planning (Mon Week 1)
    ↓
Daily Standups (Every day, 15 min)
    ↓
Development Work (Mon-Thu of both weeks)
    ↓
Sprint Review/Demo (Fri Week 2)
    ↓
Sprint Retrospective (Fri Week 2)
    ↓
[Break: Weekend]
    ↓
Next Sprint Planning (Mon Week 3)
```

---

### Why 2-Week Sprints?

**Option 1: 1-week sprints**
- ❌ Too fast - constant planning overhead
- ❌ Hard to complete meaningful features
- ✅ Good for very simple tasks

**Option 2: 2-week sprints** ← **We chose this**
- ✅ Enough time to complete 2-3 user stories
- ✅ Regular checkpoints without excessive overhead
- ✅ Standard in industry

**Option 3: 3-week+ sprints**
- ❌ Too long - problems hidden until late
- ❌ Harder to course-correct
- ✅ Good for complex enterprise products (not MVP)

---

## Team Capacity & Velocity

### Team Composition

| Name | Role | Weekly Availability | Skills |
|------|------|-------------------|--------|
| **Lekso** | Product Lead + Frontend | 12 hours/week | React, UI/UX, Project management |
| **Dato** | Engineering Lead + Backend | 15 hours/week | Node.js, PostgreSQL, APIs, DevOps |
| **Murman** | QA + Frontend Support | 10 hours/week | Testing, React basics, User research |
| **Ana** | Design + Frontend Support | 8 hours/week | Figma, CSS, User testing |

**Total Team Capacity:** ~45 hours per week × 2 weeks = **90 hours per sprint**

---

### Velocity Estimation

**Story Points:** We use T-shirt sizing (XS/S/M/L/XL) translated to hours.

| Size | Hours | Examples |
|------|-------|----------|
| **XS** | 2-4 hours | Update text, fix minor bug, add timestamp |
| **S** | 4-8 hours | Build simple UI component, write basic API endpoint |
| **M** | 8-16 hours | Complete feature with frontend + backend |
| **L** | 16-24 hours | Complex feature with multiple components |
| **XL** | 24+ hours | Should be broken down into smaller stories |

**Sprint 1 Velocity (Expected):**
- New to working together: 60-70 hours of actual productive work (out of 90 available)
- Expect 30% overhead: learning, setup, blockers

**Sprint 2-4 Velocity (Expected):**
- Team in rhythm: 70-80 hours productive work
- 20% overhead: normal coordination, testing

---

## Sprint 1: Foundation (Weeks 8-9)
### Goal: Set up infrastructure, design system, and basic data model

**Sprint Dates:** October 28 - November 8, 2025  
**Sprint Goal:** Complete project setup, design mockups, and database schema so we can build features in Sprint 2.

---

### Sprint 1 User Stories

#### US-1.1: Project Setup & Repository [XS - 3 hours]
**Owner:** Dato  
**Priority:** P0  

**Description:**  
Set up GitHub repository, CI/CD pipeline, and development environment.

**Tasks:**
- [ ] Create GitHub repo with README and .gitignore
- [ ] Set up Vite + React project structure
- [ ] Configure ESLint and Prettier
- [ ] Set up Vercel deployment (frontend)
- [ ] Set up Railway account (backend + database)
- [ ] Add all team members as collaborators
- [ ] Document setup instructions in README

**Acceptance Criteria:**
- [ ] All team members can clone repo and run locally
- [ ] Automatic deployment on push to main branch
- [ ] Linting passes on all code

**Dependencies:** None  
**Blockers:** None  
**Estimated:** 3 hours  
**Actual:** _____ hours (fill in after completion)

---

#### US-1.2: Design System & Component Library [M - 12 hours]
**Owner:** Ana (primary), Lekso (support)  
**Priority:** P0  

**Description:**  
Create Figma mockups for all screens and build reusable React component library.

**Tasks:**
- [ ] **Figma:** Create design system (colors, typography, spacing)
- [ ] **Figma:** Design homepage (location list)
- [ ] **Figma:** Design location detail view
- [ ] **Figma:** Design spotter dashboard
- [ ] **React:** Set up Tailwind CSS config with design tokens
- [ ] **React:** Build LocationCard component
- [ ] **React:** Build StatusIndicator component (green/yellow/red)
- [ ] **React:** Build Layout component (header, container)
- [ ] **Documentation:** Component usage examples in Storybook or README

**Acceptance Criteria:**
- [ ] All 3 screens designed in Figma with mobile-first approach
- [ ] Design approved by team (Friday review)
- [ ] 3+ reusable components built and documented
- [ ] Components are responsive (320px - 1440px)
- [ ] Color contrast meets WCAG AA standards

**Dependencies:** None  
**Blockers:** None  
**Estimated:** 12 hours (6 hrs Figma + 6 hrs React)  
**Actual:** _____ hours

---

#### US-1.3: Database Schema & Setup [M - 10 hours]
**Owner:** Dato  
**Priority:** P0  

**Description:**  
Design and implement PostgreSQL database schema for locations, rooms, and occupancy data.

**Tasks:**
- [ ] Design schema diagram (use dbdiagram.io or similar)
- [ ] Create `locations` table (id, name, building, max_capacity, created_at)
- [ ] Create `rooms` table (id, location_id, room_number, floor, max_capacity)
- [ ] Create `occupancy_updates` table (id, room_id, count, timestamp, spotter_id)
- [ ] Create `spotters` table (id, name, pin_hash, points, created_at)
- [ ] Add indexes for performance (location_id, timestamp)
- [ ] Write seed data for 4 locations and ~20 rooms
- [ ] Test queries for common operations

**Acceptance Criteria:**
- [ ] Schema diagram reviewed and approved by team
- [ ] All tables created in Railway PostgreSQL
- [ ] Seed data inserted (4 locations, 20 rooms)
- [ ] Can query latest occupancy for each room (<100ms)
- [ ] Foreign keys and constraints in place

**Dependencies:** Railway account setup (US-1.1)  
**Blockers:** None  
**Estimated:** 10 hours  
**Actual:** _____ hours

---

#### US-1.4: API Foundation & Health Check [S - 6 hours]
**Owner:** Dato  
**Priority:** P0  

**Description:**  
Set up Express.js API server with basic routing and error handling.

**Tasks:**
- [ ] Initialize Node.js + Express project
- [ ] Configure database connection (PostgreSQL client)
- [ ] Set up environment variables (.env for local, Railway for prod)
- [ ] Create `/health` endpoint (returns 200 OK + DB connection status)
- [ ] Create `/api/locations` endpoint stub (returns empty array for now)
- [ ] Add error handling middleware
- [ ] Set up CORS for frontend requests
- [ ] Deploy to Railway, test health endpoint

**Acceptance Criteria:**
- [ ] Express server runs locally on port 3001
- [ ] `/health` endpoint returns JSON with status and timestamp
- [ ] Database connection works (tested via health endpoint)
- [ ] Deployed to Railway, accessible via public URL
- [ ] Frontend can make requests without CORS errors

**Dependencies:** Database setup (US-1.3)  
**Blockers:** None  
**Estimated:** 6 hours  
**Actual:** _____ hours

---

#### US-1.5: Spotter Recruitment Plan [S - 4 hours]
**Owner:** Murman  
**Priority:** P1  

**Description:**  
Create plan to recruit 8 student spotters and draft training materials.

**Tasks:**
- [ ] Draft recruitment message (3 sentences, emphasizes easy + gamified)
- [ ] Identify recruitment channels (WhatsApp groups, Instagram, in-person)
- [ ] Create 1-page "Spotter Guide" explaining role
- [ ] Design simple flyer for library bulletin board
- [ ] Plan incentive structure (points, weekly prizes)
- [ ] Reach out to 15-20 candidates (aim to recruit 10, expect 20% dropout)

**Acceptance Criteria:**
- [ ] Recruitment message finalized and approved by team
- [ ] Spotter Guide document created (simple, visual)
- [ ] 8+ spotters tentatively committed by end of Sprint 1
- [ ] Training session scheduled for Sprint 2 Week 1

**Dependencies:** None  
**Blockers:** None  
**Estimated:** 4 hours  
**Actual:** _____ hours

---

### Sprint 1 Summary

**Total Story Points:** 35 hours estimated  
**Team Capacity:** 90 hours available  
**Buffer:** 55 hours (for overhead, unknowns, learning curve)

**Sprint 1 Backlog:**
```
Week 1 (Oct 28 - Nov 1):
Mon: Sprint planning (2 hrs), US-1.1 kickoff
Tue: US-1.2 (Figma design) + US-1.3 (DB schema design)
Wed: US-1.2 (Figma cont.) + US-1.3 (DB implementation)
Thu: US-1.4 (API setup) + US-1.2 (React components)
Fri: US-1.2 finish, US-1.4 finish, US-1.5 kickoff

Week 2 (Nov 4 - Nov 8):
Mon: US-1.5 (spotter recruitment execution)
Tue: Buffer day (finish any incomplete stories)
Wed: Integration testing (frontend connects to API)
Thu: Documentation, README updates
Fri: Sprint review (demo to instructor), retrospective
```

**Sprint 1 Demo:**
- Show: Design mockups in Figma
- Show: Component library (3+ components) in browser
- Show: Database with seed data (via API or DB client)
- Show: API health endpoint returning 200 OK
- Show: Spotter recruitment progress (8+ committed)

---

## Sprint 2: Core Features (Weeks 10-11)
### Goal: Build and integrate main user-facing features

**Sprint Dates:** November 11 - November 22, 2025  
**Sprint Goal:** Users can see real-time occupancy data and spotters can update it.

---

### Sprint 2 User Stories

#### US-2.1: Location List Page (Frontend) [M - 12 hours]
**Owner:** Lekso  
**Priority:** P0  

**Description:**  
Build homepage that displays list of 4 study locations with occupancy data.

**Tasks:**
- [ ] Create `/` route in React Router
- [ ] Build `HomePage` component with grid/list of locations
- [ ] Integrate `LocationCard` component (from Sprint 1)
- [ ] Fetch data from `/api/locations` on mount
- [ ] Display loading state while fetching
- [ ] Display error state if API fails
- [ ] Add auto-refresh every 30 seconds (useEffect with interval)
- [ ] Show "Last updated" timestamp for each location
- [ ] Add manual refresh button
- [ ] Make responsive (mobile-first, then desktop)

**Acceptance Criteria:**
- [ ] Page loads in <3 seconds on 4G
- [ ] Shows 4 locations with: name, building, occupancy (X/Y), status color
- [ ] Auto-refreshes every 30 seconds without user action
- [ ] Manual refresh button works, shows loading spinner
- [ ] Error message displays if API fails
- [ ] Responsive on 320px - 1440px screens

**Dependencies:** Design system (US-1.2), API foundation (US-1.4)  
**Blockers:** None  
**Estimated:** 12 hours  
**Actual:** _____ hours

---

#### US-2.2: Locations API Endpoint [M - 10 hours]
**Owner:** Dato  
**Priority:** P0  

**Description:**  
Implement `/api/locations` endpoint that returns current occupancy for all locations.

**Tasks:**
- [ ] Create `GET /api/locations` endpoint
- [ ] Write SQL query to join locations + rooms + latest occupancy_updates
- [ ] Calculate current occupancy per location (sum of room occupancies)
- [ ] Calculate occupancy percentage and status (green/yellow/red)
- [ ] Return JSON with location details + occupancy data
- [ ] Add caching (cache for 30 seconds to reduce DB load)
- [ ] Add error handling (return 500 if DB query fails)
- [ ] Write unit tests for endpoint logic
- [ ] Test with Postman/curl
- [ ] Deploy to Railway

**Acceptance Criteria:**
- [ ] Endpoint returns JSON array of 4 locations
- [ ] Each location includes: id, name, building, current_occupancy, max_capacity, status (green/yellow/red), last_updated (timestamp)
- [ ] Response time <500ms (p95)
- [ ] Handles DB connection errors gracefully
- [ ] 30-second cache reduces load
- [ ] Unit tests cover happy path and error cases

**Dependencies:** Database (US-1.3), API foundation (US-1.4)  
**Blockers:** Need seed occupancy data  
**Estimated:** 10 hours  
**Actual:** _____ hours

---

#### US-2.3: Location Detail Page (Frontend) [M - 10 hours]
**Owner:** Lekso, Ana (CSS support)  
**Priority:** P0  

**Description:**  
Build detail page showing room-by-room breakdown for a selected location.

**Tasks:**
- [ ] Create `/location/:id` route
- [ ] Build `LocationDetailPage` component
- [ ] Fetch data from `/api/locations/:id` on mount
- [ ] Display location header (building name, floor navigation)
- [ ] List all rooms with: room number, occupancy (X/Y), status color
- [ ] Group rooms by floor (if applicable)
- [ ] Add "Back" button to return to homepage
- [ ] Add amenity icons (power, whiteboard, quiet) if in room data
- [ ] Add loading and error states
- [ ] Make responsive

**Acceptance Criteria:**
- [ ] Clicking location on homepage navigates to detail page
- [ ] Detail page shows all rooms for that location
- [ ] Each room shows: number, occupancy, status indicator
- [ ] Back button returns to homepage
- [ ] Page loads instantly (data pre-fetched on homepage)
- [ ] Responsive design works on mobile + desktop

**Dependencies:** Location list page (US-2.1), location detail API (US-2.4)  
**Blockers:** None  
**Estimated:** 10 hours  
**Actual:** _____ hours

---

#### US-2.4: Location Detail API Endpoint [S - 6 hours]
**Owner:** Dato  
**Priority:** P0  

**Description:**  
Implement `/api/locations/:id` endpoint returning room-level occupancy for one location.

**Tasks:**
- [ ] Create `GET /api/locations/:id` endpoint
- [ ] Write SQL query to get all rooms for a location
- [ ] Join with latest occupancy_updates for each room
- [ ] Return JSON with location info + array of rooms
- [ ] Add error handling (404 if location doesn't exist)
- [ ] Cache for 30 seconds
- [ ] Test with Postman
- [ ] Deploy to Railway

**Acceptance Criteria:**
- [ ] Endpoint returns location object with rooms array
- [ ] Each room includes: id, room_number, floor, current_occupancy, max_capacity, status, amenities
- [ ] Returns 404 if location ID doesn't exist
- [ ] Response time <500ms
- [ ] Unit tests cover happy path and 404 case

**Dependencies:** Locations API (US-2.2)  
**Blockers:** None  
**Estimated:** 6 hours  
**Actual:** _____ hours

---

#### US-2.5: Spotter Dashboard (Frontend) [M - 14 hours]
**Owner:** Murman (primary), Lekso (support)  
**Priority:** P0  

**Description:**  
Build separate web interface for spotters to update occupancy data.

**Tasks:**
- [ ] Create `/spotter` route (separate from main app)
- [ ] Build SpotterLoginPage component (simple PIN entry)
- [ ] Build SpotterDashboard component
- [ ] Show list of locations assigned to spotter
- [ ] For each location, show current occupancy with +/- buttons
- [ ] Validate input (can't exceed max capacity)
- [ ] Build "Submit Update" button
- [ ] Show success/error feedback after submission
- [ ] Add leaderboard view (points for each spotter)
- [ ] Make mobile-optimized (spotters use phones)
- [ ] Add offline support (queue updates, sync when online)

**Acceptance Criteria:**
- [ ] Spotter can log in with 4-digit PIN
- [ ] Dashboard shows spotter's assigned locations
- [ ] Can update occupancy with +/- buttons (large touch targets)
- [ ] Submit button sends data to API
- [ ] Success message shows after submit
- [ ] Validation prevents occupancy > max capacity
- [ ] Leaderboard shows all spotters with points
- [ ] Works offline, syncs when connection restored
- [ ] Mobile-optimized (buttons 44px+, readable text)

**Dependencies:** Design mockups (US-1.2), spotter API (US-2.6)  
**Blockers:** None  
**Estimated:** 14 hours  
**Actual:** _____ hours

---

#### US-2.6: Spotter Update API Endpoint [M - 8 hours]
**Owner:** Dato  
**Priority:** P0  

**Description:**  
Implement `POST /api/occupancy` endpoint for spotters to submit updates.

**Tasks:**
- [ ] Create `POST /api/occupancy` endpoint
- [ ] Add simple PIN-based auth middleware (check spotter exists)
- [ ] Validate request body (room_id, occupancy_count)
- [ ] Validate occupancy_count <= room max_capacity
- [ ] Insert occupancy_update record into database
- [ ] Update spotter points (+1 for each update)
- [ ] Return success JSON with new occupancy data
- [ ] Add error handling (401 if auth fails, 400 if validation fails)
- [ ] Log all updates for debugging
- [ ] Test with Postman
- [ ] Deploy to Railway

**Acceptance Criteria:**
- [ ] Endpoint requires spotter PIN in request header or body
- [ ] Returns 401 if PIN invalid
- [ ] Returns 400 if occupancy > max capacity
- [ ] Returns 200 with updated occupancy data if successful
- [ ] Spotter points increment by 1 per update
- [ ] Update appears immediately in GET /api/locations
- [ ] Unit tests cover auth, validation, happy path

**Dependencies:** Database (US-1.3), spotters table with PINs  
**Blockers:** None  
**Estimated:** 8 hours  
**Actual:** _____ hours

---

#### US-2.7: Spotter Onboarding & Training [S - 4 hours]
**Owner:** Murman  
**Priority:** P1  

**Description:**  
Train 8 recruited spotters on how to use dashboard and update occupancy.

**Tasks:**
- [ ] Finalize "Spotter Guide" document (1-page with screenshots)
- [ ] Create PINs for each spotter in database
- [ ] Test spotter dashboard with 2-3 spotters
- [ ] Hold 30-minute training session (in-person or Zoom)
- [ ] Walk through: login, update process, leaderboard
- [ ] Answer questions, collect feedback
- [ ] Share PINs securely (not in group chat)
- [ ] Get commitment: 2 updates per day minimum

**Acceptance Criteria:**
- [ ] 8+ spotters trained and have PINs
- [ ] Each spotter successfully submits test update during training
- [ ] Spotter Guide document finalized and shared
- [ ] Spotters commit to 2 updates/day schedule
- [ ] Training feedback collected (what's confusing?)

**Dependencies:** Spotter dashboard (US-2.5), spotter API (US-2.6)  
**Blockers:** None  
**Estimated:** 4 hours  
**Actual:** _____ hours

---

### Sprint 2 Summary

**Total Story Points:** 64 hours estimated  
**Team Capacity:** 90 hours available  
**Buffer:** 26 hours

**Sprint 2 Backlog:**
```
Week 1 (Nov 11 - Nov 15):
Mon: Sprint planning, US-2.2 kickoff (API first!)
Tue: US-2.2 (locations API), US-2.1 kickoff (homepage)
Wed: US-2.1 (homepage cont.), US-2.4 (detail API)
Thu: US-2.3 (detail page), US-2.6 (spotter API)
Fri: US-2.5 kickoff (spotter dashboard)

Week 2 (Nov 18 - Nov 22):
Mon: US-2.5 cont. (spotter dashboard)
Tue: US-2.5 finish, integration testing
Wed: US-2.7 (spotter training)
Thu: Bug fixes, polish
Fri: Sprint review, retrospective
```

**Sprint 2 Demo:**
- Show: Homepage with 4 locations and live occupancy data
- Show: Detail page with room breakdown
- Show: Spotter dashboard + submit update
- Show: Update appearing in user-facing app within 30 seconds
- Show: 8 trained spotters ready to go

---

## Sprint 3: Polish & Testing (Weeks 12-13)
### Goal: Fix bugs, add critical UX improvements, conduct user testing

**Sprint Dates:** November 25 - December 6, 2025  
**Sprint Goal:** App is stable, fast, and tested with real users.

---

### Sprint 3 User Stories

#### US-3.1: Performance Optimization [M - 10 hours]
**Owner:** Dato (primary), Lekso (frontend)  
**Priority:** P0  

**Description:**  
Optimize page load times and API response times to meet <3 second target.

**Tasks:**
- [ ] Profile homepage load time (use Lighthouse, Chrome DevTools)
- [ ] Optimize images (compress, use WebP format)
- [ ] Code-split React bundles (lazy load detail page)
- [ ] Add React.memo to prevent unnecessary re-renders
- [ ] Optimize SQL queries (add indexes if missing)
- [ ] Implement API response caching (Redis or in-memory)
- [ ] Minify CSS and JavaScript for production
- [ ] Test on slow 3G connection
- [ ] Measure before/after metrics

**Acceptance Criteria:**
- [ ] Homepage loads in <3 seconds on 4G (Lighthouse test)
- [ ] API response time <500ms (p95)
- [ ] Lighthouse Performance score >85
- [ ] App works on slow 3G (may load slower, but doesn't break)

**Dependencies:** Core features complete (Sprint 2)  
**Blockers:** None  
**Estimated:** 10 hours  
**Actual:** _____ hours

---

#### US-3.2: Data Freshness Improvements [S - 6 hours]
**Owner:** Lekso  
**Priority:** P0  

**Description:**  
Improve how freshness indicators work and add warnings for stale data.

**Tasks:**
- [ ] Add timestamp to each location card: "Updated 3 min ago"
- [ ] Calculate time since last update (use moment.js or date-fns)
- [ ] Show warning icon if data >5 minutes old: ⚠️ "May be outdated"
- [ ] Show error state if data >15 minutes old: ❌ "Unable to get current status"
- [ ] Update timestamp every 30 seconds (match auto-refresh)
- [ ] Add tooltip on hover explaining what timestamp means
- [ ] Test edge cases (no updates ever, very old updates)

**Acceptance Criteria:**
- [ ] Every location shows "Updated X min ago" timestamp
- [ ] Warning appears at 5 min threshold
- [ ] Error state appears at 15 min threshold
- [ ] Timestamp updates every 30 seconds without refresh
- [ ] Clear visual difference between fresh/stale/error states

**Dependencies:** Location list page (US-2.1)  
**Blockers:** None  
**Estimated:** 6 hours  
**Actual:** _____ hours

---

#### US-3.3: Accessibility Improvements [M - 8 hours]
**Owner:** Ana (primary), Lekso (implementation)  
**Priority:** P1  

**Description:**  
Ensure app is accessible to screen reader users and meets WCAG AA standards.

**Tasks:**
- [ ] Add alt text to all icons and images
- [ ] Add ARIA labels to interactive elements (buttons, links)
- [ ] Test with screen reader (iOS VoiceOver or NVDA)
- [ ] Ensure keyboard navigation works (tab through all elements)
- [ ] Add focus indicators (visible outline on focused element)
- [ ] Check color contrast with tool (WebAIM contrast checker)
- [ ] Add skip-to-content link for screen reader users
- [ ] Test with accessibility checker (axe DevTools)
- [ ] Fix any critical issues flagged

**Acceptance Criteria:**
- [ ] All interactive elements keyboard-accessible
- [ ] Screen reader can navigate and understand all content
- [ ] Color contrast meets WCAG AA (4.5:1 for text)
- [ ] Focus indicators visible on all elements
- [ ] No critical accessibility errors in axe DevTools
- [ ] Status indicators use text + color (not color alone)

**Dependencies:** Core features complete  
**Blockers:** None  
**Estimated:** 8 hours  
**Actual:** _____ hours

---

#### US-3.4: Error Handling & Edge Cases [M - 8 hours]
**Owner:** Dato (backend), Murman (QA)  
**Priority:** P0  

**Description:**  
Handle all error cases gracefully and test edge cases.

**Tasks:**
- [ ] Add error handling for: API down, slow API, DB connection failed
- [ ] Add error handling for: invalid location ID, room ID doesn't exist
- [ ] Show user-friendly error messages (not technical error codes)
- [ ] Add retry logic for failed API requests (max 3 retries)
- [ ] Test with API deliberately broken (offline mode)
- [ ] Test with invalid data in database (null values, negative numbers)
- [ ] Add logging for all errors (use console.error or logging service)
- [ ] Create error state designs (Ana)
- [ ] Document error scenarios in QA test plan

**Acceptance Criteria:**
- [ ] App never shows white screen / crashes
- [ ] Every error case shows user-friendly message
- [ ] Retry logic works (retries 3 times then shows error)
- [ ] Errors logged for debugging
- [ ] QA test plan covers 10+ error scenarios

**Dependencies:** All previous features  
**Blockers:** None  
**Estimated:** 8 hours  
**Actual:** _____ hours

---

#### US-3.5: User Testing Round 1 [L - 16 hours]
**Owner:** Murman (primary), Ana (support), Entire team (observe)  
**Priority:** P0  

**Description:**  
Conduct usability testing with 5 external students to identify issues.

**Tasks:**
- [ ] Recruit 5 students who match ICP (not from interviews)
- [ ] Create usability test script (tasks + questions)
- [ ] Set up test environment (staging site, observation tools)
- [ ] Conduct 5 tests (30 min each, 1-on-1)
- [ ] Record observations (notes + screen recording)
- [ ] Identify top 3-5 issues (broken features, confusing UX)
- [ ] Synthesize findings into report
- [ ] Prioritize fixes for Sprint 3 Week 2
- [ ] Share findings with team

**Test Tasks:**
1. "You have a 2-hour gap before your next class. Use this app to find an available study room."
2. "Find a specific room: K-201. Is it available right now?"
3. "Check which building has the most available seats."
4. [Observe if they understand status indicators without explanation]
5. [Observe if they trust the data / look for timestamps]

**Acceptance Criteria:**
- [ ] 5 usability tests completed
- [ ] Top 5 issues documented with severity (critical/major/minor)
- [ ] Recommendations prioritized for fixing
- [ ] Team agrees on which issues to fix in Sprint 3 Week 2
- [ ] Usability test report shared with instructor

**Dependencies:** Core features working (Sprint 2)  
**Blockers:** Recruiting participants  
**Estimated:** 16 hours (spread across team)  
**Actual:** _____ hours

---

#### US-3.6: Bug Fixes from User Testing [L - 16 hours]
**Owner:** Entire team (divide and conquer)  
**Priority:** P0  

**Description:**  
Fix critical and major issues identified in user testing.

**Tasks:**
- [ ] Review usability test findings
- [ ] Prioritize issues: critical (breaks core flow), major (confusing), minor (polish)
- [ ] Assign critical issues to team members
- [ ] Fix critical issues first
- [ ] Fix major issues if time permits
- [ ] Re-test fixes with 1-2 users
- [ ] Document any minor issues for post-launch (v1.1)

**Acceptance Criteria:**
- [ ] All critical issues fixed and tested
- [ ] 80%+ of major issues fixed
- [ ] No regressions (old features still work)
- [ ] At least 1 re-test confirms fixes work

**Dependencies:** User testing (US-3.5)  
**Blockers:** Severity of issues (if too many critical issues, may spill into Sprint 4)  
**Estimated:** 16 hours  
**Actual:** _____ hours

---

### Sprint 3 Summary

**Total Story Points:** 64 hours estimated  
**Team Capacity:** 90 hours available  
**Buffer:** 26 hours (good buffer for unexpected bugs)

**Sprint 3 Backlog:**
```
Week 1 (Nov 25 - Nov 29):
Mon: Sprint planning, US-3.5 prep (recruit participants)
Tue: US-3.1 (performance optimization)
Wed: US-3.2 (freshness indicators), US-3.3 (accessibility)
Thu: US-3.4 (error handling), US-3.5 conduct tests 1-3
Fri: US-3.5 conduct tests 4-5, synthesize findings

Week 2 (Dec 2 - Dec 6):
Mon: US-3.6 (bug fixes from testing)
Tue: US-3.6 cont.
Wed: Re-testing fixes, polish
Thu: Final QA pass (entire team)
Fri: Sprint review, retrospective, launch prep planning
```

**Sprint 3 Demo:**
- Show: Performance improvements (Lighthouse score)
- Show: Accessibility features (screen reader demo)
- Show: Error handling (simulate API failure)
- Show: Usability test findings + fixes implemented
- Declare: "Ready to launch" ✅

---

## Sprint 4: Launch Prep (Week 14)
### Goal: Soft launch, final polish, marketing, and monitoring

**Sprint Dates:** December 9 - December 13, 2025  
**Sprint Goal:** Public launch with 50+ users by end of week.

---

### Sprint 4 User Stories

#### US-4.1: Soft Launch with Beta Testers [M - 8 hours]
**Owner:** Murman (primary), Entire team (support)  
**Priority:** P0  

**Description:**  
Launch to 20 beta testers, monitor closely for issues.

**Tasks:**
- [ ] Recruit 20 beta testers (from interviews + usability tests)
- [ ] Send launch email with instructions and survey link
- [ ] Monitor analytics dashboard hourly (Mon-Wed)
- [ ] Respond to bug reports within 2 hours
- [ ] Collect feedback via post-use survey
- [ ] Fix any critical bugs immediately
- [ ] Check spotter activity (are they updating regularly?)
- [ ] Communicate with spotters daily

**Acceptance Criteria:**
- [ ] 20 beta testers invited and confirmed
- [ ] At least 15/20 use app in first 3 days
- [ ] No critical bugs reported
- [ ] Spotter update frequency >80% (8+ updates per day target)
- [ ] Initial feedback collected (5+ survey responses)

**Dependencies:** Sprint 3 complete  
**Blockers:** None  
**Estimated:** 8 hours  
**Actual:** _____ hours

---

#### US-4.2: Marketing & Launch Communications [M - 10 hours]
**Owner:** Lekso (primary), Ana (graphics), Entire team (share)  
**Priority:** P0  

**Description:**  
Execute marketing plan to drive awareness and adoption.

**Tasks:**
- [ ] Finalize launch message (3 sentences, compelling)
- [ ] Design QR code flyer for physical locations (library, cafeteria)
- [ ] Post in KIU CS WhatsApp group (Lekso)
- [ ] Post in KIU Student WhatsApp group (entire team shares)
- [ ] Create Instagram story graphic (Ana)
- [ ] Post on personal Instagram stories (entire team)
- [ ] Request 2-min announcement in 3 classes (friendly professors)
- [ ] Print 20 flyers, post around campus (high-traffic areas)
- [ ] Track which channel drives most traffic (UTM parameters)

**Acceptance Criteria:**
- [ ] Launch message approved by team
- [ ] Flyer designed, printed, and posted (20 copies)
- [ ] Posted in at least 2 WhatsApp groups
- [ ] Instagram story posted by all 4 team members
- [ ] In-class announcements made in 3 classes
- [ ] UTM tracking set up to measure channel effectiveness

**Dependencies:** Soft launch complete (US-4.1)  
**Blockers:** Getting professor approval for announcements  
**Estimated:** 10 hours  
**Actual:** _____ hours

---

#### US-4.3: Analytics & Monitoring Setup [S - 6 hours]
**Owner:** Dato  
**Priority:** P0  

**Description:**  
Set up comprehensive analytics and monitoring for launch week.

**Tasks:**
- [ ] Set up Google Analytics 4 property
- [ ] Add GA4 tracking code to all pages
- [ ] Create custom events: location_clicked, manual_refresh, occupancy_viewed
- [ ] Set up custom dashboard in GA4 (DAU, sessions, events)
- [ ] Set up Uptime monitoring (UptimeRobot free tier)
- [ ] Set up Slack alerts for: API errors, server downtime, slow response times
- [ ] Create simple daily report template (DAU, top locations, issues)
- [ ] Document how to access analytics for team

**Acceptance Criteria:**
- [ ] GA4 tracking all page views and events
- [ ] Custom dashboard shows key metrics (DAU, sessions, time-to-decision)
- [ ] Uptime monitoring sends alert if site goes down
- [ ] Slack alerts working (test by breaking something)
- [ ] Team can access and understand analytics dashboard

**Dependencies:** None  
**Blockers:** None  
**Estimated:** 6 hours  
**Actual:** _____ hours

---

#### US-4.4: Public Launch (Thu) [S - 4 hours]
**Owner:** Entire team (all hands on deck)  
**Priority:** P0  

**Description:**  
Execute public launch and monitor closely for first 48 hours.

**Tasks:**
- [ ] Final smoke test (entire team tests on own devices)
- [ ] Deploy to production (Dato)
- [ ] Announce in all channels (messages pre-written in US-4.2)
- [ ] Monitor analytics every 2 hours (Thu + Fri)
- [ ] Respond to user questions on WhatsApp within 1 hour
- [ ] Fix any critical bugs immediately (entire team ready)
- [ ] Celebrate first 10 users 🎉
- [ ] Celebrate 50 users milestone 🎉
- [ ] Check spotter activity (ping if updates dropping off)

**Acceptance Criteria:**
- [ ] App live and accessible to public
- [ ] Launch announced in all planned channels
- [ ] 50+ users within 48 hours (Fri end of day)
- [ ] No downtime during peak hours (10 AM - 2 PM)
- [ ] Response time to user questions <1 hour
- [ ] Critical bugs (if any) fixed same-day

**Dependencies:** Soft launch successful (US-4.1), marketing ready (US-4.2)  
**Blockers:** None  
**Estimated:** 4 hours active work + monitoring  
**Actual:** _____ hours

---

#### US-4.5: Post-Launch Survey & Iteration Plan [S - 6 hours]
**Owner:** Murman  
**Priority:** P1  

**Description:**  
Collect user feedback and plan v1.1 features for Week 15+.

**Tasks:**
- [ ] Create post-launch survey (5 questions max)
  1. Did you save time? (Yes/No/Unsure)
  2. How much time? (Open text)
  3. Would you recommend to a friend? (0-10 scale - NPS)
  4. What's most confusing? (Open text)
  5. What feature do you want next? (Multiple choice)
- [ ] Add survey link to app footer
- [ ] Send survey link to beta testers
- [ ] Collect 30+ responses by end of Week 14
- [ ] Synthesize feedback into report
- [ ] Prioritize top 3 requested features for v1.1
- [ ] Draft v1.1 roadmap (2-week plan)

**Acceptance Criteria:**
- [ ] Survey live and linked in app
- [ ] 30+ responses collected
- [ ] Feedback synthesized: NPS score, top issues, top feature requests
- [ ] v1.1 roadmap drafted (top 3 features, effort estimates)
- [ ] Report shared with team and instructor

**Dependencies:** Public launch (US-4.4)  
**Blockers:** None  
**Estimated:** 6 hours  
**Actual:** _____ hours

---

### Sprint 4 Summary

**Total Story Points:** 34 hours estimated  
**Team Capacity:** 45 hours (Week 14 only, then Week 15 is final presentation)  
**Buffer:** 11 hours

**Sprint 4 Backlog:**
```
Week 14 (Dec 9 - Dec 13):
Mon: Sprint planning, US-4.1 (soft launch), US-4.3 (analytics)
Tue: US-4.1 cont., monitor beta users
Wed: US-4.2 (marketing prep), final polish
Thu: US-4.4 (PUBLIC LAUNCH) 🚀
Fri: Monitor launch, US-4.5 (survey), celebrate 🎉
```

**Sprint 4 Demo (Final Presentation Week 15):**
- Show: Live app with 50+ users
- Show: Analytics dashboard (DAU, usage patterns)
- Show: User testimonials / NPS results
- Show: Lessons learned + v1.1 roadmap
- Present: Entire product journey (problem → MVP → launch)

---

## Daily Standup Template

**When:** Every day at 10:00 AM (15 minutes max)  
**Where:** Discord voice channel or in-person

**Format:** Each person answers 3 questions:
1. **What did I complete yesterday?**
2. **What will I work on today?**
3. **Any blockers?**

**Example:**
```
Lekso:
✅ Yesterday: Finished location list page, deployed to staging
📅 Today: Start location detail page, test on mobile
🚫 Blockers: None

Dato:
✅ Yesterday: Built locations API, added caching
📅 Today: Build location detail API, fix CORS issue
🚫 Blockers: Need clarification on room amenities data structure

Murman:
✅ Yesterday: Recruited 6 spotters, scheduled training
📅 Today: Recruit 2 more spotters, draft spotter guide
🚫 Blockers: Waiting on spotter dashboard design from Ana

Ana:
✅ Yesterday: Finished Figma mockups for all 3 screens
📅 Today: Build design system in Tailwind, start components
🚫 Blockers: None
```

**Scrum Master role:** Rotates weekly. Responsibilities:
- Start standup on time
- Keep it to 15 minutes (use timer)
- Note any blockers that need follow-up
- Update sprint board after standup

---

## Risk Management

### Risk Matrix

| Risk | Likelihood | Impact | Mitigation | Owner |
|------|------------|--------|------------|-------|
| **Spotter dropout** | High | High | Gamification, backup spotters, team becomes spotters if needed | Murman |
| **Scope creep** | Medium | High | Strict "no new features" rule until MVP shipped | Lekso |
| **Technical blockers** | Medium | Medium | Daily standups catch early, pair programming | Dato |
| **Low user adoption** | Medium | High | Grassroots marketing, personal invitations, QR codes | Murman |
| **Team member unavailability** | Low | Medium | Cross-training, clear documentation, overlap in skills | Lekso |
| **API performance issues** | Low | High | Caching, load testing, monitoring | Dato |

---

### Contingency Plans

**If we're behind schedule after Sprint 1:**
- Cut US-1.5 (spotter recruitment) → do in Sprint 2 Week 1
- Reduce design polish → focus on functionality

**If we're behind schedule after Sprint 2:**
- Cut accessibility improvements (US-3.3) → do post-launch
- Reduce user testing from 5 to 3 participants
- Deploy with known minor bugs, fix in Sprint 4

**If critical bug found during launch:**
- All hands on deck (entire team drops everything)
- Fix within 4 hours or roll back to previous version
- Communicate issue to users via WhatsApp

---

## Definition of Done

A user story is "done" when:

### Code Complete
- [ ] Feature works as described in acceptance criteria
- [ ] Code reviewed by at least 1 other team member
- [ ] No linting errors
- [ ] Works on mobile and desktop (if applicable)

### Tested
- [ ] Manually tested by developer
- [ ] Tested by QA (Murman) or another team member
- [ ] Works on at least 2 devices (iOS + Android or Chrome + Safari)
- [ ] Edge cases tested (empty states, errors, slow connection)

### Deployed
- [ ] Merged to main branch
- [ ] Deployed to production (auto-deploy via Vercel/Railway)
- [ ] Smoke tested in production environment

### Documented
- [ ] README updated if setup changed
- [ ] API documentation updated (if backend change)
- [ ] User-facing documentation updated (if needed)

---

## Key Takeaways

1. **Sprints create rhythm** - 2-week cycles with clear goals
2. **Daily standups catch blockers early** - 15 min every morning
3. **Capacity planning prevents burnout** - 45 hrs/week is realistic for students
4. **Sprint review keeps team aligned** - Friday demos show progress
5. **Retrospectives improve process** - "What went well? What to improve?"
6. **Buffer time is essential** - Always have 20-30% unallocated time
7. **Definition of Done prevents confusion** - Everyone knows when story is complete

---

**Next Steps:**
- Use this sprint plan as your roadmap
- Adjust story estimates as you learn team velocity
- Don't be afraid to move stories between sprints
- Celebrate small wins every Friday
- Launch your MVP by Week 15! 🚀
