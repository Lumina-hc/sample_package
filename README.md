# sample_package

A minimal [photon](../../README.md) test package. It exists only to verify that
the package manager can install a third-party repository and build against it.

```
sample_package/
├── lumina.toml                # package manifest
├── include/sample_package.lumi  # declaration-only signatures
└── src/
    ├── sample_package.lum     # source
    └── sample_package.lumc    # precompiled library
```

## Exports

| Function | Signature | Result |
| -------- | --------- | ------ |
| `hello` | `() string` | `"hello from sample_package"` |
| `answer` | `() i32` | `42` |

## Using it

```bash
pho add github:YOUR_USER/sample_package@v0.1.0
```

```lum
use sample_package::hello, answer

fn main() i32 {
    out hello()
    out answer()
    back 0
}
```

## License

Apache License 2.0 - see [LICENSE](LICENSE).
