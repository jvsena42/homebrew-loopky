# homebrew-loopky

The Homebrew tap for [`loopky`](https://github.com/jvsena42/loopky) — the headless Loopky client
for creating and managing Pubky flashcard decks from a terminal.

```shell
brew install jvsena42/loopky/loopky
loopky --version
```

Apple Silicon and Linux x86-64 only. An Intel Mac and Linux arm64 each get a message naming the
actual reason rather than an install that fails at its first homeserver call — there is one
`darwin-aarch64` row of `libpubkycore` and no Linux arm64 build of it at all.

## This repository is generated

`Formula/loopky.rb` is **written by the `homebrew` job in the loopky repo's `release.yml`** on every
final tag: it renders `cli/packaging/loopky.rb` with the version and the two `sha256`s taken from
the release's own `.sha256` assets, so the formula can only ever describe bytes that were actually
published.

Edit the template in `jvsena42/loopky`, not the formula here — a hand-edit is overwritten by the
next release.

## Upgrading

`loopky update` deliberately **refuses** on a Homebrew install (exit 11): overwriting a file under
`Cellar/` is reverted by the next `brew upgrade` and leaves the binary lying about its version. Use

```shell
brew upgrade loopky
```
