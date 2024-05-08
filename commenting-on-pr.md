# Commenting on PR

## 1. Existing Third party action:

I discovered that the repository_messaging.yml already employs the [peter-evans/create-or-update-comment@v1](https://github.com/peter-evans/create-or-update-comment) action to write comments on PR.

Although it requires a [pull_request](https://github.com/peter-evans/create-or-update-comment/issues/104) trigger, I found it effective when used with **[opened, synchronize]**.

### code snippet:

```yaml
name: Commenting on PR

on:
  pull_request:
    types: [opened, synchronize]

jobs:
  comment-message:
    runs-on: ubuntu-latest
    if: true
    steps:
      - name: Add comment
        uses: peter-evans/create-or-update-comment@v1
        with:
          issue-number: ${{ github.event.pull_request.number }}
          body: |
            Thanks for submitting this pull request :tada:! 
```

### Screenshot of comment:
![Screenshot (1008)](https://github.com/Rd4dev/opensource-oppia_android/assets/122200035/22ff9f74-ffaf-46d8-a5db-94d951a5ecc1)


## 2. Using GitHub Scripts

Another approach could be to use the actions provided in the GitHub scripts - [GitHub Scripts](https://github.com/actions/github-script) to use comment on issue - [Comment on an Issue](https://github.com/actions/github-script?tab=readme-ov-file#comment-on-an-issue)

However, it requires some workaround to obtain the precise PR number and then utilize it in the URL.

### code snippet:

```yaml
name: Comment on PR

on:
  push:
    branches:
      - '*'

jobs:
  comment:
    runs-on: ubuntu-latest
    steps:
      - name: Get Pull Request Number
        id: pr_request_number_get
        uses: actions/github-script@v7
        with:
          script: |
            const issues = await github.rest.pulls.list({
              owner: context.repo.owner,
              repo: context.repo.repo,
              state: 'open',
              head: `${context.repo.owner}:${context.ref.replace('refs/heads/', '')}`
            });
            const pr = issues.data[0].number;
            core.setOutput('pull_request_number', pr);

      - name: Comment on PR
        uses: actions/github-script@v7
        with:
          script: |
            const prNumber = parseInt('${{ steps.pr_request_number_get.outputs.pull_request_number }}');
            const commentBody = "Thanks for the PR! You have acquired **100%** of the code coverage :tada:";
            github.rest.issues.createComment({
              issue_number: prNumber,
              owner: context.repo.owner,
              repo: context.repo.repo,
              body: commentBody
            });

```

### Screenshot of comment:
![Screenshot_8-5-2024_182848_github com](https://github.com/Rd4dev/opensource-oppia_android/assets/122200035/c6af3d59-a6b0-43b6-94b5-94c0be35d327)

## Conclusion:
While both approaches work, I would prefer to use the **third-party action** because:

- It was already being used in the source code.
- It provides a much simpler usage.

### Note:
These were tested with raw input text data and will later be tested with actual markdown files using paths.


