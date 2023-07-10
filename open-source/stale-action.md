# Stale Action

```yaml
name: Mark stale issues and pull requests

on:
  schedule:
  - cron: "0 0 * * *"

jobs:
  stale:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/stale@v8
      with:
        repo-token: ${{ secrets.GITHUB_TOKEN }}
        stale-issue-message: 'This issue is having no activity for the last 60 days. This issue has been marked as stale. It will be closed in the next 10 days if still inactive.'
        stale-pr-message: 'This pull request has no activity for the last 60 days. This pull request has been marked as stale. It will be closed in the next 10 days if still inactive.'
        stale-issue-label: 'no-issue-activity'
        stale-pr-label: 'no-pr-activity'
        days-before-close: 10
```
