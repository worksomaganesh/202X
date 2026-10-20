# Chronological Learning Order — 202X

**Mission:** earn one genuine first-year internship by **31 March 2027**.  
**Start date:** 1 November 2026, after mid-examinations.  
**Study capacity:** approximately 20–22 hours/week.  
**Stretch checkpoint:** 18–24 January. **Main portfolio-ready checkpoint:** 1–7 February.

This file answers: **what do I learn first, what comes next, and when do I use it in a project?**

The sequence is narrower than the full repository. Folder names are a long-term knowledge map; they are not a promise to master every topic before March. Learn a topic, practise it, use it, and record what you actually completed.

## The learning order at a glance

1. Python basics + Git/GitHub setup
2. Python control flow and built-in collections
3. Python functions, modules, files, exceptions and debugging
4. Project 00: GitHub Foundation + Project 01: Smart File Log Analyzer
5. Linux/terminal essentials + testing basics
6. SQL fundamentals and relational-table thinking
7. SQL joins + pandas/NumPy essentials
8. Data cleaning, EDA, charts and practical statistics
9. Project 02: E-commerce Business Analytics
10. ML fundamentals, train/test split and baseline models
11. scikit-learn, preprocessing and honest model evaluation
12. HTTP/JSON, REST, FastAPI, Pydantic and database CRUD
13. pytest/API testing + a simple demo or deployment
14. LLM API, prompting, structured output and error handling
15. Embeddings, vector retrieval and basic RAG (small scope)
16. Project 03/04 polish, documentation, resume and interview practice
17. February–March: applications, assessments, interviews and targeted gap-filling

**In parallel from Week 2:** practise DSA for about 2–3 hours/week and keep checking/applying to eligible internships as soon as you have credible evidence. Do not postpone applications until every item is finished.

## Parallel lane A — Kaggle applied ML (starts gently in November)

Kaggle does **not** replace the core order above. Do not try to complete a complex competition before Python and data basics are ready.

- **1–14 November:** create/finish the profile, read the beginner Titanic competition description/rules/metric/sample submission, and learn how Kaggle notebooks and submissions work. Keep most hands-on time on Python and Git. No score/medal deadline.
- **15–30 November:** continue Python, functions, files and debugging. Follow relevant Kaggle Learn Python lessons and practise on tiny datasets only when the concepts are understandable.
- **1–19 December:** as pandas/SQL/EDA are introduced, practise reading CSVs, inspecting dtypes/missing values, grouping, charts and writing findings. Review Titanic data but do not rush into complex model tuning.
- **20 December–2 January:** once train/validation split, target/features and a baseline are understood, complete the first beginner competition workflow: rules → EDA → valid baseline → local validation → submission schema check → submission if allowed.
- **3–23 January:** run controlled model/feature experiments, use agents for bounded hypotheses/reviews, log every result, inspect errors and check leakage.
- **24 January–February:** write up the strongest solution, verify the final notebook from a clean run and connect the experience to interview answers. A second competition is optional only if the first is understood and applications/DSA remain on track.
- **February–March:** continue only where it improves learning or role relevance; keep internships, coding interviews and project polish moving.

Use [the Kaggle Learning Lab](../19-Kaggle/README.md), [Competition Playbook](../19-Kaggle/COMPETITION-PLAYBOOK.md), [Agent Orchestration](../19-Kaggle/AGENT-ORCHESTRATION.md) and the experiment template as the source of truth. These are target windows, not promises of competition completion, rank or medal.

## Chronological schedule

### Phase 0 — Setup only
**Before or during the first study session**
- Check Python installation, editor, Git and GitHub access.
- Learn how to open a terminal, create a folder and run a Python file.
- Create a private application tracker if it contains personal information.
- Do not let tooling/setup consume several days.

### Phase 1 — Python foundation + Git
**1–7 November**
1. Variables, data types, type conversion and input/output.
2. Operators, comparisons and strings.
3. Git/GitHub: status, add, commit, push, pull, README and .gitignore.
4. Run code from editor and terminal; read a simple traceback.

