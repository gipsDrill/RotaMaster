# RotaMaster / RotaGlance web hosting

Live app: https://gipsdrill.github.io/RotaMaster/

This public repository contains only compiled browser files in .deploy/ and the GitHub Pages deployment workflow. The application source, native iOS/Android projects, and source history remain in the private RotaGlance-app repository. No source maps or server credentials are included in the web bundle.

Pages source: GitHub Actions. The workflow validates the SHA-256 digest before publishing the static client.

To update, build the private project using npm run build:pages, package pages-dist as a ZIP, split its Base64 encoding into .deploy/site-*.b64, and update EXPECTED_SHA256 in .github/workflows/pages.yml in the same commit. Push to main triggers deployment.

Repaired 8 November 2026 from RotaGlance 1.0.10, build 11.
