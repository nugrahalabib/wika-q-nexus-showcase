<!-- Showcase repository: the product is real and in use, its source code is private. -->

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/banner-dark.svg"><img src="assets/banner-light.svg" width="100%" alt="Q-NEXUS. Vendor procurement inside the tender stage, from BOQ and RFQ to evaluation, negotiation and selection."></picture>

<p align="center"><a href="https://github.com/nugrahalabib">More of my work</a> · <a href="https://nugrahalabib.com">nugrahalabib.com</a> · <a href="mailto:nugrahalabib@gmail.com">Email</a></p>

<p align="center"><a href="#the-business">The business</a> · <a href="#product-tour">Product tour</a> · <a href="#for-developers">For developers</a></p>

## Overview

Q-NEXUS is a web application for the EPCC Division of PT Wijaya Karya. It digitalises the vendor procurement work of the quantity surveying team inside the tender stage: tender, BOQ, RFQ, quotations, technical and commercial evaluation, clarification, negotiation, selected vendor and archive.

It serves ten roles, from the tender team lead and QS to engineering, supply chain, management and read-only observers. Each role gets its own dashboard and only the actions it may take.

Reading vendor offers is the hard part. Excel offers are parsed by code with no AI. PDF and Word offers are read by an AI agent, and every number it returns must be proven present in the document.

| | |
| --- | --- |
| **Status** | Live |
| **Role** | Designed, built and led by Nugraha Labib Mujaddid, Lead AI Engineer for digital transformation in the EPCC Division of PT Wijaya Karya (Persero) Tbk. |
| **Period** | Since 2026 |
| **Source** | Private. This repository presents the product; the code is not published. |

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/features-dark.svg"><img src="assets/features-light.svg" width="100%" alt="What Q-NEXUS does: Tender to RFQ list, BOQ versions, Reading vendor offers, Evaluation and recommendation, Clarification and closing, Prices, vendors and documents, Per-user data assistant, Roles, audit and practice."></picture>

## The business

Q-NEXUS is the web application the EPCC Division of PT Wijaya Karya uses to buy prices from vendors while it prepares a tender. It covers the full vendor procurement inside the tender stage: RFQ List, bill of quantities, requests for quotation, vendor quotations, technical and commercial evaluation, clarification, negotiation, selected vendor and archive, with every file kept in one document explorer per tender. Ten roles work in it, from the tender team leader, quantity surveyors and supply chain to engineering, management and read-only observers; each role sees its own dashboard and only the actions it may take, and Admin can let one person hold several roles. It matters because the vendor prices gathered here become the cost basis of the price Wijaya Karya offers its client. It was designed, built and led by Nugraha Labib Mujaddid, Lead AI Engineer for digital transformation in the EPCC Division of Wijaya Karya.

### The problem

Before Q-NEXUS, the EPCC team asked many vendors for prices, compared them, negotiated and chose a vendor through Excel files, email and WhatsApp. The work was scattered and hard to trace afterwards: which version of the item list a vendor had priced, who sent which letter, and why one vendor was preferred over another.

The stakes are high. In a tender, Wijaya Karya must know the cost of pipes, concrete, pumps and subcontract work before it can price its own bid, so one procurement can involve several disciplines, several vendors and several rounds of revision and negotiation. Price data in a state-owned company is confidential and must not leak.

The scope is deliberate. Q-NEXUS handles the relationship between Wijaya Karya and its vendors inside one tender stage. Writing the budget (RABT), management approval and submitting the bid to the client stay outside the system; the final budget documents are only uploaded as closing files.

### Who uses it

