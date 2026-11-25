# homebrew-patina

The Homebrew tap for [Patina](https://github.com/caffeines/patina): containers for your Mac,
with its own Linux VM and Docker Engine.

```sh
brew install caffeines/patina/patina           # the latest release
brew install --HEAD caffeines/patina/patina    # Patina's main branch
```

The formula builds Patina from source on your Mac (a few minutes while Rust compiles). It
installs the `patina` command and `Patina.app`; `brew info patina` shows how to add the app to
Applications. Homebrew needs current Command Line Tools to build from source.

## Releasing a version

1. In the Patina repo, set `version` in `Cargo.toml`, commit, tag (`v0.2.0`) and push the tag.
2. Here, set the same tag in `Formula/patina.rb`, commit and push.

`brew upgrade patina` then picks it up.
