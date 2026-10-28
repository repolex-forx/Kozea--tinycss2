# Repolex Knowledge Graph of Kozea/tinycss2

RDF knowledge graph data for [Kozea/tinycss2](https://github.com/Kozea/tinycss2), parsed by [repolex](https://repolex.ai).

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
rlex download Kozea/tinycss2
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 2cab2705158e2b9131e0e8537b8c62b4fb5619f5
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 2cab2705158e2b9131e0e8537b8c62b4fb5619f5
│           └── chunk-001.nq.gz
├── blob
│   ├── 032b924a5d7d122373585f523f856766db0bd6f7.nq.gz
│   ├── 0c2a4fba5fb86dcb54a97f85691db56d251cac44.nq.gz
│   ├── 0d2650c2cf226d853857fbe5b28be795b1f468bf.nq.gz
│   ├── 11b97626a1749c03397ad0cde2c00ad5d4eb9e61.nq.gz
│   ├── 147ddba26b2d990189439ddeda26e9af49fc7412.nq.gz
│   ├── 1c0fc0b2de7c17fc0abf715d083cc2eb875bb109.nq.gz
│   ├── 22107ee32262c937b306d5097fd50ec62a10dfa0.nq.gz
│   ├── 2bbbbb634f65e51df735aa89bfde4ff4b30b0536.nq.gz
│   ├── 324955d016deb63505db685fa22b7ac4449e70a7.nq.gz
│   ├── 35e4205b012b0f4bb7cce0f7421889ade3f1c659.nq.gz
│   ├── 391f7b6c18dbc8197361fbf32e855f600d66be65.nq.gz
│   ├── 44c8c9c38b44584fc944b372bde57d2402eca5b4.nq.gz
│   ├── 4d271d988d9ca8a7f7b111e044155644a7b2bf4a.nq.gz
│   ├── 507bf242221d66043daa5c8eee27d3f5db7d1a11.nq.gz
│   ├── 5278c939bdde73ffeda6642badf069162179ccae.nq.gz
│   ├── 57c8893079d52dafb22ea4d17122807cbcdc75c1.nq.gz
│   ├── 62e77dc9a917c57972c786d07a25f2eec4e686b0.nq.gz
│   ├── 66bbd726c9c8c3d897205626282d53ea63d83288.nq.gz
│   ├── 914a7740103b4dcbd32fbe075a7b43c791abba2b.nq.gz
│   ├── 953e671555de586ff230903eb8f15a1578bb33e6.nq.gz
│   ├── 95618dff387d735e97122e36e086980725721807.nq.gz
│   ├── 98fbf7c4f7747912746131a2acc78fcd06469ac1.nq.gz
│   ├── a5063a49e65a74afc1c78aa529cdfefea7ecfbd2.nq.gz
│   ├── b20cffd72317975061f5e5749f3d560057c28650.nq.gz
│   ├── b5804d3be3d53f0b5a83c0d03d290d939762ed2f.nq.gz
│   ├── b9d00667395ad1729badcf30d22e251cc887887e.nq.gz
│   ├── cdddde16b1c2f58c20f544dea8929c25cbf3c5de.nq.gz
│   ├── d1106d665e35b485dbb25b977e98618fa947e36d.nq.gz
│   ├── ef828eb29c8d818aecd5541126e30dd7eb52fb9d.nq.gz
│   └── f4b5452fc6ef437c5de8ba4f1feb29e09b1ea930.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 2cab2705158e2b9131e0e8537b8c62b4fb5619f5.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 38 files
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

[Kozea/tinycss2](https://github.com/Kozea/tinycss2)

---
*Parsed on 2026-10-28 by [repolex](https://repolex.ai)*
