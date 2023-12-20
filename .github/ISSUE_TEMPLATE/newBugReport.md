name: Bug Report
description: File a bug report
title: "[Bug]: "
labels: ["bug", "triage"]
projects: ["octp-org/1", "octo-org/44"]
assigneers:
    - octocat
body:
    - type: markdown
        attributes:
            value: |
                Thanks for taking the time to fill out this bug report!
    - type: input
        id: contact
        attributes:
            labelL Contact Details
            description: How can we get in touch with you if we need more info?
            placeholder: ex. email@example.com
        validations:
            required: false
    - type: textarea
        id: what-happened
        attributes:
            label: What happend?
            description: Also tell us, what did you expect to happen?
            placeholder: Tell us what you see!
            value: "A bug happended!"
        validations:
            required: true
    - type: dropdown
        id: version
        attributes:
            label: Version
            description: What version of out software are you running?
            options:
                - 1.0.2 (Default)
                - 1.0.3 (Edge)
            default: 0
        validations:
            required: true
    - type: dropdown
        id: browsers
        attributes:
            label: What browsers are you seeing the problem on?
            multiple: true
            option:
                - Firefox
                - Chrome
                - Safari
                - Microsoft Edge
    - type: textarea
        id: logs
        attributes:
            label: Releveant log output
            description: Please copy and paste any relevant log output. This will be automatically formatted into code, so no need for backticks.
        render: shell
    - type: checkboxes
        id: terms
        attributes:
            label: Code of Conduct
            description: By submitting this issue, you agree to follow out [Code of Conduct] (http:..example.com)
            option:
                - label: I agree to follow this project's Code of Conduct
                require: true