| Role | What they do with it |
| --- | --- |
| **KTT (Tender Team Leader)** | Registers the tender, appoints the MQS and GM Engineering, sets the stage schedule and the budget ceiling, and closes each procurement with its result. |
| **KTD (Design Team Leader)** | Builds and releases the RFQ List for the tender and is the only person who approves an RFQ or returns it for revision. |
| **Engineering** | Fills in the BOQ and vendor attachments, submits them to the KTD, and judges each quotation against the specification. Engineering never sees quoted prices. |
| **SCM (Supply Chain)** | The single door to vendors: sends requests for quotation with the tender team copied, follow-up BOQ revisions, reminders and clarifications, records replies and runs negotiation rounds. |
| **QS (Quantity Surveyor)** | Sets the Initial Price, reviews quotations commercially, validates negotiation rounds, and marks the selected vendor with a written reason. |
| **MQS (QS Manager)** | Sees all tenders and prices, but only writes the QS and SCM side of a team, including the QS and SCM person in charge of each procurement. A role with a single member on the team gets its person in charge automatically. |
| **GM Engineering** | Assembles the KTD and Engineering team and sets the Engineering person in charge; acts as backup for the RFQ List but does not approve RFQs. |
| **Admin** | Manages accounts, the primary role and any additional roles of each person, and reads the global audit trail. Every role except System Admin can be combined. A logged emergency mode, which requires a reason, lets Admin take over Engineering and QS tasks. |
| **Management (SVP, Manager)** | Reads progress across all tenders on an observer dashboard with no write actions. Only the SVP sees the Price Database. |
| **QS Coordinator** | Monitors all tenders, overdue work and the Price Database, without any write rights. |

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/before-after-dark.svg"><img src="assets/before-after-light.svg" width="100%" alt="Before and after: Item lists kept in separate Excel files becomes A BOQ inside each procurement with numbered revisions and a change history; Vendor letters and replies in personal email and WhatsApp becomes Letters sent by SCM from the app and logged per vendor in Vendor Emails; Decisions hard to trace afterwards becomes Every workflow action written to an append-only audit trail, with the reason; Status known only by asking around becomes Dashboards per role that list what is waiting for whom and what is late; Files passed around by email and chat becomes One folder tree per tender with rename, move, Trash and .zip download, judged by role."></picture>

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/journey-dark.svg"><img src="assets/journey-light.svg" width="100%" alt="How work flows: Register the tender, Build the team, Release the RFQ List, Prepare the BOQ, Approve the RFQ, Set the Initial Price, Send the request for quotation, Record quotations, Technical evaluation, Commercial evaluation, Clarification, Negotiation, Select the vendor, Close and archive."></picture>

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/value-dark.svg"><img src="assets/value-light.svg" width="100%" alt="What it changes: 10 roles, each with its own dashboard and rights; 7 workflow stages from RFQ List to archive; 60 / 40 price and technical weighting of the system recommendation; 16 item and vendor categories; 189 / 189 end-to-end scenarios passing in prototype mode on 10 Nov 2026; ID | EN every screen in Indonesian and English."></picture>

### Model and status

Q-NEXUS is an internal system of the EPCC Division of PT Wijaya Karya (Persero) Tbk, not a commercial product, so it has no pricing. It runs in production with a real database, connected to Microsoft 365 for document storage in SharePoint and for vendor letters through Outlook.

Adoption is supported inside the product. Since November 2026 a Practice Mode lets any employee start a fictional sample tender in their own browser, take their role's steps with a guide that ticks itself off, and see the result reach the next role, without touching real data or sending email.

## Product tour

### 1. Sign-in, role dashboards and two languages

Accounts are created by Admin; there is no self-registration. After sign-in every role lands on its own dashboard, built around a Needs Your Action list that names the next step and links straight to the place where it is done. Every dashboard panel can be collapsed, and the whole interface switches between Indonesian and English.

- Ten roles; the sidebar only shows the pages a role may use, in the order of that role's daily work
- Needs Your Action list, most urgent on top, with "You are PIC" tags
- MQS and GM Engineering assign persons in charge inline, with team workload in view
- Indonesian and English for every screen, switched from the top bar

<img src="assets/screens/01-login-en.jpg" width="100%" alt="Sign-in page in English, with the four parts of the process summarised on the left.">

<sub>Sign-in page in English, with the four parts of the process summarised on the left.</sub>

<p><img src="assets/screens/02-ktt-dashboard.jpg" width="49%" alt="Tender team leader dashboard: key figures and the decisions waiting for the KTT."> <img src="assets/screens/03-mqs-assign-pic.jpg" width="49%" alt="QS Manager dashboard: two procurements without SCM and QS owners, assigned inline."></p>

<sub>Left: Tender team leader dashboard: key figures and the decisions waiting for the KTT. · Right: QS Manager dashboard: two procurements without SCM and QS owners, assigned inline.</sub>

<p><img src="assets/screens/04-procurement-list-id.jpg" width="100%" alt="The procurement list in Indonesian, showing stage, state and deadline per procurement."></p>

<sub>The procurement list in Indonesian, showing stage, state and deadline per procurement.</sub>

### 2. Tender page

A tender is the client's tender; inside it, each procurement is one RFQ. The tender page shows readiness, a stage schedule against the submission deadline, every procurement, the tender documents, the RFQ List summary and the team. Each of its six panels opens and closes from its title, and the choice is remembered per account.

- Readiness checks for team, stage schedule, procurements and documents
- Stage schedule chart with today's line and the submission deadline
- Collapse All Panels; a closed panel keeps its title and a one-line summary, and links open their target panel first
- Tender Team panel names each person's load, the tenders they are in, the procurements they hold and how many are late

<img src="assets/screens/05-tender-page.jpg" width="100%" alt="Tender page of the practice tender: readiness, stage schedule and tender team.">

<sub>Tender page of the practice tender: readiness, stage schedule and tender team.</sub>

