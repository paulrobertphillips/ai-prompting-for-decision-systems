# Prompting Principles

This repository uses prompts as **thinking constraints**, not shortcuts.

## Core Principles

1. **Decision First**
   - Every prompt must be anchored to a real decision.
   - Never ask AI to “solve” without specifying what action is at stake.

2. **Role Constrained**
   - AI is explicitly assigned a role:
     - Analyst
     - Reviewer
     - Implementer (rarely)
   - Prompts must state what AI is *not allowed* to do.

3. **Tradeoffs Over Answers**
   - Good prompts ask for comparisons, critiques, and rejections.
   - Avoid prompts that request a single “best” solution.

4. **Assumptions Made Explicit**
   - Prompts should force AI to surface assumptions and uncertainty.
   - Hidden assumptions are a leading cause of pipeline failure.

5. **Humans Own Decisions**
   - AI proposes and critiques.
   - Humans approve, reject, and own consequences.

## Anti-Patterns to Avoid

- “What model should we use?”
- “What’s the best metric?”
- “Fix this pipeline”
- “Optimize accuracy”

These collapse uncertainty too early.
