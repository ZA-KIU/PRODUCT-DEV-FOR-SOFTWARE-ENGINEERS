# Event Schema Design

**Team:** [Your Team Name]  
**Date:** [Date]  
**Product:** [Your Product Name]  
**Version:** 1.0 (MVP)

---

## Overview

This document defines the **event schema** for our product's analytics instrumentation. Every user action we want to track must be captured as an event with standardized properties.

**Purpose:**
- Enable data-driven product decisions
- Track our North Star Metric and AARRR funnel
- Identify user behavior patterns and friction points
- Measure feature adoption and engagement

---

## Event Naming Conventions

**Format:** `object_action` (snake_case)

**Examples:**
- ✅ `study_session_started`
- ✅ `user_signup_completed`
- ✅ `resource_shared`
- ❌ `StudySessionStarted` (wrong case)
- ❌ `start_study_session` (wrong order)
- ❌ `study_session_start` (inconsistent verb tense)

**Rules:**
1. Always lowercase with underscores
2. Format: `[object]_[action]` (noun first, verb second)
3. Use past tense for completed actions: `_completed`, `_created`, `_deleted`
4. Use present tense for ongoing: `_started`, `_viewed`
5. Be specific: `session_started` not `action_performed`

---

## Standard Properties (All Events)

These properties MUST be included with every event:

| Property Name | Type | Description | Example |
|---------------|------|-------------|---------|
| `event_id` | string (UUID) | Unique identifier for this event | `"550e8400-e29b-41d4-a716-446655440000"` |
| `user_id` | string (UUID) | Unique identifier for the user | `"user_12345"` |
| `timestamp` | ISO 8601 datetime | When the event occurred | `"2025-10-30T14:23:45Z"` |
| `session_id` | string (UUID) | Current user session | `"session_67890"` |
| `platform` | enum | Where event occurred | `"web"`, `"ios"`, `"android"` |
| `app_version` | string | Application version | `"1.0.3"` |
| `environment` | enum | Deployment environment | `"production"`, `"staging"`, `"development"` |

---

## Core Events (6-10 Required for MVP)

### Event 1: User Signup Started

**Event Name:** `user_signup_started`

**When it fires:** User clicks "Sign Up" button and signup form is displayed

**Why we track it:** Measures top of funnel (Acquisition stage in AARRR)

**Standard Properties:** (All events include standard properties above)

**Custom Properties:**

| Property Name | Type | Required | Description | Example Values |
|---------------|------|----------|-------------|----------------|
| `signup_method` | enum | Yes | How user is signing up | `"email"`, `"google"`, `"facebook"` |
| `referral_source` | string | No | How user found us | `"google"`, `"friend_referral"`, `"instagram"` |
| `utm_campaign` | string | No | Marketing campaign | `"fall_2025_launch"` |
| `utm_source` | string | No | Traffic source | `"instagram"`, `"tiktok"` |
| `utm_medium` | string | No | Marketing medium | `"social"`, `"email"` |

**Example Event Payload:**
```json
{
  "event_name": "user_signup_started",
  "event_id": "550e8400-e29b-41d4-a716-446655440000",
  "user_id": "anonymous_abc123",
  "timestamp": "2025-10-30T14:23:45Z",
  "session_id": "session_67890",
  "platform": "web",
  "app_version": "1.0.0",
  "environment": "production",
  "signup_method": "google",
  "referral_source": "instagram",
  "utm_campaign": "fall_2025_launch"
}
```

---

### Event 2: User Signup Completed

**Event Name:** `user_signup_completed`

**When it fires:** User successfully completes signup and account is created

**Why we track it:** Measures conversion from signup start → complete. Critical for Acquisition.

**Custom Properties:**

| Property Name | Type | Required | Description | Example Values |
|---------------|------|----------|-------------|----------------|
| `signup_method` | enum | Yes | Method used to sign up | `"email"`, `"google"`, `"facebook"` |
| `account_type` | enum | Yes | Type of account created | `"student"`, `"faculty"`, `"admin"` |
| `time_to_complete` | integer | Yes | Seconds from start to completion | `45`, `120` |
| `referral_code` | string | No | If user used referral code | `"FRIEND2025"` |