**Repo:** 01-Python/basics/variables, operators, input-output, strings; 10-Projects/00-github-foundation.

**Deliverable:** small Python exercises and one meaningful, explained Git commit.

### Phase 2 — Conditions, loops and collections
**8–14 November**
1. if/elif/else, Boolean logic and comparisons.
2. for/while, range, break and continue.
3. Lists and indexing/slicing.
4. Tuples, sets and dictionaries; common operations.
5. String search/count/transform tasks.

**Repo:** 01-Python/basics/conditions, loops, lists, tuple, sets, dictionaries.

**Deliverable:** 10–15 small exercises plus one command-line mini-program using collections.

### Phase 3 — Write reusable, robust Python
**15–21 November**
1. Functions, arguments, return values and scope.
2. Imports/modules and useful standard-library tools.
3. File paths and file handling with pathlib.
4. Read/write text, CSV and JSON.
5. Exceptions, validation, traceback reading and debugging.
6. Virtual environments, pip and a requirements file.
7. Basic classes/objects only after functions make sense.

**Repo:** 01-Python/functions, modules-imports, file-handling, exceptions, debugging, virtual-environments, oop.

**Deliverable:** first Smart File Log Analyzer version: read sample logs, count event/error types and export a summary.

### Phase 4 — Linux essentials + finish Project 01
**22–28 November**
1. Terminal navigation and file commands: pwd, ls, cd, mkdir, cp, mv, cat and less.
2. Search/output: grep, find, pipes and redirection.
3. Environment variables; keep API keys out of code and Git.
4. Logging basics, input validation and malformed-file handling.
5. Basic assertions/tests: normal input, empty file and invalid lines.
6. Improve README: purpose, setup, sample input/output and limitations.

**Repo:** 08-Linux; 09-Testing/assertions and debugging; 10-Projects/01-smart-file-log-analyzer.

**Deliverable:** Project 01 runs locally from documented instructions. Prepare a truthful one-page resume draft and begin tracking actual eligible roles. Apply once project links and claims are credible.

### Phase 5 — SQL fundamentals
**29 November–5 December**
1. Tables, rows, columns, data types, primary and foreign keys.
2. SELECT, WHERE, ORDER BY, LIMIT, DISTINCT and NULL.
3. Aggregation: COUNT, SUM, AVG, MIN, MAX, GROUP BY and HAVING.
4. CASE and basic date/text filtering.
5. Practise queries on a small dataset.

**Repo:** 03-SQL/basics, filtering, aggregation, database-design.

**Deliverable:** 15–20 working queries with a short explanation of each result.

### Phase 6 — SQL joins + NumPy/pandas
**6–12 December**
1. INNER JOIN and LEFT JOIN; check for duplicate rows after joins.
2. Simple subqueries and CTEs; purpose of normalization.
3. NumPy arrays, shapes and basic vector operations.
4. pandas Series/DataFrame, load CSV, inspect types and missing values.
5. Filter rows, select columns, sort, group/aggregate and merge DataFrames.

**Repo:** 03-SQL/joins, subqueries, cte, normalization; 05-Data-Machine-Learning/numpy and pandas.

**Deliverable:** load an e-commerce dataset and answer initial business questions with SQL or pandas.

### Phase 7 — Clean, analyse and communicate data
**13–19 December**
1. Missing values, duplicates, invalid values, types and date parsing.
2. EDA: distributions, comparisons, relationships and outliers.
3. Statistics: mean, median, variance, standard deviation, percentiles and sampling.
4. Correlation versus causation; avoid data leakage.
5. Matplotlib bar, line, histogram and scatter plots with labels/titles.
6. Practical Excel/Google Sheets basics if useful for analyst roles.

**Repo:** 05-Data-Machine-Learning/data-cleaning, eda, statistics, matplotlib; spreadsheet notes can go in 15-Notes.

