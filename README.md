# BMB Language Website

> Official website for BMB programming language - bmb-lang.org

BMB 프로그래밍 언어 공식 웹사이트.

## Features

- **Landing Page**: 언어 소개 및 핵심 기능 하이라이트
- **Documentation**: 언어 레퍼런스, 튜토리얼, API 문서
- **Download**: 설치 가이드 및 바이너리 다운로드
- **Changelog**: 버전별 변경사항 및 릴리즈 노트
- **Playground**: 온라인 에디터 (playground 서브모듈 임베드)
- **Blog**: 개발 소식 및 기술 블로그

## Directory Structure

```
lang-bmb-site/
├── README.md
├── package.json
├── astro.config.mjs        # Astro 설정
├── src/
│   ├── pages/
│   │   ├── index.astro     # Landing page
│   │   ├── docs/           # Documentation
│   │   │   ├── getting-started.md
│   │   │   ├── language-reference/
│   │   │   ├── contracts/
│   │   │   └── stdlib/
│   │   ├── download.astro  # Download page
│   │   ├── changes.astro   # Changelog
│   │   └── blog/           # Blog posts
│   ├── components/
│   │   ├── Header.astro
│   │   ├── Footer.astro
│   │   ├── CodeBlock.astro # BMB syntax highlighting
│   │   └── Playground.astro
│   ├── layouts/
│   │   ├── Base.astro
│   │   └── Docs.astro
│   └── styles/
│       └── global.css
├── public/
│   ├── favicon.ico
│   ├── logo.svg
│   └── downloads/          # Binary releases
└── content/
    ├── docs/               # Markdown documentation
    └── blog/               # Blog posts
```

## Tech Stack

- **Framework**: [Astro](https://astro.build/) - Static site generator
- **Styling**: Tailwind CSS
- **Code Highlighting**: Shiki with BMB grammar
- **Search**: Pagefind (static search)
- **Hosting**: GitHub Pages / Cloudflare Pages

## Development

```bash
# Install dependencies
npm install

# Start dev server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

## Pages

### Landing Page (/)
- Hero section with BMB introduction
- Feature highlights (contracts, performance, AI-native)
- Quick start code example
- Call to action (download, docs, playground)

### Documentation (/docs)
- Getting Started guide
- Language Reference
- Contract System (pre/post/invariant)
- Standard Library
- Tooling (gotgan, bmb CLI)

### Download (/download)
- Installation methods:
  - `curl -sSf https://bmb-lang.org/install.sh | sh`
  - Pre-built binaries (Windows, macOS, Linux)
  - Build from source
- Version selector
- System requirements

### Changelog (/changes)
- Version history with release notes
- Migration guides between versions
- Breaking changes highlighted

### Blog (/blog)
- Development updates
- Technical deep-dives
- Community highlights

## Content Management

Documentation is written in Markdown with frontmatter:

```markdown
---
title: "Getting Started"
description: "Install BMB and write your first program"
section: "docs"
order: 1
---

# Getting Started

Install BMB using the installer script:

\`\`\`bash
curl -sSf https://bmb-lang.org/install.sh | sh
\`\`\`
```

## Deployment

```bash
# Build and deploy to GitHub Pages
npm run build
npm run deploy

# Or use GitHub Actions (recommended)
# See .github/workflows/deploy.yml
```

## Roadmap

| Version | Features |
|---------|----------|
| v0.1 | Landing page, basic docs structure |
| v0.2 | Full documentation, download page |
| v0.3 | Blog, changelog, search |
| v0.4 | Playground integration, i18n |
| v1.0 | Complete site with all features |

## Contributing

1. Fork the repository
2. Create content in `content/` directory
3. Follow the style guide
4. Submit a PR

## License

MIT License
