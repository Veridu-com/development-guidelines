# Code Review
Code review isn't supposed to be a very extensive process, given that the project **MUST** have unit tests.

This process MUST include:

- An overview of changes, trying to spot anything that:
	- Doesn't follow coding standards (although linters and other tools should catch this, every now and then something may slip through)
	- May break system consistency or may interfere direct or indirectly with another sub-system
	- Doesn't fit into project organization (there isn't any automated tool that enforces this)
	- Shouldn't to be merged into the main branch (e.g. testing/debugging artifacts, logs, credentials etc)


This process MAY include:

- Unit Test Suite and/or Build execution (this should be executed by CI Service on every commit)
- Local project execution/feature test
