# Contribution Guidelines

## General Workflow

1. Fork the `hummingbot/deploy-examples` repository.
2. Create a new branch from the `main` branch in your forked repository.
3. Commit your changes to your newly created branch.
4. Once your changes or features are complete:

   - Rebase upstream changes into your branch.
   - Submit a pull request to the `main` branch.
   - Make sure to provide a detailed description of your changes in the pull request.
   - Enable the `Allow edits by maintainers` option before submitting the pull request.

5. The Hummingbot team will review your changes.
6. Address any changes requested by your reviewer, fix issues raised, and push your fixes as a single new commit.
7. A member of the Hummingbot team will merge your pull request once it has been reviewed and accepted.

## Detailed Workflow

### 1. Fork the Repository

Fork the repository using GitHub's interface. Add the Hummingbot repository as an upstream remote and fetch the upstream data:

```bash
git remote add upstream https://github.com/hummingbot/deploy-examples.git
git fetch upstream
```

### 2. Create Your Branch

Create a branch using the following naming conventions:

- feat/...
- fix/...
- refactor/...
- doc/...

Then, create and switch to a new local branch based on the `main` branch of the remote upstream:

```bash
git checkout -b feat/[branch_name] upstream/main
```

### 3. Commit Changes to Your Branch

Make commits to your branch. Use these prefixes for your commits:

- (feat) - for new features
- (fix) - for fixes
- (refactor) - for refactoring
- (doc) - for documentation
- (cleanup) - for cleanup

Commit messages should be in the present tense, e.g., "(feat) add new docker compose script", with a brief summary (around 70 characters max) of the changes made in the first line. For detailed explanations, provide more information after a blank line following the summary.

### 4. Rebase Upstream Changes

To rebase upstream changes into your branch, run this command:

```bash
git pull --rebase upstream main
```

In case of conflicting changes, git will pause rebasing to let you resolve conflicts. After fixing conflicts for a specific commit, run:

```bash
git rebase --continue
```

### 5. Create a Pull Request

Create a pull request from your fork and branch to the upstream `main` branch, detailing your changes. Remember to check 'Allow edits by maintainers' for the Hummingbot team to update your branch when needed.

If changes are requested by the Hummingbot team, make more commits to your branch to address these, then follow this process again from rebasing onwards. After addressing the requests, request further review.

## Checklist

Before submitting your pull request, ensure that:

- You have created your branch from `main`.
- You have followed the correct naming convention for your branch.
- Your branch is focused on a single main change.
- All your changes directly relate to this main change.
- You have rebased the upstream `main` branch after finishing all your work.
- You have written a clear pull request message detailing what changes you made.
- You have requested a code review.
- You have made any requested changes from the code review.

Thank you for your contribution!
