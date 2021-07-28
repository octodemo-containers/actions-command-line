# Run issue comments as shell commands

This repository contains a GitHub Actions workflow which is triggered when a new
issue is created or when a comment is added to an existing issue. In both
situations, the body of the created issue/comment will be executed in a
GitHub-hosted runner as a shell command (Bash); the generated output will then
be automatically published in the issue as a comment.

This type of trick is possible because GitHub Actions has capabilities which go
far beyond what is available in traditional CI/CD platforms. GitHub Actions can
automatically execute workflows based on [a large collection of
events](https://docs.github.com/en/actions/reference/events-that-trigger-workflows)
which typically occur during the software development lifecycle such as "a label
is added to an issue", "a branch or tag is created", "a milestone is created"
and so on.