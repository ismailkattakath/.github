# .github

[![ci: build status on main](https://github.com/ismailkattakath/.github/actions/workflows/ci.yml/badge.svg?branch=main&event=push)](https://github.com/ismailkattakath/.github/actions/workflows/ci.yml)
[![license: MIT](https://img.shields.io/badge/license-MIT-blue)](LICENSE)

Default community health files for every public `ismailkattakath` repository.

GitHub serves the files in [`.github/`](.github) to every public repository of this account
that has no copy of its own
([GitHub docs](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file)):

| File | Purpose |
|---|---|
| [`CODE_OF_CONDUCT.md`](.github/CODE_OF_CONDUCT.md) | Contributor Covenant 3.0 |
| [`CONTRIBUTING.md`](.github/CONTRIBUTING.md) | How to propose a change |
| [`SECURITY.md`](.github/SECURITY.md) | How to report a vulnerability privately |
| [`SUPPORT.md`](.github/SUPPORT.md) | Where questions go |
| [`ISSUE_TEMPLATE/`](.github/ISSUE_TEMPLATE) | Bug, feature and question forms |
| [`pull_request_template.md`](.github/pull_request_template.md) | The pull request checklist |

## Maintaining

Every file except `flake.nix` and this README is **generated** by
[repo-kit](https://github.com/ismailkattakath/repo-kit). The text is shared with
[`kattakath/.github`](https://github.com/kattakath/.github), so change it in repo-kit, then:

```sh
nix flake update repo-kit
nix run .#write-files
nix flake check   # fails if any file differs from what repo-kit generates
```

The design is ADR-016 in
[kattakath/nix-config](https://github.com/kattakath/nix-config/blob/main/docs/fleet-repo-shape-adr.md).

## License

[MIT](LICENSE). The Code of Conduct is adapted from the Contributor Covenant, licensed under
CC BY-SA 4.0.
