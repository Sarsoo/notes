---
tags:
  - low-level
  - dev
title: Rust
---
## #web

# Ownership
- Each value in Rust has a variable that’s called its owner.
- There can only be one owner at a time.
- When the owner goes out of scope, the value will be dropped.

#### Backend
-   Actix-web
	-   Quick
-   Rocket
[Benchmarks](https://github.com/programatik29/rust-web-benchmarks)
#### gRPC
[rust gRPC](https://www.thorsten-hans.com/grpc-services-in-rust-with-tonic/)


## Rayon
[https://crates.io/crates/rayon](https://crates.io/crates/rayon)
-   Data parallelism

# FFI
[How to implement long-lived variables/state in a library?](https://stackoverflow.com/questions/59028838/how-to-implement-long-lived-variables-state-in-a-library)
[Foreign Function Interface - Rustonomicon](https://doc.rust-lang.org/nomicon/ffi.html#foreign-function-interface)
