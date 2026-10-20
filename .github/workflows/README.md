# Reviewed changes workflow

This workflow is the central source for Voltage's required approval-equivalence
check. Organization rulesets select it from this repository's protected `master`
branch. Keep native stale-review dismissal enabled on this source repository.

The Python source, tests, generator, consumer event helpers, and deployment
instructions live in
[voltage-terraform](https://github.com/voltagecloud/voltage-terraform/tree/master/v2/environments/github/reviewed_changes)
and its [GitHub environment README](https://github.com/voltagecloud/voltage-terraform/blob/master/v2/environments/github/README.md).
Regenerate the workflow there, then review the generated update in this repository.

Merging this workflow does not activate approval retention. Install and verify the
consumer helpers and required organization ruleset before changing native review
settings. The workflow blocks merging when it cannot establish equivalence.

The source repository is excluded from this gate and uses native review
protection. The verifier job skips source-repository PRs.
