# ML Experiment Log

Copy this template for each meaningful competition experiment. One file per experiment is preferred once the competition becomes complex. Keep data files and credentials out of public Git history.

## Experiment metadata

- **ID / date:**
- **Competition + official URL:**
- **Rules last reviewed:**
- **Question / hypothesis:**
- **Owner or agent role:**
- **Code commit / notebook version:**
- **Environment / package versions:**
- **Dataset version/source:**
- **Allowed tools/external data checked:**

## Evaluation design

- **Prediction task and target:**
- **Primary metric:**
- **Validation design and why it fits the data:**
- **Split / folds / random seed where relevant:**
- **Baseline model and result:**
- **Leakage risks checked:**

## Experiment

- **Single change being tested:**
- **Reason for the change:**
- **Expected outcome before running:**
- **Files changed:**
- **Command / notebook section run:**
- **Tests and schema checks:**
- **Actual validation result:**
- **Leaderboard result, if submitted (record separately):**
- **Runtime / resource cost:**
- **Errors or unexpected observations:**

## Decision

- **Accept, reject or investigate further:**
- **Evidence for this decision:**
- **Did this beat the baseline on the correct validation metric?**
- **Was the result reproducible from a clean run?**
- **Known limitations / remaining risks:**
- **Next experiment and why:**

## Learning check

Explain without copying the agent's wording:

1. What changed and why might it affect predictions?
2. Which concept did this experiment teach or reinforce?
3. What evidence could show that the apparent gain is noise or leakage?
4. What would you tell an interviewer about this experiment?
5. What part can you implement or debug independently now?

**Gate:** do not mark the experiment verified until the code has actually run, the metric comes from the stated validation method, rule/leakage checks are recorded, and you can explain the change.
