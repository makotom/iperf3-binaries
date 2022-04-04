# iperf3-binaries

`config.yml` for CircleCI to build executable binaries of `iperf3` for Linux, Windows and macOS. Only `x86_64` is supported.

# Quick start

Pre-built binaries are available [here](https://github.com/makotom/iperf3-binaries/releases).

# Hands-on

1.  Fork this repo.

2.  Set up a [CircleCI](https://circleci.com/) project for your own copy.

    Notes:

    - `github` context with `GITHUB_TOKEN` environment variable, which contains a personal access token for GitHub, is required by `release` job.

    See these resources for details:

    - [Creation of contexts on CircleCI](https://circleci.com/docs/2.0/contexts/#creating-and-using-a-context)
    - [Creation of personal access tokens for GitHub](https://help.github.com/en/github/authenticating-to-github/creating-a-personal-access-token-for-the-command-line#creating-a-token)

3.  Build starts on CircleCI. Once it completes, deliverables will become available on GitHub Releases of your own repo, and [artifacts on CircleCI](https://circleci.com/docs/2.0/artifacts/).

## Pipeline parameters

The pipeline parameter `force-build` enables you to forcibly build a specific revision of the source code.
The parameter accepts any valid Git revision, such as a branch name, tag name, or commit hash, and it is set to a zero-length string by default (causing the pipeline to build the latest tagged version if and only if it is never built).

This enables you to create an ad-hoc release by passing the accordingly-configured parameter, using [the API to trigger a new pipeline](https://circleci.com/docs/api/v2/#operation/triggerPipeline).

# Resources

- [Homepage of iperf3](https://software.es.net/iperf/)
- [iperf3 on GitHub](https://github.com/esnet/iperf)
