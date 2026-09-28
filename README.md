# Repolex Knowledge Graph of asimov-modules/asimov-llamacpp-module

RDF knowledge graph data for [asimov-modules/asimov-llamacpp-module](https://github.com/asimov-modules/asimov-llamacpp-module), parsed by [repolex](https://repolex.ai).

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
rlex download asimov-modules/asimov-llamacpp-module
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 6ab4f84f4913522d0aa6f57aed65f8bfade32402
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 6ab4f84f4913522d0aa6f57aed65f8bfade32402.nq.gz
│   └── repolex
│       └── 6ab4f84f4913522d0aa6f57aed65f8bfade32402
│           └── chunk-001.nq.gz
├── blob
│   ├── 0798fe0cc54f7a6513ad9ae414eb13f298b1a95e.nq.gz
│   ├── 0a133b211e4481da0e2a1f4276e8c9fce5e47c97.nq.gz
│   ├── 10b359dd05935c73efb064470f9ecda90f6d28aa.nq.gz
│   ├── 2033bc892e684ab02d14a203ff050daa30705357.nq.gz
│   ├── 3f04af4d9752741d49f5b5a7bf869bbdd8542702.nq.gz
│   ├── 4e379d2bfeab6461d0455bf5bbb8792845d9bbea.nq.gz
│   ├── 6b23d61018f43b840f8d2ff3b45a1c02d76df38d.nq.gz
│   ├── 6e88b5d3f5c4f24b5ce17c4b8f464e3afe764e72.nq.gz
│   ├── 75e3b65f99b29f48ab230e3eab3de8d0b7a9229f.nq.gz
│   ├── 9fe50de16e59d550235aa6d7d15ee12ddf054414.nq.gz
│   ├── a36fedab8db68b26a76fbbf1de1f549e4a12261b.nq.gz
│   ├── af9908b08f4b33c32a0080af73f53bc0fa0cdce4.nq.gz
│   ├── afe1aa39243fcdc86627f359e2af2aa916db86e9.nq.gz
│   ├── c62e98898a0acb61ad9a9ef97e8ef539cdc86851.nq.gz
│   ├── cf42f6893594e2f8be2b722de51123d65e4d61c4.nq.gz
│   ├── e3e57a8ce4ccbf74759a6df8fa4a3980ff1c9209.nq.gz
│   ├── e721f12824356c9def6c2d3a498e26aa4fc00d64.nq.gz
│   └── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 6ab4f84f4913522d0aa6f57aed65f8bfade32402.nq.gz
├── filetree
│   └── 6ab4f84f4913522d0aa6f57aed65f8bfade32402.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 28 files
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

[asimov-modules/asimov-llamacpp-module](https://github.com/asimov-modules/asimov-llamacpp-module)

---
*Parsed on 2026-09-28 by [repolex](https://repolex.ai)*
