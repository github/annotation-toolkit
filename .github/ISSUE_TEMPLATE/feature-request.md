name: Annotation toolkit feature request
about: Request an addition to the annotation toolkit.
title: "[Feature request] "
labels: ["feature request", "toolkit"]
body:
  - type: markdown
    attributes:
      value: |
        Have an idea for the annotation toolkit? Submit it using this issue template and we'll take it under consideration.
  - type: input
    id: short-description
    attributes:
      label: Short description of the feature
      description: Please give a high-level description of the feature you're proposing.
    validations:
      required: true
  - type: textarea
    id: long-description
    attributes:
      label: More details about the feature
      description: Please provide more information about the feature you're proposing. The more information we have, the easier it will be to evaluate the ask. Include screenshots or video recordings if you feel they will be helpful.
    validations:
      required: true
  - type: checkboxes
    id: alt-text
    attributes:
      label: Alt text
      description: Descriptive text alternatives have been provided for any images added to this Issue. How to [add alt text to images in Markdown](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#images).
      options:
        - label: My images use descriptive alt text.
          required: true
    id: code-of-conduct
    attributes:
      label: Code of Conduct
      description: By submitting this issue, you agree to follow our [Code of Conduct](https://github.com/github/annotation-toolkit/blob/main/CODE_OF_CONDUCT.md).
      options:
        - label: I agree to follow this project's Code of Conduct
          required: true