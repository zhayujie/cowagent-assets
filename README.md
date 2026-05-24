# CowAgent Assets

Centralized media assets (screenshots, GIFs, diagrams, logos) for the [CowAgent](https://github.com/zhayujie/CowAgent) project.

This repository is published separately from the main codebase to keep the main repo lightweight and to provide stable, CDN-friendly URLs for documentation in multiple languages.

## Directory Structure

```
.
├── screenshots/              # Static screenshots
│   ├── zh/                   # Chinese UI screenshots
│   └── en/                   # English UI screenshots
├── gifs/                     # Animated demos
│   ├── zh/
│   └── en/
├── architecture/             # Architecture & flow diagrams
│   ├── zh/
│   └── en/
└── logo/                     # Logos (language-agnostic)
```

## Naming Convention

- Localized assets share the **same filename** across `zh/` and `en/` directories. This way the same Markdown structure can be reused in `README.md` (Chinese) and `docs/en/README.md` (English) by only swapping the language segment in the path.
- Use lowercase, kebab-case filenames: `web-console.png`, `quick-start.gif`.
- For versioned assets, append a date or semver suffix: `architecture-v2.png`.

## How to Reference

### From Markdown (recommended via jsDelivr CDN)

```markdown
![Web Console](https://cdn.jsdelivr.net/gh/zhayujie/cowagent-assets@main/screenshots/zh/web-console.png)
```

### Or via GitHub Raw

```markdown
![Web Console](https://raw.githubusercontent.com/zhayujie/cowagent-assets/main/screenshots/zh/web-console.png)
```

### Cache Invalidation

jsDelivr caches files for ~12 hours. To force refresh:

- Append a version query: `...png?v=2`
- Pin to a commit hash instead of branch: `@a1b2c3d`
- Or call the purge endpoint: `https://purge.jsdelivr.net/gh/zhayujie/cowagent-assets@main/...`

## Asset Guidelines

- **Screenshots**: PNG, ideally `<= 1MB`. Use 2x retina if possible.
- **GIFs**: keep `<= 5MB`. For longer demos prefer MP4 or WebM.
- **Diagrams**: provide both PNG and source (SVG / Excalidraw / Mermaid) when feasible.
- **Logos**: include both raster (PNG) and vector (SVG) versions.

## License

All assets are released under the [MIT License](./LICENSE) unless noted otherwise.
