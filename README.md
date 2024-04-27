# PactNet glibc vs. musl

## What works

Distro using `glibc`.

```bash
docker build --no-cache -f Dockerfile.debian .
```

Distro using `musl` with patching `libpact_ffi.so`.

```bash
docker build --no-cache -f Dockerfile.patch .
```

## What doesn't work

Uses `musl` with `gcompat`.

```bash
docker build --no-cache -f Dockerfile.gcompat .
```
