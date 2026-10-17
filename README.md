# Repolex Knowledge Graph of colcon/colcon-cmake

RDF knowledge graph data for [colcon/colcon-cmake](https://github.com/colcon/colcon-cmake), parsed by [repolex](https://repolex.ai).

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
rlex download colcon/colcon-cmake
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 5d6bc11dae5d6f682b0e5e80e7c01204eb190833
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 5d6bc11dae5d6f682b0e5e80e7c01204eb190833
│           └── chunk-001.nq.gz
├── blob
│   ├── 0f17157ed42b486a0c57cbffddd97987a4844e6b.nq.gz
│   ├── 17149e5fd978bb9ef9b14c0588fbf89e11849fb0.nq.gz
│   ├── 29218bb61067fbf0789c2765bac4dbd508025501.nq.gz
│   ├── 326bb66d4c74f0cf8cf0dfc4e79909001f37da84.nq.gz
│   ├── 35b5fb48ded55429150b5b394d5586175b4eb936.nq.gz
│   ├── 44a7dd9b021bc7ce59b8f0df6ca127f29fbd7d9f.nq.gz
│   ├── 4c327534f25b1eb628b538613ee103367c0858ee.nq.gz
│   ├── 525ecf3a5d758cd9c2f3f755e83123ee48a6fd13.nq.gz
│   ├── 8d315d51e4f6e4f533a08823b5cc3627e9540cc2.nq.gz
│   ├── a73146d8657bb64bf1da2f0d29e7ee9f00795377.nq.gz
│   ├── ab41f6cbf0bed9385943eb839f21f2b97babf2ee.nq.gz
│   ├── ad0f038681e3c14817d5cbe2c6fa35122f1003c1.nq.gz
│   ├── af28b5dab5fb24eac7d1324fe6a68f6e3ffa7e0c.nq.gz
│   ├── b696fc29c32de9877d704233d12b4b48131d5765.nq.gz
│   ├── b7745614eac47ea349fdfc5adcf8a1054ecc3f70.nq.gz
│   ├── bd2000034b389a93bfec514c1417c90df7609ac2.nq.gz
│   ├── bfdf996b3cef52d3e7962e1af1def2acd51d4317.nq.gz
│   ├── d645695673349e3947e8e5ae42332d0ac3164cd7.nq.gz
│   ├── da5b1b1e04efbb5dfe165c252e98de7e6898cf83.nq.gz
│   ├── dffe460f162da9929178a7ce342532e7ba896425.nq.gz
│   ├── e0e14a181ce34418a10cc295a082b77c5fa326ac.nq.gz
│   ├── e572b6df11022020717675a6e75a47b893cb86e8.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e82fd0b0abbf1472480d19d468efe7819276e80d.nq.gz
│   ├── ecc6ef42bf9ca246b47b6d9d2e36cb3d4e0cda2a.nq.gz
│   ├── ee8f8e126025ed5fdd4cf0d525e1eaf4ea0661ac.nq.gz
│   ├── f2452fab90d884f8ad7e6321a2333e7b27099a7f.nq.gz
│   ├── f3e78dd24d91a593a45f6835fe7f9c71bf0953b5.nq.gz
│   ├── f83cfa6fc5e508bc73337a9bf1c7e4e040c2d7b6.nq.gz
│   └── ff937326068e0c7ede76b9ee385d496bd791818b.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 5d6bc11dae5d6f682b0e5e80e7c01204eb190833.nq.gz
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

[colcon/colcon-cmake](https://github.com/colcon/colcon-cmake)

---
*Parsed on 2026-10-17 by [repolex](https://repolex.ai)*
