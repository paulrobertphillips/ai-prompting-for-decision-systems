# Pipeline Backward Diagnostics

## Purpose
Diagnose unexpected or undesirable system outcomes by reasoning **backward**
through the data science pipeline to identify the **earliest violated assumption**.

This prompt exists to prevent:
- model blame
- metric fixation
- reactive redesign
- panic-driven retraining

The goal is understanding, not correction.

---

## AI Role
Reviewer (systemic, assumption-focused)

---

## Prompt
Act as a senior reviewer diagnosing a failure in an end-to-end data science decision system.

**Observed failure or concern:**  
[DESCRIBE WHAT IS GOING WRONG — outcomes, not metrics]

**Decision being supported:**  
[INSERT DECISION]

**High-level pipeline summary:**  
(Briefly describe, at a conceptual level)
- decision strategy (e.g., conservative vs early warning)
- data sources used
- uncertainty handling approach
- representation choices
- decision mechanism (rules / model / thresholds)

---

### Backward Reasoning Tasks

Starting from the observed failure, reason **backward** through the pipeline.

1. **Where did this failure first become possible?**  
   Identify the *earliest* pipeline stage where a different assumption
   would have prevented the failure.

   Possible stages include:
   - decision framing
   - data trust and sourcing
   - uncertainty shaping / cleaning
   - representation and feature design
   - modeling constraints
   - evaluation metrics
   - threshold strategy

2. **What assumption was made at that stage?**  
   Explicitly state the assumption in plain language.
   Example format:
   > “This system assumed that __________ would remain true.”

3. **Why does this assumption no longer hold?**  
   Consider:
   - changes in user behavior
   - changes in business process
   - scale effects
   - feedback loops
   - environmental or seasonal shifts

4. **Why did downstream components fail to detect this earlier?**  
   Explain why:
   - metrics looked acceptable
   - alerts were not triggered
   - stakeholders were surprised

---

## Constraints
Do **NOT**:
- propose fixes or improvements
- recommend retraining or redesign
- suggest new features, metrics, or thresholds
- evaluate model performance

This is a **diagnostic exercise only**.

---

## Output Expectation
The output should:
- clearly identify the *origin* of failure, not just where it surfaced
- name assumptions explicitly
- explain why the failure was silent or delayed
- treat the pipeline as a single system, not isolated steps

If multiple assumptions contributed, identify the **primary** one.

---

## Human Review Checklist
Before moving to any corrective action, confirm:

- [ ] The failure is described in decision-level terms
- [ ] The earliest violated assumption is identified
- [ ] The explanation does not rely on blaming a single component
- [ ] The system’s original design intent is understood

---

## Guiding Principle

> **When something breaks, ask which assumption broke first —  
not which component broke last.**
