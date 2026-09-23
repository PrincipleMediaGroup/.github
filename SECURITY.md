# Security Policy

## Reporting a Vulnerability or Security Concern

If you discover a security vulnerability or concern in any PMG system, report it privately rather than opening a public issue.

**Use GitHub's private vulnerability reporting.** Go to the **Security** tab of this repository and choose **Report a vulnerability**. The report is visible only to PMG and to you, and it reaches the people who triage security reports directly.

If you are a PMG staff member, the named contacts for each kind of report are listed in the internal organisation profile. Route your report to a person rather than through this form.

Please include, where possible:
- A description of the issue
- Steps to reproduce it
- Any relevant logs, screenshots, or affected repository or system

We will acknowledge your report within 2 business days and keep you updated as it is investigated.

## How reports are handled

Reports are triaged by responsibility rather than by severity alone:

| What you have found | Who handles it |
| --- | --- |
| A vulnerability or weakness in PMG source code, an application, a dashboard, a model, or a pipeline | PMG's development function |
| An active or suspected security **incident** — unauthorised access, copying, modification or exfiltration of source code or data, a compromised credential, or anything already in progress | PMG's IT provider, under PMG's Incident Management Procedure, with the development function informed |
| An infrastructure issue — cloud configuration, networking, or identity and access management | PMG's IT provider |

If you are not sure which it is, report it as an incident — over-reporting is not a problem.

## Scope

This policy applies to all PMG-owned repositories within this GitHub organisation, along with the supporting Google Cloud infrastructure.

A solution being pre-release does not put it outside this policy: report a vulnerability in an exploratory or prototype repository exactly as you would one in production.

## Our Commitment

Unauthorised access, copying, modification, or exfiltration of source code or data is treated as a security incident and handled in accordance with PMG's Incident Management Procedure, not as a routine bug report.
