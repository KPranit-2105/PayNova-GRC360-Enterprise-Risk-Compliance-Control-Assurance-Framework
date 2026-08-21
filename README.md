<div align="center">

# 🛡️ PayNova Technologies — GRC & Technology Risk Management

**Governance · Risk · Compliance — Full Operating Model**

[![Company](https://img.shields.io/badge/Company-PayNova%20Technologies%20Pvt.%20Ltd.-1B2A4A.svg)](./01_Company_Profile/Company_Profile.md)
[![Industry](https://img.shields.io/badge/Industry-FinTech%20%2F%20Digital%20Payments-2E7D32.svg)](./01_Company_Profile/Company_Profile.md)
[![Frameworks](https://img.shields.io/badge/Compliance-ISO%2027001%20%7C%20NIST%20CSF%20%7C%20SOC%202-FF9900.svg)](./04_Compliance/)
[![Status](https://img.shields.io/badge/Audit%20Readiness-PASSED%20QA%20(100%25)-brightgreen.svg)](#-quality-control--validation-report)

*A complete, realistic, end-to-end GRC operating model built from scratch for a FinTech digital payments company.*

</div>

---

## 1. Project Overview & Business Problem

This repository contains a **complete GRC (Governance, Risk, and Compliance) operating model** built for **PayNova Technologies Pvt. Ltd.** — a FinTech digital payments company with **850 employees**, processing **1.2 million daily UPI and card transactions** across AWS cloud-native infrastructure.

Ahead of an upcoming external compliance assessment, PayNova leadership put it plainly:

> *"We have security controls, but nobody has a centralized view of our risks, controls, vendors, evidence, and remediation."*

As **Junior GRC Consultant / Technology Risk Analyst**, I built a centralized, auditable GRC operating model from the ground up — risk register through executive dashboard.

---

## 2. Project Architecture & Component Index

<p align="center">
  <img src="grc01 latest/grc_architecture.svg" alt="PayNova GRC Operating Model Component Architecture" width="850">
</p>

### 📂 Deliverable Modules

| # | Module | Contents |
|---|---|---|
| 1 | [`01_Company_Profile/`](./01_Company_Profile/Company_Profile.md) | FinTech architecture, asset inventory & regulatory scope |
| 2 | [`02_Risk_Management/`](./02_Risk_Management/) | Risk Register (30 risks), Detailed Risk Assessment (10), Risk Treatment Plan |
| 3 | [`03_Control_Management/`](./03_Control_Management/) | Control Library (55 controls), Control Testing (35 tested), Effectiveness Summary |
| 4 | [`04_Compliance/`](./04_Compliance/) | ISO 27001:2022, NIST CSF v2.0, SOC 2 TSC Mappings & Gap Assessment |
| 5 | [`05_Remediation/Remediation_Tracker.xlsx`](./05_Remediation/Remediation_Tracker.xlsx) | 22 findings with SLA tracking, aging days & overdue flags |
| 6 | [`06_Vendor_Risk/`](./06_Vendor_Risk/) | Vendor Register (15 vendors), Assessment & 25-Question Security Questionnaire |
| 7 | [`07_Audit/`](./07_Audit/) | Internal Audit Plan, 16 Findings (5 Cs format) & Working Papers |
| 8 | [`08_Evidence/Evidence_Register.xlsx`](./08_Evidence/Evidence_Register.xlsx) | 45 indexed evidence items linked to controls & risks |
| 9 | [`09_Policies/Policy_Register.xlsx`](./09_Policies/Policy_Register.xlsx) | 22 corporate security policies with annual review tracking |
| 10 | [`10_Dashboard/`](./10_Dashboard/) | Executive Dashboard, 5×5 Risk Heatmap, 22 KPI/KRI metrics |
| 11 | [`11_Documentation/`](./11_Documentation/) | Operating Model, Methodologies, Executive Report, 30/60/90 Day Roadmap, GRC Maturity Assessment, 10 Scenarios, ServiceNow Mapping, 20 Automations |
| 12 | [`12_Interview_Preparation/`](./12_Interview_Preparation/) | Project Pitches (30s–5m), 75+ Q&As, 10 STAR Stories |

---

## 3. Key Findings & Dashboard Summary

### Risk Posture — Inherent vs. Residual

<p align="center">
  <img src="grc01 latest/risk_inherent_vs_residual.svg" alt="Inherent vs Residual Risk Chart" width="750">
</p>

**30 enterprise risks cataloged.** Inherent risk started at 10 Critical / 15 High. After control implementation, residual risk shows **0 Critical**, 4 High (13%), 16 Medium (53%), 10 Low (33%) — the entire critical band was closed out through treatment.

### Control Effectiveness

<p align="center">
  <img src="grc01 latest/control_effectiveness.svg" alt="Control Effectiveness Donut Chart" width="500">
</p>

**35 of 55 controls tested** to date: 80.0% Effective, 14.3% Partially Effective, 5.7% Ineffective — the ineffective and partial results feed directly into the Remediation Tracker.

### Compliance Scores by Framework

<p align="center">
  <img src="grc01 latest/compliance_scores.svg" alt="Compliance Scores by Framework Chart" width="750">
</p>

| Framework | Score |
|---|---|
| ISO 27001:2022 | **69.1%** |
| NIST CSF v2.0 | **72.7%** |
| SOC 2 Type II | **65.5%** |

All three sit below the 80% audit-readiness target — the gap analysis in `04_Compliance/` breaks down exactly which controls are driving the shortfall.

### Remediation Status

<p align="center">
  <img src="grc01 latest/remediation_status.svg" alt="Remediation Status Donut Chart" width="500">
</p>

**22 findings tracked:** 10 Closed (45.5%), 9 Open/In-Progress (40.9%), **3 Overdue SLA breaches (13.6%)** flagged for immediate escalation.

### 5×5 Risk Heatmap

<p align="center">
  <img src="grc01 latest/risk_heatmap.svg" alt="5x5 Risk Heatmap Grid" width="700">
</p>

Standard Likelihood × Impact scoring grid used across the Risk Register — every one of the 30 cataloged risks is plotted against this matrix in `10_Dashboard/`.

---

## 4. Quality Control & Validation Report

| Validation Area | Status | Issues Found | Resolution |
|---|:---:|:---:|---|
| **Risk Register (30 Risks)** | ✅ PASS | 0 | All 30 risks calculated using `=L*I` formula; ratings match matrix 100% |
| **Control Library (55 Controls)** | ✅ PASS | 0 | Every major risk mapped to ≥1 preventive/detective control |
| **Control Testing (35 Tested)** | ✅ PASS | 0 | Effective, Partially Effective, and Ineffective results documented |
| **Compliance Mapping** | ✅ PASS | 0 | Accurate mappings across ISO 27001:2022, NIST CSF v2.0, SOC 2 TSC |
| **Remediation Tracker (22 Items)** | ✅ PASS | 0 | All findings include owner, due date, status, aging-days formula, overdue flag |
| **Vendor Risk (15 Vendors)** | ✅ PASS | 0 | All 15 vendors assessed with risk scoring + 25-question questionnaire |
| **Internal Audit (16 Findings)** | ✅ PASS | 0 | Formatted using professional 5 Cs audit structure; cross-referenced to controls |
| **Evidence Register (45 Items)** | ✅ PASS | 0 | Every tested control linked to a valid evidence record with S3 vault location |
| **Policy Register (22 Policies)** | ✅ PASS | 0 | 100% of policies assigned owners, versions, and annual review timestamps |
| **Executive Dashboard & Heatmap** | ✅ PASS | 0 | Dashboard metrics and 5×5 heatmap grid derived directly from underlying datasets |
| **Data Relationships & IDs** | ✅ PASS | 0 | 100% ID consistency verified across `RISK-xxx`, `CTRL-xxx`, `FIND-xxx`, `VEND-xxx`, `AUD-xxx`, `EVID-xxx`, `POL-xxx` |

---

<div align="center">

**This is not a template exercise.** Every number in this repository traces back to an underlying dataset, every finding traces to a control, and every control traces to a risk — the way a real GRC operating model has to hold together under audit scrutiny.

</div>
