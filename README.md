# github-actions

A collection of GitHub Action workflows to extend from.

- `browserslist-regex`: creates a useragent regular expression matching [browserslist](https://github.com/browserslist) targets
- `ci-optimization`: optimizes CI by analyzing pull requests
- `dargstack-rgen`: validates the README of a [dargstack](https://github.com/dargstack) project
- `deploy-cloudflare-pages`: deploys a build artifact to [Cloudflare pages](https://pages.cloudflare.com/)
- `docker`: builds a Docker project and, for public repositories on GitHub, signs the pushed image's build provenance (verifiable with `gh attestation verify oci://<image> --owner <owner> --signer-repo dargmuesli/github-actions`), optionally uploading artifacts, requiring the `attestations: write`, `id-token: write` and `packages: write` permissions
- `ghcr-cleanup`: deletes all but the newest untagged images from the GitHub Container Registry, keeping images a tag still references, requiring the calling repository to have the Admin role under the package's "Manage Actions access" settings, and best scheduled at least weekly so its manifest cache stays warm
- `lock_file-maintenance`: maintains lock files for package managers
- `release-schedule`: pushes a release commit if no other commits have been pushed for a week
- `release-semantic`: run a [semantic release](https://github.com/semantic-release)
