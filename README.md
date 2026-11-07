# Repolex Knowledge Graph of sunpy/sunpy-dashboard

RDF knowledge graph data for [sunpy/sunpy-dashboard](https://github.com/sunpy/sunpy-dashboard), parsed by [repolex](https://repolex.ai).

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
rlex download sunpy/sunpy-dashboard
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 589a2e5a9383363b4520799d78cf6476557feea6
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 589a2e5a9383363b4520799d78cf6476557feea6
│           └── chunk-001.nq.gz
├── blob
│   ├── 08ee7af6657a94577361d12135214cb300cf7437.nq.gz
│   ├── 15ddb1d859f05458691363a7c944e59fc31966b6.nq.gz
│   ├── 1e8f8474ae53e146347354acc57fc981f600bd77.nq.gz
│   ├── 24ee5b1be9961e38a503c8e764b7385dbb6ba124.nq.gz
│   ├── 2de678147d341dae0819c9b14179f0c17798c489.nq.gz
│   ├── 3f6d7b518bde215c9fb8335e17a3947ff3e83102.nq.gz
│   ├── 432693ed156cbc71c3f5102c988fd928028aaa9b.nq.gz
│   ├── 4a78a2d1a3379fd65aad9b355e6fb66e1b58c8c6.nq.gz
│   ├── 57fdb5cd280b8f36c9015bab555353366f68421a.nq.gz
│   ├── 69421ad2802fd89580a4e85c47af2d15ddca3923.nq.gz
│   ├── 82e0072a1f130f57c334ad7086d232d6274465fd.nq.gz
│   ├── 88229803931abb407bfd935a7a4b9cab2318e39f.nq.gz
│   ├── 925f357c99e9957055ba71ede220b30adca9f323.nq.gz
│   ├── 9c27956b1022b5b693f231ff686401ad71b4c470.nq.gz
│   ├── b0ac43b9a7996ff6776985a5a999589df70d2bf2.nq.gz
│   ├── bec19cc8d89f132de785b917cea7bf80f2a9d685.nq.gz
│   ├── bedce3020e239cdb777bf065366c525b25838f7b.nq.gz
│   ├── c553dcd8689c1cb6cb53d8d5c3ec63993f551e02.nq.gz
│   ├── dcc2a23dbd99056942ec97df4288647fdbb87105.nq.gz
│   ├── de04e2f361fc2b03aab9fa6908ad9edb54093a04.nq.gz
│   ├── e44116efc27fb16532baaf5147eac27ce4db3b23.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── f116f872d5b4d46d6ec71f052b0bd6406238d0ea.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 589a2e5a9383363b4520799d78cf6476557feea6.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 31 files
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

[sunpy/sunpy-dashboard](https://github.com/sunpy/sunpy-dashboard)

---
*Parsed on 2026-11-07 by [repolex](https://repolex.ai)*
