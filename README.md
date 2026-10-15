# Repolex Knowledge Graph of astropy/astropy-sphinx-theme

RDF knowledge graph data for [astropy/astropy-sphinx-theme](https://github.com/astropy/astropy-sphinx-theme), parsed by [repolex](https://repolex.ai).

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
rlex download astropy/astropy-sphinx-theme
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── f845236c2c0f572dd3c5e22d44b91e686e7e3fc7
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── f845236c2c0f572dd3c5e22d44b91e686e7e3fc7
│           └── chunk-001.nq.gz
├── blob
│   ├── 023471a09d1f0a3e6872c224908fdd22622f3130.nq.gz
│   ├── 042069ca827231ff5f4e2aabb41c4f76facc23de.nq.gz
│   ├── 07687f2c4bc0cf8d331028dee9344c2047485830.nq.gz
│   ├── 0e46157f452ada653a287dbb8ffb1491c59138a9.nq.gz
│   ├── 16d5af74063464af10044808430b468abe9ff374.nq.gz
│   ├── 1d7e1014308affbd1447879d5e22f45d486d7efa.nq.gz
│   ├── 1fd21b116ed5453996d12b6eb0b905b53b71b588.nq.gz
│   ├── 1feb68fec1d5773f53e376074b3390cc0fa800e1.nq.gz
│   ├── 240f05c1b5e34be3cbf250325b5eb7c2546d8fcf.nq.gz
│   ├── 249fa96f7807c9bf3063f628739bdbeb984f4552.nq.gz
│   ├── 269c06aaaa2315683af253737aee4bf8f5315f5f.nq.gz
│   ├── 2a527f1ee138340fc90bb5b6c94fb9d11ceff0b6.nq.gz
│   ├── 2c20c087d14b58241b96210da9bc891b4b170f66.nq.gz
│   ├── 32bb24529f92346af26219baed295b7488b77534.nq.gz
│   ├── 3bbcee0a0f1d50ba74fd21e0b4a8451909a9e0fc.nq.gz
│   ├── 432267972c8fd559ad75cf869713e3dea797a684.nq.gz
│   ├── 483249635a40df5efb7e2dd6341bc3474a994ba9.nq.gz
│   ├── 50cf1b5c7806bc9ce2a836d94cf16dcffdc47871.nq.gz
│   ├── 6e51851d60f5db8d9eb7bf850e1429707e91cfa9.nq.gz
│   ├── 77f6f916a5b2f4e609043d410ff19c2677ad8e3d.nq.gz
│   ├── 7b52bf4baedc8d0e443fd432f20fa0ca17031e1f.nq.gz
│   ├── 7c2dc3e288c030c19bfa67e41313eb619693b0c4.nq.gz
│   ├── 8a7ba3f548688f21828cc5ec6e8ff225b6c4bde7.nq.gz
│   ├── 8bfa2f99a80d774be9221157c54e0e060329e160.nq.gz
│   ├── 93a9b2589eb52cde7c051fafb35a30de0badf73a.nq.gz
│   ├── 96208de90b530483a751bfe4c4f04836275784f6.nq.gz
│   ├── 970e5dc0fe263c2b33703eecbd0a49baf6ae1e83.nq.gz
│   ├── bae7abeabee48ba964ca89c579e530ef1db349fc.nq.gz
│   ├── c116b1d10e60cf6944c9b20737d696011ee955da.nq.gz
│   ├── d4bb2cbb9eddb1bb1b4f366623044af8e4830919.nq.gz
│   ├── d4f388d7f6ecf04ba21ef83f6f297c0d7844d740.nq.gz
│   ├── de327aedb5856cac2cbd22ae4203366d25ce4565.nq.gz
│   ├── dfd87d659738f952782d88c80b54aa438c609a86.nq.gz
│   ├── e17451ba4abf353a4181e9a417e2344b56406571.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ecbe4fc6cdd5bfffef57691bfa6029fd6d323b40.nq.gz
│   ├── fc3d93099fdfc3bfb09fb4cb9e26610a918fd874.nq.gz
│   └── fda389575008c7098235a34786e0719828d55b3c.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── f845236c2c0f572dd3c5e22d44b91e686e7e3fc7.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 46 files
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

[astropy/astropy-sphinx-theme](https://github.com/astropy/astropy-sphinx-theme)

---
*Parsed on 2026-10-15 by [repolex](https://repolex.ai)*
