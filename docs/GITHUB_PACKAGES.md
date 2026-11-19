# FRACTURE GitHub Package

FRACTURE publishes its container image to GitHub Container Registry (GHCR).
The package is created automatically by `.github/workflows/docker-publish.yml`
on the first successful push to `main` or a version tag.

## Package coordinates

```text
ghcr.io/annatchijova/fracture
```

The workflow publishes `latest`, the short commit SHA, and semantic-version
tags. It also publishes SBOM and build-provenance attestations.

## Pull the package

```bash
docker pull ghcr.io/annatchijova/fracture:latest
```

For a private package, authenticate with a GitHub token that has
`read:packages`:

```bash
echo "$CR_PAT" | docker login ghcr.io -u annatchijova --password-stdin
```

The package and repository are licensed under Apache-2.0. The Python import
namespace and `VIGIA_*` environment variables remain unchanged for backwards
compatibility with existing forensic cases and integrations.
