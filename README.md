<!-- Showcase repository: the product is real and in use, its source code is private. -->

<a href="https://q-nexus.epccwika.tech"><picture><source media="(prefers-color-scheme: dark)" srcset="assets/banner-dark.svg"><img src="assets/banner-light.svg" width="100%" alt="Q-NEXUS. Vendor procurement inside the tender stage, from BOQ and RFQ to evaluation, negotiation and selection."></picture></a>

<p align="center"><a href="https://q-nexus.epccwika.tech"><b>Open q-nexus.epccwika.tech</b></a> · <a href="https://github.com/nugrahalabib">More of my work</a> · <a href="https://nugrahalabib.com">nugrahalabib.com</a> · <a href="mailto:nugrahalabib@gmail.com">Email</a></p>

<p align="center"><a href="#the-business">The business</a> · <a href="#product-tour">Product tour</a> · <a href="#for-developers">For developers</a></p>

## Overview

Q-NEXUS is a web application for the EPCC Division of PT Wijaya Karya. It digitalises the vendor procurement work of the quantity surveying team inside the tender stage: tender, BOQ, RFQ, quotations, technical and commercial evaluation, clarification, negotiation, selected vendor and archive.

It serves ten roles, from the tender team lead and QS to engineering, supply chain, management and read-only observers. Each role gets its own dashboard and only the actions it may take.

Reading vendor offers is the hard part. Excel offers are parsed by code with no AI. PDF and Word offers are read by an AI agent, and every number it returns must be proven present in the document.

