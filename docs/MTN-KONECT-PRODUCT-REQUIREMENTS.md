# MTN Konect — Product Requirements Specification

**Status:** Build-ready specification for Phase 1 visual prototype  
**Product concept:** MTN Konect — Connect. Belong. Konect. — Be MTN  
**Repository:** `Jablo-cmd/Mtn-inside`  
**Implementation direction:** polished visual prototype first; backend follows after stakeholder validation  
**Lead capability:** employee community and belonging  
**Intended audience:** global MTN employees, with country-specific experiences

> **Governance notice:** MTN Konect is a proposal/prototype, not an official MTN product or approved initiative. MTN must approve any use of its trademarks and brand assets, employee data, internal systems, identity provider, integrations, hosting and production deployment. Use fictional people and synthetic content only in the prototype.

## 1. Product vision

Create a polished, mobile-responsive employee experience concept that helps colleagues across MTN markets feel connected, informed and included. The first release is a convincing, interactive visual prototype for review and validation—not a production employee platform.

The prototype should demonstrate how a global employee community can connect colleagues across markets while keeping local context visible and respecting that country teams may have different languages, events, communities and communications.

### Product principles

1. **Belonging first:** people and meaningful participation take priority over corporate promotional content.
2. **Global by design, local by context:** shared global experience with a clear market selector and country-aware content.
3. **Human and respectful:** inclusive language, accessible interactions, and no public exposure of sensitive employee information.
4. **Useful, not noisy:** prioritize relevant posts and clear navigation; show notification states without creating unnecessary urgency.
5. **Trustworthy:** label prototype content as sample data and never imply that real MTN systems are connected.
6. **Corporate-grade:** refined enterprise design, strong typography, restrained visual effects, consistent spacing, and responsive layouts; avoid cartoon-like visuals.

## 2. Phase 1 goals and non-goals

### Goals

- Present a coherent end-to-end employee community journey in a browser.
- Demonstrate a global feed with country-specific filtering.
- Show community discovery, post creation, reactions, comments, recognition and events using synthetic data.
- Demonstrate responsive navigation and believable empty, loading, success and error states where relevant.
- Make the concept understandable in a short stakeholder walkthrough.
- Gather feedback on usefulness, terminology, market needs, moderation and adoption before committing to backend implementation.

### Non-goals for Phase 1

- No real employee authentication, SSO, HR integration or employee directory.
- No production database, backend API, real-time updates or real notifications.
- No real employee posts, personal data, internal documents or confidential company information.
- No payroll, performance management, employee monitoring, private messaging, HR case management or manager surveillance.
- No AI assistant in the first prototype.
- No live analytics or claims about adoption, engagement or business impact.
- No production use of MTN logos, trademarks or brand assets without authorization. Use approved assets only after permission; until then use a clearly marked concept treatment.

## 3. Primary users and prototype personas

All personas and names in the prototype must be fictional.

- **Employee:** browses community posts, filters by market, reacts, comments, joins a community and shares an update.
- **New colleague:** discovers groups, welcomes, events and ways to participate across teams and countries.
- **Community host:** sees how a group could present its purpose, members, posts and upcoming activities. In the prototype, this is illustrative and not a separate authenticated role.
- **Market content steward:** conceptually curates local highlights and market-specific content. Do not build real administrative permissions in Phase 1.
- **Global communications/community steward:** conceptually highlights cross-market stories and shared communities. Do not build a real admin console in Phase 1.

The prototype must not imply that role membership, employment status or country has been verified.

## 4. Information architecture

Use a persistent, understandable primary navigation. Desktop may use a left sidebar and top utility bar; mobile should use a compact menu or bottom navigation with accessible labels.

1. **Home** — personalized sample welcome, featured community stories, quick actions and upcoming events.
2. **Community Feed** — global posts, market filter, community filter, post cards and compose interaction.
3. **Discover Communities** — searchable/browsable cards grouped by interests, professional communities and market communities.
4. **Events** — upcoming sample events, market and online filters, event detail and an RSVP demo state.
5. **Recognition** — lightweight appreciation posts or shout-outs; no performance scoring or ranking employees.
6. **My Activity / Profile** — fictional profile, selected market and interests; clearly a demo profile, not an actual employee record.

Keep the first prototype focused. Secondary destinations may be represented as clearly marked future concepts, but should not distract from the community journey.

## 5. Core user journeys

### Journey A: arrive and orient

1. User opens Home.
2. Sees the product name and a clear prototype/sample-data indicator.
3. Sees a welcome message, global community highlights and a few relevant local items.
4. Can navigate directly to Feed, Discover or Events.

### Journey B: explore global and local conversation

1. User opens Community Feed.
2. Sees a readable feed of varied fictional posts.
3. Changes the market filter between Global and specific fictional market options.
4. Feed content updates to reflect the selected filter.
5. User can reset the filter and return to the global view.

### Journey C: participate in a post

