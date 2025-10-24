---
name: Draft issue
about: Start with a basic idea and fill in details later.
title: "[Draft] "
labels: ["draft"]
body:
  - type: markdown
    attributes:
      value: |
        Use this template to quickly create a draft issue. You can add more details later!
  - type: input
    id: title-description
    attributes:
      label: Issue title or brief description
      description: What is this issue about? Keep it short and simple.
      placeholder: e.g., "Need to update documentation for mobile annotations"
    validations:
      required: true
  - type: textarea
    id: initial-notes
    attributes:
      label: Initial notes (optional)
      description: Any early thoughts or context? Feel free to leave this blank if you're still figuring things out.
      placeholder: Add any initial thoughts here...
    validations:
      required: false
  - type: markdown
    attributes:
      value: |
        ---
        ## Additional information needed

        Please come back and add the following details when you have time:

        - **Detailed description**: What are you trying to accomplish? What problem does this solve?
        - **Context**: Why is this important? Who does this affect?
        - **Acceptance criteria**: How will we know when this is complete?
        - **Screenshots or examples**: If applicable, add visuals to help explain
        - **Related issues or PRs**: Link to any related work

        You can edit this issue at any time to add these details!
  - type: checkboxes
    id: code-of-conduct
    attributes:
      label: Code of Conduct
      description: By submitting this issue, you agree to follow our [Code of Conduct](https://github.com/github/annotation-toolkit/blob/main/CODE_OF_CONDUCT.md).
      options:
        - label: I agree to follow this project's Code of Conduct
          required: true
---
