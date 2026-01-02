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
├── package.json            # npm 패키지 정의
├── astro.config.mjs        # Astro 설정
├── tsconfig.json           # TypeScript 설정
├── public/
│   └── favicon.svg         # 파비콘
├── src/
│   ├── components/
│   │   ├── Header.astro    # 헤더 네비게이션
│   │   ├── Footer.astro    # 푸터
│   │   └── CodeBlock.astro # BMB 코드 블록
│   ├── layouts/
│   │   ├── Base.astro      # 기본 레이아웃
│   │   └── Docs.astro      # 문서 레이아웃
│   ├── pages/
│   │   ├── index.astro     # 랜딩 페이지
│   │   ├── download.astro  # 다운로드 페이지
│   │   ├── changes.astro   # 변경로그
│   │   ├── docs/           # 문서 페이지
│   │   │   └── index.astro
│   │   └── blog/           # 블로그
│   │       └── index.astro
│   └── styles/
│       └── global.css      # 전역 스타일
├── content/
│   ├── docs/               # 마크다운 문서 (추후)
│   └── blog/               # 블로그 포스트 (추후)
└── README.md
```

## Tech Stack

- **Framework**: [Astro](https://astro.build/) 4.x - Static site generator
- **Styling**: Custom CSS (variables, responsive design)
- **Icons**: SVG inline icons
- **Hosting**: GitHub Pages / Cloudflare Pages (planned)

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
- Timeline visualization
- Migration guides between versions

### Blog (/blog)
- Development updates
- Technical deep-dives
- Community highlights

## Deployment

```bash
# Build and deploy to GitHub Pages
npm run build
# Upload dist/ to hosting

# Or use GitHub Actions (recommended)
# See .github/workflows/deploy.yml (planned)
```

## Roadmap

| Version | Features | Status |
|---------|----------|--------|
| v0.1 | Landing page, basic docs structure | ✅ |
| v0.2 | Full documentation, download page | 계획 |
| v0.3 | Blog, changelog, search | 계획 |
| v0.4 | Playground integration, i18n | 계획 |
| v1.0 | Complete site with all features | 계획 |

## Contributing

1. Fork the repository
2. Create content in `content/` directory
3. Follow the style guide
4. Submit a PR

## License

MIT License
