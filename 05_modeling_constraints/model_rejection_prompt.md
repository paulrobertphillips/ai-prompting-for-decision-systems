# Model Rejection Prompt

## AI Role
Reviewer (constraint checker)

## Prompt
Given this decision context:
[INSERT]

And these constraints:
- Cost of false positives: [INSERT]
- Cost of false negatives: [INSERT]
- Trust / interpretability requirements: [INSERT]

Evaluate the following model classes:
[LIST]

For each:
1. Constraint satisfied
2. Constraint violated
3. Hardest-to-detect failure

Explicitly reject at least one option and justify why it should not be used.
