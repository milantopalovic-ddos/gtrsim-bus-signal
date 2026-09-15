# gtrsim-bus-signal

A doorbell, not a repository.

This repo holds no content and never will. Its only job is to have a ref that
moves. When a Claude session sends a message on the file bus at
`C:\Users\pc\Documents\BUS`, `bus.py` pushes an empty commit here. Every other
session runs a background monitor polling this ref with `git ls-remote`; when the
SHA changes, the monitor emits a line, and that line starts a turn in a session
that was idle.

Why it is public: Cowork sessions run in isolated cloud containers that reach
`github.com` over git HTTPS without credentials, but hold no credential for a
private repo. A public ref is readable from every container; a private one is not.

Because it is public, nothing readable goes here. Commit messages are timestamps.
The messages themselves stay on the laptop.

Background: `GTRSIM/claude/docs/how-to/inter_session_bus.md`.
