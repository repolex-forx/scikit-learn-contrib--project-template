# Repolex Knowledge Graph of scikit-learn-contrib/project-template

RDF knowledge graph data for [scikit-learn-contrib/project-template](https://github.com/scikit-learn-contrib/project-template), parsed by [repolex](https://repolex.ai).

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
rlex download scikit-learn-contrib/project-template
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── fc9f82eb6b998bde744ef736d4e101a9610ad5fb
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── fc9f82eb6b998bde744ef736d4e101a9610ad5fb
│           └── chunk-001.nq.gz
├── blob
│   ├── 108342c8e02d9f8e32259fee6c04a8620b6a1095.nq.gz
│   ├── 1194fb718337c1d13666216a2cf816fb145b63bd.nq.gz
│   ├── 2c66c59490d6799179f143a4dc375ea221aba4fc.nq.gz
│   ├── 2d36622cb7e55bf87691be85e6cebfebd71b0272.nq.gz
│   ├── 30f57660a9f9fe488a8c9068eb3d9419d73e2eec.nq.gz
│   ├── 31f5c2ca507d4d352ba70d189e99cdeed3f05cef.nq.gz
│   ├── 325367769a7f99b562ab53b4dd254c31804f2695.nq.gz
│   ├── 353eb50ba089f33a17469d76d147e839e16e53aa.nq.gz
│   ├── 3d70980454c4c2348210b9a3d1927c1be8921a38.nq.gz
│   ├── 3f63ced6afa859dab2b3d5aab20c321e0f5269ca.nq.gz
│   ├── 4249e7f4e778f45eec50c6bf60cd8b8449b936ca.nq.gz
│   ├── 42639062f371a33d018720eaaf22b8fe8e740ec9.nq.gz
│   ├── 4cd9068e9207a01a621b70897cb522601e12093d.nq.gz
│   ├── 4eeaed178394b28c345b5e0c3c017a3b2d7d0c00.nq.gz
│   ├── 508376e44f20332a0a471b40ddf8c2484a99b015.nq.gz
│   ├── 527d4c63dd8dbb422b8778709aa45383dddda41d.nq.gz
│   ├── 52e3f96493791e4da205dfc6647b73c7b3a8564d.nq.gz
│   ├── 62a25f24c8aa31528e499a3af5a2b1c1f82e90bf.nq.gz
│   ├── 62b416bb4c7d96ca4a302aaf7949d76604ddaccc.nq.gz
│   ├── 64c11dbe233dabb980a4f3cd7f36633296b600b5.nq.gz
│   ├── 66806e5df3fc36ceb0cff30bc830224592e2b0c8.nq.gz
│   ├── 69e8d8aada54f3b232a1b3d7071f12c98c6b94f7.nq.gz
│   ├── 69f7ba1d2d114598b32a93552ac9bb89b3173d6d.nq.gz
│   ├── 6a1d992fabb5522cfcedb1f6cd13ae52310e8fae.nq.gz
│   ├── 7806f2a6b2c4db05788fd9ccccaa767007354be7.nq.gz
│   ├── 79c1e1984b87bc0b5c10ae5cba2cc1a94a1051c3.nq.gz
│   ├── a78c02919eca15aebba32a063843acbba9e7754b.nq.gz
│   ├── ab473da983909623f626cfb086ae7df9fab04a7d.nq.gz
│   ├── af3d586d53db170bb85860a0fac335c6d9a000a7.nq.gz
│   ├── b3340cd2605b36a6888c4a97f04e729060706e33.nq.gz
│   ├── b624f09d3cbaa842eda04ab3c019571adab57101.nq.gz
│   ├── bd170535170a3b40235482d895678e5d939e32f9.nq.gz
│   ├── bd926a25606815085b2b25f37589f6057aed00a2.nq.gz
│   ├── c09fd11f048a580bb076539023e46ca69cc76eb4.nq.gz
│   ├── d87f56998175b91b21e7ee53ea806064fe0f78e1.nq.gz
│   ├── db4cdfabc155f420d86a0254069fb68ef385e874.nq.gz
│   ├── de3d902379383c8f30e4aafc91e9a8d933ae80b0.nq.gz
│   ├── e39c114455287d57e87c0078a67c619d1d5b3b3e.nq.gz
│   └── eff12835b9aa913f8bda57c2b3dc1c69926cd770.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── fc9f82eb6b998bde744ef736d4e101a9610ad5fb.nq.gz
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

[scikit-learn-contrib/project-template](https://github.com/scikit-learn-contrib/project-template)

---
*Parsed on 2026-10-28 by [repolex](https://repolex.ai)*