<p><img src="assets/screens/35-tender-panels-collapsed.jpg" width="49%" alt="The same page with Stage Schedule, Procurement and Tender Documents closed to their one-line summaries."> <img src="assets/screens/36-tender-team-panel.jpg" width="49%" alt="Tender Team panel seen by the QS Manager: tenders and procurements held per person, with Add and Remove for the QS and SCM side."></p>

<sub>Left: The same page with Stage Schedule, Procurement and Tender Documents closed to their one-line summaries. · Right: Tender Team panel seen by the QS Manager: tenders and procurements held per person, with Add and Remove for the QS and SCM side.</sub>

<p><img src="assets/screens/06-tender-progress.jpg" width="100%" alt="Dashboard view of tender progress across the seven stages and procurement progress per stage."></p>

<sub>Dashboard view of tender progress across the seven stages and procurement progress per stage.</sub>

### 3. RFQ List

The KTD builds the RFQ List, and nothing reaches a vendor until the KTD approves the RFQ. The list is a compact table: one row per RFQ, grouped by state, with a header that stays in view while scrolling, so a tender with many RFQs fits on one screen.

- Groups: awaiting KTD, needs revision, in progress by Engineering, approved and ready to send, sent, completed
- Columns for RFQ number, name and discipline, PIC, target, BOQ state, RFQ state and actions; the KTD's revision note sits under the BOQ state
- On narrow screens the table scrolls sideways inside its panel while the RFQ number and name stay in place
- Progress and Who Is Being Waited On sit under the table; the review window lists BOQ items, attachments and who is notified

<img src="assets/screens/07-rfq-list.jpg" width="100%" alt="The KTD's RFQ List as a compact table: awaiting KTD, needs revision with the KTD's note, in progress and approved.">

<sub>The KTD's RFQ List as a compact table: awaiting KTD, needs revision with the KTD's note, in progress and approved.</sub>

<p><img src="assets/screens/37-rfq-list-progress.jpg" width="49%" alt="Bottom of the same list: sent RFQs, then approval progress and who the list is waiting on."> <img src="assets/screens/08-ktd-review-rfq.jpg" width="49%" alt="KTD review of one RFQ: BOQ items, the attachment for vendors, and Approve or Request Revision."></p>

<sub>Left: Bottom of the same list: sent RFQs, then approval progress and who the list is waiting on. · Right: KTD review of one RFQ: BOQ items, the attachment for vendors, and Approve or Request Revision.</sub>

### 4. BOQ versions

The bill of quantities often changes after vendors already received it. Q-NEXUS keeps numbered revisions with a required reason, records which revision each quotation answers, and tells SCM which vendors still hold an old version. Sending the new revision lists the changes for the vendor.

- Rev 0 is the BOQ approved by the KTD; later revisions need a reason
- Per-item comparison: volume changed, new item, removed item
- Quotations answering an older revision stay valid but are flagged
- Vendors who declined to quote are skipped when the new revision is sent

<img src="assets/screens/09-boq-revision-history.jpg" width="100%" alt="BOQ revision history: reason, summary and item-by-item comparison of Rev 1 and Rev 2.">

<sub>BOQ revision history: reason, summary and item-by-item comparison of Rev 1 and Rev 2.</sub>

<p><img src="assets/screens/10-boq-rev-ribbon.jpg" width="49%" alt="Vendor quotations with the notice that two vendors still hold an older BOQ."> <img src="assets/screens/11-send-latest-boq.jpg" width="49%" alt="Sending BOQ Rev 2: the changes, the receiving vendors and the vendor that was skipped."></p>

<sub>Left: Vendor quotations with the notice that two vendors still hold an older BOQ. · Right: Sending BOQ Rev 2: the changes, the receiving vendors and the vendor that was skipped.</sub>

### 5. Requests for quotation

Each procurement has one workspace with a seven-stage tracker and a What You Need to Do list for the person signed in. SCM picks vendors in one window: the match follows the category SCM searches for, a second box searches the items a vendor supplies, and the letter goes out with the tender team copied.

- Category filter decides what counts as a match; without one, the procurement's discipline is mapped to a category
- Search material item narrows vendors by the categories and materials they supply, and ranks material matches first
- Blacklisted vendors are hidden and vendors without a valid email cannot be chosen
- Cc prefilled with the sending SCM, the RFQ creator, the KTD, the QS PIC and the KTT; editable, at most 10, invalid addresses refused

<img src="assets/screens/12-procurement-workspace.jpg" width="100%" alt="Procurement workspace: stage tracker and the SCM's three next steps.">

<sub>Procurement workspace: stage tracker and the SCM's three next steps.</sub>

<p><img src="assets/screens/13-send-rfq-vendor-picker.jpg" width="49%" alt="Send Request for Quotation: category Mekanikal & Pompa plus the item search &quot;pompa&quot; leave 13 of 37 vendors, two ticked."> <img src="assets/screens/47-send-rfq-cc.jpg" width="49%" alt="The same window further down: the letter to the vendor with the tender team prefilled as Cc."></p>

