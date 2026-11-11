# KAREST Solar — GitHub Pages Cutover Receipt

Status: **STAGING_GREEN / PAGES_ENABLE_PENDING / DOMAIN_CUTOVER_PENDING**

- Repository: `saeedfaai/karest-solar`
- Source branch: `main`
- Custom domain declaration: `solar.karest.net`
- Planned DNS target after Pages domain registration: `saeedfaai.github.io`
- Current production route: Liara (`mont-blanc.liara.cloud`) — intentionally unchanged for rollback.
- Search indexing: blocked until final production QA (`noindex,nofollow` + `robots.txt Disallow: /`).
- Renderer: self-contained; `index.html` references local `cards/` assets.
- Manifest: `2026-11-11-github-pages-cutover-v1`, 7/7 canonical card URLs.
- Integrity: all seven SVG files were read back from GitHub and matched the WebsitePublisher source content exactly.

## Source version hashes → Git blob SHAs

- KS-P-009: 463cdd1c → de0f1469be8d3a71a744c521346cf14f6c5d3b10
- KS-P-010: 1cbcd97d → bb9bd396cc9d49bf4357a6f59b1aba73731b9285
- KS-P-011: 780d88a1 → 492bfcd65db724570705c535d794f6c9e2517385
- KS-P-012: 3ac17b39 → e6f0289648faa10539ce6bed78f8646f40b38004
- KS-P-013: 0bf99467 → 06c692acbfb0c0aaae7769f7630c6f82a53c408c
- KS-P-014: 45e1587d → 4eb1a41e27c6cc411b92778622de73efbb3d4c2d
- KS-P-015: 56dd317b → 0f9692ccc1dce12225995874a839e5150f5c1406

## Cutover order

1. Enable GitHub Pages from `main / root`.
2. Register `solar.karest.net` as the Pages custom domain.
3. Only then replace the DNS record for host `solar` from Liara to `saeedfaai.github.io`.
4. Verify DNS, HTTPS, homepage, manifest and all 7 SVG files.
5. Keep Liara rollback path until acceptance is green.
6. Remove noindex/robots block only after final production acceptance.
