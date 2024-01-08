<p align="center">
  <h1 style="font-size:80px; font-weight: 800;" align="center">SAP Data Integration using DBT, Dagster, and DuckDB</h1>
  <p align="center">Using a Minimal Stack of Open Source Tools for Extracting SAP Data</a> </p>
</p>

<br>

This repository is based on [datadex](https://github.com/davidgasquez/datadex).


### 🚀 What can you do with this stack?

This stack shows up on how to extract and transform data from a SAP system.


Open source, serverless, and local-first Data Platform to collaborate on Open Data! Built on top of [Dagster](https://dagster.io/), [dbt](https://www.getdbt.com/), [Quarto](https://quarto.org/), [DuckDB](https://www.duckdb.org/), and [ERPL](https://www.erpl.io/).


### 💡 Principles

- **Open**: Code, standards, infrastructure, and data, are public and open source.
- **Modular and Interoperable**: Each component can be replaced, extended, or removed. Works well in many environments (your laptop, in a cluster, or from the browser), can be deployed to many places (S3 + GH Pages, IPFS, ...), and integrates with multiple tools (thanks to the Arrow ecosystem). [Use open tool, standards, infrastructure, and share data in accesible formats](https://voltrondata.com/codex/a-new-frontier).
- **Data as Code**. Declarative stateless transformations tracked in `git`. Version your data as code! Publish and share your reusable models for others to build on top.
- **Glue**: Be a bridge between tools and approaches. E.g.: Use software engineering good practices like types, tests materialized views, and more.



## ⚙️ Setup

This repo consists of several components and requires some setup to get started.

### 🐳 Docker / Dev Containers

The fastest way to start is via [VSCode Remote Containers](https://code.visualstudio.com/docs/remote/containers). Once inside the development environment, you'll only need to run `make dev` to spin up the [Dagster UI locally](http://127.0.0.1:3000).

[![](https://github.com/codespaces/badge.svg)](https://codespaces.new/davidgasquez/datadex)

The development environment can also run in your browser thanks to GitHub Codespaces!

You can also build the [Dockerfile](Dockerfile) image locally and run it with:

```bash
docker build -t datadex .
docker run -it -v $(pwd):/workspaces/datadex -p 3000:3000 datadex
```

### 🐍 Python Virtual Environment

Clone the repository and run the following commands from the root folder:

```bash
# Create a virtual environment
python3 -m venv .venv

# On Linux
source .venv/bin/activate

# On Windows
.venv/bin/activate

# Install the package and dependencies
pip install -e .[dev]
```

Now, you should be able to spin up Dagster UI and [access it locally](http://127.0.0.1:3000).

## 🎯 Motivation

Link to Datadex.

## 👏 Acknowledgements

- This proof of concept was created thanks to open source projects like [DuckDB](https://www.duckdb.org/), [dbt](https://getdbt.com), [Dagster](https://dagster.io/), [Quarto](https://quarto.org/), and [ERPL](https://erpl.io/).
