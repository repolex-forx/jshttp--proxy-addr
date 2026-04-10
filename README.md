# Repolex Knowledge Graph of jshttp/proxy-addr

RDF knowledge graph data for [jshttp/proxy-addr](https://github.com/jshttp/proxy-addr), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download jshttp/proxy-addr
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 9f78739c5333ebea49442235ce720f1d37605706
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 9f78739c5333ebea49442235ce720f1d37605706.nq.gz
│   └── repolex
│       └── 9f78739c5333ebea49442235ce720f1d37605706
│           └── chunk-001.nq.gz
├── blob
│   ├── 19f7fd368ff34448ef5d7960a84373adc1c1d4ea.nq.gz
│   ├── 1eece14ad8cb98de2093fac5eef5ccee89472ff8.nq.gz
│   ├── 2d8d77e1550218149b10155731c4eb47b6b4b6d5.nq.gz
│   ├── 43b5a6587709a7b49ab5994b7ffbadf22432243f.nq.gz
│   ├── 76b1021d09a5774679c815f83d1c9a4bccf21c28.nq.gz
│   ├── 797d5da29a1a902fad9cbdc48c33140fe03f3588.nq.gz
│   ├── 8c176ea56e62fcd2894b296349cc267c6c024180.nq.gz
│   ├── 915b237bb4124b0d4f5b580be0804c3b4c6687a9.nq.gz
│   ├── 9808c3b2b6602da61eb4afcb4caf33368e3e2bd4.nq.gz
│   ├── 9a42ef646964f859f35a6aa39547d32e2c0633fb.nq.gz
│   ├── a909b05064a377ed49b5aea673d0849970f050e9.nq.gz
│   ├── be765b7f1b907dd71f4ab8b04d653b4314cec44c.nq.gz
│   ├── c39ee50f9c9d88f2d7deee36d91e32fc7bca12d0.nq.gz
│   ├── c5f71f9d526c00b050ca6470e02452d3fb5c0242.nq.gz
│   └── cab251c2b9a81318267600f68130faa3a290e5fd.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 9f78739c5333ebea49442235ce720f1d37605706.nq.gz
├── filetree
│   └── 9f78739c5333ebea49442235ce720f1d37605706.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 25 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |

## Source repository

[jshttp/proxy-addr](https://github.com/jshttp/proxy-addr)

---
*Parsed on 2026-04-10 by [repolex](https://repolex.ai)*