<sub>Left: Send Request for Quotation: category Mekanikal & Pompa plus the item search "pompa" leave 13 of 37 vendors, two ticked. · Right: The same window further down: the letter to the vendor with the tender team prefilled as Cc.</sub>

### 6. Recording and reading vendor offers

Replies are recorded against deadlines and against the BOQ revision they answer. Offers can be read from the vendor's own file instead of retyped: Excel by code, PDF and Word by an AI agent whose numbers must appear in the document.

- Late replies, missing replies and declined quotations are marked per vendor
- Excel offers are mapped by column headings in code, with no AI
- Side-by-side source and result, arithmetic check, and nothing saved until a person presses Save

<img src="assets/screens/14-quotations-deadline.jpg" width="100%" alt="Quotations after the deadline: lowest offer, a late reply and vendors with no response.">

<sub>Quotations after the deadline: lowest offer, a late reply and vendors with no response.</sub>

<p><img src="assets/screens/15-offer-reading-excel.jpg" width="100%" alt="Reading a synthetic Excel offer: columns recognised without AI, one arithmetic mismatch flagged."></p>

<sub>Reading a synthetic Excel offer: columns recognised without AI, one arithmetic mismatch flagged.</sub>

### 7. Technical and commercial evaluation

Engineering judges specification compliance without seeing prices; QS judges the price. A quotation becomes FINAL only when both gates are met. The technical evaluation matrix scores each item per vendor and produces the TBE score used later in the recommendation.

- Technical Evaluation page lists quotations awaiting the engineer, with no price columns
- TBE matrix: Comply 100, Comply with Note 1 to 99 with a required note, Not Comply 0
- TBE score per vendor appears once all items are scored
- FINAL requires Meets Spec and Reasonable, enforced in the database

<img src="assets/screens/16-technical-evaluation.jpg" width="100%" alt="Engineering's Technical Evaluation page: quotations awaiting assessment, no prices shown.">

<sub>Engineering's Technical Evaluation page: quotations awaiting assessment, no prices shown.</sub>

<p><img src="assets/screens/17-tbe-matrix.jpg" width="49%" alt="Technical evaluation matrix for three vendors, with the average TBE score per vendor."> <img src="assets/screens/18-final-quotations.jpg" width="49%" alt="Quotations that passed both gates: Meets spec, Reasonable and FINAL, ready to select."></p>

<sub>Left: Technical evaluation matrix for three vendors, with the average TBE score per vendor. · Right: Quotations that passed both gates: Meets spec, Reasonable and FINAL, ready to select.</sub>

### 8. Clarification and negotiation

All letters to vendors go through SCM. Engineering or QS drafts a clarification, SCM reviews and sends it, and the answer reopens the evaluation. Sessions with vendors are scheduled in one calendar, and every negotiation round is recorded and validated by QS.

- Clarification drafts wait for SCM, with a default answer deadline from the stage schedule
- Clarification and negotiation sessions in an agenda or week view, always in WIB
- Negotiation needs at least one FINAL quotation and a target or reason
- Each round shows the price before and after and the reduction

<img src="assets/screens/19-clarification.jpg" width="100%" alt="A clarification drafted by Engineering waiting for SCM, next to a scheduled session.">

<sub>A clarification drafted by Engineering waiting for SCM, next to a scheduled session.</sub>

<p><img src="assets/screens/20-session-schedule.jpg" width="49%" alt="Clarification and negotiation schedule with sessions that still need a result."> <img src="assets/screens/21-negotiation-rounds.jpg" width="49%" alt="Negotiation rounds with the price reduction per vendor, next to Initial Price and lowest offer."></p>

<sub>Left: Clarification and negotiation schedule with sessions that still need a result. · Right: Negotiation rounds with the price reduction per vendor, next to Initial Price and lowest offer.</sub>

### 9. Selected vendor and archive

The system recommends a vendor from FINAL quotations using 60% relative price and 40% TBE score. QS may mark a selected vendor, which can differ from the recommendation, with a reason that goes to the audit trail. The KTT closes the procurement with an explicit result.

- Recommendation text shows the relative price, TBE score and combined score
- Selected vendor prices are recorded as Selected in the Price Database
- Closing results: Completed, Failed, Canceled or Merged
- Reverse paths exist: repeat the RFQ, withdraw the selected vendor, reopen an archive

<img src="assets/screens/22-recommendation-archive.jpg" width="100%" alt="Recommendation and Archive: system recommendation, the vendor QS selected and its reason.">

<sub>Recommendation and Archive: system recommendation, the vendor QS selected and its reason.</sub>

<p><img src="assets/screens/23-close-procurement.jpg" width="100%" alt="The KTT closing a procurement, with the four possible results and what happens next."></p>