1. User opens the composer.
2. Enters text and optionally selects a community or audience label.
3. Sees a preview or validation message before submitting.
4. Submits the post; it appears in the local prototype feed for the current session.
5. A clear confirmation appears. If the content is blank, submission is prevented with helpful inline feedback.

No data is transmitted to a server. If session persistence is implemented, use browser-local demo state only and disclose that it is not secure storage and may reset.

### Journey D: react and comment

1. User reacts to a post.
2. The reaction state and visible count update.
3. User opens the comments area, adds a non-empty sample comment and sees it in the current prototype state.
4. Repeated clicks must toggle or update predictably, not inflate counts accidentally.

### Journey E: discover and join a community

1. User browses or searches community cards.
2. Can filter by market or interest.
3. Opens a community detail panel or page showing purpose, sample members, recent posts and next activity.
4. Clicks Join/Joined; the button state changes and explains this is a demo interaction, not a real membership change.

### Journey F: explore an event

1. User opens Events.
2. Filters by market and online/in-person format.
3. Opens event details, including local time zone where practical.
4. Clicks RSVP; a visible demo confirmation updates the state. Do not send invitations or calendar events.

## 6. Functional requirements

### P0 — required for prototype acceptance

- Responsive Home, Feed, Discover Communities, Events, Recognition and Profile views.
- Shared navigation with a clear active state and usable back/navigation behaviour.
- Global and market-specific content states; market selector works and affects visible content.
- Synthetic posts with author display name, fictional role/team or market label, timestamp label, body, optional topic/community tag, and reaction/comment counts.
- Compose-post flow with required-field validation, character guidance and a successful demo state.
- Working reaction toggle and comment add flow.
- Community search/filter and Join/Joined demo state.
- Event filters, event detail and RSVP demo state.
- Recognition examples that focus on gratitude and contribution rather than scores or leaderboards.
- Clear sample-data/prototype disclosure, including on interactive forms.
- Keyboard-operable controls, visible focus states, semantic labels, appropriate contrast and reduced reliance on color alone.
- Consistent empty, validation, success and no-results states.

### P1 — desirable if it does not delay P0

- Search across sample posts and communities.
- Topic chips such as volunteering, learning, wellbeing, customer impact and innovation.
- A simple notification drawer with synthetic unread states.
- Save/bookmark post demo state.
- A polished onboarding panel explaining how to find communities and choose a market.
- Light/dark theme only if both are consistently implemented and tested.

### Explicitly deferred

Real SSO, backend services, PostgreSQL, authorization, moderation queues, image uploads, push/email notifications, analytics, multilingual content management, AI search, employee directory, integrations and administrative workflows.

## 7. Global and country-specific experience

The experience must make the global/local relationship obvious without making the app feel fragmented.

- Provide a **Global** feed state and a market selector with fictional/sample market options. Do not imply that the listed markets are an approved rollout scope.
- Distinguish global posts from posts intended for a particular market.
- Display the market or audience label on relevant cards.
- Filtering must be predictable: Global shows cross-market content and may show selected global highlights; a selected market shows global content plus content tagged to that market. Document this behaviour in the UI.
- Avoid assuming all markets share the same holidays, language, event times or policies.
- Show time zone context on event details. In Phase 1, do not claim automatic localization if dates and translations are static.
- Build layouts that can accommodate translated strings and longer labels; do not hard-code layout widths that break with localization.
- Use synthetic, neutral sample content; do not fabricate official statements, product offers, policies or employee announcements.

## 8. Content design and moderation cues

- Use a mix of short updates, questions, appreciation, learning moments, volunteering and cross-market collaboration.
- Every sample post must be clearly fictional and must not be presented as an official MTN announcement.
- Include a visible report/flag affordance only as a demo interaction, with explanatory text that it does not notify a real moderator.
- Do not add public follower counts, employee popularity rankings, performance scores or inferred sentiment labels.
- Avoid sensitive topics and real personal details in seed content.
- Show a simple community guideline panel: be respectful, do not share confidential information, and report harmful content through approved real-world channels once a production process exists.
- Do not create a misleading promise that a report or moderation action is actually processed.

## 9. Visual and interaction design requirements

- Premium, modern enterprise product; warm, human and confident rather than overly formal or playful.
- Use MTN branding only if approved. Until then, make the concept visually polished with a neutral, clearly provisional brand treatment.
- Establish a restrained color system, typography scale, spacing scale, border radius, elevation and icon style. Use color contrast that supports accessibility.
- Use a consistent post-card system, community cards, event cards, filter controls, avatars/initials and buttons.
- Use fictional initials or neutral avatars; do not use real employee photographs.
- Avoid excessive gradients, glassmorphism, animated backgrounds or decorative motion that harms readability.
- Use short, natural microcopy and specific feedback after each action.
- Make important actions obvious but not visually aggressive.
- Provide responsive behaviour for desktop, tablet and mobile, including long posts, narrow viewports and keyboard focus.

## 10. Technical implementation direction for Phase 1

