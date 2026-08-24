# soothe-assets

Runtime assets for the [Soothe Vault](https://github.com/trustsoothe/vault) browser extension, served from GitHub Pages:

- `networks.json` / `assets.json` — network and asset lists the extension refreshes every ~20 minutes (`NETWORKS_CDN_URL` / `ASSETS_CDN_URL`)
- `pokt-chains-map.json` / `pokt-testnet-chains-map.json` — chain id → label maps for stake transactions
- `chains-images/` — chain icons (also referenced by `iconUrl` inside the JSON files)

Base URL: `https://pokt-network.github.io/soothe-assets/`

Changing a file on `main` publishes it (GitHub Pages deploys the branch); installed extensions pick the change up within ~20 minutes — no extension release needed. Treat edits like code: PRs + review. History note: these files previously lived in the `soothe-vault` DigitalOcean Space; the initial commit is a faithful snapshot of it (plus the reviewed networks.json changes: Pocket Beta enabled, Morse shutdown notice, explorer URL and Arbitrum Sepolia fixes).

`networks-candidates.json` / `assets-candidates.json` are the **staging** variants: the extension's `stage` CI builds point at them, so config changes can be tried on a stage build before editing the production files. `networks-with-local.json`, `delegators.json`, `providers.json` and `pocket-beta/` are kept for reference (some still reference the separate `poktscan-v1` Space, left as-is).
