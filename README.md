# Repolex Knowledge Graph of pytest-dev/pytest-libfaketime

RDF knowledge graph data for [pytest-dev/pytest-libfaketime](https://github.com/pytest-dev/pytest-libfaketime), parsed by [repolex](https://repolex.ai).

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
rlex download pytest-dev/pytest-libfaketime
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 364e1ce7a4350d63a70e678723818bba56c01c2d
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 364e1ce7a4350d63a70e678723818bba56c01c2d
│           └── chunk-001.nq.gz
├── blob
│   ├── 10465d5605a8a338c4e16291ed923f77c2f9636e.nq.gz
│   ├── 174110f75d4a58d1229c586a024e77df83583f80.nq.gz
│   ├── 378c7fd13fdd5bea51a168d491b9b0708c680bfa.nq.gz
│   ├── 451676ebf216bc77fb40982a897ec1b6c8fda5d6.nq.gz
│   ├── 5492f2c9c2fc8bc6bab478d932ac5dba528b7175.nq.gz
│   ├── 6f525b65ebaddbf5530dbd925ebd0752e6685d3f.nq.gz
│   ├── 768968db548da53f2b7f38268157ca8f512295f8.nq.gz
│   ├── acc033f9dedc341d0db71fc6b2dedda7d5d54495.nq.gz
│   ├── bfaf81929acd723a55a436a2c59a94082dd80bc8.nq.gz
│   ├── cb1b8653bf96fccba9ac6c03221066d781451484.nq.gz
│   └── cf70ba9868c9bf3b216dc6380ad8e606c6740a9e.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 364e1ce7a4350d63a70e678723818bba56c01c2d.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 19 files
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

[pytest-dev/pytest-libfaketime](https://github.com/pytest-dev/pytest-libfaketime)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
