# Reproduce

```shell
uv sync
pylyzer
```

gives

```
thread 'pylyzer' panicked at /Users/runner/.cargo/registry/src/index.crates.io-1949cf8c6b5b557f/erg_compiler-0.6.53-nightly.5/context/generalize.rs:374:13:
internal error: entered unreachable code
note: run with `RUST_BACKTRACE=1` environment variable to display a backtrace
Thread panicked: Any { .. }

```

Removing

```py
import matplotlib.pyplot as plt
```

fixes it
