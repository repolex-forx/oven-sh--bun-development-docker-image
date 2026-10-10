# Repolex Knowledge Graph of oven-sh/bun-development-docker-image

RDF knowledge graph data for [oven-sh/bun-development-docker-image](https://github.com/oven-sh/bun-development-docker-image), parsed by [repolex](https://repolex.ai).

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
rlex download oven-sh/bun-development-docker-image
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 88381bd1b6d41350622df2594e9656549620a0a8
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 88381bd1b6d41350622df2594e9656549620a0a8
│           └── chunk-001.nq.gz
├── blob
│   ├── 1f139fb92f8f86e9dcf11885700a10fdaa4c5087.nq.gz
│   ├── 2b01bb3cbe7f8be62e097ccd4b9f4640e4e46ef8.nq.gz
│   ├── 31d100b1900c9db3b18de01a0ccb8c14b9e54340.nq.gz
│   ├── 47df7d291700335a8ddb8a3980c0a89b3f1ded3d.nq.gz
│   ├── 607f80b7f7a3e67aad6911fb489a872e486b3337.nq.gz
│   ├── 64ab9ba1f92a85300a66a704f97f4ad8a1a8b34b.nq.gz
│   ├── 87f68d10e7f9539a9e071119be60cfecb66c5d3a.nq.gz
│   ├── 93be3745595c3199bf1a1168b5ca658fda09cf11.nq.gz
│   ├── aea7384a07b16cd9e99714d1435c1a54df3de265.nq.gz
│   ├── b1976e9525503463c4da5669e0ba8e5596b3b530.nq.gz
│   ├── c1b3cc258a4d9ceca21c02d54a861b56174127e2.nq.gz
│   ├── db4112bdb4b6cd2c9083d7b547584a8afcddec0a.nq.gz
│   └── f6082c071aaf22f1c3e904df7eeaa2e497673df9.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 88381bd1b6d41350622df2594e9656549620a0a8.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 21 files
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

[oven-sh/bun-development-docker-image](https://github.com/oven-sh/bun-development-docker-image)

---
*Parsed on 2026-10-10 by [repolex](https://repolex.ai)*
