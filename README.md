# 1st-Project-Clinical-data-management-of-phase-III-clinical-trials-
### From CRF Design to Database Lock

An academic portfolio project that simulates the clinical data management (CDM) workflow for a fictional Phase III hypertension trial (**Drug X vs Control**), built in Excel and Google Sheets.

> **Disclaimer:** All data, participants, responses, roles and approvals are synthetic. This is a training project, not a real trial, a validated EDC system, an audit trail, a regulatory submission or professional clinical-trial experience.

**Author:** Mahamad Zaid Fattaullah Sayyed

---

## Project at a glance

| Item | Detail |
|---|---|
| Protocol ID | HTN-X-EDU-001 (educational version 1.0) |
| Design | Simulated randomised, controlled, parallel-group study, 1:1 Drug X vs Control |
| Participants | 20 fictional adults aged 18-65 (10 per group) |
| Visits | Screening, Baseline, Week 4, Week 8, Week 12 (100 participant-visit records) |
| Primary endpoint | Week 12 systolic BP minus Baseline systolic BP (mmHg); derived only, no efficacy inference |
| Tools | Microsoft Excel, Google Sheets, data validation, formulas, conditional formatting, named ranges |

## CDM workflow covered

Protocol review -> CRF design -> database design -> data entry -> validation (edit checks) -> discrepancy management and queries -> AE / medication reconciliation -> review and mock database lock -> final report.

## Repository structure (one file per day)

| Day | Deliverable | File |
|---|---|---|
| 1 | Protocol summary and CDM workflow | `Day1_Protocol_Summary.xlsx` |
| 2 | CRF worksheet, data dictionary, controlled lists | `Day2_CRF_Worksheet.xlsx` |
| 3 | Database structure (keys, relationships, participant register) | `Day3_Database_Worksheet.xlsx` |
| 4 | Working dataset and validation rules | `Day4_Working_Dataset_and_Validation.xlsx` |
| 5 | Data review and query tracker | `Day5_Data_Review_and_Query_Tracker.xlsx` |
| 6 | Completed review documentation and mock lock checklist | `Day6_Review_and_Lock_Checklist.xlsx` |
| 7 | Final project report and portfolio | `Day7_Final_Project_Report.xlsx` |

Each file opens with an `About_Day_N` sheet and carries the supporting data it needs, so every file works on its own.

## What each day shows

**Day 1 - Protocol summary.** One-page protocol summary, a ten-stage CDM workflow, and a table linking each protocol element to the data management decision it drives.

**Day 2 - CRF worksheet.** A blank, printable CRF with dropdowns and numeric/date validation, required-field markers, units (mmHg), and explicit missing-data rules (a blank is never treated as No or None). Includes the data dictionary and controlled lists.

**Day 3 - Database structure.** One row per participant-visit with the composite key Study_ID + Visit, a participant register, and repeatable AE and concomitant-medication logs. Live structure checks confirm 20 participants, 100 unique keys and 10 / 10 allocation.

**Day 4 - Working dataset and validation rules.** 100 synthetic visit records containing five deliberate errors, 26 documented validation rules, and formula-based checks (ID, age, treatment, visit, date window, SBP/DBP, BP order, AE, required fields, unique key, consistency, AE/CM reconciliation, source match). The validation summary shows 95 records passing and 5 with issues.

**Day 5 - Data review and query tracker.** The five discrepancies, each traced through a query lifecycle (Open -> Answered -> Resolved) with original and corrected values, source reference, change log and recheck:

| Query | Variable | Entered | Corrected |
|---|---|---|---|
| Q-001 | Age (HTN-006) | 175 | 57 |
| Q-002 | Treatment_Group (HTN-008) | Placebo 2 | Control |
| Q-003 | SBP (HTN-011) | ABC | 151 |
| Q-004 | AE_Reported (HTN-014) | Maybe | No |
| Q-005 | Visit (HTN-017) | Week 6 | Baseline |

**Day 6 - Review and mock lock.** A 12-point review checklist, a 9-item mock database-lock checklist, AE and medication reconciliation, an endpoint summary of 20 paired SBP changes, and medical coding practice (principles only, no official codes assigned).

**Day 7 - Final report.** A ten-section project report, a results summary, skills and resume wording, and a portfolio index.

## Key results

- 20 participants, 100 visit records, all keys unique
- 26 validation rules documented; 5 deliberate discrepancies identified
- 5 queries raised and resolved, with 15 history entries and 5 change records
- 100 of 100 final records pass validation; 0 open issues
- 6 AE events and 7 medication records reconciled internally
- 20 paired Baseline and Week 12 SBP values ready for analysis
- Mock database lock checklist complete (simulated roles only)

## How to use

1. Download the `.xlsx` files and keep all seven in one folder.
2. To use Google Sheets: upload to Google Drive, open with Google Sheets, then File > Save as Google Sheets.
3. After importing, check that dropdowns, date formats and formulas still work.
4. Work on a copy. Changing data does not automatically update narrative text, query responses or report wording, so rerun the checks and update the documentation after any edit.

## Limitations

- Excel validation can be bypassed by pasted data, so formula checks and documented review are still needed.
- The change log is an editable spreadsheet, not an immutable, access-controlled audit trail.
- Review ranges (for example SBP 70-240 mmHg) are teaching triggers, not clinical reference ranges.
- Medical coding (MedDRA, WHODrug), safety database reconciliation and real database lock approvals are outside the scope of this project.

## Next steps

Learn EDC systems, CDASH and SDTM standards, and clinical trial regulations such as GCP and 21 CFR Part 11.

## Resume wording

> Academic project: Clinical Data Management of a Simulated Phase III Clinical Trial (synthetic data). Designed a study-specific CRF and data dictionary, organised 20 fictional participants and 100 visit records in Excel / Google Sheets, applied entry controls and formula-based validation, documented five discrepancies with evidence-based corrections, and completed internal AE/medication review and mock database-lock documentation.

Use only claims that accurately describe the work you personally completed.
