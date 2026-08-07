# homebrew-roost

Homebrew tap for [roost](https://github.com/navbytes/roost) — a session-native
terminal multiplexer for AI agent CLIs (pi, Claude Code, codex, gemini,
opencode, your shell). No daemon, ever.

```sh
brew install navbytes/roost/roost
```

Or tap first, if you prefer:

```sh
brew tap navbytes/roost
brew install roost
```

Installs a prebuilt binary — macOS and Linux, arm64 and x86_64 — from the
matching [GitHub Release](https://github.com/navbytes/roost/releases), verified
against that release's `SHA256SUMS.txt`. No Rust toolchain needed.

## What this repo is

One formula, and nothing else. The source of truth is
[`packaging/homebrew/roost.rb`](https://github.com/navbytes/roost/blob/main/packaging/homebrew/roost.rb)
in the main repo; `Formula/roost.rb` here is a copy of it. When a release is
cut, that file is updated with the new version and checksums and copied across
— the checklist lives in the main repo's `packaging/README.md`.

Issues and pull requests belong in
[navbytes/roost](https://github.com/navbytes/roost), not here.

## Other ways to install

roost doesn't need Homebrew. See the
[Install section](https://github.com/navbytes/roost#install) for `mise`,
`cargo binstall`, `cargo install`, or just downloading a binary.

Note for anyone reaching for crates.io: the name `roost` there belongs to an
unrelated 2018 crate, so a bare `cargo binstall roost` installs something else.
Use `cargo binstall --git https://github.com/navbytes/roost roost`.

MIT licensed, same as roost.
