---
name: Emergency change — post-implementation review
about: Mandatory record for a change authorised outside the standard process. Due within 5 working days.
title: 'Emergency change review: '
labels: emergency-change
assignees: ''
---

*Required by PMG's Secure Development Protocol. Complete and close within **5 working days** of the change reaching production. The closed issue is the retained record.*

## The change
**Date/time deployed:**
**Repository / PR:**
**Authorised by:** (Software Development Lead or designated backup)
**Lightweight review performed by:** (must not be the author)

## Why it was an emergency
What made this unable to wait for the standard process?

## What changed
Summary of the change as deployed.

## Security requirements considered
The five categories from the PR template — data classification, access control, encryption, logging/monitoring, legal/contractual. Note any that applied and how they were handled.

## Was it appropriate?
- [ ] Yes — the change was correct and the emergency route was justified
- [ ] Partly — see notes
- [ ] No — see notes, and raise a Risk Register entry

Notes:

## Follow-up
- [ ] Change is now reflected in `main` through the normal process
- [ ] Any shortcuts taken have been remediated
- [ ] Risk Register entry raised (if required)
- [ ] No further action needed

## Prevention
What would stop this needing an emergency change next time?
