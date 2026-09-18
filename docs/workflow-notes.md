# Workflow and Repository Standards

This document establishes the standardized Git workflow and team practices for the repository, resolving previous collaboration deficiencies.

## Historical Issues Identified & Remediated
- **Direct Commits on Main**: Previously, developers pushed unreviewed commits directly to `main` (`6ea8416 testing`, `7697267 changes`, `9d38d52 fix issue`). Direct pushes are now restricted.
- **Vague Commit Messages**: Replaced vague messages with Conventional Commits providing traceable context.
- **Poor Branch Naming**: Deprecated ad-hoc branch names (`test123`, `temp`, `newbranch`, `feature1`). Standardized prefix-based naming is enforced.
- **Botched Merge Conflict in `src/config.js`**: Conflicting declarations of `PORT` (lines 2 and 4) have been resolved. Port fallback defaults cleanly to 3000.
- **Abandoned / Uncoordinated Branches**: Cleaned up unmerged notes and consolidated documentation.

## Established Git Workflow Standards
1. **Branch Naming Conventions**:
   - `feature/<description>` for new capabilities
   - `fix/<description>` for bug fixes
   - `docs/<description>` for documentation updates
2. **Commit Message Guidelines**:
   - Use imperative mood and conventional prefixes: `feat:`, `fix:`, `docs:`, `chore:`, `refactor:`.
   - Explain *what* and *why* in the commit body when necessary.
3. **Pull Request Discipline**:
   - Every merge into `main` requires an isolated feature branch and Pull Request.
   - PR descriptions must detail:
     - What was changed
     - Why the change was needed
     - How the change was verified
4. **Safe Merging**:
   - Always verify CI checks / local execution tests prior to merging.
   - Use explicit merge commits or squashed releases to maintain clean auditability.
