---
description: A GitHub Actions workflow to push changes to pull request
---

# Push to Pull Requests Action

```yml
name: Push changes to Pull Request's Source Branch

on:
    push:
    pull_request:

jobs:
    create-and-push:
        name: Create file and push
        runs-on: ubuntu-latest
        permissions: write-all
        steps:
            - name: Checkout repository
              uses: actions/checkout@v4
              with:
                ref: ${{ github.event.pull_request.head.sha }}
            - name: Create a test txt file
              run: touch test.txt
            - name: Commit changes
              run: |
                git config --global user.email "41898282+github-actions[bot]@users.noreply.github.com"
                git config --global user.name "github-actions[bot]"
                git add .
                if [[ $(git status --porcelain) ]]; then
                   git commit -m "style: Formatted Java files"
                fi
            - name: Push changes
              if: github.event_name != 'pull_request'
              run: git push
```