**Relationship to other events:**
- Follows: `user_signup_started`
- Conversion metric: `signup_completed / signup_started` = Signup Completion Rate

---

### Event 3: [Your Core Event Name]

**Event Name:** `[object_action]`

**When it fires:** [Specific user action that triggers this event]

**Why we track it:** [Which metric/stage this supports - reference NSM or AARRR stage]

**Custom Properties:**

| Property Name | Type | Required | Description | Example Values |
|---------------|------|----------|-------------|----------------|
| `[property_1]` | [type] | Yes/No | [Description] | [Examples] |
| `[property_2]` | [type] | Yes/No | [Description] | [Examples] |
| `[property_3]` | [type] | Yes/No | [Description] | [Examples] |

**Example Event Payload:**
```json
{
  "event_name": "[event_name]",
  "event_id": "...",
  "user_id": "...",
  "timestamp": "...",
  "session_id": "...",
  "platform": "...",
  "app_version": "...",
  "environment": "...",
  "[custom_property_1]": "[value]",
  "[custom_property_2]": "[value]"
}
```

---

### Event 4: [Your Core Event Name]

**Event Name:** `[object_action]`

**When it fires:** [Description]

**Why we track it:** [Metric/stage this supports]

**Custom Properties:**

| Property Name | Type | Required | Description | Example Values |
|---------------|------|----------|-------------|----------------|
| `[property_1]` | [type] | Yes/No | [Description] | [Examples] |
| `[property_2]` | [type] | Yes/No | [Description] | [Examples] |

---

### Event 5: [Your Core Event Name]

**Event Name:** `[object_action]`

**When it fires:** [Description]

**Why we track it:** [Metric/stage this supports]

**Custom Properties:**

| Property Name | Type | Required | Description | Example Values |
|---------------|------|----------|-------------|----------------|
| `[property_1]` | [type] | Yes/No | [Description] | [Examples] |
| `[property_2]` | [type] | Yes/No | [Description] | [Examples] |

---

### Event 6: [Your Core Event Name]

**Event Name:** `[object_action]`

**When it fires:** [Description]

**Why we track it:** [Metric/stage this supports]

**Custom Properties:**

| Property Name | Type | Required | Description | Example Values |
|---------------|------|----------|-------------|----------------|
| `[property_1]` | [type] | Yes/No | [Description] | [Examples] |
| `[property_2]` | [type] | Yes/No | [Description] | [Examples] |

---

### Event 7: [Your Core Event Name] (Optional - if needed)

**Event Name:** `[object_action]`

**When it fires:** [Description]

**Why we track it:** [Metric/stage this supports]

**Custom Properties:**

| Property Name | Type | Required | Description | Example Values |
|---------------|------|----------|-------------|----------------|
| `[property_1]` | [type] | Yes/No | [Description] | [Examples] |

---

### Event 8: [Your Core Event Name] (Optional - if needed)

**Event Name:** `[object_action]`

**When it fires:** [Description]

**Why we track it:** [Metric/stage this supports]

**Custom Properties:**

| Property Name | Type | Required | Description | Example Values |
|---------------|------|----------|-------------|----------------|
| `[property_1]` | [type] | Yes/No | [Description] | [Examples] |

---

## Event-to-Metric Mapping

### North Star Metric

**Our NSM:** [Your North Star Metric from north-star-metric.md]

**Events that power it:**
1. `[event_name]` - [How it contributes]
2. `[event_name]` - [How it contributes]
3. `[event_name]` - [How it contributes]

