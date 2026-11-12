# Minimum Lab Deployment (MLD)

## Definition

A Minimum Lab Deployment is the smallest working deployment of a technology that lets a learner exercise and observe its essential behavior. It is a learning artifact, not a product. Its purpose is to reach a verifiable, hands-on understanding of the fundamentals as quickly as possible.

The human chooses what to learn and validates the result. The AI coding agent handles most of the implementation and explains the parts that matter. Learning comes from running, changing, observing, and inspecting the deployment, rather than building every piece manually.

## Instructions for the AI coding agent

1. **Start with the ABC.** Identify the technology's core concept, the few components required to demonstrate it, and one simple end-to-end use case. State any necessary assumptions briefly and proceed.
2. **Deploy the smallest real example.** Make it runnable in the requested environment, or locally by default. Include only what is needed to demonstrate the chosen use case. Prefer the technology's normal tools and conventions over custom scaffolding. Do not substitute a mock when the real technology can reasonably run.
3. **Make learning active.** Provide one short exercise in which the learner runs the example, changes one input or setting, and observes the effect. State the expected result and what it demonstrates.
4. **Explain the artifact.** Write a concise project-root README with the basic mental model, prerequisites, exact setup/run/exercise/stop commands, expected output, and a map of the essential files and learning documents. Add brief English comments beside decisions that would otherwise be hard for a beginner to understand. Avoid comments that merely restate the code.
5. **Create the learning guide.** Generate the eight documents specified below in a root-level `mld/` directory. Make them specific to the chosen technology and consistent with the actual deployment. Keep them short, useful for exploration, and linked from the project README.
6. **Use sound basics.** Keep setup reproducible, declare dependencies and versions where practical, keep secrets out of the repository, and include only the checks needed to verify the core behavior. Avoid premature abstractions, extra services, and production infrastructure unless essential to the learning goal.
7. **Verify and stop.** Run the deployment and exercise when the environment permits. Report what you actually observed, any unverified step, and how to resolve a blocker. Stop when the fundamental use case works; suggest deeper experiments separately rather than implementing them by default.

## Required learning guide

Create these eight Markdown files in the Lab project's root-level `mld/` directory:

| File | What it should help the learner understand |
| --- | --- |
| `concepts-and-fundamentals.md` | The few core concepts, how they relate, and where they appear in this Lab. |
| `tutorial.md` | A step-by-step walkthrough of the actual deployment and the run → change → observe exercise, with expected results. |
| `use-cases.md` | A few concrete uses of the technology, including the one demonstrated here and its limits. |
| `essential-links.md` | A curated set of authoritative starting points, especially official documentation, with a sentence explaining each link. Verify URLs when access permits; identify any that could not be checked. |
| `github-repositories.md` | A small selection of relevant GitHub repositories, prioritizing the official project and useful examples. Give each URL, why it matters, and what to inspect. Verify repository URLs when access permits; identify any that could not be checked. |
| `best-practices.md` | Practical, technology-specific practices relevant to this Lab, with brief reasons. |
| `bad-practices.md` | Common, technology-specific mistakes or anti-patterns, their consequences, and the better approach. |
| `next-iterations.md` | A short, ordered list of small extensions to this Lab. For each, state the one change to make, the concept it teaches, and the result to observe. Suggest these iterations without implementing them by default. |

Write for a beginner and prioritize the fundamentals. Do not fill the documents with generic advice or claims unsupported by the implemented example or cited sources.

Keep all project instructions, documentation, user-facing text, and explanatory code comments in English.

## Completion criteria

The learner can start the deployment, exercise the core behavior, predict and observe a small change, and find a short explanation of why it happened. The eight `mld/` documents support further exploration of the chosen technology. The agent has verified the path it claims works.