| | |
| --- | --- |
| **Status** | Live at [q-nexus.epccwika.tech](https://q-nexus.epccwika.tech) |
| **Role** | Designed, built and led by Nugraha Labib Mujaddid, IT Specialist at the EPCC Division of PT Wijaya Karya (Persero) Tbk. |
| **Period** | Since 2026 |
| **Source** | Private. This repository presents the product; the code is not published. |

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/features-dark.svg"><img src="assets/features-light.svg" width="100%" alt="What Q-NEXUS does: Tender to RFQ list, BOQ versions, Reading vendor offers, Evaluation and recommendation, Clarification and closing, Price and vendor databases, Per-user data assistant, Audit and practice mode."></picture>

## The business

Q-NEXUS is the web application the EPCC Division of PT Wijaya Karya uses to buy prices from vendors while it prepares a tender. It covers the full vendor procurement inside the tender stage: RFQ List, bill of quantities, requests for quotation, vendor quotations, technical and commercial evaluation, clarification, negotiation, selected vendor and archive. Ten roles work in it, from the tender team leader, quantity surveyors and supply chain to engineering, management and read-only observers, and each role sees its own dashboard and only the actions it may take. It matters because the vendor prices gathered here become the cost basis of the price WIKA offers its client. It was designed, built and led by Nugraha Labib Mujaddid, IT Specialist at the EPCC Division of WIKA.

### The problem

Before Q-NEXUS, the EPCC team asked many vendors for prices, compared them, negotiated and chose a vendor through Excel files, email and WhatsApp. The work was scattered and hard to trace afterwards: which version of the item list a vendor had priced, who sent which letter, and why one vendor was preferred over another.

The stakes are high. In a tender, WIKA must know the cost of pipes, concrete, pumps and subcontract work before it can price its own bid, so one procurement can involve several disciplines, several vendors and several rounds of revision and negotiation. Price data in a state-owned company is confidential and must not leak.

The scope is deliberate. Q-NEXUS handles the relationship between WIKA and its vendors inside one tender stage. Writing the budget (RABT), management approval and submitting the bid to the client stay outside the system; the final budget documents are only uploaded as closing files.

### Who uses it

| Role | What they do with it |
| --- | --- |
| **KTT (Tender Team Leader)** | Registers the tender, appoints the MQS and GM Engineering, sets the stage schedule and the budget ceiling, and closes each procurement with its result. |
| **KTD (Design Team Leader)** | Builds and releases the RFQ List for the tender and is the only person who approves an RFQ or returns it for revision. |
| **Engineering** | Fills in the BOQ and vendor attachments, submits them to the KTD, and judges each quotation against the specification. Engineering never sees quoted prices. |
| **SCM (Supply Chain)** | The single door to vendors: sends requests for quotation, follow-up BOQ revisions, reminders and clarifications, records replies and runs negotiation rounds. |
| **QS (Quantity Surveyor)** | Sets the Initial Price, reviews quotations commercially, validates negotiation rounds, and marks the selected vendor with a written reason. |
| **MQS (QS Manager)** | Sees all tenders and prices, but only writes the QS and SCM side of a team, including the QS and SCM person in charge of each procurement. |
| **GM Engineering** | Assembles the KTD and Engineering team and sets the Engineering person in charge; acts as backup for the RFQ List but does not approve RFQs. |
| **Admin** | Manages accounts and roles and reads the global audit trail. A logged emergency mode, which requires a reason, lets Admin take over Engineering and QS tasks. |
| **Management (SVP, Manager)** | Reads progress across all tenders on an observer dashboard with no write actions. Only the SVP sees the Price Database. |
| **QS Coordinator** | Monitors all tenders, overdue work and the Price Database, without any write rights. |

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/before-after-dark.svg"><img src="assets/before-after-light.svg" width="100%" alt="Before and after: Item lists kept in separate Excel files becomes A BOQ inside each procurement with numbered revisions and a change history; Vendor letters and replies in personal email and WhatsApp becomes Letters sent by SCM from the app and logged per vendor in Vendor Emails; Decisions hard to trace afterwards becomes Every workflow action written to an append-only audit trail, with the reason; Status known only by asking around becomes Dashboards per role that list what is waiting for whom and what is late."></picture>

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/journey-dark.svg"><img src="assets/journey-light.svg" width="100%" alt="How work flows: Register the tender, Build the team, Release the RFQ List, Prepare the BOQ, Approve the RFQ, Set the Initial Price, Send the request for quotation, Record quotations, Technical evaluation, Commercial evaluation, Clarification, Negotiation, Recommendation and selected vendor, Close and archive."></picture>

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/value-dark.svg"><img src="assets/value-light.svg" width="100%" alt="What it changes: 10 roles, each with its own dashboard and rights; 7 workflow stages from RFQ List to archive; 60 / 40 price and technical weighting of the system recommendation; 16 item and vendor categories; 189 / 189 end-to-end scenarios passing in prototype mode on 10 Nov 2026; ID | EN every screen in Indonesian and English."></picture>

### Model and status

Q-NEXUS is an internal system of the EPCC Division of PT Wijaya Karya (Persero) Tbk, not a commercial product, so it has no pricing. It has been in production at q-nexus.epccwika.tech since September 2026 with a real database, connected to Microsoft 365 for document storage in SharePoint and for vendor letters through Outlook.

Adoption is supported inside the product. Since November 2026 a Practice Mode lets any employee start a fictional sample tender in their own browser, take their role's steps with a guide that ticks itself off, and see the result reach the next role, without touching real data or sending email.

## Product tour

### 1. Roles, dashboards and two languages

Accounts are created by Admin; there is no self-registration. After sign-in every role lands on its own dashboard, built around a Needs Your Action list that names the next step and links straight to the place where it is done. The whole interface switches between Indonesian and English.

- Ten roles; the sidebar only shows the pages a role may use
- Needs Your Action list, most urgent on top, with "You are PIC" tags
- MQS and GM Engineering assign persons in charge inline, with team workload in view
- Indonesian and English for every screen, switched from the top bar

<img src="assets/screens/01-login-en.jpg" width="100%" alt="Sign-in page in English, with the four parts of the process summarised on the left.">

<sub>Sign-in page in English, with the four parts of the process summarised on the left.</sub>

<p><img src="assets/screens/02-ktt-dashboard.jpg" width="49%" alt="Tender team leader dashboard: key figures and the decisions waiting for the KTT."> <img src="assets/screens/03-mqs-assign-pic.jpg" width="49%" alt="QS Manager dashboard: two procurements without SCM and QS owners, assigned inline."></p>

<sub>Left: Tender team leader dashboard: key figures and the decisions waiting for the KTT. · Right: QS Manager dashboard: two procurements without SCM and QS owners, assigned inline.</sub>

<p><img src="assets/screens/04-procurement-list-id.jpg" width="100%" alt="The procurement list in Indonesian, showing stage, state and deadline per procurement."></p>

<sub>The procurement list in Indonesian, showing stage, state and deadline per procurement.</sub>

### 2. Tender page and RFQ List

A tender is the client's tender; inside it, each procurement is one RFQ. The tender page shows readiness, a stage schedule against the submission deadline, the team with their workload and every procurement. The KTD builds the RFQ List, and nothing reaches a vendor until the KTD approves the RFQ.

- Readiness checks for team, stage schedule, procurements and documents
- Stage schedule chart with today's line and the submission deadline
- RFQ List grouped by state: awaiting KTD, needs revision, with Engineering, approved, sent
- Review window lists BOQ items, attachments and exactly who is notified after approval

<img src="assets/screens/05-tender-page.jpg" width="100%" alt="Tender page of the practice tender: readiness, stage schedule and tender team.">

<sub>Tender page of the practice tender: readiness, stage schedule and tender team.</sub>

<p><img src="assets/screens/06-tender-progress.jpg" width="49%" alt="Tender progress across the seven stages and procurement progress per stage."> <img src="assets/screens/07-rfq-list.jpg" width="49%" alt="The KTD's RFQ List with overdue RFQs, the KTD's next steps and approval progress."></p>

<sub>Left: Tender progress across the seven stages and procurement progress per stage. · Right: The KTD's RFQ List with overdue RFQs, the KTD's next steps and approval progress.</sub>

<p><img src="assets/screens/08-ktd-review-rfq.jpg" width="100%" alt="KTD review of one RFQ: BOQ items, the attachment for vendors, and Approve or Request Revision."></p>

<sub>KTD review of one RFQ: BOQ items, the attachment for vendors, and Approve or Request Revision.</sub>

### 3. BOQ versions

The bill of quantities often changes after vendors already received it. Q-NEXUS keeps numbered revisions with a required reason, records which revision each quotation answers, and tells SCM which vendors still hold an old version. Sending the new revision lists the changes for the vendor.

- Rev 0 is the BOQ approved by the KTD; later revisions need a reason
- Per-item comparison: volume changed, new item, removed item
- Quotations answering an older revision stay valid but are flagged
- Vendors who declined to quote are skipped when the new revision is sent

<img src="assets/screens/09-boq-revision-history.jpg" width="100%" alt="BOQ revision history: reason, summary and item-by-item comparison of Rev 1 and Rev 2.">

<sub>BOQ revision history: reason, summary and item-by-item comparison of Rev 1 and Rev 2.</sub>

<p><img src="assets/screens/10-boq-rev-ribbon.jpg" width="49%" alt="Vendor quotations with the notice that two vendors still hold an older BOQ."> <img src="assets/screens/11-send-latest-boq.jpg" width="49%" alt="Sending BOQ Rev 2: the changes, the receiving vendors and the vendor that was skipped."></p>

<sub>Left: Vendor quotations with the notice that two vendors still hold an older BOQ. · Right: Sending BOQ Rev 2: the changes, the receiving vendors and the vendor that was skipped.</sub>

### 4. Requests for quotation and vendor offers

Each procurement has one workspace with a seven-stage tracker and a What You Need to Do list for the person signed in. SCM picks vendors matched by category, the system writes the BOQ file for vendors, and replies are recorded against deadlines. Offers can be read from the vendor's file instead of retyped.

- Vendor picker matches categories and materials and hides blacklisted vendors
- Late replies, missing replies and declined quotations are marked per vendor
- Excel offers are mapped by column headings in code, with no AI
- Side-by-side source and result, arithmetic check, and nothing saved until a person presses Save

<img src="assets/screens/12-procurement-workspace.jpg" width="100%" alt="Procurement workspace: stage tracker and the SCM's three next steps.">

<sub>Procurement workspace: stage tracker and the SCM's three next steps.</sub>

<p><img src="assets/screens/13-send-rfq-vendor-picker.jpg" width="49%" alt="Send Request for Quotation: vendors matched by category, one blacklisted vendor hidden."> <img src="assets/screens/14-quotations-deadline.jpg" width="49%" alt="Quotations after the deadline: lowest offer, a late reply and vendors with no response."></p>

<sub>Left: Send Request for Quotation: vendors matched by category, one blacklisted vendor hidden. · Right: Quotations after the deadline: lowest offer, a late reply and vendors with no response.</sub>

<p><img src="assets/screens/15-offer-reading-excel.jpg" width="100%" alt="Reading a synthetic Excel offer: columns recognised without AI, one arithmetic mismatch flagged."></p>

<sub>Reading a synthetic Excel offer: columns recognised without AI, one arithmetic mismatch flagged.</sub>

### 5. Technical and commercial evaluation

Engineering judges specification compliance without seeing prices; QS judges the price. A quotation becomes FINAL only when both gates are met. The technical evaluation matrix scores each item per vendor and produces the TBE score used later in the recommendation.

- Technical Evaluation page lists quotations awaiting the engineer, with no price columns
- TBE matrix: Comply 100, Comply with Note 1 to 99 with a required note, Not Comply 0
- TBE score per vendor appears once all items are scored
- FINAL requires Meets Spec and Reasonable, enforced in the database

<img src="assets/screens/16-technical-evaluation.jpg" width="100%" alt="Engineering's Technical Evaluation page: quotations awaiting assessment, no prices shown.">

<sub>Engineering's Technical Evaluation page: quotations awaiting assessment, no prices shown.</sub>

<p><img src="assets/screens/17-tbe-matrix.jpg" width="49%" alt="Technical evaluation matrix for three vendors, with the average TBE score per vendor."> <img src="assets/screens/18-final-quotations.jpg" width="49%" alt="Quotations that passed both gates: Meets spec, Reasonable and FINAL, ready to select."></p>

<sub>Left: Technical evaluation matrix for three vendors, with the average TBE score per vendor. · Right: Quotations that passed both gates: Meets spec, Reasonable and FINAL, ready to select.</sub>

### 6. Clarification and negotiation

All letters to vendors go through SCM. Engineering or QS drafts a clarification, SCM reviews and sends it, and the answer reopens the evaluation. Sessions with vendors are scheduled in one calendar, and every negotiation round is recorded and validated by QS.

- Clarification drafts wait for SCM, with a default answer deadline from the stage schedule
- Clarification and negotiation sessions in an agenda or week view, always in WIB
- Negotiation needs at least one FINAL quotation and a target or reason
- Each round shows the price before and after and the reduction

<img src="assets/screens/19-clarification.jpg" width="100%" alt="A clarification drafted by Engineering waiting for SCM, next to a scheduled session.">

<sub>A clarification drafted by Engineering waiting for SCM, next to a scheduled session.</sub>

<p><img src="assets/screens/20-session-schedule.jpg" width="49%" alt="Clarification and negotiation schedule with sessions that still need a result."> <img src="assets/screens/21-negotiation-rounds.jpg" width="49%" alt="Negotiation rounds with the price reduction per vendor, next to Initial Price and lowest offer."></p>

<sub>Left: Clarification and negotiation schedule with sessions that still need a result. · Right: Negotiation rounds with the price reduction per vendor, next to Initial Price and lowest offer.</sub>

### 7. Selected vendor and archive

The system recommends a vendor from FINAL quotations using 60% relative price and 40% TBE score. QS may mark a selected vendor, which can differ from the recommendation, with a reason that goes to the audit trail. The KTT closes the procurement with an explicit result.

- Recommendation text shows the relative price, TBE score and combined score
- Selected vendor prices are recorded as Selected in the Price Database
- Closing results: Completed, Failed, Canceled or Merged
- Reverse paths exist: repeat the RFQ, withdraw the selected vendor, reopen an archive

<img src="assets/screens/22-recommendation-archive.jpg" width="100%" alt="Recommendation and Archive: system recommendation, the vendor QS selected and its reason.">

<sub>Recommendation and Archive: system recommendation, the vendor QS selected and its reason.</sub>

<p><img src="assets/screens/23-close-procurement.jpg" width="100%" alt="The KTT closing a procurement, with the four possible results and what happens next."></p>

<sub>The KTT closing a procurement, with the four possible results and what happens next.</sub>

### 8. Price and vendor databases

The Price Database keeps unit prices from vendor quotations in the system and from past project contracts, so QS can check a price before trusting it. The vendor database is the source of RFQ recipients, with categories, umbrella contracts and a blacklist.

- Tender prices and project contract prices kept apart and filterable
- Latest price check with the tender versus project difference and a rough 6-month estimate
- Trend chart of the monthly median, optionally with vendor quotations
- Vendor database flags blacklisted vendors still in ongoing procurements and contracts about to end

<img src="assets/screens/24-price-database.jpg" width="100%" alt="Price Database with synthetic records: totals by origin and the record list.">

<sub>Price Database with synthetic records: totals by origin and the record list.</sub>

<p><img src="assets/screens/25-price-check-estimate.jpg" width="49%" alt="Latest price check for one item: tender price, project price, difference and estimate."> <img src="assets/screens/26-price-trend.jpg" width="49%" alt="Price trend for one item, project contracts and vendor quotations as two series."></p>

<sub>Left: Latest price check for one item: tender price, project price, difference and estimate. · Right: Price trend for one item, project contracts and vendor quotations as two series.</sub>

<p><img src="assets/screens/27-vendor-database.jpg" width="100%" alt="Vendor database: active, umbrella contract, incomplete and blacklisted vendors, with next actions."></p>

<sub>Vendor database: active, umbrella contract, incomplete and blacklisted vendors, with next actions.</sub>

### 9. Documents, vendor email and accounts

Every tender gets a folder tree per procurement with sections for BOQ, technical documents, vendor quotations, TBE and final documents. Each folder states who may view, upload or delete. Vendor letters are composed by the system and kept in one outbox. Admin creates accounts, primary roles and additional roles.

- Folder access follows the role: vendor quotation folders are closed to Engineering
- Files stored in the database or in SharePoint, per deployment
- Vendor Emails keeps every letter with its attachments, even when sending is off
- One account may hold more than one role; each account gets a personal assistant profile

<img src="assets/screens/28-document-explorer.jpg" width="100%" alt="Document explorer inside a vendor quotation folder, with its access rule spelled out.">

<sub>Document explorer inside a vendor quotation folder, with its access rule spelled out.</sub>

<p><img src="assets/screens/29-vendor-emails.jpg" width="49%" alt="Vendor Emails outbox with reminder and invitation letters generated by the system."> <img src="assets/screens/30-admin-accounts.jpg" width="49%" alt="Administration: account counts by group and the new account form with additional roles."></p>

<sub>Left: Vendor Emails outbox with reminder and invitation letters generated by the system. · Right: Administration: account counts by group and the new account form with additional roles.</sub>

### 10. Data assistant, practice and oversight

Each user has a data assistant that reads the same data their screens show, read-only, and cites its sources. Practice Mode runs a fictional tender in the browser with a guide per role. Observers get a dashboard sized for a wall screen, and Admin reads an audit trail that cannot be changed.

- Assistant scope equals the user's scope; answers list their sources
- Practice Mode: role switch, start over, guide steps that tick themselves
- Observer dashboard has no action buttons and enlarges on wall screens
- Audit trail groups process, technical and commercial decisions

<img src="assets/screens/31-data-assistant.jpg" width="100%" alt="Data assistant in Practice Mode (simulated answers from system data) listing who has not replied, with sources.">

<sub>Data assistant in Practice Mode (simulated answers from system data) listing who has not replied, with sources.</sub>

<p><img src="assets/screens/32-practice-mode.jpg" width="49%" alt="Practice Mode as SCM, with the practice guide listing the role's steps."> <img src="assets/screens/33-observer-wall-dashboard.jpg" width="49%" alt="Management overview at 1920 pixels wide, the wall-screen layout for observers."></p>

<sub>Left: Practice Mode as SCM, with the practice guide listing the role's steps. · Right: Management overview at 1920 pixels wide, the wall-screen layout for observers.</sub>

<p><img src="assets/screens/34-audit-trail.jpg" width="100%" alt="Audit trail with counts per decision class and the latest actions, including a vendor selection."></p>

<sub>Audit trail with counts per decision class and the latest actions, including a vendor selection.</sub>

## For developers

### Architecture

Q-NEXUS has three layers. The app is a React 19 single-page application built with Vite, TypeScript and Zustand, using a hash router so it runs from any static host. The API is Fastify 5 on Node.js with PostgreSQL through the pg driver. Between them sits a shared core, inti, that holds the business rules, types, access guards and formulas, and is compiled without browser or Node types so it can be imported by both sides.

Access guards return a decision with a sentence. The app shows that sentence as a message and the server returns it with HTTP 403, so the screen and the API can never disagree about who may do what. Guards are written as permissions, not prohibitions, so a new role is denied by default.

The app has two modes. Prototype mode keeps all data in the browser and is the target of the end-to-end suite. Server mode, switched on by one variable, replaces each store action with an API call while the pages stay the same. One read endpoint returns everything the caller may see in the same shape as the browser store, filtered by the shared scope rules, and the workspace reloads after every write instead of guessing optimistically.

Live updates use server-sent events that carry no data, only a heartbeat sent after each transaction commits. Clients react by reloading their own scoped workspace, so the scope rules are never written twice. The stream is read with fetch so the session token stays in a header, not in a URL.

Files go either into the database or into SharePoint under tender, procurement, section and vendor folders, chosen by one setting, and each row remembers where its file lives so storage can move gradually. Outbound letters are written to an outbox table inside the transaction and sent through Outlook after commit, with retries. A per-user AI agent reads data through a read-only MCP endpoint that the API itself serves.

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/architecture-dark.svg"><img src="assets/architecture-light.svg" width="100%" alt="How Q-NEXUS is built."></picture>

### Data model

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/data-model-dark.svg"><img src="assets/data-model-light.svg" width="100%" alt="Data model: Tender (tender), Procurement (paket), BOQ and items (daftar_boq, boq_item), Vendor (vendor), RFQ and recipients (rfq, rfq_vendor), Quotation and TBE (quotation, quotation_harga, rfq_tbe), Clarification (klarifikasi), Sessions and rounds (jadwal_sesi, putaran_negosiasi), Catalogue and price records (material, catatan_harga), Reference prices (initial_price, target_pagu), Selected vendor and archive (vendor_terpilih, arsip_paket), Audit (audit)."></picture>

### Key flows

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/flow-1-dark.svg"><img src="assets/flow-1-light.svg" width="100%" alt="Reading a vendor offer: Excel: the first sheet is read with SheetJS and known column headings are mapped in code, with no AI. Then Only when headings are unknown are the first rows sent to the agent, which may only say which column means what; a checker rejects bad mappings. Then Code moves the values and compares source and result cell by cell; if anything differs, the result is discarded. Then PDF or Word: the server applies the same guard used for recording a quotation, caps the file at 20 MB and reads the BOQ item names itself. Then Text is extracted; empty or scanned files are rejected before the agent is called, and the text is cut at 24,000 characters. Then Every number written in the document is collected into a set; the agent runs one-shot with a 180-second limit and is told never to compute or round. Then Each returned price must be found in that set or the row is dropped with a reason; totals and specifications are checked the same way. Then The preview shows source and result side by side with arithmetic and deviation warnings, and nothing is saved until a person presses Save."></picture>

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/flow-2-dark.svg"><img src="assets/flow-2-light.svg" width="100%" alt="RFQ List approval gate: Engineering submits an RFQ only if they are its person in charge, the BOQ has at least one item and the tender has a KTD. Then Only a KTD on the tender team may decide; a revision request needs a note. Then If the BOQ changed after the KTD opened the review, the decision is refused until the KTD confirms the latest content. Then Approval in one transaction sets the RFQ approved, releases the BOQ and moves the procurement to stage 2. Then Sending to vendors checks the approval again on the server and refuses an unapproved RFQ."></picture>

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/flow-3-dark.svg"><img src="assets/flow-3-light.svg" width="100%" alt="BOQ revision after the RFQ was sent: Engineering saves a new revision with a required reason; removed items are marked, not deleted. Then SCM is notified, the Initial Price drops to needs revalidation, and the KTD is informed without approving again. Then The vendor panel shows which vendors still hold an older revision. Then SCM sends the latest BOQ; the letter lists the changes, and vendors who declined to quote are skipped. Then Revised quotations record the revision they answer, and their evaluation returns to not assessed."></picture>

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/flow-4-dark.svg"><img src="assets/flow-4-light.svg" width="100%" alt="From evaluation to recommendation: Engineering rates specification compliance and fills the TBE matrix; QS rates the price. Then A database constraint requires both gates before a quotation can be FINAL. Then The total of each quotation is the sum of unit price times BOQ volume. Then If every FINAL candidate has a TBE score, score = 0.6 x (lowest total / total) x 100 + 0.4 x TBE; otherwise the cheapest is shown with the reason. Then The same function feeds the screen, the exported working paper and the assistant's comparison tool; QS marks the selected vendor separately."></picture>

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/flow-5-dark.svg"><img src="assets/flow-5-light.svg" width="100%" alt="Sign-in and session: The password is checked with scrypt and a constant-time comparison; unknown emails are checked against a dummy hash so timing reveals nothing. Then A random 32-byte token is issued and only its SHA-256 hash is stored, valid for 12 hours. Then A global hook resolves the session on every request and re-checks that the account is still active. Then Signing out deletes the session row, so access ends on the next request; a password change ends all other sessions."></picture>

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/flow-6-dark.svg"><img src="assets/flow-6-light.svg" width="100%" alt="Data assistant request: The browser calls the API, which forwards the question to the user's own agent through a self-hosted agent gateway. Then The agent calls back into Q-NEXUS on a read-only MCP endpoint that accepts only per-user agent tokens. Then Each request builds a fresh MCP server for that user; every tool reads the same scoped workspace as the user's screens, with prices removed for roles that may not see them. Then No tool accepts a user id and none can write, so the agent can never see or change more than its user."></picture>

### Security

- Every route passes a global authentication hook; agent tokens can only reach the read-only MCP endpoint.
- Passwords are hashed with scrypt and sessions are opaque random tokens stored as SHA-256 hashes, so logout and deactivation take effect on the next request.
- Quoted prices are removed at the read layer for Engineering, the budget ceiling is visible only to the owning KTT, and original offer files stay out of Engineering's reach.
- Key rules are enforced by the database: one selected vendor per procurement, FINAL only with both evaluation gates, and an append-only audit table guarded by a trigger.
- CORS uses an allowlist from the environment, database errors are logged instead of returned, and request logs drop query strings.
- Folder access is derived from the file key and the tender team before content is accepted; SharePoint access is limited to one site.
- Inbound vendor mail that fails DMARC or SPF is queued for a person instead of being mapped automatically, and attachments are limited by type, size and count.
- The web server sets HSTS, nosniff, frame, referrer and permissions policies and a self-only content security policy.

### Quality

- CI on GitHub Actions runs against a PostgreSQL 18 service: type checks for server and core, core unit tests, all migrations from an empty database twice (the second run must find nothing new), a schema check against a golden schema file, lint, translation checks, the app build and database-free server tests.
- The end-to-end suite passed 189 of 189 scenarios in prototype mode on 10 Nov 2026 (tools/hasil-uji-v5.json).
- The schema is built by 58 plain SQL migrations, and cek-skema compares the live database with the golden schema so drift shows up.
- A dedicated checker verifies the read-only MCP tools and their scoping with 151 assertions.
- Two translation checks keep every screen string wrapped for translation and present in the English dictionary.

### Deployment and operations

Production runs on one company VPS behind nginx with TLS: nginx serves the built app and forwards API calls to the Node.js server on the loopback interface, with PostgreSQL 18 and Node.js 26.

Releases come from a GitHub Actions workflow started by hand on main after CI is green; the deploy script builds, migrates, restarts and then proves the result with a health check, a test login and the build hash.

The production database is backed up daily at 02:30 WIB and backups are kept for 14 days.

Microsoft 365 provides document storage in SharePoint and vendor letters through Outlook; without it, files stay in PostgreSQL and letters stay in the outbox.

### Decisions

| Decision | Why |
| --- | --- |
| One shared core for app and API | Screen and server must never disagree about who may do what, and both explain a refusal with the same sentence. |
| Plain SQL migrations with a golden schema | Much of the design lives in CHECK constraints, partial indexes and triggers, which an ORM migration tool can drop silently; the schema check makes drift visible. |
| Opaque session tokens stored as hashes, not JWT | Logout and account deactivation must take effect on the next request, and a leaked database must not hand out live sessions. |
| Excel offers read by code, not AI | A model copying hundreds of numbers makes silent mistakes; the file is structured, so code moves the values and the path keeps working when the AI is down. |
| Every AI-read number must appear in the document | The model may only point at numbers, never compute them, because a computed figure would flow straight into the procurement decision. |
| One read-only agent per user over MCP | Identity comes from the token and scope equals the user's screens; decisions belong to people, so agents get no write tools. |
| Data-free live updates after commit | Filtering broadcasts per user would mean writing the scope rules a second time; clients reload their own scoped data instead. |
| Practice prices disguised with a secret salt | Practice data reaches every role's browser, including Engineering, so prices derived from real ones are scaled by a salted factor that cannot be undone from the code. |

### Built with

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/stack-dark.svg"><img src="assets/stack-light.svg" width="100%" alt="Q-NEXUS stack."></picture>

### Engineering highlights

- A number read from a PDF or Word offer is accepted only if it can be found in the document text.
- The business rules live in a shared core with no browser or Node dependency, so the app and the API apply the same logic.
- Passwords are hashed with scrypt and sessions use opaque tokens stored as hashes, so logging out revokes access at once.
- CI checks types, tests, a migration from zero against the reference schema, lint and the build against a real PostgreSQL.
- The audit trail is immutable and visible to admins only. Practice mode keeps training data apart from real prices.

---

<sub>Built by [Nugraha Labib Mujaddid](https://github.com/nugrahalabib). This page describes a private codebase; questions about the product or a demo are welcome at [nugrahalabib@gmail.com](mailto:nugrahalabib@gmail.com).</sub>

## Related

- [HC Platform for WIKA EPCC](https://github.com/nugrahalabib/wika-hc-platform-showcase)
- [DashPro for WIKA EPCC](https://github.com/nugrahalabib/wika-pms-showcase)
- [Spead AI Pro for WIKA EPCC](https://github.com/nugrahalabib/spead-pro-wika-showcase)
- [All my work on GitHub](https://github.com/nugrahalabib)
