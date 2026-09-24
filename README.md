# terraform-github-starter

A production-ready reference starter repository provisioned, configured, and governed declaratively via Terraform and the GitHub Provider.

---

## Project Overview

`terraform-github-starter` serves as a reference implementation demonstrating Infrastructure as Code (IaC) principles applied to GitHub repository management. It illustrates how organizations can automate repository initialization, branch protection rules, automated workflows, and metadata management rather than manually configuring settings through the web UI.

---

## Features

- **Declarative Repository Management**: Fully codified configuration defining visibility, features (issues, wiki, projects), and licensing.
- **Automated CI/CD Baseline**: Preconfigured GitHub Actions workflow (`.github/workflows/demo.yml`) executing sanity checks, environment introspection, and validation on `push` and `pull_request`.
- **Branch Protection Rules**: Codified policies enforcing code reviews and continuous integration checks prior to merging.
- **Reproducible Governance**: Enables consistent auditability, peer review, and rollback capabilities for infrastructure configurations.

---

## Prerequisites

- **Git**: Installed and configured locally.
- **GitHub Account**: With access to view and contribute to the repository.
- **Terraform** *(Optional)*: Required only if re-running or modifying the upstream IaC module that governs this repository.

---

## Usage

### Working with this Repository

1. **Clone the repository**:
   ```bash
   git clone https://github.com/AntonioHellin/my-awesome-terraform-repo.git
   cd my-awesome-terraform-repo
   ```

2. **Branch and Create Changes**:
   ```bash
   git checkout -b feature/my-enhancement
   # make edits
   git add .
   git commit -m "feat: add enhancement"
   git push origin feature/my-enhancement
   ```

3. **Continuous Integration**:
   - Pushing triggers the automated GitHub Actions workflow defined in `.github/workflows/demo.yml`.
   - The workflow validates branch integrity and reports status checks directly to pull requests.

---

## CI/CD Automation

The integrated workflow performs automated verification:
- Checks out the repository codebase (`actions/checkout@v4`).
- Introspects runner environment and Git metadata.
- Validates repository file structure.
- Runs validation checks for IaC definitions when Terraform manifests are present.

---
