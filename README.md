# Specification Phase Exercise

A little exercise to get started with the specification phase of the software development lifecycle. See the [instructions](instructions.md) for more detail.

## Team members

* [Jasmine Zhu](https://github.com/jasminezjr) - Clickable Prototype
* [Esther Feng](https://github.com/yf2685-beep) - Product Vision Statement + User Requirements
* [Eason Huang](https://github.com/GILGAMESH605) - Wireframe Diagrams
* [Majo Salgado](https://github.com/mariajsalgadoq) - Stakeholder Interview
* [Matthew Zhou](https://github.com/mzhou3299) - UML Activity Diagrams

## Stakeholders

## Who we talked to & how we listened
We ran short, open-ended interviews and some lightweight observation to elicit real requirements (not guess them). We started broad (“What makes pet adoption hard right now?”), then drilled into concrete tasks (“Walk me through how you contact a shelter”), and finally very specific details (“What info must be on a pet profile for you to feel safe applying?”). We kept space for people to change their minds and add late-breaking insights.

Each summary below includes goals/needs, problems/frustrations, current workarounds, success measures, and security notes across Product, People, and Process.


## Stakeholder 1 — Sofia (First-time Adopter, college student)

**Context (in their words):**  
“I’m scrolling three sites and two Instagram accounts, saving screenshots so I don’t lose a dog I like. Half the time the pet’s already adopted.”

**Goals / Needs**
- Find adoptable pets nearby without hopping across websites.
- Trust the info: age, size, temperament, health/vaccinations, adoption fee, location.
- Ask quick questions and get fast replies.
- Save/favorite pets and receive notifications on status changes and replies.
- Filters that match lifestyle (apartment-friendly, shedding level, weight range, energy level).

**Problems / Frustrations**
- Scattered, often out-of-date listings.
- Slow or no responses; conversations split across email, DMs, and forms.
- Anxiety about a poor match due to missing behavior context.
- Re-typing the same application info repeatedly.

**Current Workarounds**
- Screenshots plus notes; follows shelters on social; personal reminders.
- Copy-pastes the same “about me” paragraph into forms.

**What success looks like**
- One place to search and message; same-day acknowledgement from a shelter.
- Consistent, transparent profiles; fewer dead ends.
- Clear next steps after applying.

**Security & Trust (Product / People / Process)**
- Product: Protect PII (address, phone); private messaging.  
- People: Education about scams and off-platform deposits.  
- Process: Verified shelter accounts; visible status history.  

**Implications for Petport**  
Accurate status, rich profiles, in-app messaging and notifications, strong filters, application autofill.

## Stakeholder 2 — Luis (Shelter Coordinator, small municipal shelter)

**Context:**  
“I post on multiple platforms and answer calls while cleaning kennels. I need one inbox and a way to update status once.”

**Goals / Needs**
- List animals quickly with photos, temperament notes, and medical info.
- Change status in one place and propagate everywhere.
- Centralize applications and messages; templates for FAQs.
- Highlight long-stay and special-needs pets.

**Problems / Frustrations**
- Duplicate work across platforms; information drifts out of sync.
- Missed or delayed replies because communication is fragmented.
- Unqualified applications clog the queue; repetitive Q&A.

**Current Workarounds**
- Spreadsheets to track animals; weekly mass updates; canned email responses.

**What success looks like**
- A single dashboard for listings, status, messages, and applications.
- Fewer duplicate questions; faster time-to-adoption (example target: under 14 days median).

**Security & Compliance (Product / People / Process)**
- Product: Role-based access; audit trail; export for records.  
- People: Volunteer accounts with limited permissions; quick training prompts.  
- Process: Consistent data fields (vaccine dates, microchip); no PII leakage to public pages.  

**Implications for Petport**  
Bulk status update, templates, smart message triage, role permissions, audit logging.


## Stakeholder 3 — Mira (Rescue Volunteer and Foster Coordinator)

**Context:**  
“When a shelter is full, I need to know today who has space and which pets are urgent.”

**Goals / Needs**
- Visibility into capacity and urgent cases across nearby shelters.
- Shareable, up-to-date profiles for cross-posting and transfers.
- Lightweight tracking of foster placements and outcomes.

**Problems / Frustrations**
- Fragmented info and stale lists; coordination buried in chat threads.
- Re-collecting the same medical and behavior info with each transfer.

**Current Workarounds**
- Shared spreadsheets and group chats; manual status pings; cloud folders of photos.

**What success looks like**
- A reliable source of truth for availability and quick transfer workflows.

**Security (Product / People / Process)**
- Product: Control public versus partner-only details (medical documents).  
- People: Avoid accidental sharing of foster home addresses.  
- Process: Partner verification; consent prompts before sharing files.  

**Implications for Petport**  
Phase 2: Partner view, transfer workflow, private document sharing.

## Stakeholder 4 — Dr. Chen (Clinic Partner / Vet Tech liaison)

**Context:**  
“Adopters ask what ‘heartworm positive’ means. Consistent health notes would save time.”

**Goals / Needs**
- Consistent medical fields and simple health flags with plain-language explanations.
- Ability to attach or verify vaccination and microchip information.

**Problems / Frustrations**
- Medical information is inconsistent or missing across listings.

**Security (Product / Process)**
- Product: Protect medical documents; redact sensitive owner details when present.  
- Process: Only shelters upload clinical records; verification badges.  

**Implications for Petport**  
Structured health fields with tooltips; optional record attachments.

## Secondary Stakeholders
- Fosters (need simple check-ins).  
- Donors (interested in impact stories).  
- Municipal administrators (reporting).  
- Accessibility users (screen-reader friendly UI, keyboard navigation, sufficient contrast).  

## Traceability: Stakeholder Needs → User Stories

**Sofia (Adopter)**  
- Browse and filter by species and traits → covered by existing stories.  
- Detailed profiles with photos, age, breed, temperament → covered.  
- Favorite/save and receive notifications → covered.  
- Direct in-app messaging → covered.  

**Luis (Shelter Staff)**  
- Post quickly; update status (available, pending, adopted) → covered.  
- Manage incoming requests/messages in one place → covered.  
- Highlight special-needs/long-stay pets → planned (add story).  

**Mira (Rescue)**  
- Cross-organization visibility and transfers → planned for Phase 2 (add epic).  

**Dr. Chen (Clinic Partner)**  
- Structured health fields and explanations → planned (add to profile schema).  

## Security Requirements (organized by the 3 Ps)

**Product**
- Private messaging with transport encryption; PII encrypted at rest.  
- Role-based access control for staff, volunteers, and adopters.  
- Audit trail for listing edits and status changes.  
- Verified shelter badge and report-scam flow.  

**People**
- Anti-scam education for adopters (avoid off-platform deposits).  
- Authoring tips for staff to avoid posting personal phone numbers publicly.  
- Minimal-data principle in forms; explain why each field is collected.  

**Process**
- Moderation and onboarding for new shelters; periodic status checks with automated nudges.  
- Data retention policy for applications; export/delete upon request.  
- Regular access reviews for staff and volunteers.  

## Interview and Observation Notes (method snapshot)
- Techniques used: Open interviews (30–40 minutes), a short scripted observation (“show how you would try to adopt this dog today”), and a brief brainstorming segment to validate ideas (“Would a ‘status changed to pending’ notification help or be noisy?”).  
- Why elicit rather than prescribe: Letting stakeholders speak freely surfaced real blockers (for example, status drift across platforms) and converted vague desires (“faster replies”) into specific, testable requirements (single inbox, templates, notifications, audit log).


## Product Vision Statement

For adopters and shelters frustrated by scattered listings and slow communication, **Petport** is a mobile app that streamlines communication and makes pet adoption faster and easier.

## User Requirements



- As an adopter, I want to browse available pets by type (dog, cat, small animal, etc.) so that I can quickly find pets that match my preferences.

- As an adopter, I want to see detailed pet profiles with photos, age, breed, and temperament so that I can make an informed decision before contacting the shelter.

- As an adopter, I want to favorite or save pets I’m interested in so that I can easily return to their profiles later.

- As an adopter, I want to apply filters (e.g., age, size, breed, location) so that I can narrow down my search to pets that fit my lifestyle.

- As an adopter, I want to message shelters directly through the app so that I can ask questions and arrange visits without delay.

- As a shelter staff member, I want to quickly post new pet listings with photos and descriptions so that adopters can see them right away.

- As a shelter staff member, I want to update pet status (e.g., “available,” “adopted,” “pending”) so that adopters always have accurate information.

- As an adopter, I want to receive notifications when a shelter responds to my message so that I can reply promptly.

- As a shelter staff member, I want to view and manage all incoming adoption requests in one place so that I can respond efficiently.

- As an adopter, I want the app to suggest pets based on my saved preferences so that I can discover new matches I might not have searched for.


## Activity Diagrams

## Diagrams

### User Story 1  
*As a user, I want to browse pets by category so that I can easily find adoptable animals that match my preferences.*  

![Activity Diagram - Browsing Pets](diagrams/activity_diagram_browsing.jpeg)

---

### User Story 2  
*As a user, I want to apply to adopt a pet by providing my contact information to the shelter so that I can start the adoption process.*  

![Activity Diagram - Apply to Adopt](diagrams/activity_diagram_application.jpeg)

## Supplementary UML Diagrams

### Use Case Diagram  
Shows the main interactions between adopters and shelter staff.  

![Use Case Diagram](diagrams/use_case_diagram.jpeg)

---

### Class Diagram  
Shows the system’s main entities and their relationships.  

![Class Diagram](diagrams/class_diagram.jpeg)

## Clickable Prototype

The wireframe diagrams outline a user-friendly pet adoption app built around a standard bottom navigation bar (Home, Favorites, Messages, Profile). The core flow allows users to browse pets on the home screen, filter by species, view detailed profiles, and submit an adoption application, culminating in a confirmation screen. The design focuses on clarity and ease of use.


![wireframe](wireframe.png)

Experience the full user flow and interact with every screen through our [clickable prototype](https://www.figma.com/proto/LVHAVQ2Y52o2i5guBrtj5d/SWE-project-1-wireframe?node-id=4-12&p=f&t=q0jvsskKfnVIZdwh-0&scaling=scale-down&content-scaling=fixed&page-id=0%3A1&starting-point-node-id=4%3A12)

