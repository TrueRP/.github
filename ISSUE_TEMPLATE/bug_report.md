name: "Bug Report"
description: "Report a bug or issue"
body:
  - type: dropdown
    id: type
    attributes:
      label: "Type"
      description: "Select the type of issue"
      options:
        - "🐞 Bug Fix"
        - "🔄 Update"
        - "⚠️ Security"
    validations:
      required: true

  - type: dropdown
    id: scope
    attributes:
      label: "Scope"
      description: "Where does the issue occur?"
      options:
        - "client"
        - "server"
        - "both"
    validations:
      required: true

  - type: checkboxes
    id: criticality
    attributes:
      label: "Criticality"
      description: "Select what applies"
      options:
        - label: "Breaks existing functionality"
        - label: "Security vulnerability"
        - label: "Performance impact"

  - type: textarea
    id: console_error
    attributes:
      label: "Console Error Message"
      description: "For example: resources/scripts/[name]/client/main.lua line number"
    validations:
      required: false

  - type: textarea
    id: screenshot
    attributes:
      label: "Screenshot Console"
      description: "Attach a full page screenshot of the error message."
    validations:
      required: false

  - type: textarea
    id: reproduction_steps
    attributes:
      label: "Reproduction Steps"
      description: "Describe the steps to reproduce the problem as detailed as possible."
    validations:
      required: true