The approved direction is **polished visual prototype first, then backend**, with Next.js and TypeScript as the planned application stack.

- Use Next.js App Router and TypeScript, consistent with the repository's technical architecture document.
- Build reusable UI components and typed synthetic data fixtures.
- Keep prototype state local to the client where interactions require it; do not add a backend just to simulate a response.
- Keep sample data and UI behaviour separate so a later backend can replace the fixture layer without rewriting the whole interface.
- Use semantic, maintainable component boundaries for navigation, feed cards, filters, composer, community cards, event cards, dialogs/drawers and status feedback.
- Add linting, type checking and a production build check to the development workflow.
- Do not place secrets, API keys, real employee data or service credentials in the client bundle.
- Avoid adding a database, SSO library, third-party analytics or external data dependency in this phase unless required and explicitly approved.
- Do not claim that the current static prototype is already a Next.js application; this specification defines the intended next implementation step.

## 11. Privacy, security and governance constraints

- Use only invented names, roles, markets, posts, comments and event data.
- No real employee identifiers, phone numbers, emails, photographs, HR records or internal documents.
- Do not connect to MTN systems or attempt to access internal endpoints.
- Keep the prototype clearly labelled as non-production.
- No real authentication or authorization claims; if a login screen is shown, it must be a non-functional concept screen and must not collect credentials.
- Do not persist personal information. If local browser state is used, limit it to non-sensitive demo interactions and provide a reset path where practical.
- Before backend work, obtain stakeholder approval for identity provider, data classification, hosting, retention, audit requirements, cross-border data handling, market-level access and incident response.
- The production design must use server-side authorization and enforce access to market/community data on the server; hiding a UI control is not authorization.
- Review applicable privacy law and MTN policies, including POPIA where applicable, with authorized stakeholders before real employee data is processed.

## 12. Accessibility and quality bar

Target WCAG 2.2 AA as a design and testing objective, subject to validation.

- Full keyboard access to navigation, menus, dialogs and interactive cards.
- Visible focus indicators and logical focus order.
- Semantic headings, landmarks, labels and buttons.
- Accessible names for icon-only controls; do not rely on icon shape alone.
- Adequate text and non-text contrast; communicate selected/error/success states with text or symbols as well as color.
- Respect reduced-motion preferences and avoid motion-dependent information.
- Validation messages should be clear and associated with the relevant control.
- Test at narrow mobile widths and with browser zoom; prevent horizontal overflow.

## 13. Acceptance criteria

The prototype is ready for stakeholder review when:

1. All P0 views can be reached from primary navigation.
2. The layout works at mobile, tablet and desktop sizes without broken controls or horizontal overflow.
3. Switching Global/market filters visibly changes the feed and can be reset.
4. A valid post can be composed and appears in the current demo state; an empty post is rejected with helpful feedback.
5. Reaction toggles, comments, community join state and event RSVP state behave consistently.
6. Search/filter controls return sensible results and show a useful no-results state.
7. All sample content is fictional and visibly identified as prototype content.
8. No interaction claims to send a real notification, update an official system or create a real membership/RSVP.
9. No credentials, real employee data, secrets or internal service endpoints are present.
10. Type checking, linting and production build complete successfully in the chosen implementation environment.
11. Keyboard navigation and basic contrast/label checks are completed; identified blockers are fixed or documented.
12. The README explains how to run the prototype, known limitations and the non-production status.

## 14. Stakeholder validation questions

Before backend development, validate:

- What employee community tools already exist, and what gaps remain?
- Which markets and employee groups should participate in discovery and any eventual pilot?
- What does belonging mean in measurable, non-invasive terms for this organization?
- Which content types are appropriate globally versus market-specific?
- Who owns moderation, escalation and community governance in each market?
- What languages and accessibility requirements must be supported first?
- Which identity provider, hosting environment and data stores are approved?
- Which employee data is necessary, who may access it, and for how long should it be retained?
- What are the baseline and success criteria for any pilot?
- Who has authority to approve brand use, content, integrations and production launch?

## 15. Suggested delivery sequence

1. **Foundation:** Next.js + TypeScript setup, design tokens, responsive shell, prototype banner and typed synthetic fixtures.
2. **Community core:** Home, feed, market filter, post cards, compose, reactions and comments.
3. **Belonging journeys:** community discovery, community detail/join state, recognition and events/RSVP state.
4. **Polish:** empty/error/success states, responsive QA, accessibility pass and stakeholder demo walkthrough.
5. **Review:** capture feedback and revise scope; do not begin production backend work until governance and integration decisions are approved.
6. **Backend planning:** update the technical architecture based on stakeholder answers, then design auth, APIs, data model, moderation, audit and deployment controls.

## 16. Definition of done

Phase 1 is done when the prototype convincingly demonstrates the employee community and belonging experience for a global workforce with local market context, all P0 interactions work with synthetic data, the interface meets the quality bar, and stakeholders can review the concept without mistaking it for an approved or connected MTN system.
