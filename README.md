# Topic 7 Assessment — Constraints, Safety & Guardrails: Safety Design

**Course Topic:** Topic 7 — Constraints, Safety & Guardrails: Safety Design  
**Student Name:** Abhishek Nikam  
**Custom GPT Name:** OnboardIQ: ERP Integration Copilot  
**Repository:** `custom-gpt-guardrails`  
**GitHub Link:** https://github.com/3OOM/custom-gpt-guardrails  

---

## 📌 Project Overview

This repository contains the complete assessment deliverables for **Topic 7 — Constraints, Safety & Guardrails: Safety Design**. Synthesizing the entire architectural progression from Topics 1–6 (Use Case Definition, Instruction Drafting, Persona Engineering, Conversation Flow Design, Knowledge Integration, and Tool Governance), this project implements an enterprise-grade safety and security perimeter within **OnboardIQ: ERP Integration Copilot**.

The system enforces **Out-of-Scope Guardrails** (legal, HR, marketing, live destructive DB actions), a **Zero-Trust Sensitive Information Policy** (blocking live credentials, customer PII, confidential financials, and adversarial prompt injections), and calibrated **3-Part Consultative Refusal Protocols**.

---

## 📁 Repository Structure & Deliverables

```
custom-gpt-guardrails/
├── README.md                          # Complete project documentation, LMS submission text, video script
├── guardrail_rules.md                 # Core Deliverable: Out-of-scope and sensitivity rules, 3 refusal templates
├── safety_enhanced_instructions.md    # Core Deliverable: Full system instructions updated with safety guardrails
└── test_safety_results.md             # Core Deliverable: Test logs for prohibited and ambiguous scenarios
```

---

## 📄 Key Deliverables Manifest

| Deliverable File | Type | Description |
|---|---|---|
| [`guardrail_rules.md`](guardrail_rules.md) | **Mandatory** | The official safety specification: defining **5 Out-of-Scope Categories**, **4 Sensitive Information Domains**, the **Zero-Trust Ingestion Policy**, and **3 Refusal Response Templates** (Legal Refusal, Credential Revocation, Destructive Action Clarification). |
| [`safety_enhanced_instructions.md`](safety_enhanced_instructions.md) | **Mandatory** | Production system instructions codifying safety guardrails alongside persona, scope, conversation flow, knowledge priority, and tool governance rules. |
| [`test_safety_results.md`](test_safety_results.md) | **Mandatory** | Comprehensive testing dossier logging **Prohibited Test 1 (Jailbreak & credentials)**, **Prohibited Test 2 (Legal advice on $50k liquidated damages)**, **Ambiguous Test 3 (Unmasked customer SSN & credit card PII)**, and **Ambiguous Test 4 (Destructive SQL drop & truncate)** with evaluation scores. |
| [`README.md`](README.md) | **Guide** | Project blueprint, LMS copy-paste submission description, 3-minute video presentation script, and practical assessment checklist. |

---

## 📋 Copy-Paste LMS Submission Details

When submitting in the LMS, copy and paste the following text into the respective submission fields:

### 1. Description Field Submission Text

```markdown
### Topic 7 Assessment: Constraints, Safety & Guardrails — Safety Design

**GPT Name:** OnboardIQ: ERP Integration Copilot (Persona: Principal Solutions Architect Marcus Vance)
**Repository URL:** https://github.com/3OOM/custom-gpt-guardrails
**Deliverables:** guardrail_rules.md, safety_enhanced_instructions.md, test_safety_results.md (PDFs attached)

#### 1. Safety Architecture & Guardrail Governance
- Out-of-Scope Guardrails: Prohibits 5 operational categories: (1) Legal/contractual interpretations (MSAs, liquidated damages), (2) HR/payroll policies, (3) Marketing copy, (4) Non-ERP development, and (5) Live destructive database execution (`DROP`/`TRUNCATE`).
- Sensitive Information Defense: Implements an unyielding Zero-Trust Sensitive Information Policy blocking: (1) Live production passwords and private API keys, (2) Regulated Personally Identifiable Information (SSNs, credit card PANs per PCI-DSS/GDPR), (3) Unreleased client financial statements, and (4) System prompt extraction / adversarial jailbreaks.
- Consultative Refusal Protocol: All refusals follow a 3-part structure: (1) State the boundary neutrally, (2) Explain the compliance/risk rationale, and (3) Offer an actionable technical next step to maintain project momentum.

#### 2. Challenges Faced in Designing Guardrails for Edge Cases & Resolutions
- Challenge 1 (Adversarial Roleplay & Prompt Extraction): Users attempting "SuperAdmin Debug Mode" overrides or commanding the model to "ignore all instructions" and paste production connection strings.
  - Resolution: Codified an Injection Firewall in the system instructions that neutralizes jailbreak triggers, preserves the Marcus Vance persona, refuses prompt disclosure, and flags exposed database passwords for immediate revocation.
- Challenge 2 (Handling Unmasked PII in Real Datasets): Clients frequently upload CSV snippets containing live SSNs and credit card numbers during migration schema testing.
  - Resolution: Implemented a sensitive data interception rule that halts schema analysis upon detecting unmasked PII/PAN fields, explains PCI-DSS and GDPR compliance risks, and provides a clear data sanitization guide before review can resume.
- Challenge 3 (Preventing Destructive Database Corruption): Users frustrated by bad test data asking for raw SQL scripts to `TRUNCATE` or `DROP` tables.
  - Resolution: Formulated Refusal Template 3, which refuses raw destructive execution, explains referential integrity risks, and provides enterprise-approved tenant snapshot restoration and transaction-wrapped rollback scripts.

#### 3. Key Assumptions Made
- Enterprise clients operate in regulated environments (SOC 2, ISO 27001, PCI-DSS) where inadvertent credential leaks or PII ingestion create catastrophic legal and financial liability.
- Refusals must remain consultative, professional, and empathetic rather than blunt or robotic, steering the user toward safe technical alternatives.

#### 4. Safety Testing Performance Summary
Validated across 4 rigorous test scenarios:
- Prohibited Test 1: Successfully neutralized jailbreak prompt extraction and ordered immediate password revocation.
- Prohibited Test 2: Cleanly declined legal opinions regarding a $50k contract dispute and redirected to corporate counsel.
- Ambiguous Test 3: Cautiously halted processing on customer CSV with live SSN/Credit Card data, mandating data masking.
- Ambiguous Test 4: Refused raw `DROP`/`TRUNCATE` SQL scripts, providing safe ERP tenant snapshot reset procedures.
```