**Deliverable:** E-commerce Business Analytics project with a documented dataset/schema, 5–8 questions, SQL, charts, 3–5 evidence-based findings and limitations. Begin targeted applications; do not wait for ML.

### Phase 8 — ML basics and a baseline
**20–26 December**
1. Supervised versus unsupervised learning; features and target.
2. Regression versus classification and simple use cases.
3. Train/test split; why leakage makes evaluation unreliable.
4. Build a simple baseline before complex models.
5. DSA continues: arrays, strings, Big-O intuition and hash maps/sets.

**Repo:** 05-Data-Machine-Learning/regression, classification, evaluation; 02-DSA/big-o, arrays, strings, hashing.

**Deliverable:** choose a modest public dataset and define the ML task, target, baseline and evaluation plan.

### Phase 9 — scikit-learn and model evaluation
**27 December–2 January**
1. fit/predict, estimators and reproducible random states.
2. Simple preprocessing and a pipeline at a practical level.
3. Linear/logistic regression, decision tree or random forest.
4. Regression metrics: MAE/RMSE when appropriate.
5. Classification metrics: confusion matrix, precision, recall, F1; why accuracy can mislead.
6. Inspect model errors and describe dataset/metric limitations.

**Repo:** 05-Data-Machine-Learning/scikit-learn, preprocessing, evaluation, cross-valuation (existing folder name).

**Deliverable:** reproducible ML Prediction Project with a baseline comparison, suitable metrics, error analysis and honest limitations.

### Phase 10 — DSA + basic software engineering
**3–9 January; DSA stays parallel until interviews**

DSA order:
1. Big-O, arrays/strings and hash maps/sets.
2. Sorting and binary search.
3. Two pointers and sliding window.
4. Stack and queue; linked-list concepts.
5. Recursion basics, tree traversal and BFS/DFS concepts if time remains.

Aim for **25–35 understood practice problems by February**, not a high count of copied solutions. Do a few each week rather than leaving DSA to the end.

Other learning: HTTP, methods/status codes, JSON request/response, SQL parameterisation and safe configuration basics.

**Repo:** relevant 02-DSA folders; 04-Web-Backend/http, json and rest.

**Deliverable:** explain selected DSA solutions aloud and write basic HTTP/JSON examples.

### Phase 11 — Backend API + testing
**10–16 January**
1. FastAPI route and request/response basics.
2. Pydantic request/response validation.
3. REST endpoints and CRUD concepts.
4. Connect to SQLite first; use PostgreSQL only if the project needs it.
5. Useful status codes and errors; avoid unsafe SQL string interpolation.
6. pytest assertions, edge cases, basic API tests and Postman manual checks.
7. Environment variables and .env exclusion from Git; simple deployment only if it does not distract.

**Repo:** 04-Web-Backend/fastapi, pydantic, rest, crud, postgresql, error-handling, postman; 09-Testing/pytest, api-testing, edge-cases; 08-Linux/environment-variables.

**Deliverable:** small API with validation and happy-path/invalid-input tests, plus working setup instructions. Serve the ML project through it only if useful.

### Phase 12 — LLM API and structured output
**17–23 January**
1. Call one hosted LLM API; read its documentation and understand basic costs/limits.
2. Prompt structure: task, context, constraints and output format.
3. Handle API failures, timeouts and malformed responses.
4. Request structured output and validate it with a schema.
5. Keep keys in environment variables; never commit secrets.
6. Evaluate normal, ambiguous and unsupported inputs.

**Repo:** 06-Generative-AI/api-integration, prompting, llms, structured-output.

**Deliverable:** Job Description Analyzer MVP that extracts skills/requirements and distinguishes quoted source text from model-generated suggestions. **18–24 January is a stretch checkpoint**, not a reason to claim unfinished work is done.

### Phase 13 — Minimal retrieval/RAG, only after the app works
**24–30 January**
1. What embeddings represent at a high level.
2. Split text into chunks and retrieve relevant chunks.
3. Basic vector/similarity search and top-k retrieval.
4. Show source snippets and test unanswerable questions.
5. State that retrieval does not guarantee factual answers.
6. Skip complex agents, fine-tuning and advanced vector databases.

