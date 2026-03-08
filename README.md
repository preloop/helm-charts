# Preloop Helm Charts

Helm chart repository for [Preloop](https://github.com/preloop/preloop).

## Usage

[Helm](https://helm.sh) must be installed. Add the repo:

```bash
helm repo add preloop https://charts.preloop.ai
helm repo update
```

Install Preloop:

```bash
helm install preloop preloop/preloop
```

To pin a specific version:

```bash
helm install preloop preloop/preloop --version 0.8.0-beta.3
```

## Custom Domain

This repository is served via GitHub Pages. To use `https://charts.preloop.ai`:

1. In **Settings → Pages**: Deploy from branch `main`, root.
2. Set **Custom domain** to `charts.preloop.ai`.
3. Add a CNAME record: `charts.preloop.ai` → `preloop.github.io`.

## Automation

The index is updated automatically when [preloop/preloop](https://github.com/preloop/preloop) creates a release. The preloop release workflow triggers this repo via `repository_dispatch`. Ensure `CHARTS_REPO_TOKEN` (a PAT with `repo` scope) is set in the preloop repo secrets.