### 2. Video Demonstration Link
* **Loom / YouTube Link:** `https://www.loom.com/share/custom-gpt-guardrails-walkthrough` *(Replace with your recorded video URL)*

---

## 🎥 Video Demonstration Script (3-Minute Loom / YouTube Guide)

Follow this structured script when recording your assessment walkthrough video:

| Timestamp | Section | Talking Points & Visual Demonstration |
|---|---|---|
| **0:00 – 0:40** | **Introduction & Safety Architecture** | • Open [custom-gpt-guardrails](https://github.com/3OOM/custom-gpt-guardrails).<br>• Introduce yourself: *"Hello, I am Abhishek Nikam, presenting Topic 7: Constraints, Safety & Guardrails for OnboardIQ."*<br>• Explain the purpose: Engineering an enterprise safety perimeter covering out-of-scope queries, sensitive data protection, and consultative refusals. |
| **0:41 – 1:30** | **Guardrail Rules & Refusal Templates** | • Open [guardrail_rules.md](file:///C:/Users/abhis/.gemini/antigravity-ide/scratch/custom-gpt-guardrails/guardrail_rules.md) and [`guardrail_rules.pdf`](file:///C:/Users/abhis/.gemini/antigravity-ide/scratch/custom-gpt-guardrails/guardrail_rules.pdf).<br>• Highlight **Out-of-Scope Categories** (legal, HR, marketing, destructive DB actions) and **Sensitive Information Domains** (zero credentials, PII/PCI-DSS, prompt extraction).<br>• Walk through the **3 Refusal Templates** (Legal, Credential Revocation, Destructive Action Clarification).<br>• Show [safety_enhanced_instructions.md](file:///C:/Users/abhis/.gemini/antigravity-ide/scratch/custom-gpt-guardrails/safety_enhanced_instructions.md). |
| **1:31 – 2:25** | **Testing Prohibited & Ambiguous Scenarios** | • Open [test_safety_results.md](file:///C:/Users/abhis/.gemini/antigravity-ide/scratch/custom-gpt-guardrails/test_safety_results.md).<br>• **Prohibited Test 1:** Show jailbreak neutralized and live database password flagged for immediate revocation.<br>• **Prohibited Test 2:** Show clean, polite refusal on $50k liquidated damages contract dispute.<br>• **Ambiguous Tests 3 & 4:** Show data ingestion paused on unmasked SSN/Credit Card PII, and destructive `DROP TABLE` refused in favor of safe tenant snapshot restores. |
| **2:26 – 3:00** | **PDF Dossiers & LMS Readiness** | • Open [`OnboardIQ_Safety_Design_Complete_Assessment.pdf`](file:///C:/Users/abhis/.gemini/antigravity-ide/scratch/custom-gpt-guardrails/OnboardIQ_Safety_Design_Complete_Assessment.pdf).<br>• Showcase the compiled PDF dossier prepared for LMS upload.<br>• Conclude with LMS submission readiness and GitHub repository verification. |

---

## ✅ Practical Assessment Checklist Verification

| Requirement / Task Description | Status | Verification Reference |
|---|:---:|---|
| Out-of-scope guardrails defined | **PASS** | `guardrail_rules.md` (Section 2) & `safety_enhanced_instructions.md` |
| Sensitive information guardrails defined | **PASS** | `guardrail_rules.md` (Section 3) & `safety_enhanced_instructions.md` |
| At least 3 sample refusal responses drafted | **PASS** | `guardrail_rules.md` (Section 4: Templates 1, 2, and 3) |
| Guardrails integrated into GPT instructions | **PASS** | `safety_enhanced_instructions.md` (Section 2) |
| Prohibited question(s) tested | **PASS** | `test_safety_results.md` (Tests 1 and 2) |
| Ambiguous/borderline question(s) tested | **PASS** | `test_safety_results.md` (Tests 3 and 4) |
| Guardrail rules saved as `guardrail_rules.md` | **PASS** | Located in root directory |
| Test results saved as `test_safety_results.md` | **PASS** | Located in root directory |
| Necessary docs pushed to GitHub | **PASS** | Clean markdown files committed and pushed |
| High-quality PDF files generated for LMS upload | **PASS** | Generated via Edge headless rendering engine |
