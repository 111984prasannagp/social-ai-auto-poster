# Failure Matrix

| Failure | Safe response |
|---|---|
| AI timeout | Retry within a bounded limit |
| Invalid AI JSON | Reject and request regeneration |
| Approval missing | Do not publish |
| Authentication failure | Stop and report; do not retry blindly |
| Rate limit | Respect provider guidance and back off |
| Duplicate detected | Skip publication and report |
| Network timeout after publish | Verify publication status before retrying |

The safest default for uncertain publication state is verification, not another publish attempt.