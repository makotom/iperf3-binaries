# iperf3-binaries

CircleCI `config.yml` to build executable binaries of `iperf3` for Linux, Windows and macOS. Only `x86_64` is supported.

# Quick start

Pre-build binaries are available as [releases](https://github.com/makotom/iperf3-binaries/releases).

# Hands-on

1. Fork this repo.

2. Set up a [CircleCI](https://circleci.com/) project for your own copy.

   Note 1: You need a paid CircleCI subscription as macOS is not available for the free plan. See also: https://circleci.com/pricing/#comparison-table

   Note 2: `github` context having `GITHUB_TOKEN` envar is required by `release` job. See https://circleci.com/docs/2.0/contexts/#creating-and-using-a-context for creation of context. See https://help.github.com/en/github/authenticating-to-github/creating-a-personal-access-token-for-the-command-line#creating-a-token for creation of GitHub personal access token.

3. Build starts on CircleCI.

4. Check artifacts to find your desired binary.

# Resources (with source code)

* iperf3: https://github.com/esnet/iperf
* OpenSSL (binary bundled with Windows and macOS executables): https://www.openssl.org/
* Cygwin (binary bundled with Windows executables): https://cygwin.com/
