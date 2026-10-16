# Disposable M3 GitHub App fixture

This repository contains only controlled acceptance-test files. No customer code,
secrets, AI execution or automatic merge is allowed. Keep the initial `dev` commit
and its workflow in place before running the coding-agent GitHub App harness.

The `m3-quality` job runs on the exact pushed `agent/**` commit. It deliberately
waits briefly so pending status can be observed. A literal `FORCE_CI_FAILURE` in a
`.coding-agent-m3/*.txt` file makes the job fail without executing file contents.
Only a trusted human may prepare a separate failure fixture; the default harness
expects successful checks. Never add secrets or write permissions to this workflow.
