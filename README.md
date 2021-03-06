# homebrew formulae

### Usage
```bash
brew tap starrwulfe/formulae
brew install <formula>
```

### Formulae
- [browserpass](https://github.com/browserpass/browserpass-native) native binary for browserpass web extension
  - homebrew-core won't accept as a formula, but might not work as cask. 
  - [homebrew issue](https://github.com/Homebrew/homebrew-core/pull/21039)
- [libguestfs](http://libguestfs.org/), a library for editing VM disk images
  - current working: `brew install libguestfs@1.32`
  - should be added to homebrew after some options are tested/removed
  - related: [cmake, cdrtools, hivex issue](https://github.com/Homebrew/legacy-homebrew/pull/2765) in `legacy-homebrew`
  - unfortunately, the older v1.32 is currently the most recent stable which builds+tests OK on mac. v1.36 times out on tests, and v1.40 has issues building (easily).
  - Will likely rebase this on something else because the dependency `:osxfuse` has been obsoleted in Homebrew. I changed it to `depends on: libfuse`, so we'll see     if that works.
- automake-1.15, (autotools)
  - this version was a build dep for older versions of libguestfs
  - current homebrew version >= 1.16
- [matterhorn](https://github.com/matterhorn-chat/matterhorn) terminal mattermost client
  - i don't feel like building it from source right now
  - [homebrew issue](https://github.com/Homebrew/homebrew-core/pull/36196)
- [xi-mac](https://github.com/xi-editor/xi-mac) - fast, modern text editor with a backend written in rust
  - very alpha stage: doesn't have stable releases yet
- [endoh1](https://www.ioccc.org/2012/endoh1/hint.html)
  - neat IOCCC submission on fluid dynamics rendered as ascii

### Obsolete
- 04/06/2019: [Ghidra added to homebrew-cask](https://github.com/Homebrew/homebrew-cask/pull/59872)
- 02/07/2021: Matterhorn has been in homebrew for a while now I guess.