# rusty_crypto_key

> **This repository has moved.** `rusty_crypto_key` now lives at
> [`crates/rusty_crypto_key`](https://github.com/Rusty-Mill/rusty_mill/tree/main/crates/rusty_crypto_key)
> in the [`rusty_mill`](https://github.com/Rusty-Mill/rusty_mill) monorepo, with full commit
> history preserved. This repository is kept for historical reference and is no longer
> developed; please open issues and pull requests against `rusty_mill` instead.

[![CI](https://github.com/baileyrd/rusty_crypto_key/actions/workflows/ci.yml/badge.svg)](https://github.com/baileyrd/rusty_crypto_key/actions/workflows/ci.yml)

A zeroize-on-drop key storage micro-crate for Rust.

`rusty_crypto_key` provides `SecretBytes`, a secure key container that volatile-zeroes memory on `Drop`, redacts debug prints, and performs constant-time equality comparisons. Behind the default `std` feature, `save_to_file`/`load_from_file` persist a secret to disk, restricted to `0600` (owner read/write only) on Unix; Windows has no equivalent ACL restriction applied yet.

## License

Licensed under either of [Apache License, Version 2.0](./LICENSE-APACHE) or [MIT license](./LICENSE-MIT) at your option.
