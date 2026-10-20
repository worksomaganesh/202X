# Kaggle — Applied ML Learning Lab

**Journey start:** 1 November 2026  
**Primary career target:** one genuine first-year technical internship by 31 March 2027  
**Purpose:** learn machine learning by solving real prediction problems while building evidence that hiring teams can inspect.

Kaggle is not a substitute for fundamentals, and a leaderboard score is not proof that every decision was correct. Use competitions to create a repeating loop:

**Learn a concept → form a hypothesis → implement → evaluate correctly → explain the result → document evidence → repeat.**

## How Kaggle fits the two tracks

| Track | Skills built here | Evidence to keep |
|---|---|---|
| **A — AI/ML specialization** | Python, NumPy/pandas, SQL when useful, statistics, data cleaning, EDA, feature engineering, model selection, evaluation, data engineering basics and later deep learning/AI systems | Notebooks, experiment logs, valid submissions, score history, technical write-ups and verified competition achievements |
| **B — general engineering ability** | Git, readable code, debugging, tests, reproducibility, CLI/Linux, data structures, APIs where appropriate, documentation, problem-solving and communication | Meaningful commits, tests, runnable instructions, failure analyses, code reviews and interview explanations |

Python is a shared foundation. SQL, Git, testing, debugging and documentation should not be postponed until after a competition.

## The staged plan

### 1. November — learn foundations, understand the arena

- Follow the main 202X chronological learning order; do not abandon Python and Git to chase leaderboard points.
- Create a Kaggle account/profile and inspect the beginner [Titanic competition](https://www.kaggle.com/competitions/titanic).
- Read the problem statement, evaluation metric, submission format and competition rules before using any dataset or tool.
- Use relevant [Kaggle Learn](https://www.kaggle.com/learn/) lessons alongside the concepts being learned. Start with Intro to Programming/Python; move to Pandas and Intro to Machine Learning only when ready.
- No medal or submission deadline is imposed on November. Understanding Python and producing working code is the priority.

### 2. December — first complete beginner competition

- After enough Python, pandas and basic evaluation concepts, inspect the competition dataset and document the target, features, missing values and risks.
- Establish a simple baseline and a local validation method before trying advanced models.
- Generate a submission that matches the competition's sample format, check it, and submit only if the rules permit.
- Keep the first result even if it is weak. It is the reference point for later experiments.

### 3. January — controlled experimentation and agent assistance

- Change one meaningful component at a time: preprocessing, feature engineering, model family or hyperparameters.
- Compare experiments against the same validation strategy; document score, runtime, errors and trade-offs.
- Introduce clearly scoped AI-agent roles to generate candidate ideas, draft code, debug, review data leakage and explain concepts. Run and inspect every accepted change.
- Turn the final approach into a reproducible notebook or code project and a plain-English technical write-up.

### 4. February–March — stronger evidence, not endless competition grinding

- Polish the strongest solution so another person can reproduce it and understand why it works.
- Pursue a second or harder competition only when the first solution is documented and doing so will not damage interview preparation or internship applications.
- Apply to eligible internships in parallel. Do not wait for a medal, Kaggle tier, or “complete” syllabus before applying.
- Use competition results to support interview answers, not replace Python/SQL/DSA/software-engineering preparation.

These are sequencing targets, not guaranteed completion dates, competition rankings, medals or job outcomes. Adjust the pace to actual understanding and college workload.

## How to choose a competition

Before joining, record:

- Task type, target, evaluation metric, deadline and submission limits.
- Whether individual/team participation is allowed and what counts for progression or medals.
- Rules on external data, pretrained models, internet access, code sharing, APIs, paid tools, AI tools and licenses.
- Compute needs and whether the task is feasible on available hardware/time.
- What concept it can teach now. Prefer a manageable problem that develops one or two skills over a fashionable but opaque challenge.

Competition rules can differ. Read the rules for the specific competition and re-check them before using new data, tools, collaborators or models. Never assume that a tool or dataset allowed in one competition is allowed in another.

## Achievements and resume evidence

Track these as separate items; they are not interchangeable:

1. **Valid participation/submission:** an honest record of taking part. A participation certificate is not guaranteed.
2. **Technical work:** a reproducible solution, notebook, experiments and explanation.
3. **Rank/medal:** record only the official outcome for the relevant competition.
4. **Kaggle progression tier:** record the tier shown on your profile and the track/category; do not imply it is a competition medal.
5. **Kaggle Learn certificate:** keep the actual certificate link if earned. Certificates are supporting evidence, not a replacement for applied work.

Keep a private/local copy of certificates and application details if needed; do not commit personal contact information. Never claim a medal, certificate, rank or metric that you cannot verify on the official source. A medal is an aspirational outcome, not a promise or a prerequisite for the internship target.

Useful official links:
- [Kaggle Learn](https://www.kaggle.com/learn/)
- [Kaggle progression](https://www.kaggle.com/progression)
- [Titanic: Machine Learning from Disaster](https://www.kaggle.com/competitions/titanic)
- [Google Research: MLE-STAR](https://research.google/blog/mle-star-a-state-of-the-art-machine-learning-engineering-agents/)

MLE-STAR is inspiration for targeted iteration, experiments that isolate the impact of a component, and explicit debugging/data-leakage checks. This repository does **not** claim to reproduce MLE-STAR or any other research system. We will implement the useful engineering habits gradually and verify them ourselves.

## Required artifacts for each serious competition

- A completed entry in [the competition tracker](./COMPETITION-TRACKER-TEMPLATE.csv).
- A copy of the rules/metric notes and a recorded date when they were checked.
- A baseline, a documented validation approach and a submission-format check.
- An [experiment log](./EXPERIMENT-LOG-TEMPLATE.md) for every meaningful model change.
- A short write-up: problem, data, baseline, validation, experiments, results, errors, limitations and lessons.
- A link to the Kaggle notebook/submission/profile achievement where public, and a GitHub README or note that explains your own contribution.
- An end-of-competition reflection that answers: “What can I now explain, implement, test or debug that I could not do before?”

## Ground rules

- Learn first; ask an agent to explain and assist, not to hide the reasoning.
- Keep the initial baseline intact. Agents work in a separate candidate file/branch or clearly named version.
- Never trust public leaderboard changes alone; local validation and leakage checks come first.
- Do not expose competition credentials, API tokens, private datasets or personal data.
- Respect competition terms, licenses, attribution and team rules.
- Keep accurate records of agent assistance and your own work.
- If a result cannot be reproduced or explained, mark it unverified rather than presenting it as a proven achievement.

The goal is to become a stronger ML engineer through competition practice, not to turn this repo into a collection of copied notebooks.
