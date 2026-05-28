# pleme-invalidating-setter-derive

Per-field setter that bumps a cache-invalidation seqno after every assignment. Generates pub fn set_<field>(&mut self, v) { self.<field> = v; self.last_seqno = 0; } for every named field except those listed in skip_fields. Built for mado render.rs.

[![Build](https://github.com/pleme-io/pleme-invalidating-setter-derive/actions/workflows/auto-release.yml/badge.svg)](#)
[![crates.io](https://img.shields.io/crates/v/pleme-invalidating-setter-derive.svg)](https://crates.io/crates/pleme-invalidating-setter-derive)

## Install

```toml
[dependencies]
pleme-invalidating-setter-derive = "*"
```

## Generation

This crate is mechanically emitted by [`tatara-rust-ast`](https://github.com/pleme-io/tatara-rust-ast). The author surface is a typed `(defmacro …)` Spec — the proc-macro implementation, tests, Nix flake, caixa wrapper, and CI workflow are all generated. See the catalog at `catalog.json` in the parent registry.
