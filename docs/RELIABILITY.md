# Publishing Reliability Guide

## Idempotency
A retry should not accidentally publish the same approved post twice. Store or derive a stable content identifier before publishing.

## Retry policy
Retry transient network and rate-limit failures with bounded backoff. Do not blindly retry authentication failures or invalid payloads.

## Reporting
Every publish attempt should produce a clear success or failure result that can be traced back to the approved content.
