# Repolex Knowledge Graph of ibis-project/realtime-fraud-detection

RDF knowledge graph data for [ibis-project/realtime-fraud-detection](https://github.com/ibis-project/realtime-fraud-detection), parsed by [repolex](https://repolex.ai).

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
rlex download ibis-project/realtime-fraud-detection
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── f5ea8ea15093df60f6adccf274338feea8a02c43
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── f5ea8ea15093df60f6adccf274338feea8a02c43
│           └── chunk-001.nq.gz
├── blob
│   ├── 194533e847b8582c92c85c7d2762543448789b3f.nq.gz
│   ├── 52bd32e9d61a4f475ce415c7303456aa35b22984.nq.gz
│   ├── 57b9533997559cdeed0041f8daedeb756304578a.nq.gz
│   ├── 91e583167d4509c10bb5afae2954f9709a164ff4.nq.gz
│   ├── 9f343fa6ae3b93a713a93a39ecb49908caaad03b.nq.gz
│   ├── bc35feacbda7a4e1f9bcebc86c7a59ff43324f96.nq.gz
│   ├── be4100db077bdc90b1393cec8d9bbbb748db4ea7.nq.gz
│   ├── d51182dc16ea58bf66bcbe7f85e167b128d21617.nq.gz
│   ├── e04ea4221bf96717266a0e98232553cd47a166c9.nq.gz
│   └── e9c3dc9bfa0e08f4f9e473533a7eb4d340017fab.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── f5ea8ea15093df60f6adccf274338feea8a02c43.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 16 files
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

[ibis-project/realtime-fraud-detection](https://github.com/ibis-project/realtime-fraud-detection)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
