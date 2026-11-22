# Repolex Knowledge Graph of programatik29/axum-server

RDF knowledge graph data for [programatik29/axum-server](https://github.com/programatik29/axum-server), parsed by [repolex](https://repolex.ai).

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
rlex download programatik29/axum-server
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 0d0e181093d5683858a858921deffa0e739f61a0
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 0d0e181093d5683858a858921deffa0e739f61a0.nq.gz
│   └── repolex
│       └── 0d0e181093d5683858a858921deffa0e739f61a0
│           └── chunk-001.nq.gz
├── blob
│   ├── 08c2a85fa5d7448e44c7d1d771e2105f0f80a553.nq.gz
│   ├── 0fc75938e166c469be164829379bf3c23783283d.nq.gz
│   ├── 1616304531a2915a2d076ab089dc4c83eb5c8e3f.nq.gz
│   ├── 17346ec9db84130d656681b2ee303889c3a2f5e4.nq.gz
│   ├── 182dd1ba1d534b1df8168a495db1efadfb20ae3a.nq.gz
│   ├── 2ae086236f53859fb62880357378b8839ec56a58.nq.gz
│   ├── 30963f4c970c697641a8c8a1e0da661419626d3f.nq.gz
│   ├── 32d94c7251aa6291c6dcc95e1833d36786be3ca0.nq.gz
│   ├── 3c7afdced7b468e783606266c10872dd730a567d.nq.gz
│   ├── 3d58d9b6bcc1adaed507d20e2dc956b82f4601d5.nq.gz
│   ├── 452906eb0caf572f66f8188d0a7cff5adc82ecb9.nq.gz
│   ├── 45a3460bc4443c6e88ea01357e747503201a4c7a.nq.gz
│   ├── 4fffb2f89cbd8f2169ce9914bd16bd43785bb368.nq.gz
│   ├── 52034738e356898c5d855a15e77e75934c4018c1.nq.gz
│   ├── 545c0aec646771e080aafaaa71739a453f756ce1.nq.gz
│   ├── 58d97d0e58314d71d1ca00753191c6244050dacf.nq.gz
│   ├── 6627d610d1ebf7762f299ede61e180f79f12003c.nq.gz
│   ├── 8227f327bef9ea950fbebfd1c7edc895034792ca.nq.gz
│   ├── 830e172b68ace58ef54ceb86c5212e0dfbec6971.nq.gz
│   ├── 89aedbeae38d155db15d4049313432b2a55fa1d3.nq.gz
│   ├── 96ef6c0b944e24fc22f51f18136cd62ffd5b0b8f.nq.gz
│   ├── 984d8d2f676642ce8ada96aabb89c32ec7871a04.nq.gz
│   ├── 98c11b97ab7e838dab1acf60013a70199c685ec1.nq.gz
│   ├── ab5db2b9f1496a5b1e82b2c92ff67dd5076b8ed3.nq.gz
│   ├── bc7dccf8635c01220bb7a8df051e2c72fd714e86.nq.gz
│   ├── c0ebc094f27dcfdba9ce8c69e30d63e442d342d2.nq.gz
│   ├── c329a2d836ef9ac75aadddde8d5cae43a24d480d.nq.gz
│   ├── c6f5ea9ce84d31e74e91daab21b2fc3c697a4002.nq.gz
│   ├── cd5a49f7b15712ae13541db40657a902b49ad505.nq.gz
│   ├── d0df28f19b1a929ceeb860fab91fe0db1c6c45bf.nq.gz
│   ├── d32083862680b17b39acb3c78adcf62ab558f79b.nq.gz
│   ├── de0792bdaaea366ce13e51e2a65e49c9274c98af.nq.gz
│   ├── e1fbeacc7e560e3014479a37d907b4ba7b2bde26.nq.gz
│   ├── ef08373bccef5dc50204bb5b9c29e73d334b76ba.nq.gz
│   ├── f48ea028136cef0d4dac80c79f65044ecb7534dc.nq.gz
│   ├── f5c2f16b7926a68f08c68a984c717e28af4d0c39.nq.gz
│   └── f8b09eb69521f47ac67377f8b50987153d1bbe41.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 0d0e181093d5683858a858921deffa0e739f61a0.nq.gz
├── filetree
│   └── 0d0e181093d5683858a858921deffa0e739f61a0.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 47 files
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

[programatik29/axum-server](https://github.com/programatik29/axum-server)

---
*Parsed on 2026-11-22 by [repolex](https://repolex.ai)*
