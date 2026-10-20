# Repolex Knowledge Graph of adamchainz/django-auto-prefetch

RDF knowledge graph data for [adamchainz/django-auto-prefetch](https://github.com/adamchainz/django-auto-prefetch), parsed by [repolex](https://repolex.ai).

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
rlex download adamchainz/django-auto-prefetch
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 3df0e0ec2ab4ea48c9a0c31011271656fb57e191
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 3df0e0ec2ab4ea48c9a0c31011271656fb57e191
│           └── chunk-001.nq.gz
├── blob
│   ├── 22ddbb118475b52ce8ecba56d9ec45009923da58.nq.gz
│   ├── 25a2ac1bc3654e8cbe06768ab349c5f492d861ab.nq.gz
│   ├── 2a7f84f54867d02714727f82eef95d3be939d666.nq.gz
│   ├── 3564583f69c5d7960720737684df8a3a0450cb33.nq.gz
│   ├── 3ba13e0cec6cbbfd462e9ebf529dd2093148cd69.nq.gz
│   ├── 40f4ac757715bb1a8c355eda9124141fdda3aeff.nq.gz
│   ├── 478ad29c5855f58e4622a9c53a1bba704ad704c2.nq.gz
│   ├── 4c096935d45531d40b29271476ae73bf1cc0acd0.nq.gz
│   ├── 51bdf0d5159b458d83cf0e21f920e7e50cdd5e97.nq.gz
│   ├── 5cbfca2b35e896ef4edfe8509af3a4dd15824c3f.nq.gz
│   ├── 7f1d007c01048570d774e58f46203d3e92056c39.nq.gz
│   ├── 93acb639926ccf42e9a2f76f02419eeaf0405c3a.nq.gz
│   ├── 94b7ff32bc63c6b2fb1af01f8b0dd36e9bad09bc.nq.gz
│   ├── a9679bdb313bb75a0e5906fab92b01702a4613a8.nq.gz
│   ├── accddb3c1821c87f2a2f6873e61d1236cb26dc2c.nq.gz
│   ├── c1a8326c61f962958e3146e03ab10a437a3efe96.nq.gz
│   ├── c20e66be98ed245a7ffb3b9f9abdc57f7add8faa.nq.gz
│   ├── d92f836bafe6519a6e66016ebfa074c3534194bd.nq.gz
│   ├── dea0450b9829c75c1a4e0bf11c38488d54aaea7d.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── fc800c6d9c6aac568df8a66ad391bfa8bce43a56.nq.gz
│   └── fe713e8d276df6cb9e234f4b29a64a31a1b09602.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 3df0e0ec2ab4ea48c9a0c31011271656fb57e191.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 30 files
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

[adamchainz/django-auto-prefetch](https://github.com/adamchainz/django-auto-prefetch)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
