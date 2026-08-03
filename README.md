# Awesome Scrapers [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

[![Stars](https://img.shields.io/github/actions/workflow/status/edwardtay/awesome-scrapers/update-stars.yml?label=star%20updates)](https://github.com/edwardtay/awesome-scrapers/actions/workflows/update-stars.yml)
[![Links](https://img.shields.io/github/actions/workflow/status/edwardtay/awesome-scrapers/links.yml?label=links)](https://github.com/edwardtay/awesome-scrapers/actions/workflows/links.yml)
[![Last Commit](https://img.shields.io/github/last-commit/edwardtay/awesome-scrapers)](https://github.com/edwardtay/awesome-scrapers/commits/main)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/edwardtay/awesome-scrapers/pulls)
[![License: CC0](https://img.shields.io/badge/License-CC0-lightgrey.svg)](LICENSE)

> A curated list of scrapers, crawlers, browser automation tools, extraction libraries, and managed services.

> ⚠️ = known maintenance concern; verify repository status before adoption.

## How to Choose

| I need to... | Start here |
|---|---|
| Extract data with AI / natural language | [AI-Powered Scraping](#-ai-powered-scraping) |
| Bypass Cloudflare / bot detection | [Stealth & Anti-Detection](#-stealth--anti-detection) |
| Give my LLM agent web access | [MCP Servers](#-mcp-servers-model-context-protocol) |
| Scrape JavaScript-heavy sites | [Browser Automation](#-browser-automation) |
| Build a production crawler | [Web Scraping Frameworks](#️-web-scraping-frameworks) |
| Parse HTML / extract text | [HTML & XML Parsing](#-html--xml-parsing) or [Content Extraction](#-content--text-extraction) |
| Download videos / images | [Media Downloaders](#-media-downloaders) |
| Extract tables from PDFs | [Document & PDF Extraction](#-document--pdf-extraction) |
| Read text from images | [OCR & Screen Scraping](#️-ocr--screen-scraping) |
| Just pay someone to handle it | [Managed Scraping APIs](#️-managed-scraping-apis) |

---

## 🤖 AI-Powered Scraping

LLMs understand page structure, extract via natural language, and output LLM-ready formats.

| Tool | Stars | Language | Description |
|------|-------|----------|-------------|
| [Firecrawl](https://github.com/firecrawl/firecrawl) | 160k | TypeScript | Websites → LLM-ready markdown or structured data via API. |
| [browser-use](https://github.com/browser-use/browser-use) | 108k | Python | AI agents that control a browser to complete tasks autonomously. |
| [Crawl4AI](https://github.com/unclecode/crawl4ai) | 76k | Python | LLM-friendly web crawler with structured extraction. |
| [Docling](https://github.com/docling-project/docling) | 64k | Python | IBM — parse PDFs, DOCX into AI-ready output. |
| [ScrapeGraphAI](https://github.com/ScrapeGraphAI/Scrapegraph-ai) | 29k | Python | Graph pipelines + LLMs to extract data via plain English. |
| [Stagehand](https://github.com/browserbase/stagehand) | 24k | TypeScript | Browser automation combining natural language with code precision. |
| [Skyvern](https://github.com/Skyvern-AI/skyvern) | 23k | Python | Browser workflows with computer vision + LLMs, no selectors needed. |
| [Jina Reader](https://github.com/jina-ai/reader) | 12k | TypeScript | Any URL → LLM-friendly markdown with vision model support. |
| [llm-scraper](https://github.com/mishushakov/llm-scraper) | 7k | TypeScript | Structured data from any webpage using LLMs with Zod schemas. |
| [Spider](https://github.com/spider-rs/spider) | 3k | Rust | Async, configurable web crawler with streaming and browser support. |

<p align="right">(<a href="#readme">⬆ back to top</a>)</p>

## 🥷 Stealth & Anti-Detection

The cat-and-mouse game of modern scraping.

| Tool | Stars | Language | Description |
|------|-------|----------|-------------|
| [Scrapling](https://github.com/D4Vinci/Scrapling) | 72k | Python | Adaptive scraping with built-in anti-detection and auto-matching. |
| [SeleniumBase](https://github.com/seleniumbase/SeleniumBase) | 13k | Python | Browser automation with UC (Undetected Chrome) mode. |
| [Camoufox](https://github.com/daijro/camoufox) | 11k | Python | Firefox-based browser automation project with fingerprint-management features. |
| [curl_cffi](https://github.com/lexiforest/curl_cffi) | 6k | Python | HTTP client with browser TLS/JA3/HTTP2 fingerprint impersonation. |
| [Nodriver](https://github.com/ultrafunkamsterdam/nodriver) | 5k | Python | Successor to undetected-chromedriver — direct CDP, no WebDriver. |
| [Botasaurus](https://github.com/omkarcloud/botasaurus) | 6k | Python | Scraping framework with anti-detection, parallelism, and caching. |
| [Patchright](https://github.com/Kaliiiiiiiiii-Vinyzu/patchright) | 4k | JavaScript | Undetected Playwright fork that passes bot detection. |

<p align="right">(<a href="#readme">⬆ back to top</a>)</p>

## 🔌 MCP Servers (Model Context Protocol)

Connect LLM agents (Claude, GPT, etc.) directly to scraping tools.

| Server | Stars | Description |
|--------|-------|-------------|
| [Playwright MCP](https://github.com/microsoft/playwright-mcp) | 36k | Browser automation via accessibility snapshots (by Microsoft). |
| [Firecrawl MCP](https://github.com/firecrawl/firecrawl-mcp-server) | 7k | Web scraping and search in Claude/Cursor via Firecrawl API. |
| [Browserbase MCP](https://github.com/browserbase/mcp-server-browserbase) | 3k | Cloud browser control with Stagehand AI. |
| [Bright Data MCP](https://github.com/brightdata/brightdata-mcp) | 3k | Web access with geo-unblocking and bot evasion. |

<p align="right">(<a href="#readme">⬆ back to top</a>)</p>

## 🌐 Browser Automation

The foundation for dynamic/JS-heavy scraping.

| Tool | Stars | Language | Description |
|------|-------|----------|-------------|
| [Puppeteer](https://github.com/puppeteer/puppeteer) | 95k | JavaScript | Google's Chrome/Firefox control via DevTools Protocol. |
| [Playwright](https://github.com/microsoft/playwright) | 94k | Multi | Cross-browser automation (Chromium, Firefox, WebKit) by Microsoft. |
| [Selenium](https://github.com/SeleniumHQ/selenium) | 34k | Multi | The OG browser automation (W3C WebDriver standard). |
| [Crawlee](https://github.com/apify/crawlee) | 25k | TypeScript | Scraping/automation library with proxy rotation by Apify. |

<p align="right">(<a href="#readme">⬆ back to top</a>)</p>

## 🕷️ Web Scraping Frameworks

### Python

| Tool | Stars | Description |
|------|-------|-------------|
| [Scrapy](https://github.com/scrapy/scrapy) | 64k | Python scraping framework — middleware, pipelines, extensions. |
| [MechanicalSoup](https://github.com/MechanicalSoup/MechanicalSoup) | 5k | Stateful browser-like interaction for simple scraping. |
| [scrapy-playwright](https://github.com/scrapy-plugins/scrapy-playwright) | 1k | Playwright integration for Scrapy — JS rendering with full pipeline. |

### Go

| Tool | Stars | Description |
|------|-------|-------------|
| [Colly](https://github.com/gocolly/colly) | 25k | Fast scraping framework for Go. |
| [Katana](https://github.com/projectdiscovery/katana) | 17k | Crawling and spidering framework by ProjectDiscovery. |
| [Ferret](https://github.com/MontFerret/ferret) | 6k | Declarative scraping with FQL query language. |

### Ruby

| Tool | Stars | Description |
|------|-------|-------------|
| [Nokogiri](https://github.com/sparklemotion/nokogiri) | 6k | Standard HTML/XML parser for Ruby. |

<p align="right">(<a href="#readme">⬆ back to top</a>)</p>

## 📡 HTTP Clients

The network layer — making requests that look human.

| Tool | Stars | Language | Description |
|------|-------|----------|-------------|
| [aiohttp](https://github.com/aio-libs/aiohttp) | 17k | Python | Async HTTP client/server for high-concurrency scraping. |
| [httpx](https://github.com/encode/httpx) | 15k | Python | Async/sync HTTP client with HTTP/2 support. |
| [curl_cffi](https://github.com/lexiforest/curl_cffi) | 6k | Python | HTTP client impersonating browser TLS fingerprints (also in Stealth). |
| [got-scraping](https://github.com/apify/got-scraping) | 766 | Node.js | HTTP client with header/TLS mimicry by Apify. |

<p align="right">(<a href="#readme">⬆ back to top</a>)</p>

## 🧩 HTML & XML Parsing

| Tool | Stars | Language | Description |
|------|-------|----------|-------------|
| [Cheerio](https://github.com/cheeriojs/cheerio) | 30k | JavaScript | jQuery-like HTML manipulation for Node.js. |
| [goquery](https://github.com/PuerkitoBio/goquery) | 15k | Go | jQuery-like HTML selector for Go. |
| [jsoup](https://github.com/jhy/jsoup) | 11k | Java | HTML parser with CSS selectors and XSS sanitization. |
| [AngleSharp](https://github.com/AngleSharp/AngleSharp) | 6k | C# | W3C-compliant HTML5 parser for .NET. |
| [Beautiful Soup](https://pypi.org/project/beautifulsoup4/) | - | Python | Most popular Python HTML/XML parser. |
| [lxml](https://github.com/lxml/lxml) | 3k | Python | Fast XML/HTML parser with XPath and XSLT. |
| [html5ever](https://github.com/servo/html5ever) | 3k | Rust | Browser-grade HTML5 parser from Mozilla Servo. |
| [selectolax](https://github.com/rushter/selectolax) | 2k | Python | 5-30x faster than Beautiful Soup using Lexbor engine. |
| [parsel](https://github.com/scrapy/parsel) | 1k | Python | CSS/XPath selectors for HTML+JSON (powers Scrapy). |

<p align="right">(<a href="#readme">⬆ back to top</a>)</p>

## 📝 Content & Text Extraction

Pull clean text out of messy HTML — essential for LLM/RAG pipelines.

| Tool | Stars | Language | Description |
|------|-------|----------|-------------|
| [Readability.js](https://github.com/mozilla/readability) | 11k | JavaScript | Mozilla's article extractor (powers Firefox Reader View). |
| [Trafilatura](https://github.com/adbar/trafilatura) | 6k | Python | Web text extraction with metadata and language detection. |
| [html2text](https://github.com/Alir3z4/html2text) | 2k | Python | HTML → clean Markdown. |
| [Markdownify](https://github.com/matthewwithanm/python-markdownify) | 2k | Python | Flexible HTML-to-Markdown with customizable options. |
| [newspaper4k](https://github.com/AndyTheFactory/newspaper4k) | 1k | Python | News article extraction with NLP and multilingual support. |

<p align="right">(<a href="#readme">⬆ back to top</a>)</p>

## 📱 Social Media Scrapers

> Platforms frequently change APIs and block scrapers. Check issue trackers for current status.

| Tool | Stars | Platform | Description |
|------|-------|----------|-------------|
| [Instaloader](https://github.com/instaloader/instaloader) | 13k | Instagram | Posts, stories, reels, highlights with metadata. |
| [TikTok-Api](https://github.com/davidteather/TikTok-Api) | 7k | TikTok | Unofficial API wrapper for Python. |
| [PRAW](https://github.com/praw-dev/praw) | 4k | Reddit | Official Python Reddit API Wrapper. |

<p align="right">(<a href="#readme">⬆ back to top</a>)</p>

## 🎬 Media Downloaders

| Tool | Stars | Description |
|------|-------|-------------|
| [yt-dlp](https://github.com/yt-dlp/yt-dlp) | 182k | YouTube and 1000+ sites (fork of youtube-dl). |
| [lux](https://github.com/iawia002/lux) | 32k | Go video downloader — 40+ sites (formerly annie). |
| [spotdl](https://github.com/spotDL/spotify-downloader) | 26k | Spotify tracks/playlists with metadata and album art. |
| [gallery-dl](https://github.com/mikf/gallery-dl) | 19k | Image galleries from 100+ sites (Pixiv, Twitter, Reddit). |

<p align="right">(<a href="#readme">⬆ back to top</a>)</p>

## 📄 Document & PDF Extraction

| Tool | Stars | Language | Description |
|------|-------|----------|-------------|
| [Docling](https://github.com/docling-project/docling) | 64k | Python | IBM — PDFs, DOCX, PPTX into AI-ready output. |
| [Unstructured](https://github.com/Unstructured-IO/unstructured) | 15k | Python | ETL pipeline for documents → structured data for LLMs. |
| [pdfplumber](https://github.com/jsvine/pdfplumber) | 11k | Python | Text, tables, and layout from PDFs with precision. |
| [PyMuPDF](https://github.com/pymupdf/PyMuPDF) | 10k | Python | Fast PDF/XPS/EPUB extraction and rendering. |
| [Tabula](https://github.com/tabulapdf/tabula) | 7k | Java | Data tables from PDFs. ⚠️ |
| [pdfminer.six](https://github.com/pdfminer/pdfminer.six) | 7k | Python | PDF text extraction with layout analysis. |
| [Camelot](https://github.com/camelot-dev/camelot) | 4k | Python | PDF table extraction — lattice and stream modes. |
| [tabula-py](https://github.com/chezou/tabula-py) | 2k | Python | Python wrapper for Tabula. ⚠️ |

<p align="right">(<a href="#readme">⬆ back to top</a>)</p>

## 👁️ OCR & Screen Scraping

| Tool | Stars | Language | Description |
|------|-------|----------|-------------|
| [Tesseract](https://github.com/tesseract-ocr/tesseract) | 76k | C++ | Google's OCR engine — 100+ languages. |
| [PaddleOCR](https://github.com/PaddlePaddle/PaddleOCR) | 87k | Python | Lightweight OCR — 100+ languages with LLM integration. |
| [EasyOCR](https://github.com/JaidedAI/EasyOCR) | 30k | Python | Ready-to-use OCR — 80+ languages, PyTorch. |
| [pytesseract](https://github.com/madmaze/pytesseract) | 6k | Python | Python wrapper for Tesseract. |

<p align="right">(<a href="#readme">⬆ back to top</a>)</p>

## ⛓️ Blockchain & On-Chain

| Tool | Type | Description |
|------|------|-------------|
| [The Graph](https://github.com/graphprotocol/graph-node) | Open Source (3k) | Blockchain indexing via GraphQL subgraphs. |
| [Subsquid](https://github.com/subsquid) | Open Source | Blockchain indexer — 50k+ blocks/sec. |
| [Dune Analytics](https://dune.com/) | SaaS | SQL-based blockchain analytics. |
| [Etherscan APIs](https://etherscan.io/apis) | Freemium API | REST APIs for Ethereum data. |

<p align="right">(<a href="#readme">⬆ back to top</a>)</p>

## ☁️ Managed Scraping APIs

Pay-per-request services that handle proxies, browsers, and anti-bot for you.

| Service | Best For | Key Feature |
|---------|----------|-------------|
| [Apify](https://apify.com/) | Full-stack platform | Marketplace of pre-built Actors plus Crawlee-based development and managed execution. |
| [ScrapingBee](https://www.scrapingbee.com?fpr=edward77) | Simple API access | JavaScript rendering, screenshots, and search APIs. |
| [ZenRows](https://www.zenrows.com/) | Anti-bot bypass | Managed scraping API with browser rendering and proxy rotation. |
| [ScrapFly](https://scrapfly.io/) | Multi-API | Scraping, screenshots, extraction, and crawler APIs. |
| [Browserless](https://www.browserless.io/) | Headless browsers | Headless Chrome in Docker, BrowserQL, self-hostable. |
| [Browserbase](https://www.browserbase.com/) | AI browser agents | Cloud browsers for AI, session persistence, Stagehand integration. |
| [Oxylabs](https://oxylabs.io/products/scraper-api) | Enterprise | ML-driven proxy rotation, e-commerce specialized. |
| [Bright Data](https://brightdata.com/products/web-unlocker) | Scale | Web Unlocker with CAPTCHA solving, geo-routing, mobile UA. |
| [SerpApi](https://serpapi.com/) | SERP data | Structured results from Google, Bing, Yahoo. |
| [ScraperAPI](https://www.scraperapi.com/?fp_ref=edward66) | Getting started | Proxy rotation, browser rendering, and structured scraping endpoints. |

<p align="right">(<a href="#readme">⬆ back to top</a>)</p>

## 🧪 CAPTCHA Solving

| Service | Method | Pricing | Supports |
|---------|--------|---------------|----------|
| [2Captcha](https://2captcha.com/auth/register/?from=27588755) | Human workers | Usage-based; see current pricing | reCAPTCHA, Turnstile, FunCaptcha, GeeTest, image. |
| [Anti-Captcha](https://anti-captcha.com/) | Human workers | Usage-based; see current pricing | reCAPTCHA, hCaptcha, FunCaptcha, Turnstile. |
| [CapSolver](https://www.capsolver.com/) | Automated solving | Usage-based; see current pricing | reCAPTCHA, AWS WAF, Cloudflare, GeeTest. |
| [CapMonster Cloud](https://capmonster.cloud/) | Automated solving | Usage-based; see current pricing | reCAPTCHA, hCaptcha, and Turnstile. |

<p align="right">(<a href="#readme">⬆ back to top</a>)</p>

## 🌍 Proxy Providers

| Provider | Coverage | Pricing | Highlights |
|----------|-------------|---------------|------------|
| [Bright Data](https://brightdata.com/) | Residential, ISP, mobile, and datacenter proxies | Pay-as-you-go | Broad proxy and web-data product portfolio with geographic targeting. |
| [Oxylabs](https://oxylabs.io/) | Residential, ISP, mobile, and datacenter proxies | Contact sales | Enterprise proxy services with country, city, and ZIP targeting options. |
| [Decodo](https://decodo.com/) | Residential, ISP, mobile, and datacenter proxies | Published plans | Geographic targeting and rotating or sticky sessions. |
| [IPRoyal](https://iproyal.com/) | Residential, ISP, mobile, and datacenter proxies | Published plans | Proxy services with geographic targeting and pay-as-you-go options. |
| [NetNut](https://netnut.io?ref=mzjimtc) | Residential, ISP, mobile, and datacenter proxies | Contact sales | ISP-sourced proxy connectivity and geographic targeting. |
| [Webshare](https://www.webshare.io/?referral_code=petnjy3bdxeh) | Residential and datacenter proxies | Published plans | Self-service proxy plans and a limited free tier. |

<p align="right">(<a href="#readme">⬆ back to top</a>)</p>

## 🆓 Try Free

| Service | Free Tier | Try It |
|---------|-----------|--------|
| [ScraperAPI](https://www.scraperapi.com/?fp_ref=edward66) | Trial credits; check current terms | [Start free →](https://www.scraperapi.com/?fp_ref=edward66) |
| [ScrapingBee](https://www.scrapingbee.com?fpr=edward77) | Trial credits; check current terms | [Start free →](https://www.scrapingbee.com?fpr=edward77) |
| [Webshare](https://www.webshare.io/?referral_code=petnjy3bdxeh) | Limited free tier; check current terms | [Start free →](https://www.webshare.io/?referral_code=petnjy3bdxeh) |
| [2Captcha](https://2captcha.com/auth/register/?from=27588755) | Promotional terms vary | [View offer →](https://2captcha.com/auth/register/?from=27588755) |
| [NetNut](https://netnut.io?ref=mzjimtc) | Trial availability varies | [Request trial →](https://netnut.io?ref=mzjimtc) |

<p align="right">(<a href="#readme">⬆ back to top</a>)</p>

## 🪦 Deprecated Tools Graveyard

| Dead Tool | Why | Use Instead |
|-----------|-----|-------------|
| PhantomJS | Archived 2018 | Playwright, Puppeteer. |
| CasperJS | Depended on PhantomJS | Playwright, Puppeteer. |
| Nightmare | Unmaintained since 2020 | Playwright. |
| Zombie.js | Unmaintained | Playwright, Puppeteer. |
| SlimerJS | Unmaintained, Gecko-based | Playwright (Firefox). |
| Splash | Scrapinghub, deprecated | Scrapy-Playwright. |
| twint | Archived Mar 2023, blocked by Twitter | Official API. |
| Goutte (PHP) | Deprecated by Symfony | Symfony BrowserKit + DomCrawler. |
| snscrape | Unmaintained since Nov 2023 | Official APIs. |
| undetected-chromedriver | Aging, last push Jul 2025 | Nodriver, Camoufox. |
| puppeteer-extra-stealth | Unmaintained since Jul 2024 | Patchright, Camoufox. |
| playwright-stealth | Unmaintained since Nov 2023 | Patchright, Camoufox. |
| curl-impersonate | Unmaintained since Jul 2024 | curl_cffi. |
| GoogleScraper | Unmaintained since Jul 2021 | SerpApi. |
| pyautogui | Unmaintained since Aug 2024 | pytesseract + Playwright. |
| SikuliX | Stale, niche | Playwright, pytesseract. |

<p align="right">(<a href="#readme">⬆ back to top</a>)</p>

---

## Disclosure

Some links in the Managed Scraping APIs, CAPTCHA Solving, Proxy Providers, and Try Free sections are affiliate/referral links. These help support the maintenance of this list. All tools are included based on merit — affiliate status does not influence placement or rankings.

<p align="right">(<a href="#readme">⬆ back to top</a>)</p>

## 🔗 Related Awesome Lists

| List | Description |
|------|-------------|
| [awesome-ai](https://github.com/edwardtay/awesome-ai) | AI APIs, tools, frameworks, platforms, and learning resources. |
| [awesome-robotics](https://github.com/edwardtay/awesome-robotics) | Robotics frameworks, simulators, and platforms. |
| [awesome-web3-ai](https://github.com/edwardtay/awesome-web3-ai) | Web3 x AI tools, agent frameworks, and protocols. |

## Contributing

Contributions welcome! Please read the [contribution guidelines](CONTRIBUTING.md) first.

- Add tools you've actually used or evaluated
- Include star count and language where applicable
- Note if a tool is unmaintained (last commit >1 year ago)
- Commercial tools/services are fine but must be clearly labeled


To the extent possible under law, [Edward Tay](https://github.com/edwardtay) has waived all copyright and related or neighboring rights to this work.
