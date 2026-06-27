# homebrew-slop

A [Homebrew](https://brew.sh) tap for [SLOP](https://github.com/slop-lang/slop),
the Symbolic LLM-Optimized Programming language toolchain.

## Install (macOS)

```bash
brew tap slop-lang/slop
brew trust slop-lang/slop   # Homebrew 6.0+ requires trusting third-party taps
brew install slop
```

This builds the native toolchain from source and installs the `slop` CLI in an
isolated virtualenv, alongside the standalone `slop-parser`, `slop-checker`,
`slop-compiler`, and `slop-tester` binaries.

`slop build` transpiles to C and invokes `cc`, so it requires the Xcode Command
Line Tools:

```bash
xcode-select --install
```

```bash
slop --version
slop build examples/fibonacci.slop -o fib && ./fib
```

## License

Apache-2.0 — see [LICENSE](LICENSE).
