# CI pipeline

## What the scripts do
build.sh checks that my scripts have no errors and that the important files are in the repo.

test.sh runs a few small tests on the repo and fails if any of them don't pass.

## The failure the pipeline caught
I deleted .gitignore on purpose in a pull request. The pipeline failed with the message "Missing: .gitignore", so the pull request was stopped.
Link: https://github.com/BelleSangthong/devops-repo/actions/runs/40206899715