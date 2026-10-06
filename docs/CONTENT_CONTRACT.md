# Content Contract

AI-generated publishing metadata should be treated as structured data.

## Required fields
A generated post should identify its target platform and contain the platform-specific text needed for publication.

## Validation
Reject malformed JSON, missing required fields, unsupported platforms, and values that exceed platform limits.

Keep media handling separate from text generation so the original image is preserved.