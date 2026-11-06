# Shared Renovate preset

Shared dependency update policy for Scio repositories: Monday updates, a three-day release delay (except digests), grouped changes, update-type labels, and checked patch/digest/pin automerges Monday–Thursday during Prague working hours. Extend it in a repository’s `renovate.json` with `"extends": ["github>sciocz/renovate-config"]` and add any repository-specific rules locally.

Renovate's npm is held below 12 (`constraints.npm`). npm 12 sets `allow-remote=none` by default and then refuses to fetch some registry tarballs while it rebuilds a lock (`EALLOWREMOTE` on `@tailwindcss/oxide-wasm32-wasi`, so `package-lock.json` is never refreshed; see [npm/cli#9347](https://github.com/npm/cli/issues/9347)). Lift the constraint once npm 12 locks these repos again.
