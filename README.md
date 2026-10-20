# Shared Renovate preset

Shared dependency update policy for Scio repositories: Monday updates, a three-day release delay (except digests), grouped changes, update-type labels, and checked patch/digest/pin automerges Monday–Thursday during Prague working hours. Extend it in a repository’s `renovate.json` with `"extends": ["github>sciocz/renovate-config"]` and add any repository-specific rules locally.