<sub>The KTT closing a procurement, with the four possible results and what happens next.</sub>

### 10. Price and vendor databases

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

### 11. Documents explorer

Every tender gets one folder tree: Tender Documents, then per procurement BOQ and Attachments, Technical Documents, Vendor Quotations, Technical Evaluation, Final Documents and Other. The explorer works like a shared drive: open, download, rename, move, see details, copy a link, create folders and delete to a Trash, with every action checked against the same rule on screen and on the server.

- Each folder states who fills it, who may open it and whether it is shared outside
- Rename, move and delete follow one rule: the uploader, the procurement PIC for the folders of their task, or a holder of extra delete access
- Move offers only folders of the same procurement or Tender Documents; folders of a different price nature are dimmed with the reason
- Folders made by people can be renamed, downloaded as .zip or deleted; system folders keep their names

<img src="assets/screens/38-documents-folder-view.jpg" width="100%" alt="Technical Documents of one procurement, with its folders, the command bar and the access rule of the folder.">

<sub>Technical Documents of one procurement, with its folders, the command bar and the access rule of the folder.</sub>

<p><img src="assets/screens/40-documents-file-menu.jpg" width="49%" alt="File menu: download, rename, move, details, copy link and delete, which sends the file to Trash for 30 days."> <img src="assets/screens/41-documents-details.jpg" width="49%" alt="Details of one file: type, uploader, date, full folder path and where it is stored."></p>

<sub>Left: File menu: download, rename, move, details, copy link and delete, which sends the file to Trash for 30 days. · Right: Details of one file: type, uploader, date, full folder path and where it is stored.</sub>

<p><img src="assets/screens/42-documents-move.jpg" width="100%" alt="Moving a file: allowed folders, dimmed folders with their reason, and what changes after the move."></p>

<sub>Moving a file: allowed folders, dimmed folders with their reason, and what changes after the move.</sub>

### 12. Selecting many, Trash, sharing and folder rules

Several files can be ticked at once; the bar says how many of them can be moved or deleted and why the rest stay. Deleted files wait in a Trash for 30 days and can be restored by whoever may still delete them. Folders are shared with named outside people for a limited time, and folders that may not be shared say why.

- Selection bar: Download .zip of the ticked files, Move n of m, Delete n of m, with the reason for files left behind
- Trash keeps files closed to downloads, Admin and the data assistant until they are restored or removed after 30 days
- Sharing: SCM shares with invited vendors, the KTT with the owner or consultants, view only or upload, with an end date
- Folders freeze when the tender stops running or the procurement is completed: download stays, changes are refused

<img src="assets/screens/39-documents-multi-select.jpg" width="100%" alt="Three files ticked by an engineer who uploaded one of them: Move 1 of 3 and Delete 1 of 3, with the reason for the other two.">

<sub>Three files ticked by an engineer who uploaded one of them: Move 1 of 3 and Delete 1 of 3, with the reason for the other two.</sub>

<p><img src="assets/screens/44-documents-trash.jpg" width="49%" alt="Trash: a deleted file with the days left, who deleted it, its original folder and Restore."> <img src="assets/screens/43-documents-share.jpg" width="49%" alt="Sharing Technical Documents from the local Microsoft 365 mock: invited vendors, view or upload, and an end date."></p>

<sub>Left: Trash: a deleted file with the days left, who deleted it, its original folder and Restore. · Right: Sharing Technical Documents from the local Microsoft 365 mock: invited vendors, view or upload, and an end date.</sub>

<p><img src="assets/screens/48-documents-share-reason.jpg" width="49%" alt="Tender Documents cannot be shared outside, and the folder says why and what to share instead."> <img src="assets/screens/28-document-explorer.jpg" width="49%" alt="A vendor quotation folder seen by SCM, with its access rule spelled out: closed to Engineering, KTD and GM Engineering."></p>

<sub>Left: Tender Documents cannot be shared outside, and the folder says why and what to share instead. · Right: A vendor quotation folder seen by SCM, with its access rule spelled out: closed to Engineering, KTD and GM Engineering.</sub>

### 13. Vendor letters, email settings and notifications

Vendor letters are composed by the system and kept in one outbox, even when sending is switched off. The Email Settings page says plainly where a person's letters leave from, based on the last letter actually sent, and the notification panel scrolls with its header fixed.

- Vendor Emails keeps every letter with its attachments and Cc
- Letters from an address outside the Microsoft 365 mailboxes leave from the procurement service mailbox, with vendor replies still going to the person
- Notification panel scrolls, stays above the sidebar, and fits a phone screen

<img src="assets/screens/29-vendor-emails.jpg" width="100%" alt="Vendor Emails outbox with invitation letters generated by the system.">

<sub>Vendor Emails outbox with invitation letters generated by the system.</sub>

