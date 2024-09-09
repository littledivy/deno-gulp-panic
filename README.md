https://github.com/denoland/deno/issues/25515

Build deno with `core/debug_refcell` feature:

```
cargo +nightly b --target x86_64-unknown-linux-gnu -Zbuild-std -Zbuild-std-features="core/debug_refcell" --bin deno -p deno
```

```
RUST_BACKTRACE=full deno --inspect-brk --strace-ops -A ./node_modules/.bin/gulp deno-watch
```
