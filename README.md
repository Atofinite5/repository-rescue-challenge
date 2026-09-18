# Repository Rescue Challenge

## Story

A development team has been working directly on `main` and using inconsistent branch names. The history includes messy direct commits and poor branch names. They have also left a configuration drift issue in the documentation. Your responsibility is to stabilize the repository before the next release by cleaning the Git workflow, resolving collaboration issues, and fixing the environment instructions.

## Learning Objective

Practice Git repository diagnosis, branch workflow cleanup, pull request discipline, commit history improvement, merge safety, and environment drift repair using a small Node.js application.

## Setup Instructions

1. Clone the repository:

   ```bash
   git clone <repo-url>
   cd repository-rescue-challenge
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Start the application:

   ```bash
   npm start
   ```

## Investigation Commands

Use these commands to inspect the repository and workflow:

```bash
git log --oneline --all --graph
git branch -a
git status
```

## Expected Deliverables

Submit one PDF containing five screenshots:

1. Repository diagnosis and initial repository state
2. Feature branch creation and isolated development workflow
3. Pull Request creation and review evidence
4. Commit history improvement and successful merge
5. Final clean repository state

## Task Guidance

### Task 1: Repository Diagnosis

Inspect the branch history and repository state to identify workflow problems such as:

* messy commit history
* direct commits on `main`
* poor branch naming
* inconsistent collaboration practices
* branches that should be isolated from production work

Review the repository using:

```bash
git log --oneline --graph --all
git branch -a
git status
```

---

### Task 2: Branch Workflow Improvement

Create **at least two properly named feature branches** following the module naming convention.

Example:

```bash
git checkout -b feature/workflow-cleanup
git checkout -b feature/readme-improvement
```

Make **at least one meaningful commit on each feature branch**.

For example:

```bash
git commit -m "docs: improve README instructions"
git commit -m "fix: update workflow documentation"
```

The objective is to demonstrate:

* branch isolation
* organized development workflow
* avoiding direct development on `main`

---

### Task 3: Pull Request, Commit Improvement, and Safe Merge

Create a Pull Request from one of your feature branches into `main`.

The Pull Request description should include:

* What was changed
* Why the change was needed
* How the change was verified

Review the existing commit history and identify at least one unclear or poor commit message.

Improve readability by creating a meaningful replacement commit as part of your work and complete the merge using a safe Git workflow.

Finally, verify that the repository history is easier to understand and remains in a stable state.

---

### Task 4: Environment Drift Repair

Identify the startup mismatch documented in the README.

Correct the environment configuration and verify the application runs successfully:

```bash
npm install
npm start
```

## Notes

* The application reads the port from `process.env.PORT` and falls back to `3000` if the variable is not provided.
* The README intentionally contains an incorrect startup command to simulate environment drift.
* Follow safe Git practices throughout the exercise by performing development on feature branches and integrating changes through a Pull Request rather than committing directly to `main`.
