# Kaggle Competition Playbook

Use this sequence for each competition. Adapt it to the competition's actual rules and evaluation design; do not blindly apply a fixed recipe to every task.

## Stage 0 — eligibility, rules and scope

- [ ] Read the official problem statement and full rules.
- [ ] Write down the target, prediction task, evaluation metric, deadline and submission constraints.
- [ ] Check individual/team limits, medal/progression eligibility and code-sharing rules.
- [ ] Check whether external data, pretrained weights, AI tools, internet access, external APIs or paid compute are allowed.
- [ ] Check dataset and model licenses, attribution and privacy restrictions.
- [ ] Estimate the compute/time needed. Choose an achievable first experiment.

**Stop condition:** do not start modelling until the rules and metric are understood well enough to explain them.

## Stage 1 — inspect and define the data

1. Read the file list and data dictionary; inspect row/column counts, dtypes, missingness, duplicates and target distribution.
2. Identify the unit of observation and the meaning of each row.
3. Decide what information would be available at prediction time. Flag leakage risks.
4. Inspect the sample submission; confirm required columns, row order/ID handling and output type.
5. Write 3–5 findings in plain English. Distinguish observations from guesses.

Do not commit competition data to GitHub unless its license, size, competition rules and privacy terms clearly permit it. Usually keep datasets outside the public repository and document where they came from.

## Stage 2 — create a baseline before complex ideas

- State the baseline hypothesis.
- Create a valid train/validation split that fits the data-generating process. Random splitting is not always appropriate; groups, time or repeated entities may require a different split.
- Build the simplest reasonable baseline and choose a metric that matches the competition.
- Record the exact split, random seed when relevant, preprocessing, model, metric and score.
- Check for leakage and make sure validation labels are not used to train or construct features improperly.
- Generate a submission file and validate its schema, row count, IDs and missing predictions before submitting.

The baseline is the comparison point, not a result to delete when a more complex model appears.

## Stage 3 — improve through controlled experiments

For each iteration:

1. Write a hypothesis before running the experiment.
2. Change one major factor, or use a planned ablation that isolates component effects.
3. Use the same validation strategy for a fair comparison.
4. Record metrics, uncertainty/variation where feasible, runtime, errors and any trade-off.
5. Keep a result only if it improves the chosen validation outcome or teaches something useful.
6. Inspect errors and failure slices; do not rely only on one aggregate score.
7. Re-run the best pipeline from a clean state to verify reproducibility.

Examples of factors: imputation, encoding, feature construction, model family, regularization, class weighting, hyperparameters and ensembling. Advanced methods come only after a reliable baseline.

## Stage 4 — use the leaderboard carefully

- Public leaderboard scores may be based on only part of the hidden evaluation data; a public improvement is not proof of better generalization.
- Do not repeatedly tune decisions to tiny public leaderboard movements.
- Prefer a sound local validation estimate, appropriate cross-validation and clear error analysis.
- Keep the best validated local candidate even when a leaderboard submission is noisy.
- Check competition-specific submission limits and deadlines.

## Stage 5 — final verification and write-up

- [ ] Re-run the solution from a clean kernel/environment.
- [ ] Confirm deterministic or documented reproducible behaviour.
- [ ] Confirm no accidental use of hidden labels, prohibited data/tools, or information unavailable at inference time.
- [ ] Validate submission schema, IDs, row count and prediction range/type.
- [ ] Record the final official rank/medal/certificate only after it is visible and verifiable.
- [ ] Write a technical note: task, data, metric, validation, baseline, experiments, final result, limitations and concepts learned.
- [ ] Add a 60–90 second interview explanation and likely follow-up questions.
- [ ] Update the competition tracker and GitHub links.

## AI-agent use: a repeatable contract

Agents can propose, implement or review work, but every experiment must pass the same gates as human-written code.

**Task card for each agent**
- **Context:** competition rules, task, data dictionary, current baseline, split and existing results.
- **Task:** one bounded action (e.g. audit leakage risks or compare two encodings).
- **Constraints:** allowed libraries/tools/data, no access to hidden labels, preserve the baseline, no secrets, no unrequested file overwrites.
- **Required output:** hypothesis, files changed, commands run, results, assumptions, limitations and tests.
- **Acceptance criteria:** code executes, tests pass, validation is comparable, result is logged, and the learner can explain the change.
- **Failure path:** report blockers and evidence instead of inventing success; revert any unverified candidate.

See [Agent Orchestration](./AGENT-ORCHESTRATION.md) for role definitions and staged adoption.
