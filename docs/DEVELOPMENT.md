# Social AI Auto Poster Development Guide

## Pipeline boundaries
Keep media intake, AI copy generation, approval, platform publishing, and reporting as separate stages.

## Workflow
1. Preserve the original media asset.
2. Generate structured copy.
3. Validate the generated payload.
4. Require human approval.
5. Publish through official APIs.
6. Report success or failure with enough context to retry safely.

## Commit standard
Prefer atomic commits that describe one pipeline improvement.
