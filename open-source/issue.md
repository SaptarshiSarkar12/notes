---
description: Issue Templates commonly used in various Open-Source projects
---

# Issue Template

## Bug Report For Application

```yml
name: 🐞 Bug Report
description: File a bug report
title: "[BUG] "
labels: ["bug", "App"]
body:
  - type: textarea
    id: bug-description
    attributes:
      label: Describe the bug
      description: A clear and concise description of what the bug is.
      placeholder: Tell us what you have seen!
    validations:
      required: true
  - type: textarea
    id: steps-to-reproduce
    attributes:
      label: Steps To Reproduce
      description: Steps to reproduce the behavior.
      placeholder: |
        1. Open '...'
        2. Enter '....'
        3. Scroll down to '....'
        4. See error
    validations:
      required: true
  - type: textarea
    id: expected-behaviour
    attributes:
      label: Expected Behavior
      description: A concise description of what you expected to happen.
    validations:
      required: false
  - type: dropdown
    id: os
    attributes:
      label: Operating System
      description: Please select the operating system that you have used.
      options:
        - Windows
        - MacOS
        - Linux
    validations:
      required: true
  - type: textarea
    id: screenshots
    attributes:
      label: Screenshots
      description: |
        Please add as many relevant screenshots as possible to convey a perfect bug report.
		    Tip:- You can attach images or log files by clicking this area to highlight it and then dragging files in.
    validations:
      required: false
  - type: textarea
    id: extrainfo
    attributes:
      label: Additional information
      description: Add anything that will give us more context about the issue you are encountering!
    validations:
      required: false
  - type: textarea
    id: logs
    attributes:
      label: Relevant log output
      description: Please copy and paste any relevant log output. This will be automatically formatted into code, so no need for backticks.
      render: shell
  - type: checkboxes
    id: terms
    attributes:
      label: Code of Conduct
      description: By submitting this issue, you agree to follow our [Code of Conduct](https://github.com/github_user/repo/blob/main/CODE_OF_CONDUCT.md).
      options:
        - label: I agree to follow this project's Code of Conduct
          required: true
```

## Bug Report For Website

```yml
name: 🐞 Bug Report
description: File a bug report
title: "[BUG] "
labels: ["bug", "Website"]
body:
  - type: textarea
    id: bug-description
    attributes:
      label: Describe the bug
      description: A clear and concise description of what the bug is.
      placeholder: Tell us what you have seen!
    validations:
      required: true
  - type: textarea
    id: steps-to-reproduce
    attributes:
      label: Steps To Reproduce
      description: Steps to reproduce the behavior.
      placeholder: |
        1. Open '...'
        2. Enter '....'
        3. Scroll down to '....'
        4. See error
    validations:
      required: true
  - type: textarea
    id: expected-behaviour
    attributes:
      label: Expected Behavior
      description: A concise description of what you expected to happen.
    validations:
      required: false
  - type: dropdown
    id: browsers
    attributes:
      label: What browsers are you seeing the problem on?
      multiple: true
      options:
        - Firefox
        - Chrome
        - Safari
        - Microsoft Edge
    validations:
      required: true
  - type: textarea
    id: screenshots
    attributes:
      label: Screenshots
      description: |
        Please add as many relevant screenshots as possible to convey a perfect bug report.
		    Tip:- You can attach images or log files by clicking this area to highlight it and then dragging files in.
    validations:
      required: false
  - type: textarea
    id: extrainfo
    attributes:
      label: Additional information
      description: Add anything that will give us more context about the issue you are encountering!
    validations:
      required: false
  - type: checkboxes
    id: terms
    attributes:
      label: Code of Conduct
      description: By submitting this issue, you agree to follow our [Code of Conduct](https://github.com/github_user/repo/blob/main/CODE_OF_CONDUCT.md).
      options:
        - label: I agree to follow this project's Code of Conduct
          required: true	
```

## Docs Request 📄

```yml
name: 📄 Documentation Change request
description: Change regarding improving the docs to be more accessible
title: "[DOCS] "
labels: [documentation]
body:
  - type: textarea
    attributes:
      label: Category of documentation update
      description: |
        What category does this change fall under? For example, Typo error, New category addition, Rephrasing the sentences, fixing broken links, etc. 
    validations:
      required: true
  - type: textarea
    attributes:
      label: Describe the change you think might work
      description: Please describe the change & need of the change in atmost detail possible.
    validations:
      required: true
  - type: textarea
    id: extrainfo
    attributes:
      label: Additional information
      description: Add any other context about the change in the documentation here.
    validations:
      required: false
```

## Feature Request

```yml
name: 💡 Feature Request for Application
description: Suggest a new feature request
title: '[FEATURE] '
labels: ['enhancement']
body:
  - type: textarea
    id: related-problem-for-feature-request
    attributes:
      label: Is your feature request related to a problem? Please describe.
      description: A clear and concise description of what the problem is.
      placeholder: I'm always frustrated when [...]
    validations:
      required: false
  - type: textarea
    id: feature-description
    attributes:
      label: Describe the solution you'd like.
      description: A clear and concise description of what feature you want to include.
    validations:
      required: true
  - type: textarea
    attributes:
      label: How would this feature be beneficial for the project
      description: A clear and concise description about the importance of the feature
    validations:
      required: false
  - type: textarea
    id: screenshots
    attributes:
      label: Screenshots
      description: Please add relevant screenshots for the feature.
    validations:
      required: false
  - type: textarea
    id: extrainfo
    attributes:
      label: Additional information
      description: Add any other context about the feature here.
    validations:
      required: false
```
