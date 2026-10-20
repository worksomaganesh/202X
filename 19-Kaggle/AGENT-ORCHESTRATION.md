# AI-Agent Orchestration for Kaggle

**Design goal:** use agents to accelerate experimentation while the learner develops independent ML and software-engineering ability. A larger agent team is not automatically better.

## When to introduce agents

### Stage 1 — November foundations: tutor, not autopilot

Use an assistant to explain Python, generate small exercises, discuss errors and review a solution after you attempt it. You should type and run the foundational code yourself. Keep Git, variables, loops, functions, lists/dictionaries, file handling and debugging understandable before delegating whole pipelines.

### Stage 2 — first competition baseline: one bounded helper

After you can load and inspect a dataset, ask one agent to review your EDA or suggest baseline hypotheses. Make your own baseline first where possible. Compare suggestions with the actual data, then accept/reject them with a reason.

### Stage 3 — controlled multi-role workflow

Once you have a working, understood baseline, separate the work into roles. These roles may be separate models or different prompts to the same model; treat them as responsibilities, not guaranteed independent expertise.

| Role | Bounded responsibility | Required deliverable |
|---|---|---|
| Competition researcher | Summarise task, metric, rules, deadline and allowed resources from official sources | Rule/metric checklist with URLs and uncertainties |
| Data analyst | Inspect schema, missingness, distributions, leakage and unusual rows | EDA report with reproducible evidence |
| ML engineer | Propose and implement one baseline or one controlled experiment | Candidate code, hypothesis, validation score and run instructions |
| Experiment planner | Recommend the next one or two high-value experiments based on previous results | Ranked hypotheses with expected evidence and cost |
| Debugging agent | Diagnose a reproduced error using traceback, minimal example and environment | Root-cause hypothesis, fix, regression test |
| Leakage/data-use reviewer | Search for train/validation contamination, target leakage and prohibited data/tool use | Findings with file/line evidence and explicit checks |
| Tutor / interview coach | Explain each accepted change, quiz the learner and simulate reviewer questions | Concept explanation, quiz and concise interview answer |
| Human learner / orchestrator | Define objective, approve tasks, run code, compare results and decide what ships | Logged accept/reject decision and understanding check |

The human learner role is not optional. Agents do not get final authority over competition rules, validation design, claims on a resume or what counts as a verified result.

## Orchestration loop

1. **Establish the baseline.** Save a stable version, baseline metric, validation split and environment.
2. **Ask for a plan, not an unbounded rewrite.** Request a short list of hypotheses and why each is worth testing.
3. **Choose one experiment.** State its expected result and acceptance criteria.
4. **Isolate the change.** Use a separate candidate file/branch or clearly named version; do not silently overwrite the last good baseline.
5. **Execute and test.** Run the code, inspect errors, run tests and calculate the agreed metric locally.
6. **Review the evidence.** Ask a reviewer to inspect leakage, correctness, allowed data/tools and reproducibility. Verify findings yourself.
7. **Teach back.** The learner explains the concept, changed lines and score movement in their own words. If that fails, pause optimization and learn the concept.
8. **Promote or reject.** Promote only if the improvement is supported by valid evidence or the experiment provides a documented lesson. Record why.
9. **Repeat with feedback.** Use prior results to select the next targeted change; periodically rerun the best pipeline from clean state.

## Prompt template for a bounded agent task

> **Task:** [one specific task]  
> **Competition:** [name and official URL]  
> **Rules checked:** [date and constraints relevant to this task]  
> **Current baseline:** [model, split, metric and score]  
> **Data context:** [schema/data dictionary; never include private credentials]  
> **Allowed resources:** [libraries, models, external data, internet/API/compute restrictions]  
> **Constraints:** Preserve the baseline; do not access or infer hidden labels; do not change the evaluation method without explaining why; do not claim code/tests ran unless they actually ran.  
> **Deliverables:** Hypothesis; proposed change; exact files; run command; tests; measured result; assumptions; limitations; next recommendation.  
> **Acceptance gate:** It executes, the validation is appropriate and comparable, no leakage/rule violation is identified, the experiment is recorded, and I can explain it.

## Quality and safety gates

- Read the actual competition rules each time. Tool/data permission is competition-specific.
- Keep credentials, tokens, private data and account access out of prompts, notebooks, repository files and logs.
- Do not upload confidential or personal data to an external model.
- Treat generated code as untrusted until inspected and run in an appropriate environment.
- No result without a real run; no “tests passed” claim without test output.
- A reviewer is a second check, not proof by itself. Independently verify important claims.
- Avoid changing many unrelated pipeline stages in one experiment; use ablations to learn what mattered.
- Keep public leaderboard scores separate from local validation results.
- A high score obtained through leakage, prohibited resources or an invalid split is not a valid achievement.
- Never put an unearned rank, medal, certificate or model claim on a resume.

## How we will evaluate the agents themselves

Track not only model score but engineering reliability:

- Percentage of suggestions that execute without repair.
- Defects/leakage risks found before submission.
- Human review time and debugging time.
- Whether the experiment is reproducible.
- Whether the learner can explain the accepted change.
- Whether suggestions improve the agreed validation metric without making the system fragile.

These are local project metrics, not official Kaggle scores. The goal is to discover which model/agent is reliable for which task instead of assuming one model is best at everything.
