# Repolex Knowledge Graph of xarray-contrib/xarray_leaflet

RDF knowledge graph data for [xarray-contrib/xarray_leaflet](https://github.com/xarray-contrib/xarray_leaflet), parsed by [repolex](https://repolex.ai).

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
rlex download xarray-contrib/xarray_leaflet
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── e3f9c5d5690e65c5617abbcf2f83000394102da6
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── e3f9c5d5690e65c5617abbcf2f83000394102da6
│           └── chunk-001.nq.gz
├── blob
│   ├── 06c0b416974612489787073776dcd59f1c60d360.nq.gz
│   ├── 0ca10ea1883e9ad6f500c9fe43de6cac06d7e3a0.nq.gz
│   ├── 0ded5324e99547d6d3f563f9e7a5572bf903dfec.nq.gz
│   ├── 133bed06c25daa19cb274decebc5329d7664063b.nq.gz
│   ├── 18b037433d952ca12f277a1e6b86b4747a6c05a7.nq.gz
│   ├── 1d7f1f1d11da32e32ad14817acd2fadbb67d761b.nq.gz
│   ├── 234f2bc8cdd1452734acb0f336247b6758f2d00c.nq.gz
│   ├── 250649964bbc36f4bec2942f69238aa6f7c02c1a.nq.gz
│   ├── 292d6dd96d5e94746582980e10b38599cf6ba644.nq.gz
│   ├── 3ac3335f282c893d8e306d8503e2ed553e719b3c.nq.gz
│   ├── 400726b268fe8134afafff254773c3c8970a2bb3.nq.gz
│   ├── 482cefbfd629aefc709286dc2626581ce402915f.nq.gz
│   ├── 4c574dec6686321bdb984ae143625a5aefccf4ff.nq.gz
│   ├── 4e886df27f1f305b4a34e6e82f328853bea0bc1a.nq.gz
│   ├── 50d945a598a5caf9acb518b1ee97663e716df3a4.nq.gz
│   ├── 5407d897d2ad16f941e7925651488ad67532d345.nq.gz
│   ├── 549141524dc0ed428a6c004f5e675bfebcb97c98.nq.gz
│   ├── 69ad686a736a23bf5c5cafcd62ccc9730aca7f65.nq.gz
│   ├── 6c216fd15a54070166a659a7e85e756403359ad3.nq.gz
│   ├── 729053e4d57ca4d5e83b02df437436f872573dd2.nq.gz
│   ├── 76de9fe87525c3fcdb1a5bf9b1bd6b71a029214b.nq.gz
│   ├── 76ed25437d76e6befe10083c866dcac98035b3b0.nq.gz
│   ├── 7a2da43bd91aca4d8e3280e428628ca0f2e07e2a.nq.gz
│   ├── 7d77e94bc3e49722252a9ee3f50b624b9cc3630f.nq.gz
│   ├── 88c31391dde1f1e6f36953760997fa45eaa3b5c0.nq.gz
│   ├── 8af2c642071233bf3d48de842ee61a58fa4efa50.nq.gz
│   ├── 8e5c7eb5621c78305277ae2e9d20cd39109e86a2.nq.gz
│   ├── 937d835dc574deff3729db6c476e896f79411299.nq.gz
│   ├── 974e6ba435f217595dfd73bb1fb1fa7a5ff773f3.nq.gz
│   ├── a17a5d219ce63341bc385b3e1c182af5ddb2bcc0.nq.gz
│   ├── a369a00c2cf7c02df1928ba698238685e61e0a60.nq.gz
│   ├── a64b77c35369308879d6b02c6af08f92430c6be8.nq.gz
│   ├── b26f034d3df458b1b6d46692dd3fb4bf78c4dda7.nq.gz
│   ├── b3dab64e10f78b53ae1195a16f998ba709386fad.nq.gz
│   ├── bacb93775018bbb252848edab3b2dcdb3de512d4.nq.gz
│   ├── cf2b5cbb68eec9878ade38f707947b1b83371ad2.nq.gz
│   ├── d37ae08bfb8f6f60fe97161cc1556ec8764771cb.nq.gz
│   ├── e582053ea018c369be05aae96cf730744f1dc616.nq.gz
│   ├── e8c144fd4f2a2fe218194b15bb667cca4a8e4ddd.nq.gz
│   └── f0313c36dbefdaf7755647ed7beabb0104809a89.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── e3f9c5d5690e65c5617abbcf2f83000394102da6.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 48 files
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

[xarray-contrib/xarray_leaflet](https://github.com/xarray-contrib/xarray_leaflet)

---
*Parsed on 2026-10-28 by [repolex](https://repolex.ai)*