<p><img src="assets/screens/51-email-settings.jpg" width="49%" alt="Email Settings: where letters are sent from, explained for an account that has not sent yet (signature preview partly masked)."> <img src="assets/screens/50-notification-panel.jpg" width="49%" alt="Notification panel open over the SCM dashboard, listing BOQ updates and PIC assignments."></p>

<sub>Left: Email Settings: where letters are sent from, explained for an account that has not sent yet (signature preview partly masked). · Right: Notification panel open over the SCM dashboard, listing BOQ updates and PIC assignments.</sub>

### 14. Accounts, role stacking and menus

Admin creates accounts and sets each person's primary role and any additional roles; every role except System Admin can be combined. The person switches the role in use from the name card, and every guard reads the role in use, while inside one tender a person holds exactly one role. The sidebar follows the daily work of the role in use.

- May also work as: KTT, MQS, GM Engineering, KTD, Engineering, SCM, Management, QS Coordinator
- An additional role cannot be removed while the person still holds an ongoing tender in that role
- Name card menu lists each role with what the person holds in it
- Extra folder access is judged by the role the person holds in that tender, so switching roles never widens it

<img src="assets/screens/30-admin-accounts.jpg" width="100%" alt="Administration: account counts by group and the new account form with additional roles.">

<sub>Administration: account counts by group and the new account form with additional roles.</sub>

<p><img src="assets/screens/45-admin-role-stacking.jpg" width="49%" alt="Editing an account: a QS staff member who may also work as MQS and Engineering (ID number cleared for the capture)."> <img src="assets/screens/46-role-switch-menu.jpg" width="49%" alt="The same person's name card: QS in use, MQS and Engineering available, and Role Practice."></p>

<sub>Left: Editing an account: a QS staff member who may also work as MQS and Engineering (ID number cleared for the capture). · Right: The same person's name card: QS in use, MQS and Engineering available, and Role Practice.</sub>

<p><img src="assets/screens/52-sidebar-per-role.jpg" width="100%" alt="Sidebar order for SCM, Engineering, KTD and Admin, each following that role's daily work (four real captures side by side)."></p>

<sub>Sidebar order for SCM, Engineering, KTD and Admin, each following that role's daily work (four real captures side by side).</sub>

### 15. Data assistant, practice and oversight

Each user has a data assistant that reads the same data their screens show, read-only, and cites its sources. Practice Mode runs a fictional tender in the browser with a guide per role. Observers get a dashboard sized for a wall screen, Admin's governance dashboard folds like the others, and Admin reads an audit trail that cannot be changed.

- Assistant scope equals the user's scope; answers list their sources
- Practice Mode: role switch, start over, guide steps that tick themselves
- Observer dashboard has no action buttons and enlarges on wall screens
- Audit trail groups process, technical and commercial decisions

<img src="assets/screens/31-data-assistant.jpg" width="100%" alt="Data assistant in Practice Mode (simulated answers from system data) listing RFQ reply status per procurement, with sources.">

<sub>Data assistant in Practice Mode (simulated answers from system data) listing RFQ reply status per procurement, with sources.</sub>

<p><img src="assets/screens/32-practice-mode.jpg" width="49%" alt="Practice Mode as SCM, with the practice guide listing the role's steps."> <img src="assets/screens/33-observer-wall-dashboard.jpg" width="49%" alt="Management overview at 1920 pixels wide, the wall-screen layout for observers."></p>

<sub>Left: Practice Mode as SCM, with the practice guide listing the role's steps. · Right: Management overview at 1920 pixels wide, the wall-screen layout for observers.</sub>

<p><img src="assets/screens/49-admin-dashboard-collapsible.jpg" width="49%" alt="Admin's governance dashboard with three cards closed to their title and summary."> <img src="assets/screens/34-audit-trail.jpg" width="49%" alt="Audit trail with counts per decision class and the latest actions, including a vendor selection."></p>

<sub>Left: Admin's governance dashboard with three cards closed to their title and summary. · Right: Audit trail with counts per decision class and the latest actions, including a vendor selection.</sub>

## For developers

### Architecture

Q-NEXUS has three layers. The app is a React 19 single-page application built with Vite, TypeScript and Zustand, using a hash router so it runs from any static host. The API is Fastify 5 on Node.js with PostgreSQL through the pg driver. Between them sits a shared core, inti, that holds the business rules, types, access guards and formulas, and is compiled without browser or Node types so it can be imported by both sides.

Access guards return a decision with a sentence. The app shows that sentence as a message and the server returns it with HTTP 403, so the screen and the API can never disagree about who may do what. Guards are written as permissions, not prohibitions, so a new role is denied by default.

The app has two modes. Prototype mode keeps all data in the browser and is the target of the end-to-end suite. Server mode, switched on by one variable, replaces each store action with an API call while the pages stay the same. One read endpoint returns everything the caller may see in the same shape as the browser store, filtered by the shared scope rules, and the workspace reloads after every write instead of guessing optimistically.

