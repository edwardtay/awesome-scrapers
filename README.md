# Awesome Scrapers [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of scrapers, crawlers, and data extraction tools. 150+ tools across 17 categories.

> ⚠️ = aging (6-12 months since last commit) — may still work but watch for staleness.

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
| [Firecrawl](https://github.com/firecrawl/firecrawl) | 87k | TypeScript | Websites → LLM-ready markdown or structured data via API |
| [browser-use](https://github.com/browser-use/browser-use) | 79k | Python | AI agents that control a browser to complete tasks autonomously |
| [Crawl4AI](https://github.com/unclecode/crawl4ai) | 61k | Python | LLM-friendly web crawler with structured extraction |
| [Docling](https://github.com/docling-project/docling) | 54k | Python | IBM — parse PDFs, DOCX into AI-ready output |
| [ScrapeGraphAI](https://github.com/ScrapeGraphAI/Scrapegraph-ai) | 23k | Python | Graph pipelines + LLMs to extract data via plain English |
| [Stagehand](https://github.com/browserbase/stagehand) | 21k | TypeScript | Browser automation combining natural language with code precision |
| [Skyvern](https://github.com/Skyvern-AI/skyvern) | 21k | Python | Browser workflows with computer vision + LLMs, no selectors needed |
| [Jina Reader](https://github.com/jina-ai/reader) | 10k | TypeScript | Any URL → LLM-friendly markdown with vision model support ⚠️ |
| [llm-scraper](https://github.com/mishushakov/llm-scraper) | 6k | TypeScript | Structured data from any webpage using LLMs with Zod schemas |
| [Spider](https://github.com/spider-rs/spider) | 2k | Rust | Async web crawler — 100-1000x faster than Python alternatives |

## 🥷 Stealth & Anti-Detection

The cat-and-mouse game of modern scraping.

| Tool | Stars | Language | Description |
|------|-------|----------|-------------|
| [Scrapling](https://github.com/D4Vinci/Scrapling) | 19k | Python | Adaptive scraping with built-in anti-detection and auto-matching |
| [SeleniumBase](https://github.com/seleniumbase/SeleniumBase) | 12k | Python | Browser automation with UC (Undetected Chrome) mode |
| [Camoufox](https://github.com/daijro/camoufox) | 6k | Python | Firefox fork patched at engine level — 0% bot detection rate |
| [curl_cffi](https://github.com/lexiforest/curl_cffi) | 5k | Python | HTTP client with browser TLS/JA3/HTTP2 fingerprint impersonation |
| [Nodriver](https://github.com/ultrafunkamsterdam/nodriver) | 4k | Python | Successor to undetected-chromedriver — direct CDP, no WebDriver |
| [Botasaurus](https://github.com/omkarcloud/botasaurus) | 4k | Python | Scraping framework with anti-detection, parallelism, and caching |
| [Patchright](https://github.com/Kaliiiiiiiiii-Vinyzu/patchright) | 2k | JavaScript | Undetected Playwright fork that passes bot detection |

## 🔌 MCP Servers (Model Context Protocol)

Connect LLM agents (Claude, GPT, etc.) directly to scraping tools.

| Server | Stars | Description |
|--------|-------|-------------|
| [Playwright MCP](https://github.com/microsoft/playwright-mcp) | 28k | Browser automation via accessibility snapshots (by Microsoft) |
| [Firecrawl MCP](https://github.com/firecrawl/firecrawl-mcp-server) | 6k | Web scraping and search in Claude/Cursor via Firecrawl API |
| [Browserbase MCP](https://github.com/browserbase/mcp-server-browserbase) | 3k | Cloud browser control with Stagehand AI |
| [Bright Data MCP](https://github.com/brightdata/brightdata-mcp) | 2k | Web access with geo-unblocking and bot evasion |

## 🌐 Browser Automation

The foundation for dynamic/JS-heavy scraping.

| Tool | Stars | Language | Description |
|------|-------|----------|-------------|
| [Puppeteer](https://github.com/puppeteer/puppeteer) | 94k | JavaScript | Google's Chrome/Firefox control via DevTools Protocol |
| [Playwright](https://github.com/microsoft/playwright) | 83k | Multi | Cross-browser automation (Chromium, Firefox, WebKit) by Microsoft |
| [Selenium](https://github.com/SeleniumHQ/selenium) | 34k | Multi | The OG browser automation (W3C WebDriver standard) |
| [Crawlee](https://github.com/apify/crawlee) | 22k | TypeScript | Scraping/automation library with proxy rotation by Apify |

## 🕷️ Web Scraping Frameworks

### Python

| Tool | Stars | Description |
|------|-------|-------------|
| [Scrapy](https://github.com/scrapy/scrapy) | 60k | Python scraping framework — middleware, pipelines, extensions |
| [MechanicalSoup](https://github.com/MechanicalSoup/MechanicalSoup) | 5k | Stateful browser-like interaction for simple scraping |
| [scrapy-playwright](https://github.com/scrapy-plugins/scrapy-playwright) | 1k | Playwright integration for Scrapy — JS rendering with full pipeline |

### Go

| Tool | Stars | Description |
|------|-------|-------------|
| [Colly](https://github.com/gocolly/colly) | 25k | Fast scraping framework for Go |
| [Katana](https://github.com/projectdiscovery/katana) | 16k | Crawling and spidering framework by ProjectDiscovery |
| [Ferret](https://github.com/MontFerret/ferret) | 6k | Declarative scraping with FQL query language |

### Ruby

| Tool | Stars | Description |
|------|-------|-------------|
| [Nokogiri](https://github.com/sparklemotion/nokogiri) | 6k | Standard HTML/XML parser for Ruby |

## 📡 HTTP Clients

The network layer — making requests that look human.

| Tool | Stars | Language | Description |
|------|-------|----------|-------------|
| [aiohttp](https://github.com/aio-libs/aiohttp) | 16k | Python | Async HTTP client/server for high-concurrency scraping |
| [httpx](https://github.com/encode/httpx) | 15k | Python | Async/sync HTTP client with HTTP/2 support |
| [curl_cffi](https://github.com/lexiforest/curl_cffi) | 5k | Python | HTTP client impersonating browser TLS fingerprints (also in Stealth) |
| [got-scraping](https://github.com/apify/got-scraping) | 736 | Node.js | HTTP client with header/TLS mimicry by Apify |

## 🧩 HTML & XML Parsing

| Tool | Stars | Language | Description |
|------|-------|----------|-------------|
| [Cheerio](https://github.com/cheeriojs/cheerio) | 30k | JavaScript | jQuery-like HTML manipulation for Node.js |
| [goquery](https://github.com/PuerkitoBio/goquery) | 15k | Go | jQuery-like HTML selector for Go |
| [jsoup](https://github.com/jhy/jsoup) | 11k | Java | HTML parser with CSS selectors and XSS sanitization |
| [AngleSharp](https://github.com/AngleSharp/AngleSharp) | 5k | C# | W3C-compliant HTML5 parser for .NET |
| [Beautiful Soup](https://pypi.org/project/beautifulsoup4/) | - | Python | Most popular Python HTML/XML parser |
| [lxml](https://github.com/lxml/lxml) | 3k | Python | Fast XML/HTML parser with XPath and XSLT |
| [html5ever](https://github.com/servo/html5ever) | 3k | Rust | Browser-grade HTML5 parser from Mozilla Servo |
| [selectolax](https://github.com/rushter/selectolax) | 2k | Python | 5-30x faster than Beautiful Soup using Lexbor engine |
| [parsel](https://github.com/scrapy/parsel) | 1k | Python | CSS/XPath selectors for HTML+JSON (powers Scrapy) |

## 📝 Content & Text Extraction

Pull clean text out of messy HTML — essential for LLM/RAG pipelines.

| Tool | Stars | Language | Description |
|------|-------|----------|-------------|
| [Readability.js](https://github.com/mozilla/readability) | 11k | JavaScript | Mozilla's article extractor (powers Firefox Reader View) |
| [Trafilatura](https://github.com/adbar/trafilatura) | 5k | Python | Web text extraction with metadata and language detection |
| [html2text](https://github.com/Alir3z4/html2text) | 2k | Python | HTML → clean Markdown |
| [Markdownify](https://github.com/matthewwithanm/python-markdownify) | 2k | Python | Flexible HTML-to-Markdown with customizable options |
| [newspaper4k](https://github.com/AndyTheFactory/newspaper4k) | 1k | Python | News article extraction with NLP and multilingual support |

## 📱 Social Media Scrapers

> Platforms frequently change APIs and block scrapers. Check issue trackers for current status.

| Tool | Stars | Platform | Description |
|------|-------|----------|-------------|
| [Instaloader](https://github.com/instaloader/instaloader) | 12k | Instagram | Posts, stories, reels, highlights with metadata |
| [TikTok-Api](https://github.com/davidteather/TikTok-Api) | 6k | TikTok | Unofficial API wrapper for Python |
| [PRAW](https://github.com/praw-dev/praw) | 4k | Reddit | Official Python Reddit API Wrapper |

## 🎬 Media Downloaders

| Tool | Stars | Description |
|------|-------|-------------|
| [yt-dlp](https://github.com/yt-dlp/yt-dlp) | 149k | YouTube and 1000+ sites (fork of youtube-dl) |
| [lux](https://github.com/iawia002/lux) | 31k | Go video downloader — 40+ sites (formerly annie) |
| [spotdl](https://github.com/spotDL/spotify-downloader) | 24k | Spotify tracks/playlists with metadata and album art |
| [gallery-dl](https://github.com/mikf/gallery-dl) | 17k | Image galleries from 100+ sites (Pixiv, Twitter, Reddit) |

## 📄 Document & PDF Extraction

| Tool | Stars | Language | Description |
|------|-------|----------|-------------|
| [Docling](https://github.com/docling-project/docling) | 54k | Python | IBM — PDFs, DOCX, PPTX into AI-ready output |
| [Unstructured](https://github.com/Unstructured-IO/unstructured) | 14k | Python | ETL pipeline for documents → structured data for LLMs |
| [pdfplumber](https://github.com/jsvine/pdfplumber) | 10k | Python | Text, tables, and layout from PDFs with precision |
| [PyMuPDF](https://github.com/pymupdf/PyMuPDF) | 9k | Python | Fast PDF/XPS/EPUB extraction and rendering |
| [Tabula](https://github.com/tabulapdf/tabula) | 7k | Java | Data tables from PDFs ⚠️ |
| [pdfminer.six](https://github.com/pdfminer/pdfminer.six) | 7k | Python | PDF text extraction with layout analysis |
| [Camelot](https://github.com/camelot-dev/camelot) | 4k | Python | PDF table extraction — lattice and stream modes |
| [tabula-py](https://github.com/chezou/tabula-py) | 2k | Python | Python wrapper for Tabula ⚠️ |

## 👁️ OCR & Screen Scraping

| Tool | Stars | Language | Description |
|------|-------|----------|-------------|
| [Tesseract](https://github.com/tesseract-ocr/tesseract) | 73k | C++ | Google's OCR engine — 100+ languages |
| [PaddleOCR](https://github.com/PaddlePaddle/PaddleOCR) | 71k | Python | Lightweight OCR — 100+ languages with LLM integration |
| [EasyOCR](https://github.com/JaidedAI/EasyOCR) | 29k | Python | Ready-to-use OCR — 80+ languages, PyTorch |
| [pytesseract](https://github.com/madmaze/pytesseract) | 6k | Python | Python wrapper for Tesseract |

## ⛓️ Blockchain & On-Chain

| Tool | Type | Description |
|------|------|-------------|
| [The Graph](https://github.com/graphprotocol/graph-node) | Open Source (3k) | Blockchain indexing via GraphQL subgraphs |
| [Subsquid](https://github.com/subsquid) | Open Source | Blockchain indexer — 50k+ blocks/sec |
| [Dune Analytics](https://dune.com/) | SaaS | SQL-based blockchain analytics |
| [Etherscan APIs](https://etherscan.io/apis) | Freemium API | REST APIs for Ethereum data |

## ☁️ Managed Scraping APIs

Pay-per-request services that handle proxies, browsers, and anti-bot for you.

| Service | Best For | Key Feature |
|---------|----------|-------------|
| [Apify](https://apify.com/) | Full-stack platform | 20,000+ pre-built scrapers, works with Crawlee/Scrapy/Playwright |
| [ScrapingBee](https://www.scrapingbee.com?fpr=edward77) | Simple API access | JS rendering, screenshots, Google Search API, 1k free calls |
| [ZenRows](https://www.zenrows.com/) | Anti-bot bypass | >99% success vs Cloudflare, Puppeteer/Playwright support |
| [ScrapFly](https://scrapfly.io/) | Multi-API | Scraping + screenshots + crawler APIs, 130M+ proxy IPs |
| [Browserless](https://www.browserless.io/) | Headless browsers | Headless Chrome in Docker, BrowserQL, self-hostable |
| [Browserbase](https://www.browserbase.com/) | AI browser agents | Cloud browsers for AI, session persistence, Stagehand integration |
| [Oxylabs](https://oxylabs.io/products/scraper-api) | Enterprise | ML-driven proxy rotation, e-commerce specialized |
| [Bright Data](https://brightdata.com/products/web-unlocker) | Scale | Web Unlocker with CAPTCHA solving, geo-routing, mobile UA |
| [SerpApi](https://serpapi.com/) | SERP data | Structured results from Google, Bing, Yahoo |
| [ScraperAPI](https://www.scraperapi.com/?fp_ref=edward66) | Getting started | 40M+ proxies, 5k free credits |

## 🧪 CAPTCHA Solving

| Service | Method | Starting Price | Supports |
|---------|--------|---------------|----------|
| [2Captcha](https://2captcha.com/auth/register/?from=27588755) | Human workers | $1/1k solves | reCAPTCHA, Turnstile, FunCaptcha, GeeTest, image |
| [Anti-Captcha](https://anti-captcha.com/) | Human workers | $0.0005/token | reCAPTCHA, hCaptcha, FunCaptcha, Turnstile |
| [CapSolver](https://www.capsolver.com/) | AI/ML | $0.65/1k | reCAPTCHA, AWS WAF, Cloudflare, GeeTest |
| [CapMonster Cloud](https://capmonster.cloud/) | AI/ML | $0.02/1k images | reCAPTCHA, hCaptcha, Turnstile, <2s solve |

## 🌍 Proxy Providers

| Provider | Network Size | Starting Price | Highlights |
|----------|-------------|---------------|------------|
| [Bright Data](https://brightdata.com/) | 150M+ IPs | Pay-as-you-go | Largest network, 195 countries |
| [Oxylabs](https://oxylabs.io/) | 100M+ IPs | Contact sales | Fastest latency, city/ZIP targeting |
| [Decodo](https://decodo.com/) | 125M+ IPs | $8.50/GB | Good value, 50 US states |
| [IPRoyal](https://iproyal.com/) | 34M+ IPs | $1.75/GB | Cheapest residential, ethically sourced |
| [NetNut](https://netnut.io?ref=mzjimtc) | 85M+ IPs | Contact sales | One-hop ISP connectivity (faster) |
| [Webshare](https://www.webshare.io/?referral_code=petnjy3bdxeh) | 10M+ IPs | $2.99/mo | Budget-friendly, free tier |

## 🆓 Try Free

| Service | Free Tier | Try It |
|---------|-----------|--------|
| [ScraperAPI](https://www.scraperapi.com/?fp_ref=edward66) | 5,000 free API credits | [Start free →](https://www.scraperapi.com/?fp_ref=edward66) |
| [ScrapingBee](https://www.scrapingbee.com?fpr=edward77) | 1,000 free API calls | [Start free →](https://www.scrapingbee.com?fpr=edward77) |
| [Webshare](https://www.webshare.io/?referral_code=petnjy3bdxeh) | Free tier with 10 proxies | [Start free →](https://www.webshare.io/?referral_code=petnjy3bdxeh) |
| [2Captcha](https://2captcha.com/auth/register/?from=27588755) | $1 starting balance | [Start free →](https://2captcha.com/auth/register/?from=27588755) |
| [NetNut](https://netnut.io?ref=mzjimtc) | 7-day free trial | [Start free →](https://netnut.io?ref=mzjimtc) |

## 🪦 Deprecated Tools Graveyard

| Dead Tool | Why | Use Instead |
|-----------|-----|-------------|
| PhantomJS | Archived 2018 | Playwright, Puppeteer |
| CasperJS | Depended on PhantomJS | Playwright, Puppeteer |
| Nightmare | Unmaintained since 2020 | Playwright |
| Zombie.js | Unmaintained | Playwright, Puppeteer |
| SlimerJS | Unmaintained, Gecko-based | Playwright (Firefox) |
| Splash | Scrapinghub, deprecated | Scrapy-Playwright |
| twint | Archived Mar 2023, blocked by Twitter | Official API |
| Goutte (PHP) | Deprecated by Symfony | Symfony BrowserKit + DomCrawler |
| snscrape | Unmaintained since Nov 2023 | Official APIs |
| undetected-chromedriver | Aging, last push Jul 2025 | Nodriver, Camoufox |
| puppeteer-extra-stealth | Unmaintained since Jul 2024 | Patchright, Camoufox |
| playwright-stealth | Unmaintained since Nov 2023 | Patchright, Camoufox |
| curl-impersonate | Unmaintained since Jul 2024 | curl_cffi |
| GoogleScraper | Unmaintained since Jul 2021 | SerpApi |
| pyautogui | Unmaintained since Aug 2024 | pytesseract + Playwright |
| SikuliX | Stale, niche | Playwright, pytesseract |

---

## Disclosure

Some links in the Managed Scraping APIs, CAPTCHA Solving, Proxy Providers, and Try Free sections are affiliate/referral links. These help support the maintenance of this list. All tools are included based on merit — affiliate status does not influence placement or rankings.

## Contributing

Contributions welcome! Please read the [contribution guidelines](CONTRIBUTING.md) first.

- Add tools you've actually used or evaluated
- Include star count and language where applicable
- Note if a tool is unmaintained (last commit >1 year ago)
- Commercial tools/services are fine but must be clearly labeled
