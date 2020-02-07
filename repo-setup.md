# Setup for developing on this repository

This repo is utilizing git hooks and [pre-commit](https://pre-commit.com/) to run some checks and automate readme documentation prior to committing to git

Install using homebrew:
```bash
brew install pre-commit gawk terraform-docs tflint
```

Install the git hook for you local environment to run the configured `pre-commit` actions automatically on `git commit`
```bash
pre-commit install
```

If you want to run all the pre-commit configured checks without doing a commit.
```bash
pre-commit run --all-files
```

### Firewall Note
If you are working from a location that restricts outgoing requests on non-standard ports.  Note that pre-commit pulls dependent github repos via port `9418`
