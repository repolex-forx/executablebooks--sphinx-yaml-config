# Repolex Knowledge Graph of executablebooks/sphinx-yaml-config

RDF knowledge graph data for [executablebooks/sphinx-yaml-config](https://github.com/executablebooks/sphinx-yaml-config), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download executablebooks/sphinx-yaml-config
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── b2339a3cd04f452f6e1bbe9c738ce4361360037d
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── b2339a3cd04f452f6e1bbe9c738ce4361360037d
│           └── chunk-001.nq.gz
├── blob
│   ├── 0c9e0fc1447e98b7f63ae8c9eb552c2af7b83f45.nq.gz
│   ├── 27873932770653045a5e7a180f00e1bc45eb4339.nq.gz
│   ├── 2c19663ba2b8eb7d0fe53abed687c647279ae92a.nq.gz
│   ├── 3390fa44a8052765c5729e9c1a4b2fc297d82a1a.nq.gz
│   ├── 3b7948b5cdb8270d1e66ed7862f4176cb16a06bb.nq.gz
│   ├── 443bb8bd6b31587592c485fc566e1858ace80f2d.nq.gz
│   ├── 5a7c4bb01876f4bd3d6235ad521d26c9581bbf0e.nq.gz
│   ├── 638dac8e0157a21706c44d642953c9486ef264f5.nq.gz
│   ├── 8045a790252bda660737c70111106c267c9137bb.nq.gz
│   ├── b479b797024b613ef9d9f4ccac735b9085095e6b.nq.gz
│   ├── ca3fc65ad16f6ad847e659cb8e8eecb00811b4ba.nq.gz
│   ├── cd017d28a3c492f868875b538aeeb360e6183062.nq.gz
│   ├── dab6ba48f3dcb26eae65920afb84113b1ebb141f.nq.gz
│   ├── e267f3f115fa9ec00e025fb6fdb511918965b2d4.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── eeba1f6f8fe6eb1a3dc2f52a67be39a4caacb969.nq.gz
│   └── f9e50006b37281b6307ed32e3f90bbad7c4d23a5.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── b2339a3cd04f452f6e1bbe9c738ce4361360037d.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 23 files
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
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[executablebooks/sphinx-yaml-config](https://github.com/executablebooks/sphinx-yaml-config)

---
*Parsed on 2026-10-15 by [repolex](https://repolex.ai)*