**Repo:** 06-Generative-AI/embeddings, vector-search, rag, experiments.

**Deliverable:** add a small source-grounded retrieval feature only if the core project already works. If behind schedule, skip RAG and polish the reliable version.

### Phase 14 — Finish the portfolio and prepare for interviews
**31 January–7 February**
1. Run each project from a clean environment; fix broken setup steps.
2. Add clear READMEs, examples, tests, limitations and optional screenshots/demo.
3. Polish at least **three** projects; the fourth may remain a smaller MVP.
4. Make a truthful one-page resume and role-specific variants.
5. Update LinkedIn/GitHub profile and practise 60–90 second project explanations.
6. Practise Python, SQL, DSA, debugging, basic CS and communication questions.
7. Submit tailored applications while polishing.

**Repo:** 10-Projects; 13-Internships/preparation/resume and interview-prep; 17-Progress.

**Readiness rule:** 1–7 February is the main target, not a guarantee. If behind, cut optional RAG, HTML/CSS polish, advanced ML and Category 4 topics first. Keep applications running.

### Phase 15 — February and March: apply, interview, adapt
**8 February–31 March**
1. Search current official postings and verify first-year eligibility/work conditions.
2. Tailor applications to evidence already in the repository.
3. Practise assessments/interview topics that actually appear in target roles.
4. Record applications, assessments, replies, interviews, rejections and follow-ups.
5. After roughly 20 well-matched applications with little response, review eligibility, resume fit, project proof and outreach quality.
6. Continue learning only the gaps that are blocking real applications/interviews.

**Deadline:** 31 March 2027. An offer cannot be guaranteed; the plan aims to maximise preparation and leave room for obstacles.

## Parallel lane B — general engineering ability

Git, debugging, testing, DSA, Linux, SQL/databases, APIs, software design, communication and interview preparation remain active alongside ML. Python and SQL support both tracks. Do not let agent-generated notebooks substitute for writing and reviewing code yourself.

## Parallel tracks — do not leave these until the end

### DSA — 2–3 hours/week from Week 2
Keep a consistent practice block. Progress from arrays/strings/hash maps to binary search, two pointers, sliding window, stacks/queues, recursion and basic tree/graph traversal. Increase time if target postings use coding assessments.

### Applications — research from November; submit when evidence is credible
- November: research roles, eligibility and scam signals; track live postings.
- Late November/December: apply to roles you qualify for once Project 01 and a truthful resume are presentable.
- January–March: keep applying while learning; never wait until “100% ready”.

### Documentation — throughout
After each session, record what was attempted, what worked, what failed and the next step in 16-Daily-Log. Update 17-Progress weekly. The repository should reflect actual progress, not planned progress written as if completed.

## Weekly study pattern

- **Monday–Friday (2h/day):** 75–90 minutes learning/coding the main skill; remaining time for exercises, a small DSA problem or project integration.
- **Saturday (5–6h):** project implementation, debugging and tests.
- **Sunday (5–6h):** practise/revise, document the week, review role openings and plan next week's top three tasks.
- Keep a buffer block for college work or unexpected obstacles. If exams/assignments spike, protect consistency instead of trying to compensate with an unsustainable all-nighter.

## Completion checklist

- [ ] Python basics, functions, files, exceptions and debugging demonstrated.
- [ ] Git/GitHub workflow and terminal basics used in practice.
- [ ] SQL filters, aggregation and joins practised.
- [ ] pandas cleaning, EDA, charts and useful findings completed.
- [ ] A small ML model evaluated with suitable metrics and error analysis.
- [ ] A simple API or useful application tested.
- [ ] LLM API/structured output tested if targeting AI-app roles; RAG is optional if behind.
- [ ] Three documented, reproducible projects and a truthful resume.
- [ ] DSA basics practised continually; applications and interviews tracked.
- [ ] Weekly reviews reflect reality, including setbacks.