**Calculation:**  
[How you'll calculate NSM from these events]

**Example:**
- **NSM:** Weekly Active Study Sessions Completed
- **Events:** 
  - `study_session_started` - Tracks session initiation
  - `study_session_completed` - Tracks successful completion
- **Calculation:** `COUNT(DISTINCT user_id WHERE event='study_session_completed' AND timestamp WITHIN last_7_days)`

---

### AARRR Funnel Mapping

| AARRR Stage | Events | Metric Calculation |
|-------------|--------|-------------------|
| **Acquisition** | `user_signup_started`, `user_signup_completed` | Signup completion rate = `signup_completed / signup_started` |
| **Activation** | `[your activation event(s)]` | [How you calculate activation] |
| **Retention** | `[your retention event(s)]` | [How you calculate retention] |
| **Referral** | `[your referral event(s)]` | [How you calculate referral] |
| **Revenue** | `[your revenue event(s)] - if applicable` | [How you calculate revenue] |

**Example:**
- **Acquisition:** `user_signup_started` → `user_signup_completed` (Conversion: 68%)
- **Activation:** `first_session_completed` within 48 hours (Target: 60% of new users)
- **Retention:** `user_logged_in` on Day 7 (Target: 40% of activated users)
- **Referral:** `invite_sent` → `invite_accepted` (Referral rate: 15%)
- **Revenue:** N/A for MVP

---

## Data Types Reference

| Type | Description | Example | Validation Rules |
|------|-------------|---------|------------------|
| `string` | Text value | `"hello world"` | Max 255 characters unless noted |
| `integer` | Whole number | `42`, `0`, `-5` | No decimals |
| `float` | Decimal number | `3.14`, `0.5` | Up to 2 decimal places |
| `boolean` | True/false | `true`, `false` | Lowercase only |
| `enum` | Fixed set of values | `"pending"`, `"active"`, `"inactive"` | Must match allowed values |
| `ISO 8601 datetime` | Timestamp | `"2025-10-30T14:23:45Z"` | Must include timezone (Z or offset) |
| `UUID` | Unique identifier | `"550e8400-e29b-41d4..."` | 36 characters with dashes |
| `array` | List of values | `["math", "physics"]` | Max 20 items unless noted |
| `object` | Nested structure | `{"key": "value"}` | Max 5 levels deep |

---

## Event Volume Estimates

Estimate how often each event will fire to plan infrastructure:

| Event Name | Expected Daily Volume | Expected Monthly Volume | Notes |
|------------|----------------------|------------------------|-------|
| `user_signup_started` | [Estimate] | [Estimate] | Based on [assumptions] |
| `user_signup_completed` | [Estimate] | [Estimate] | ~70% of signup_started |
| `[event_3]` | [Estimate] | [Estimate] | [Notes] |
| `[event_4]` | [Estimate] | [Estimate] | [Notes] |
| **TOTAL** | [Sum] | [Sum] | - |

**Example:**
- `user_signup_started`: 50/day, 1,500/month (assuming 50 new users/day)
- `user_signup_completed`: 35/day, 1,050/month (~70% conversion)
- `study_session_started`: 200/day, 6,000/month (average 4 sessions/user/week)
- **TOTAL**: ~500 events/day, ~15,000 events/month

---

## Implementation Guidelines

### Where to Instrument Events

**Frontend (Web/Mobile):**
- User interactions (clicks, form submissions)
- Page views and navigation
- UI state changes

**Backend (API):**
- Data mutations (create, update, delete)
- Successful transactions
- System-generated events

**Rule of Thumb:**  
Track events **where they happen** - UI events in frontend, data events in backend. Avoid double-tracking.

---

### Event Sending Pattern

**Synchronous vs. Asynchronous:**
- ✅ **Asynchronous** (preferred): Don't block user actions waiting for analytics
- ❌ **Synchronous** (avoid): Only for critical events where you need confirmation

**Retry Logic:**
- Retry failed events up to 3 times with exponential backoff
- After 3 failures, log locally and send in next batch

**Batching:**
- Batch events every 30 seconds or when 50 events accumulate
- Send immediately for critical events (signup_completed, payment_completed)

---

### Code Example (Pseudocode)

```javascript
// Initialize analytics on app load
analytics.init({
  apiKey: process.env.ANALYTICS_API_KEY,
  environment: process.env.NODE_ENV
});

// Track an event
function trackEvent(eventName, properties = {}) {
  const standardProps = {
    event_id: generateUUID(),
    user_id: getCurrentUserId(),
    timestamp: new Date().toISOString(),
    session_id: getSessionId(),
    platform: 'web',
    app_version: APP_VERSION,
    environment: process.env.NODE_ENV
  };
  
  const eventPayload = {
    event_name: eventName,
    ...standardProps,
    ...properties
  };
  
  // Send asynchronously
  analytics.track(eventPayload);
}

// Usage example
button.addEventListener('click', () => {
  trackEvent('study_session_started', {
    session_type: 'group',
    subject: 'mathematics',
    estimated_duration: 60
  });
});
```

---

## Privacy & Compliance

### PII (Personally Identifiable Information) Rules

**NEVER include in event properties:**
- ❌ Email addresses
- ❌ Phone numbers
- ❌ Full names
- ❌ Physical addresses
- ❌ Social security numbers or IDs
- ❌ Passwords (obviously)

**Use instead:**
- ✅ Hashed user IDs
- ✅ Anonymized identifiers
- ✅ Aggregated data

**Example:**
- ❌ Bad: `{ "email": "student@kiu.edu.ge" }`
- ✅ Good: `{ "user_id": "hashed_user_abc123", "email_domain": "kiu.edu.ge" }`

---

### Data Retention

**Storage period:** [e.g., 24 months for raw events, indefinitely for aggregated metrics]

**Deletion policy:** [e.g., Users can request data deletion via settings]

**Compliance:** [e.g., GDPR-compliant, user consent obtained at signup]

---

## Testing Your Events

### Pre-Launch Checklist

Before deploying to production, verify each event:

- [ ] Event fires when expected user action occurs
- [ ] All required properties are present
- [ ] Property values match expected data types
- [ ] Event appears in analytics dashboard within 1 minute
- [ ] No PII is being sent
- [ ] Event volume is within expected range
- [ ] Events work across all platforms (web, mobile)

---

### Testing Tools

**Development:**
- [ ] Browser console logging for web events
- [ ] Analytics debugger extension (if applicable)
- [ ] Proxy tool (Charles, Fiddler) to inspect network requests

**Staging:**
- [ ] Test environment with separate analytics project
- [ ] QA team manual testing checklist
- [ ] Automated tests for critical user flows

**Production:**
- [ ] Real-time event monitoring dashboard
- [ ] Alerts for event volume anomalies
- [ ] Weekly event health check

---

## Event Schema Evolution

### Adding New Events (Post-MVP)

**Process:**
1. Document new event in this file
2. Define properties and data types
3. Update event-to-metric mapping
4. Implement instrumentation
5. Test in staging
6. Deploy to production
7. Monitor for 1 week

---

### Modifying Existing Events

**CRITICAL:** Never break backwards compatibility

**Safe changes:**
- ✅ Adding new optional properties
- ✅ Updating event descriptions
- ✅ Adding new enum values

**Unsafe changes (require versioning):**
- ❌ Changing property names
- ❌ Changing data types
- ❌ Removing properties
- ❌ Changing event names

**If unsafe change is required:**
Create v2 of the event and sunset v1 after migration period.

---

## Documentation & References

**Related Documents:**
- North Star Metric: `/02-analytics/north-star-metric.md`
- Analytics Plan: `/02-analytics/analytics-plan.md`
- Problem Statement: `/01-discovery/synthesis/final-problem-statement.md`

**External Resources:**
- Week 5 Lecture: Event Instrumentation
- [Segment Spec](https://segment.com/docs/connections/spec/) (industry standard)
- [Snowplow Event Dictionary](https://docs.snowplow.io/docs/) (reference)

---

## Team Sign-off

**All team members have reviewed this event schema:**

- [Name 1] - Role - Date
- [Name 2] - Role - Date  
- [Name 3] - Role - Date
- [Name 4] - Role - Date
- [Name 5] - Role - Date (if applicable)

**Tech Lead approval:**  
[Name] - Date

---

## Change Log

| Date | Version | Changes | Author |
|------|---------|---------|--------|
| [Date] | 1.0 | Initial schema for MVP | [Name] |

---

## Notes & Decisions

[Space for any additional context, debates, or decisions made during schema design]

**Example:**
"We debated tracking `study_session_paused` but decided against it for MVP to keep schema simple. Will revisit in V2 if retention analysis shows significant mid-session drop-off."

---

**Remember: This schema is your source of truth for what data you're collecting. Keep it updated, version it properly, and never send PII.**
