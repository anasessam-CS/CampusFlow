# University Student Activities Management System

### نظام إدارة أنشطة الكلية

A proposed web platform for managing student communities and faculty activities at **Innovation University — Faculty of Computers and Information Technology (FCIT)**.

The system connects students, community leaders, team heads, treasurers, activities administrators, faculty management, and the departments responsible for resources and approvals. It brings the activity lifecycle into one place: from recruitment and proposals to preparation, execution, financial settlement, and archiving.

> **Project stage:** Concept and planning. This README describes the proposed system and its business rules. Implementation progress, installation instructions, and a live demo are not established by the concept document.

## Table of Contents

- [Problem Statement](#problem-statement)
- [Project Objectives](#project-objectives)
- [Scope](#scope)
- [Users and Permissions](#users-and-permissions)
- [Planned Modules](#planned-modules)
- [Activity Approval Workflow](#activity-approval-workflow)
- [Activity Lifecycle](#activity-lifecycle)
- [Financial Management Rules](#financial-management-rules)
- [Example Scenario](#example-scenario)
- [Proposed Technology Stack](#proposed-technology-stack)
- [Proposed Data Model](#proposed-data-model)
- [Security and Accountability](#security-and-accountability)
- [Implementation Roadmap](#implementation-roadmap)
- [Project Team](#project-team)

## Problem Statement

Student activity planning often relies on scattered chats, spreadsheets, and documents. This makes it difficult to identify the latest proposal, track approvals, assign responsibility, monitor resource shortages, or reconcile spending.

The proposed platform gives each activity a central record containing its proposals, decisions, team plans, tasks, requests, bookings, documents, budget, attendance, and final reports. Authorized users can see what is complete, what is pending, and who owns the next action.

## Project Objectives

- Centralize activity information and preserve document and decision history.
- Establish clear approval paths and responsibilities.
- Coordinate communities, teams, faculty management, and service departments.
- Track tasks, dependencies, deadlines, and deliverables.
- Manage budgets, sponsorships, purchases, payments, and settlements.
- Support recruitment, membership, attendance, evaluations, and certificates.
- Provide dashboards and reports for operational and administrative follow-up.

## Scope

The platform is designed to support communities such as **IEEE**, **ICPC**, and **AutoVroom**, with configurable teams and membership rules.

Supported activity types include events, workshops, competitions, recurring training programs, campaigns, meetings, and internal activities.

Each person uses one account and may hold different roles across communities, teams, seasons, and activities. Attending an event does not automatically grant organizational membership or internal permissions.

## Users and Permissions

| Role | Main responsibilities |
| --- | --- |
| Faculty Management | Make final decisions on activities, budgets, and changes requiring management approval. |
| Activities Administrator | Review completeness, coordinate requests, forward proposals, and monitor faculty activities. |
| Community President | Approve ideas internally, manage activities, assign teams, and approve team plans. |
| Treasurer | Review financial proposals internally and oversee budgets, sponsorship finances, spending, and settlements. |
| Team Head | Assign tasks, review submissions, and submit the team's final plan. |
| Team Member | Complete assigned tasks, submit deliverables, and report requirements or blockers. |
| Responsible Department | Review and fulfill requests within its authority, such as venue booking, entry permits, or procurement. |
| Student / Participant | Apply to communities, register for activities, and access personal attendance and certificates. |
| Technical System Administrator | Manage accounts and technical configuration through permissions separate from administrative approvals. |

Permissions are scoped to the relevant community, team, activity, and record. A person holding multiple roles acts under a recorded role for each decision. Delegation has a defined scope and expiry.

## Planned Modules

### 1. Communities, Recruitment, and Membership

- Community profiles, seasons, leadership, teams, and activity plans.
- Recruitment rounds with configurable questions, requirements, deadlines, and team preferences.
- Application screening, missing-information requests, interviews, assignments, and evaluations.
- Acceptance decisions, waiting lists, offer confirmation, and onboarding.
- Membership history, optional probation periods, and leadership handover.

Internal interview scores and reviewer notes are visible only to authorized reviewers.

### 2. Activity Proposals and Approvals

- Proposals containing objectives, audience, dates, venue, expected attendance, requirements, and estimated cost.
- Sequential review by the community president, treasurer, activities administrator, and faculty management.
- Recorded approvals, rejections, revision requests, and approval conditions.
- Versioned negotiations and amendments with reasons and financial impact.
- A central activity record with its current status, owner, attachments, and decision history.

### 3. Team Operations and Task Management

- Team assignments with expected outputs and deadlines.
- Member tasks with owners, contributors, priorities, attachments, and dependencies.
- Submission review, revision requests, and acceptance by the team head.
- Final team-plan approval by the community president.
- Recorded reasons for reassignment, deadline changes, blocking, and cancellation.

Planned task states: **Not Started**, **In Progress**, **Blocked**, **Submitted for Review**, **Revision Required**, **Completed**, and **Cancelled**.

| Team | Typical responsibilities |
| --- | --- |
| Public Relations (PR) | Sponsors, guests, supporting documents, and sponsorship obligations. |
| Technical | Content, trainers, software requirements, equipment specifications, and technical testing. |
| Logistics | Consolidate operational needs, check attachments, route requests, and confirm delivery or return. |
| Organizing | Reception, organizer allocation, participant flow, and the activity-day schedule. |
| Media | Designs, publishing plans, photography, coverage, and post-activity outputs. |
| Human Resources (HR) | Recruitment, member allocation, training, commitment, and evaluations. |
| Finance | Budget details, sponsorship records, procurement, payments, and settlement documents. |

### 4. Operational Requests, Resources, and Documents

- Venue and lab bookings, furniture, electricity, internet, and technical support.
- Entry requests for guests, equipment, and vehicles.
- Purchase and disbursement requests linked to approved budget items.
- Document versions, required attachments, decisions, and access restrictions.
- Separate tracking of requested, approved, and delivered quantities.
- Booking conflict checks that include setup and clearance time.
- Independent processing of unrelated requests, with dependencies recorded where needed.

The request route is: originating team and team-head review, Logistics completeness check, Activities Administrator coordination, then the responsible department's decision and fulfillment.

For example, requesting 13 tables and receiving approval for 10 must leave a visible shortage of 3. Approval alone does not mark a request as fulfilled.

### 5. Budgets, Sponsorships, and Procurement

- Proposed and approved budget versions with funding sources and restrictions.
- Separate records for commitments, actual expenses, payments, and outstanding amounts.
- Community-managed purchases and university procurement workflows.
- Cash, in-kind, and service sponsorships, including sponsor obligations and delivery evidence.
- Advances, supporting invoices, refunds, and financial settlement.
- Equipment loan records with condition, custodian, and return deadlines.

### 6. HR, Meetings, and Performance

- Member profiles covering roles, tasks, training, meetings, attendance, and evaluations.
- Role-specific performance criteria, announced before the assessment period.
- Evaluation evidence, qualitative feedback, and review requests.
- Meeting minutes and decisions that can become assigned tasks.
- Recurring training programs with separate sessions and attendance records.

Delays caused by another approving party should be attributed to that dependency when the member submitted their work on time.

### 7. Registration, Attendance, and Certificates

- Registration windows, target audiences, capacity limits, waiting lists, and cancellation rules.
- Duplicate-registration prevention and seat promotion according to configured rules.
- Proposed QR-based attendance with authorized scanning and duplicate check-in prevention.
- Documented manual entry or corrections when required.
- Certificate eligibility rules for participants, organizers, trainers, and speakers.
- Unique certificate references, verification, correction, reissue, and revocation history.

Registration, organizational membership, and external guest entry permission remain separate processes.

### 8. Dashboards, Notifications, and Reports

- A personal action dashboard showing pending reviews, deadlines, priorities, and blockers.
- Role-specific views for presidents, teams, treasurers, administrators, management, and students.
- Calendars for activities, bookings, interviews, and deadlines.
- In-system notifications, configurable reminders, and escalation periods.
- Term plans, monthly reports, resource use, processing times, attendance comparisons, and activity financial reports.
- Search, filters, and exports restricted by user permissions.

Email notifications are a possible later integration, subject to available infrastructure.

## Activity Approval Workflow

1. **Prepare the proposal:** Record the idea, objectives, audience, proposed schedule, requirements, estimated cost, and funding sources.
2. **Community president review:** Approve the idea internally, return it for revision, or reject it.
3. **Treasurer review:** Review costs and funding, then approve the financial proposal internally.
4. **Activities administrator review:** Check completeness and apparent conflicts; return missing information or forward the proposal.
5. **Faculty management decision:** Approve with recorded conditions, reject with reasons, or request negotiation and changes.
6. **Start preparation:** After approval, the president assigns teams and the detailed plans and requests begin.

When management requests changes, a new proposal version records the differences. The treasurer reviews the financial impact again, and the president reviews changes affecting the activity's scope before resubmission.

**Activity approval does not automatically confirm a venue, issue an entry permit, release funds, or authorize publication.** Each related process has its own requirements and status.

## Activity Lifecycle

| Stage | Planned statuses |
| --- | --- |
| Proposal | Draft; President Review; Financial Review; Administrator Review; Management Review. |
| Decision and preparation | Revision / Negotiation Required; Rejected; Approved; In Preparation; Ready for Execution. |
| Execution and closure | In Progress; Operationally Completed; Pending Closure; Closed; Archived. |
| Exceptions | Postponement Requested; Cancellation Requested; Postponed; Cancelled, with a documented decision. |

Registration, operational requests, and financial records retain their own statuses. Finishing the event does not close unsettled advances, outstanding payments, equipment returns, or sponsor obligations.

Postponement, cancellation, urgent requests, joint activities, incidents, and review requests should retain their reasons, responsible parties, decisions, and effects on dependent records.

## Financial Management Rules

| Item | Required treatment |
| --- | --- |
| Available budget | Approved budget minus actual expenses and outstanding unpaid commitments. |
| Cash balance | Funds actually collected minus payments actually made within the relevant account or custody. |
| Sponsor promise | Track separately from confirmed sponsorship and collected funds; a promise is not available cash. |
| University supplier payment | Record as direct university funding and expense without treating it as community-held cash. |
| Invoice | Track separately from payment; recording an invoice does not mean it has been paid. |
| Advance | Keep open until supporting expenses and returned balances have been reviewed and settled. |
| Double counting | Do not count the same amount as both an advance and a final expense, or as both a paid expense and an outstanding commitment. |
| Remaining funds | Apply funding restrictions and the authorized decision; do not automatically transfer balances to another activity. |

Preparing a financial transaction and approving it require separate authority. If the requester normally holds the approval role, an authorized alternative must be defined.

## Example Scenario

The concept document illustrates an **IEEE technical day** with a workshop and a sponsor. All amounts and outcomes below are hypothetical.

1. A student applies to Media, completes screening and an interview, confirms acceptance, and begins onboarding.
2. The president submits an activity proposal estimated at **EGP 20,000**. After review and negotiation, management approves a revised **EGP 15,000** budget.
3. Teams prepare their plans. Technical requests internet for 5 computers; Organizing requests 13 tables and 6 power points. Logistics tracks shortages and missing guest-entry documents.
4. University procurement pays **EGP 10,000** directly to suppliers. The community collects **EGP 5,000** in confirmed cash sponsorship.
5. Community expenses total **EGP 4,000**. Within that amount, a Media advance of **EGP 1,500** is settled with **EGP 1,300** in supported expenses and **EGP 200** returned.
6. After readiness checks, registration and attendance are managed under the applicable rules. Teams submit results, HR reviews participation, and Finance reconciles records.
7. Total actual expense is **EGP 14,000**, including direct university payments. The remaining sponsorship cash is **EGP 1,000**, handled according to funding conditions and the authorized decision.
8. Closure follows settlement, equipment returns, outstanding obligations, final reporting, and the required approval. Eligible certificates are issued through their own approval process.

## Proposed Technology Stack

| Layer | Proposed technology |
| --- | --- |
| Application language | PHP |
| Web framework | Laravel |
| Database | MySQL |
| User interface | Web interface; frontend implementation to be selected during detailed design. |

These are the initial choices in the concept document. Framework versions, deployment configuration, and supporting services remain to be defined. Setup and run instructions should be added once the application structure and dependencies are available.

## Proposed Data Model

The following are candidate entity groups for detailed analysis, rather than a finalized database schema:

| Domain | Candidate entities |
| --- | --- |
| Identity and organization | Users, Communities, Seasons, Teams, Memberships, Roles, Delegations. |
| Recruitment | Recruitment Rounds, Applications, Interviews, Assessments, Offers. |
| Activities and operations | Activities, Proposal Versions, Decisions, Team Plans, Tasks, Meetings, Training Sessions. |
| Resources and documents | Requests, Resources, Bookings, Permits, Documents, Document Versions. |
| Finance | Budgets, Budget Items, Sponsors, Sponsorships, Purchases, Commitments, Payments, Advances, Settlements. |
| Participation and oversight | Registrations, Attendance, Evaluations, Certificates, Notifications, Audit Logs. |

## Security and Accountability

- Enforce permissions on records, attachments, downloads, and exports.
- Restrict identity documents and internal evaluations to authorized users.
- Record who created, changed, approved, rejected, cancelled, or delegated an action, with its time, role, reason, and relevant version.
- Preserve financial and attendance corrections rather than erase their history.
- Update access during leadership handover while preserving historical records and open work.
- Validate permitted upload types and sizes.
- Define retention periods, backup procedures, and recovery checks before production use.
- Define a documented fallback for temporary attendance recording during connectivity problems, followed by authorized reconciliation.

These are proposed requirements and must be verified during implementation.

## Implementation Roadmap

The concept prioritizes **approvals, tasks, operational requests, and budgets** before expansion into the remaining modules.

- [ ] Convert the concept into detailed requirements, business rules, use cases, and acceptance criteria.
- [ ] Confirm official forms, approval authorities, delegation limits, and faculty policies.
- [ ] Design the permission matrix, user flows, screens, and database schema.
- [ ] Implement the core activity approval and versioning workflow.
- [ ] Implement team plans, tasks, operational requests, and resource bookings.
- [ ] Implement budgets, procurement, sponsorships, payments, and settlements.
- [ ] Extend the system with recruitment, membership, HR, attendance, and certificates.
- [ ] Add dashboards, reports, notifications, and authorized exports.
- [ ] Validate the complete example scenario and alternative cases, including partial fulfillment, cancellation, amendments, and pending settlement.
- [ ] Document installation, configuration, deployment, and verified application behavior.

Before detailed implementation, the faculty must confirm review periods, spending authority, budget-transfer rules, membership limits, publication conditions, certificate approval, closure criteria, and data retention periods.

## Project Team

**Institution:** Innovation University  
**Faculty:** Faculty of Computers and Information Technology

Names as listed in the concept document:

| Name | Attribution |
| --- | --- |
| أنس عصام محمد — Anas Essam Mohamed | Project owner. |
| ابراهيم لطفي | Listed project team member. |
| ماركو مجدي نسيم | Listed project team member. |
| ابانوب بهائ نبيل | Listed project team member. |

---

Based on the project concept document dated **21 November 2026, Version 1**.
