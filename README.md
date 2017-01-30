# fastcmp
[![Build Status](https://travis-ci.org/saschagrunert/fastcmp.svg)](https://travis-ci.org/saschagrunert/fastcmp) [![Build status](https://ci.appveyor.com/api/projects/status/hdv8d12xgjbvsiju?svg=true)](https://ci.appveyor.com/project/saschagrunert/fastcmp) [![Coverage Status](https://coveralls.io/repos/github/saschagrunert/fastcmp/badge.svg?branch=master)](https://coveralls.io/github/saschagrunert/fastcmp?branch=master) [![master doc fastcmp](https://img.shields.io/badge/master_doc-peel_ip-blue.svg)](https://saschagrunert.github.io/fastcmp) [![License MIT](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/saschagrunert/fastcmp/blob/master/LICENSE) [![Crates.io](https://img.shields.io/crates/v/fastcmp.svg)](https://crates.io/crates/fastcmp) [![doc.rs](https://docs.rs/fastcmp/badge.svg)](https://docs.rs/fastcmp)
## A fast byte slice comparison library
The library is intended to provide a faster byte slice comparison than the standard library. Also raw string literals
`b"like this"` are compareable this way. It also supports simd comparisons by enabling the feature `simd_support` in the
`Cargo.toml`.

## Example usage

```rust
use fastcmp::Compare;

let vec = vec![1, 2, 3, 4, 5];
assert!(vec.feq(&[1, 2, 3, 4, 5]));
```

## Benchmarks
The benchmarking results for comparison of two `&[u8]` with a size of 256:

```
running 2 tests
test fast_compare  ... bench:          13 ns/iter (+/- 8) = 19692 MB/s
test slice_compare ... bench:          34 ns/iter (+/- 4) = 7529 MB/s
```

## Contributing
You want to contribute to this project? Wow, thanks! So please just fork it and send me a pull request.
