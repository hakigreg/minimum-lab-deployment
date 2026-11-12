# Minimum Lab Deployment

**Minimum Lab Deployment (MLD)** is a way to learn a technology by deploying the smallest working example of its essential behavior. It is smaller in scope than a Minimum Viable Product: the result only needs to teach, not serve users or test a business idea.

Generative AI and coding agents accelerate implementation while the set of technologies a professional must understand keeps growing. MLD uses that division of work deliberately: the human defines the learning goal, then runs and validates the result; the agent builds and explains the lab. The learning loop is **run → change → observe → understand**.

The method is in [MINIMUM_LAB_DEPLOYMENT.md](MINIMUM_LAB_DEPLOYMENT.md). [AGENTS.md](AGENTS.md) gives Codex the standing instructions for a Lab. Copy both files into each new learning project.

## Where the instructions belong

| Location | Purpose |
| --- | --- |
| `AGENTS.md` | Short, persistent rules Codex should apply when creating or changing the Lab. |
| `MINIMUM_LAB_DEPLOYMENT.md` | The method and detailed requirements for the learning artifact. |
| Starter prompt | Only the chosen technology, learning goal, and any environment constraints for this Lab. |

Codex [loads project-level `AGENTS.md` automatically](https://learn.chatgpt.com/docs/agent-configuration/agents-md). Keeping it short avoids repeating the full method in every task and avoids imposing a long checklist on unrelated edits.

## Start a new lab

1. Choose one technology and one fundamental behavior you want to understand.
2. Create a new Codex project and a new local directory, then point the project to that directory.
3. Copy `AGENTS.md` and `MINIMUM_LAB_DEPLOYMENT.md` into the directory.
4. Give Codex the prompt below, filling in the technology and learning goal.
5. When Codex finishes, run the documented exercise yourself. Change one input or setting, compare the observed result with the explanation, and use the generated `mld/` guide to explore further. Ask for a deeper iteration only when you need one.

Each Lab produces a root-level `mld/` directory containing eight short guides on its chosen technology: `concepts-and-fundamentals.md`, `tutorial.md`, `use-cases.md`, `essential-links.md`, `github-repositories.md`, `best-practices.md`, `bad-practices.md`, and `next-iterations.md`.

## Starter prompt

```text
I want to learn [TECHNOLOGY] by doing.

Learning goal: [ONE FUNDAMENTAL QUESTION OR BEHAVIOR]
Environment or constraints: [OPTIONAL; LOCAL BY DEFAULT]

Build and verify a Minimum Lab Deployment for this goal in this project.
```
