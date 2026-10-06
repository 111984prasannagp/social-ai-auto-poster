# Social AI Auto Poster Testing

## Test stages
- Validate Telegram intake with synthetic media.
- Test AI JSON parsing with valid and malformed responses.
- Verify approval gates block unapproved publishing.
- Mock platform APIs for failure and retry scenarios.
- Test duplicate protection before enabling live publishing.

## Safety rule
Live credentials should never be required for ordinary unit tests.
