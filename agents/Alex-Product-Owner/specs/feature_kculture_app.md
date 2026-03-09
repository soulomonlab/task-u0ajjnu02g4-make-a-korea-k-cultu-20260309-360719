# Feature: K-Culture App (MVP)
**Goal:** Deliver an engaging mobile + web app that introduces and connects users to Korean (K) culture through curated content, events, and community features.
**North Star Impact:** Increase weekly active users and session time by providing discoverable, high-quality K-culture content and social engagement.
**Users:**
- Tourist Enthusiast (persona): International users wanting accessible K-culture content (music, drama, food, travel). Use case: discover culturally relevant content and local events.
- K-fan Community Member: Existing K-culture fans who want to share, discuss, and attend events. Use case: join communities, post, RSVP to meetups.
- Content Creators / Curators: Local creators and small businesses. Use case: publish short-form content and event listings.

**RICE Score:** Reach=20,000 users/quarter × Impact=2 (high) × Confidence=80% / Effort=8w = 4,000
**Kano Category:** Performance

**MVP Scope / Core Features:**
- Home feed: Personalized content cards (articles, short videos, event highlights).
- Content detail: Rich content page with media, translations, and related links.
- Events & Meetups: Event listing, RSVP, basic ticketing (external links).
- Community: Topic-based discussion boards and comments.
- Creator onboarding: Simple content submission flow and moderation queue.
- Basic user auth: Email + OAuth (Google, Apple, Kakao optional later).

**Acceptance Criteria:**
- [ ] Users can view a personalized home feed with content cards (images, title, snippet).
- [ ] Tapping a card opens a content detail page with media playback and translations.
- [ ] Users can view and RSVP to events; RSVP is stored and retrievable from profile.
- [ ] Users can create posts in community boards and comment on posts.
- [ ] Creators can submit content which appears in a moderation queue for admins.
- [ ] Auth flow supports email signup/login and OAuth (Google). Session persists for 30 days.
- [ ] Backend supports 10k concurrent users with basic horizontal scalability (stateless APIs + managed DB).
- [ ] Page/API response time: median <300ms; 95th percentile <800ms.

**Out of Scope (MVP):**
- In-app payments / full ticketing flow
- Advanced personalization ML models
- Full multi-language localization beyond English/Korean
- Native-only features requiring deep mobile integration (push notifications in Phase 2)

**Success Metrics:**
- Weekly Active Users (WAU) ≥ 15k within Q1 post-launch
- Average session length ≥ 6 minutes
- Community DAU/MAU ratio ≥ 20%
- Creator submissions ≥ 200 within first 3 months

**Initial Technical Decisions / Constraints:**
- Platforms: Responsive web + iOS/Android (React Native considered for parity)
- API: RESTful JSON APIs; GraphQL considered in Phase 2
- Storage: Managed relational DB (Postgres) + CDN for media
- Auth: JWT sessions with refresh tokens; OAuth for major providers

**Roadmap (Phase 1 - MVP, 8w):**
- Week 0-1: Design concept & wireframes
- Week 2-4: Core frontend pages + auth
- Week 3-6: Backend APIs + event system
- Week 5-7: Community & creator flows
- Week 7-8: QA, performance tuning, launch prep

**GitHub Issue:** TBD (created by Product Owner)
