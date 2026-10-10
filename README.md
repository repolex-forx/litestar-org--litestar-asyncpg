# Repolex Knowledge Graph of litestar-org/litestar-asyncpg

RDF knowledge graph data for [litestar-org/litestar-asyncpg](https://github.com/litestar-org/litestar-asyncpg), parsed by [repolex](https://repolex.ai).

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
rlex download litestar-org/litestar-asyncpg
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 23fd93d733c74c9b8825c6758d57d34433a540c3
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 23fd93d733c74c9b8825c6758d57d34433a540c3
│           └── chunk-001.nq.gz
├── blob
│   ├── 0e7be0638f89a816bc866e07fd9fb693cb9ea702.nq.gz
│   ├── 123014908bebbfb7ecfa1d15daaceb272fabe05b.nq.gz
│   ├── 19fb0b308623b543d7f3f66632e62472e9f1fb02.nq.gz
│   ├── 1b73029021d7501159a932a3d96bf904ceb99796.nq.gz
│   ├── 1d36fa9bd4b65e30492cee2df85b96bbb0cce59c.nq.gz
│   ├── 26e54fb0e1cf4ffe71d2b4ec827bbe3dee354ba3.nq.gz
│   ├── 28f173a748069495dcc9e4a52cbfea03898fe555.nq.gz
│   ├── 4585d1c150b4909cf675e116fde7868a4a3f62c0.nq.gz
│   ├── 4dba67b421cb79959c77ea920de502bb28304835.nq.gz
│   ├── 50835800a6138ee90e7f21cd6c374f111f7636fd.nq.gz
│   ├── 586cbc25096495940eec5638c455fc438039b4ee.nq.gz
│   ├── 65aac163c7104b2e349427bb03332b284cc9250d.nq.gz
│   ├── 7198445f8b00b050a19f0ed15a8b18fa4930c658.nq.gz
│   ├── 7bc7f50c6a7789e9e8a6aa95b131582662aef5bb.nq.gz
│   ├── 7e140204a236e070383f8a5406727227bac4fa2f.nq.gz
│   ├── 8502513b8f7200b26e357e678d4f460102d4ce9d.nq.gz
│   ├── 8d0ef71a705069a55931cbc9ef73dccffef729d2.nq.gz
│   ├── 9201ef4c614eadac037863fc018f6fb3c7b802e6.nq.gz
│   ├── 9ecf976e358d07a3eb7daf57be1545da83c59d3a.nq.gz
│   ├── a1f9d02dddf2d5e1bee7d954d6f1252c5015f9d4.nq.gz
│   ├── a3de5a6a1ee6d7ce07f7b5f6fac3239a17043688.nq.gz
│   ├── b4491ff3676ad4ddab44598029f3dfdec778ffb6.nq.gz
│   ├── b4b1a2f2d14063ca4a7f02d0866aaaeb618be229.nq.gz
│   ├── b6d1cebf0dcb3bba30e388475a8163092d028b05.nq.gz
│   ├── b7e2662126805fa37004d79bb18dc894ff40b19a.nq.gz
│   ├── bbb6ae86a18e0267bb43791b865c8f8970dadb42.nq.gz
│   ├── bbd440e7a11cd492aeadbc4fe999f354366866df.nq.gz
│   ├── bd28b9c5c27e0dfa60da94179ec9b23f2be8be0c.nq.gz
│   ├── ca065bc7696f5797a17dce595bc47fc20ec1eb17.nq.gz
│   ├── ce1f7f7887332c34f51fc7a7fd16846d6c8f1cdd.nq.gz
│   ├── d4bb2cbb9eddb1bb1b4f366623044af8e4830919.nq.gz
│   ├── d525c719d5391bce87c2228600dc27999490a09c.nq.gz
│   ├── dad1b1538a9d35c3ba8296677180bc6cdacee099.nq.gz
│   ├── e3af341de28f6b89192feaaa5806a283ca208c66.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e8c1b27f3861d1fce7b86597bf4f51f7f15d453d.nq.gz
│   ├── ef1921377e37dd8397e89bced757f91fd0a63fc7.nq.gz
│   ├── f0a73bb14c1f096d673e24ecde4cf71cd21fd5e3.nq.gz
│   └── f4c1ca717cd8b20448bbcdd843868c181852107d.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 23fd93d733c74c9b8825c6758d57d34433a540c3.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 47 files
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

[litestar-org/litestar-asyncpg](https://github.com/litestar-org/litestar-asyncpg)

---
*Parsed on 2026-10-10 by [repolex](https://repolex.ai)*
