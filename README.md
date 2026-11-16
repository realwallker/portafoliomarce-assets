# portafoliomarce-assets

Public media repository for Marcelo Ramírez's portfolio (`realwallker/portafoliomarce`). It holds photos, videos, logos and CV PDFs only, no application code. The site references every file by URL through jsDelivr, so the site repo stays light and media never counts against Vercel bandwidth or image optimization quota.

## URL pattern

```
https://cdn.jsdelivr.net/gh/realwallker/portafoliomarce-assets@<tag>/<path>
```

Publish a new tag (`v1`, `v2`, ...) on every change and point the site to it (`NEXT_PUBLIC_ASSETS_URL` or the default in `lib/assets.ts`). Tagged URLs are immutable, so jsDelivr can cache them for good. Files over 20 MB are not served by jsDelivr.

## Layout

```
hero/                 reel 16:9 and 9:16, with WebP posters
yo/                   portrait and action photos
marcas/               client logos (SVG, one color)
trabajo/<caso>/       screenshots, clips and ads per case study
cv/                   CV PDFs in Spanish and English
```

The full list of expected files, with sizes and briefs, lives in `docs/ASSETS.md` in the site repo, generated from `content/assets.ts`.
