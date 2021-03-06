homebrew-ghc
================

You found this repository because the existing GHC formula is not updated as frequently as I would like and because I also need a formula that allows me to install multiple versions of GHC side by side so I can easily switch between them.

It also installs from the provided binary distributions from GHC instead of installing from source. The exception is ghc783x86 (32 bits) since there is no binary distribution for this.

Tap into this
============
First add the homebrew-ghc tap:

```bash
brew tap rodlogic/homebrew-ghc
```

Installing a specific GHC version
=================================

Now, for instance, install ghc-7.8.3:

```bash
> brew install ghc783
...
```

And link the binaries to the /usr/loca/bin folder:

```bash
> brew link ghc783
Linking /usr/local/Cellar/ghc783/7.8.3... 17 symlinks created
```

Test it out:

```
> ghc --version
The Glorious Glasgow Haskell Compilation System, version 7.8.3
```

Installing a second version of GHC
==================================

Let's install ghc-7.6.3:

```bash
> brew install ghc763
...
```

And now, let's switch to it:

```bash
> brew unlink ghc783
Unlinking /usr/local/Cellar/ghc768/7.8.3... 17 symlinks removed
> brew link ghc763
Linking /usr/local/Cellar/ghc763/7.6.3... 17 symlinks created
```

```bash
> ghc --version
The Glorious Glasgow Haskell Compilation System, version 7.6.3
```







