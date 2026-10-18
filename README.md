# Repolex Knowledge Graph of rapidfuzz/Levenshtein

RDF knowledge graph data for [rapidfuzz/Levenshtein](https://github.com/rapidfuzz/Levenshtein), parsed by [repolex](https://repolex.ai).

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
rlex download rapidfuzz/Levenshtein
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 83575b7b25e51fab746249a95b5104309ae51db1
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 83575b7b25e51fab746249a95b5104309ae51db1
│           └── chunk-001.nq.gz
├── blob
│   ├── 0209ee8976cb0abb531e773c0e3134551f127949.nq.gz
│   ├── 067dfb6025e9e478e99626647db64710196831c0.nq.gz
│   ├── 08ebcbfd947f59c18d31552fab3db05598c2b8ea.nq.gz
│   ├── 1c02ef8c337854383cca87ddfc42e9f6f2139639.nq.gz
│   ├── 23153a11f07847466c5f2f2a64950cf9fb34932d.nq.gz
│   ├── 286d9b7c9cbb8fc51d27d0dd409b4e8c03564621.nq.gz
│   ├── 2a1d4bd69723b5b814031a999fef2275ec496711.nq.gz
│   ├── 3794ee856df47b95f6f40d81c09ddb5ce4a1bdd9.nq.gz
│   ├── 3b942f31a2d01b07f262f3d2554ed0b7b22e299b.nq.gz
│   ├── 540c24bdd0f4ad28dba0c4ff82cb153c15abff66.nq.gz
│   ├── 5ad4a63b0a0f37d201d15b610818a4c843765eab.nq.gz
│   ├── 5ee3b91778162a753868820198729e36e046857e.nq.gz
│   ├── 6ef3f7218fb1a6fa02bccc5f79c5547c96e02737.nq.gz
│   ├── 771bbc957fc0ee6dd29992fa21149de8aa879f8c.nq.gz
│   ├── 8b51e2709c32bbc7867a111b0fe3b495094f3781.nq.gz
│   ├── 90987ad9db3d61b562d1773b89e5291a627fc673.nq.gz
│   ├── 9c56a1be3e2bd19bb2875e05dd3ed85d16fe72a2.nq.gz
│   ├── 9e15a04308dd0fa97508a17b86d6f4fb59542d6d.nq.gz
│   ├── 9ed9e3236af0b6fb0eb457957346b19a232f9375.nq.gz
│   ├── 9f8b427a5e6f1cff20f9dfa92d6a16de5e8c0110.nq.gz
│   ├── be006de9a1ae3b9628e796c74277cd6d61e0a34a.nq.gz
│   ├── c197d6cca597f197c790e2d04abd9268f4e65c00.nq.gz
│   ├── c1e582d2f6e990c4fecaa366b0b50664e9b19580.nq.gz
│   ├── c7e7deea87daeac5a3b272e41f3f884796cb03ff.nq.gz
│   ├── ce9d47589ea831024f5efb4664536faff1d19b00.nq.gz
│   ├── cfa9f8ac234957c1d5b3220e3bb4e3b0b82c669a.nq.gz
│   ├── d26b4c21379f41757deca689fc1577c8c5f6509b.nq.gz
│   ├── df8f2c201acabe953b6799b8aa0dbf11327cf8ca.nq.gz
│   ├── e121a7d3380abda6a9154e8e19a03c4a974b67ab.nq.gz
│   ├── e2256fd680c9e4e9484d90dc96d44bcb2d5ce912.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f6e960d01dd04925049748e039f61b5a2c09463a.nq.gz
│   ├── f715a04fa1e338760bad1facf7bac23ee2f07ed7.nq.gz
│   ├── f79fafc494802f7a9e26c2527f99445517f33f83.nq.gz
│   ├── f7ac383808651ab2cdae8fc5a61fd4580a2e641d.nq.gz
│   ├── f7fa66b347389cbb163726fb66310aad1a8d8be9.nq.gz
│   ├── f95ea66f222efe8b2a3e7b1601b29d45f9667653.nq.gz
│   ├── fdebfd864dc6cf3d99ef293cd35ff0f4ca439495.nq.gz
│   └── ffaf2b0e62bc571e45699d72a445a5c9af1cdde6.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 83575b7b25e51fab746249a95b5104309ae51db1.nq.gz
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

[rapidfuzz/Levenshtein](https://github.com/rapidfuzz/Levenshtein)

---
*Parsed on 2026-10-18 by [repolex](https://repolex.ai)*
