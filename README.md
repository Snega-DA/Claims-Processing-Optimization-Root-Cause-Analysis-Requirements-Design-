# Claims Processing Optimization — Business Analyst Case Study

[![Status](https://img.shields.io/badge/status-complete-brightgreen)]()
[![Domain](https://img.shields.io/badge/domain-health%20insurance-blue)]()
[![Methodology](https://img.shields.io/badge/methodology-Agile%2FScrum-orange)]()

A complete business analyst workflow applied to a real dataset of 4,500 health insurance claims — from raw data investigation through root cause analysis, formal requirements documentation, Agile backlog creation, and Jira sprint execution.

---

## Problem statement

A health insurance provider processes claims across three submission channels (Online, Paper, Phone) and five provider specialties. Leadership flagged a rising claim denial rate as a driver of member complaints, rework cost, and delayed reimbursements. This project investigates whether denials are random or concentrated in a specific, correctable pattern — and if so, defines and delivers a fix.

## Key finding

| Metric | Value |
|---|---|
| Total claims analyzed | 4,500 |
| Overall denial rate | 33.6% |
| General Practice denial rate | 35.5% |
| **General Practice + Online channel denial rate** | **39.2%** |

General Practice claims submitted online deny at nearly 6 points above the portfolio average — a specific channel × specialty risk combination, not a general quality issue. Root cause: the online intake portal has no pre-submission validation confirming a claim's procedure code matches its diagnosis code.

## Project workflow
## Repository contents

| Document | Description |
|---|---|
| [`01_Root_Cause_Analysis.docx`](./01_Root_Cause_Analysis.docx) | SQL-based denial-rate breakdown, 5 Whys drill-down, Fishbone (Ishikawa) analysis, and validation |
| [`02_Business_Requirements_Document.docx`](./02_Business_Requirements_Document.docx) | Full BRD — objectives, stakeholders, RACI, AS-IS/TO-BE, 7 business requirements (BR-01–BR-07), risks, KPIs, sign-off |
| [`03_User_Stories_Acceptance_Criteria.docx`](./03_User_Stories_Acceptance_Criteria.docx) | 7-story Agile backlog in Gherkin (Given/When/Then) format, traced to source BRD requirements |
| [`/screenshots`](./screenshots) | Jira Scrum board, groomed backlog |

## Methodology

- **Root Cause Analysis** — SQL aggregation across specialty/channel/claim type, 5 Whys, Fishbone categorization (People, Process, Technology, Policy, Data)
- **Requirements** — Business Requirements Document with MoSCoW-prioritized functional requirements, non-functional requirements, business rules, and a stakeholder RACI matrix
- **Agile delivery** — Requirements translated into a 7-story backlog with Gherkin acceptance criteria, executed in a Jira Scrum board with sprint goals, story point estimation, and burndown tracking
- **Traceability** — Every user story is labeled back to its source BRD requirement (e.g. `BR-01`), so business need → requirement → story → delivery can be traced end-to-end

## Recommended solution

Introduce real-time, specialty-specific pre-submission validation on the online claims portal — beginning with General Practice — checking diagnosis-to-procedure code consistency before a claim can be submitted, with inline error messaging so providers can correct issues immediately rather than waiting days for a denial.

**Target outcome:** Reduce the General Practice online denial rate from 39.2% to ≤33.6% (portfolio average) within two quarters, without increasing average submission time by more than 15 seconds.

## Tools used

`SQL` · `MS Excel` · `Power BI` · `Jira` · `Draw.io`

## Dataset

`enhanced_health_insurance_claims.csv` — 4,500 records covering claim amount, diagnosis/procedure codes, provider specialty, submission channel, claim status, and patient demographics.
