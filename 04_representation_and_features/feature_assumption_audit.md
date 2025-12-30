# Feature Assumption Audit

## Purpose
Audit proposed features to make **implicit assumptions explicit** before they are
implemented, optimized, or ranked.

This prompt exists to prevent:
- silent bias introduction
- shortcut learning
- inappropriate signal amplification
- feature-level leakage

Features are not neutral.
Each one encodes a belief about the world.

---

## AI Role
Reviewer (assumption-focused, risk-oriented)

---

## Prompt
Act as a reviewer auditing proposed feature concepts for the following decision system:

**Decision being supported:**  
[INSERT DECISION]

**Proposed feature concepts:**  
[List each feature concept separately, using plain language — no formulas]

For **each** feature concept, answer:

1. **What behavior does this feature make visible?**  
   - What pattern, change, or signal is the system now allowed to notice?

2. **What assumption does this feature encode?**  
   Consider assumptions about:
   - user behavior
   - timing and causality
   - stability vs volatility
   - uniformity across cohorts

3. **When would this assumption fail?**  
   - In what real-world scenarios would this feature become misleading?

4. **What risk does this feature introduce?**  
   Examples include:
   - noise amplification
   - proxy bias
   - leakage (temporal or structural)
   - feedback loops
   - false confidence

5. **Which cohorts might be misrepresented?**  
   - Who could this feature systematically over- or under-represent?

---

## Constraints
Do **NOT**:
- rank features
- recommend keeping or dropping features
- suggest transformations or encodings
- discuss model performance

The goal is **assumption visibility**, not feature selection.

---

## Output Expectation
The output should:
- surface hidden assumptions clearly
- name failure conditions explicitly
- describe risks in concrete, real-world terms

Ambiguity is acceptable.
Unexamined assumptions are not.

---

## Human Review Checklist
Before moving forward, confirm:

- [ ] Every feature’s core assumption is documented
- [ ] Failure scenarios are realistic, not hypothetical
- [ ] Risks are understood without relying on metrics
- [ ] No feature is treated as “obviously safe”

---

## Guiding Principle

> **A feature is a policy choice disguised as data.**
