# iperf3-binaries

`config.yml` for CircleCI to build executable binaries of `iperf3` for Linux, Windows and macOS. Only `x86_64` is supported.

# Quick start

Pre-built binaries are available [here](https://github.com/makotom/iperf3-binaries/releases).

# Hands-on

1. Fork this repo.

2. Set up a [CircleCI](https://circleci.com/) project for your own copy.

   Note 1: You need a paid CircleCI subscription as macOS is not available for the free plan. See also: https://circleci.com/pricing/#comparison-table

   Note 2: `circleci` context with `CIRCLE_TOKEN` envar is required by `setup` job. See https://circleci.com/docs/2.0/contexts/#creating-and-using-a-context for creation of context. See https://help.github.com/en/github/authenticating-to-github/creating-a-personal-access-token-for-the-command-line#creating-a-token for creation of GitHub personal access token.

   Note 3: `github` context with `GITHUB_TOKEN` envar is required by `release` job. See https://circleci.com/docs/2.0/contexts/#creating-and-using-a-context for creation of context. See https://help.github.com/en/github/authenticating-to-github/creating-a-personal-access-token-for-the-command-line#creating-a-token for creation of GitHub personal access token.

3. Build starts on CircleCI. Once it completes, deliverables will become available on GitHub Releases of your own repo and [artifacts on CircleCI](https://circleci.com/docs/2.0/artifacts/).

## Pipeline parameters

There is a pipeline parameter `force-build` configured to manipulate the behaviour of the pipeline.
The parameter accepts any valid Git revision, such as branch, tag, or commit hash, and its default value is a zero-length string.
Setting a non-empty string for this parameter will build the source code of the designated revision _forcibly_ - regardless of other conditions.
