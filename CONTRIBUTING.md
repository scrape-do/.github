<!-- SPDX-License-Identifier: Apache-2.0 -->
# Contributing to Scrape.do's open-source projects

Thank you for your interest. These are the organisation-wide ground rules; a
repository's own `CONTRIBUTING.md`, when it has one, adds the specifics (tool
versions, how to run the tests, release process) and takes precedence.

## Before you start

- **Bugs and features go through issues first.** Open an issue (the templates
  ask for what we need) before a large change, so the approach is agreed before
  you spend time on it. Small fixes can go straight to a pull request.
- **Security issues are never public issues.** See [SECURITY.md](SECURITY.md).
- **Never commit a credential.** No API tokens, no URLs that carry one, not in
  code, tests, fixtures, logs or examples. The sdo repositories
  (`sdo-go`, `sdo-sdk-js`, `sdo-sdk-python`, `sdo-cli`, `sdo-mcp`, the
  Homebrew tap and the Scoop bucket) have GitHub secret scanning with push
  protection enabled, and the five code repositories also run gitleaks in CI;
  a pull request that contains a secret is closed and the secret must be
  rotated.

## Pull requests

- One topic per pull request, with a clear title in
  [Conventional Commits](https://www.conventionalcommits.org/) form
  (`fix: …`, `feat: …`, `docs: …`), and a description that says what changed
  and why.
- Add or update tests for every behaviour change; keep the repository's
  formatter, linter and type checks green. CI runs them on every pull request.
- Sign off your commits (`git commit -s`): the sign-off is your
  [Developer Certificate of Origin](https://developercertificate.org) statement
  that you have the right to submit the change under the repository's license.
  The five code repositories (`sdo-go`, `sdo-sdk-js`, `sdo-sdk-python`,
  `sdo-cli`, `sdo-mcp`) check every commit's Conventional Commit subject and
  sign-off in CI (the `commits` job); a pull request fails until they are
  fixed.
- A maintainer reviews every pull request before it is merged. In the sdo
  repositories every pull request is squash-merged with its title as the
  commit subject, so the title follows Conventional Commits too; the `commits`
  job still checks each commit on the branch, so fix a failing one with
  `git commit --amend -s` or `git rebase -i` and force-push your branch.

## License

By contributing, you agree that your contribution is licensed under the license
of the repository you contribute to (Apache-2.0 unless the repository says
otherwise), with no additional terms.

## Code of conduct

Everyone participating in these projects is expected to follow our
[Code of Conduct](CODE_OF_CONDUCT.md).