Live updates use server-sent events that carry no data, only a heartbeat sent after each transaction commits. Clients react by reloading their own scoped workspace, so the scope rules are never written twice. The stream is read with fetch so the session token stays in a header, not in a URL.

Files go either into the database or into SharePoint under tender, procurement, section and vendor folders, chosen by one setting, and each row remembers where its file lives so storage can move gradually. Outbound letters are written to an outbox table inside the transaction and sent through Outlook after commit, with retries. A per-user AI agent reads data through a read-only MCP endpoint that the API itself serves.

Documents follow one rule set in the core. Rename and move reuse the delete rule, and a move goes to SharePoint first with conflict detection; the database row, the audit entry and the notice to the uploader then commit in one transaction, and the item is moved back if that fails. Deleted files go to a closed Trash folder for 30 days, because Microsoft Graph restores deleted items only on OneDrive Personal.

Role stacking keeps a single role in use. Admin sets a primary role and additional roles, the person switches from the name card, and every guard keeps reading the role in use. Inside a tender a person holds one role, stored on the team row, so access to price folders is judged by that tender role and never by whichever role happens to be switched on.

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/architecture-dark.svg"><img src="assets/architecture-light.svg" width="100%" alt="How Q-NEXUS is built."></picture>

### Data model

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/data-model-dark.svg"><img src="assets/data-model-light.svg" width="100%" alt="Data model: Accounts and roles (pengguna), Tender (tender), Procurement (paket), BOQ and items (daftar_boq, boq_item), Vendor (vendor), RFQ and recipients (rfq, rfq_vendor), Quotation and TBE (quotation), Clarifications (klarifikasi), Catalogue and prices (material), Selected vendor (vendor_terpilih), Audit (audit), Trash (berkas_sampah)."></picture>

### Key flows

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/flow-1-dark.svg"><img src="assets/flow-1-light.svg" width="100%" alt="Reading a vendor offer: Excel: the first sheet is read with SheetJS and known column headings are mapped in code, with no AI. Then Only when headings are unknown are the first rows sent to the agent, which may only say which column means what; a checker rejects bad mappings. Then Code moves the values and compares source and result cell by cell; if anything differs, the result is discarded. Then PDF or Word: the server applies the same guard used for recording a quotation, caps the file at 20 MB and reads the BOQ item names itself. Then Text is extracted; empty or scanned files are rejected before the agent is called, and the text is cut at 24,000 characters. Then Every number written in the document is collected into a set; the agent runs one-shot with a 180-second limit and is told never to compute or round. Then Each returned price must be found in that set or the row is dropped with a reason; totals and specifications are checked the same way. Then The preview shows source and result side by side with arithmetic and deviation warnings, and nothing is saved until a person presses Save."></picture>

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/flow-2-dark.svg"><img src="assets/flow-2-light.svg" width="100%" alt="RFQ List approval gate: Engineering submits an RFQ only if they are its person in charge, the BOQ has at least one item and the tender has a KTD. Then Only a KTD on the tender team may decide; a revision request needs a note. Then If the BOQ changed after the KTD opened the review, the decision is refused until the KTD confirms the latest content. Then Approval in one transaction sets the RFQ approved, releases the BOQ and moves the procurement to stage 2. Then Sending to vendors checks the approval again on the server and refuses an unapproved RFQ."></picture>

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/flow-3-dark.svg"><img src="assets/flow-3-light.svg" width="100%" alt="BOQ revision after the RFQ was sent: Engineering saves a new revision with a required reason; removed items are marked, not deleted. Then SCM is notified, the Initial Price drops to needs revalidation, and the KTD is informed without approving again. Then The vendor panel shows which vendors still hold an older revision. Then SCM sends the latest BOQ; the letter lists the changes, and vendors who declined to quote are skipped. Then Revised quotations record the revision they answer, and their evaluation returns to not assessed."></picture>

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/flow-4-dark.svg"><img src="assets/flow-4-light.svg" width="100%" alt="Moving a document: Move is offered only to people who may delete the file: its uploader, the PIC for their folders, or extra delete access. Then Destinations are folders of the same procurement or Tender Documents; others are dimmed with a reason. Then The window says what changes: the category, who can open the file, and who loses extra access. Then The server locks the document and its content, then moves the SharePoint item first; a name clash returns 409. Then Row, audit entry and notice to the uploader commit in one transaction; on failure the item is moved back."></picture>

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/flow-5-dark.svg"><img src="assets/flow-5-light.svg" width="100%" alt="From evaluation to recommendation: Engineering rates specification compliance and fills the TBE matrix; QS rates the price. Then A database constraint requires both gates before a quotation can be FINAL. Then The total of each quotation is the sum of unit price times BOQ volume. Then If every FINAL candidate has a TBE score, score = 0.6 x (lowest total / total) x 100 + 0.4 x TBE; otherwise the cheapest is shown with the reason. Then The same function feeds the screen, the exported working paper and the assistant's comparison tool; QS marks the selected vendor separately."></picture>

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/flow-6-dark.svg"><img src="assets/flow-6-light.svg" width="100%" alt="Data assistant request: The browser calls the API, which forwards the question to the user's own agent through a self-hosted agent gateway. Then The agent calls back into Q-NEXUS on a read-only MCP endpoint that accepts only per-user agent tokens. Then Each request builds a fresh MCP server for that user; every tool reads the same scoped workspace as the user's screens, with prices removed for roles that may not see them. Then No tool accepts a user id and none can write, so the agent can never see or change more than its user."></picture>

