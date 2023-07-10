# Issue Template

## Bug Report 

```yml
name: 🐞 Bug Report
description: File a bug report
title: "[BUG] "
labels: ["bug"]
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
  - type: checkboxes
    id: terms
    attributes:
      label: Code of Conduct
      description: By submitting this issue, you agree to follow our [Code of Conduct](https://github.com/github_user/repo/blob/main/CODE_OF_CONDUCT.md).
      options:
        - label: I agree to follow this project's Code of Conduct
          required: true	
```
