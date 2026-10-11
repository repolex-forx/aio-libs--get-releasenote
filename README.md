# Repolex Knowledge Graph of aio-libs/get-releasenote

RDF knowledge graph data for [aio-libs/get-releasenote](https://github.com/aio-libs/get-releasenote), parsed by [repolex](https://repolex.ai).

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
rlex download aio-libs/get-releasenote
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── ad89ff3bd631f45622773d5de19d9783729aacfd
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── ad89ff3bd631f45622773d5de19d9783729aacfd
│           └── chunk-001.nq.gz
├── blob
│   ├── 0b2f7b0655f41276d418ca8302dbaec8b7e7e829.nq.gz
│   ├── 0cb2270d59f4380487058a2174c3594549386a03.nq.gz
│   ├── 1525dfaf18f8100ca5589445d7c0992e7af38f3e.nq.gz
│   ├── 1f18e837253537f4d0caa0d7d413edafec660cdf.nq.gz
│   ├── 26a4239386834a4cc7b6647898b3acc3abbf5965.nq.gz
│   ├── 329226d0b0e94d60382a7ccbeb53625eae595405.nq.gz
│   ├── 44588100f265b199343e24216bd7a8668cee832c.nq.gz
│   ├── 4bc60f738d7fe15c05d8f5d277b07f268c3b6975.nq.gz
│   ├── 5688ac2004800e06631684758c871333c9038d79.nq.gz
│   ├── 647ae33dead96e717944d15bd79a98a25edb3214.nq.gz
│   ├── 72c7eb16194a8ad7ae13c8d67081865ac31d4213.nq.gz
│   ├── 8ff2918f82ed3c0250af0a56f87faef33cc79ce7.nq.gz
│   ├── 9179b31d8080ff573c9eccae5f2a0535c8defa1f.nq.gz
│   ├── a40b927aa697e4694edd1d9bf58498fbf23419fe.nq.gz
│   ├── c3bbbc6729fbd53961ddf0191264432c4f99611b.nq.gz
│   ├── c78dc046fd798edec1b9bed4e680a6777b425e8a.nq.gz
│   ├── d7bed169be8714a5d8f8ba8941476aebb73b51e5.nq.gz
│   ├── e66ea850a02f74db1f0af6ab1da096db2bdae4dc.nq.gz
│   ├── e689b90e3bca0d78bf69033220bf420e23ec02cd.nq.gz
│   └── eae16e85bde209b9f95851bb7948e28c250032f7.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── ad89ff3bd631f45622773d5de19d9783729aacfd.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 28 files
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

[aio-libs/get-releasenote](https://github.com/aio-libs/get-releasenote)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