### Security

- Every route passes a global authentication hook; agent tokens can only reach the read-only MCP endpoint.
- Passwords are hashed with scrypt and sessions are opaque random tokens stored as SHA-256 hashes, valid for 12 hours, so logout and deactivation take effect on the next request.
- Quoted prices are removed at the read layer for Engineering, the budget ceiling is visible only to the owning KTT, and original offer files stay out of Engineering's reach.
- Key rules are enforced by the database: one selected vendor per procurement, FINAL only with both evaluation gates, and an append-only audit table guarded by a trigger.
- Rename, move and delete reuse the delete rule on screen, in the store and on the server; observers, MQS and GM Engineering stay read-only, and folders freeze when the tender stops running or the procurement is completed.
- Extra folder access is judged by the role the person holds in that tender; while the person works in a role without prices, price folders stay closed in the app.
- Files in Trash are closed to downloads, Admin and the data assistant, and the Trash list is a separate route so it never reaches the agent's workspace.
- Folder access is derived from the file key and the tender team before content is accepted; SharePoint access is limited to one site.
- Inbound vendor mail that fails DMARC or SPF is queued for a person instead of being mapped automatically, and attachments are limited by type, size and count.
- CORS uses an allowlist, database errors are logged instead of returned, and the web server sets HSTS, nosniff, frame, referrer and permissions policies and a self-only content security policy.

### Quality

- CI on GitHub Actions runs against a PostgreSQL 18 service: type checks for server and core, core unit tests, all migrations from an empty database twice (the second run must find nothing new), a schema check against a golden schema file, lint, translation checks, the app build and database-free server tests.
- The shared core has 512 unit tests; all 512 passed when re-run locally for this showcase on 27 Nov 2026 at commit 5a43340.
- The end-to-end suite passed 189 of 189 scenarios in prototype mode on 10 Nov 2026 (tools/hasil-uji-v5.json).
- The schema is built by 61 plain SQL migrations, 78 tables after a run from an empty database, and cek-skema compares the live database with the golden schema so drift shows up.
- A dedicated checker verifies the read-only MCP tools and their scoping per role, and two translation checks keep every screen string wrapped for translation and present in the English dictionary.

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
| A Trash inside Q-NEXUS | Microsoft Graph restores deleted items only on OneDrive Personal, so deleted files move to a closed Trash folder for 30 days and are restored from the app. |
| One role in use, one role per tender | Every guard already reads the role in use, so stacking roles needed no second rule set, and access inside a tender never depends on which role is switched on. |

### Built with

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/stack-dark.svg"><img src="assets/stack-light.svg" width="100%" alt="Q-NEXUS stack."></picture>

### Engineering highlights

- A number read from a PDF or Word offer is accepted only if it can be found in the document text.
- The business rules live in a shared core with no browser or Node dependency, so the app and the API apply the same logic.
- Passwords are hashed with scrypt and sessions use opaque tokens stored as hashes, so logging out revokes access at once.
- CI checks types, tests, a migration from zero against the reference schema, lint and the build against a real PostgreSQL.
- The audit trail is immutable and visible to admins only. Practice mode keeps training data apart from real prices.
- Rename, move and delete in the document explorer follow one rule on screen and on the server, deleted files wait 30 days in Trash, and folders freeze once a procurement closes.

## Related

- [HC Platform for Wijaya Karya](https://github.com/nugrahalabib/wika-hc-platform-showcase)
- [DashPro for Wijaya Karya](https://github.com/nugrahalabib/wika-pms-showcase)
- [Spead AI Pro for Wijaya Karya](https://github.com/nugrahalabib/spead-pro-wika-showcase)
- [All my work on GitHub](https://github.com/nugrahalabib)

---

<sub>Built by [Nugraha Labib Mujaddid](https://github.com/nugrahalabib). This page describes a private codebase; questions about the product or a demo are welcome at [nugrahalabib@gmail.com](mailto:nugrahalabib@gmail.com).</sub>
