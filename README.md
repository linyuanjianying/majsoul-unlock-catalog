# Public Unlock Catalog

This repository serves the versioned unlock catalog consumed by the private Android module. The data is public numeric catalog metadata; it contains no account allowlist, signing key, or application source.

Runtime endpoints:

- `https://raw.githubusercontent.com/linyuanjianying/majsoul-unlock-catalog/main/catalog/manifest.json`
- `https://raw.githubusercontent.com/linyuanjianying/majsoul-unlock-catalog/main/catalog/unlock-data.json`

The daily GitHub Actions workflow checks the public source `Avenshy/MajsoulMax` at `config/max_data.yaml` (UTC 04:17 / Beijing 12:17). It validates the fixed catalog sections and numeric IDs, updates the version and SHA-256 only when content changes, and commits only the two catalog JSON files. No secrets are required.
