# Contributing to PMG Repositories

## Before you start

- Repository access is granted through GitHub Team membership, and is approved before it is provisioned. If you need access to a repository, ask your team lead.
- Two-factor authentication is mandatory across the organisation, and accounts must be individually identifiable — no shared or generic logins.
- Google Cloud access is managed separately through GCP IAM rather than through GitHub. Request it through the Software Development Lead.
- Check the repository's own README for project-specific setup (dependencies, environment variables, and so on).

## Branching

- **main** — production; deploys to the production GCP project. Protected.
- **dev** — integration branch; deploys to the development GCP project.
- **Feature branches** — created from `dev`, named by type so intent is clear at a glance:
  - `feature/<short-description>` — new functionality
  - `fix/<short-description>` — bug fixes
  - `docs/<short-description>` — documentation-only changes
  - `chore/<short-description>` — maintenance or tooling

## Making a change

1. **Think about security before you write code, not at the PR.** If the change touches data classification, authentication or access control, encryption, logging, or anything with a contractual obligation attached, work that out during planning — the PR template asks you to record the outcome, it isn't the place to first consider it.
2. Branch from `dev`.
3. Open a pull request into `dev` and fill out the PR template completely — the security requirements section isn't a formality, it's reviewed.
4. Automated review and any CI checks configured on that repository run automatically; address anything they flag.
5. Once merged and validated in dev, a further PR promotes the change from `dev` into `main`.

## Branch protection

Organisation-wide rulesets cover every repository. They apply a lighter bar on the integration branch than at production, by design:

- Pull requests are required on both `dev` and `main` — no direct pushes.
- Automated code review is requested on each push to both branches.
- Promotion into `main` additionally requires an approving human review. Stale approvals are dismissed on new pushes, and the most recent push must itself be approved.
- Force pushes and branch deletion are blocked on both.

**No bypass actors are configured on either ruleset** — nobody, including the Software Development Lead, can merge to `main` without review. This is deliberate: PMG's Secure Development Policy requires that code review not be bypassed.

## Automated review

Copilot Code Review runs on every repository, requested by the rulesets on each push to `dev` and `main`.

Automated review supplements human review; it does not replace it. A clean automated review is not an approval — a human reviewer is still expected to assess the change for correctness, security, and code quality.

## CI

CI is configured per repository rather than organisation-wide. Treat a failing check as blocking.

## Emergency changes

Only the Software Development Lead or the designated backup may authorise a change outside this process. An emergency change still goes through a pull request with a lightweight review — a second person confirms the change. A post-implementation review must be completed within 5 working days.

## Dependencies

Dependabot security updates are enabled and open pull requests to remediate vulnerabilities. Remediation targets: Critical — 7 days, High — 30 days, Medium/Low — next routine release. Dependabot pull requests go through the same review process as any other change.

## Security concerns

Do not open a public issue for a security concern. See [SECURITY.md](SECURITY.md) for who to contact in which case.

## Questions

Ask your team lead.
