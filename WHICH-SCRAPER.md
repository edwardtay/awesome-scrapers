# Which scraper should I use?

A side-by-side comparison of the scrapers people actually choose between, with maintenance evidence pulled from GitHub and prices read from each vendor's own pricing page.

Checked on **14 November 2026**. "Commits (90d)" counts commits to the default branch from 16 August to 14 November 2026, which ignores bot branches and forks. Prices change often, so confirm on the vendor's page before you commit.

Back to the full list: [awesome-scrapers](README.md)

## Start from your situation

| Your situation | Start with | Move up to |
|---|---|---|
| Static HTML, a few thousand pages, Python | [httpx](https://github.com/encode/httpx) + a parser, or [Scrapy](https://github.com/scrapy/scrapy) | Scrapy with [scrapy-playwright](https://github.com/scrapy-plugins/scrapy-playwright) once pages need JavaScript |
| Static HTML in Node.js or TypeScript | [Crawlee](https://github.com/apify/crawlee) (CheerioCrawler) | Crawlee's PlaywrightCrawler, same code shape |
| Pages built by JavaScript | [Playwright](https://github.com/microsoft/playwright) | Crawlee or Scrapy on top of it for queues, retries and storage |
| The site blocks you (Cloudflare, DataDome, Akamai) | [curl_cffi](https://github.com/lexiforest/curl_cffi) for TLS fingerprints, then [Scrapling](https://github.com/D4Vinci/Scrapling) or [Camoufox](https://github.com/daijro/camoufox) | A managed unblocker (see the pricing table) |
| Clean markdown for an LLM or RAG pipeline | [Crawl4AI](https://github.com/unclecode/crawl4ai) self-hosted | [Firecrawl](https://github.com/firecrawl/firecrawl) cloud if you want no infrastructure |
| Fields out of messy pages without writing selectors | [ScrapeGraphAI](https://github.com/ScrapeGraphAI/Scrapegraph-ai) or Crawl4AI's LLM extraction | Write selectors once the layout is known; it is cheaper per page |
| A multi-step task (log in, search, click, download) | [Stagehand](https://github.com/browserbase/stagehand) or [browser-use](https://github.com/browser-use/browser-use) | [Skyvern](https://github.com/Skyvern-AI/skyvern) for form-heavy workflows |
| An AI assistant that can browse | [Playwright MCP](https://github.com/microsoft/playwright-mcp) | A hosted browser (Browserbase, Browserless) for many sessions |
| Discover the URLs and endpoints of a site (security recon) | [Katana](https://github.com/projectdiscovery/katana) | |
| Search engine results | A SERP API (SerpApi, DataForSEO) | Scraping Google directly gets blocked fast |

## Open-source frameworks and browsers

| Tool | What it is | Runs JS | License | Latest release | Commits (90d) | Watch out for |
|---|---|---|---|---|---|---|
| [Scrapy](https://github.com/scrapy/scrapy) | Python crawling framework | Via plugin | BSD-3 | 2.20.0 (Nov 2026) | 422 | No JavaScript out of the box; add scrapy-playwright. The Twisted async model takes time to learn. |
| [Crawlee](https://github.com/apify/crawlee) | Node.js crawling framework, also [in Python](https://github.com/apify/crawlee-python) | Yes | Apache-2.0 | v3.18.2 (Sep 2026) | 432 | Runs anywhere: storage defaults to a local folder and proxies take any provider. Apify's own docs and examples assume its platform. |
| [Playwright](https://github.com/microsoft/playwright) | Browser automation, Chromium, Firefox and WebKit | Yes | Apache-2.0 | v1.65.1 (Nov 2026) | 776 | Rendering costs far more memory and CPU than HTTP fetching; share one browser across contexts to keep it down. Default headless browsers are easy to fingerprint. |
| [Puppeteer](https://github.com/puppeteer/puppeteer) | Chrome and Firefox automation from Google | Yes | Apache-2.0 | Nov 2026 | 293 | The popular puppeteer-extra stealth plugin has had no commits since March 2023. |
| [Selenium](https://github.com/SeleniumHQ/selenium) | WebDriver standard, every language | Yes | Apache-2.0 | 4.52.0 (Oct 2026) | 597 | Slower and more verbose than Playwright. WebDriver is easy for sites to detect. |
| [Colly](https://github.com/gocolly/colly) | Go crawling framework | No | Apache-2.0 | v2.2.0 (Mar 2025) | 8 | Slow release pace. Pair it with chromedp for JavaScript pages. |
| [Katana](https://github.com/projectdiscovery/katana) | Crawler for URL and endpoint discovery | Optional headless | MIT | v1.8.0 (Oct 2026) | 300 | Built for recon. Field extraction is regex-based, so use a scraping framework for structured data. |
| [Spider](https://github.com/spider-rs/spider) | Rust crawler with streaming | Optional | MIT | v2.53.9 (Oct 2026) | 48 | Smaller community than the Python and Node options. |
| [Trafilatura](https://github.com/adbar/trafilatura) | Main-text extraction from HTML | No | Apache-2.0 | v2.3.1 (Oct 2026) | 124 | Extracts main text, comments, tables and metadata. It does not render JavaScript, so fetch those pages with a browser first. |

## Getting past bot detection

| Tool | Approach | Browser | License | Latest release | Commits (90d) | Watch out for |
|---|---|---|---|---|---|---|
| [curl_cffi](https://github.com/lexiforest/curl_cffi) | HTTP client that copies browser TLS and HTTP/2 fingerprints | None | MIT | v0.17.0 (Oct 2026) | 71 | Fixes fingerprint blocks only. It cannot run JavaScript challenges. |
| [Scrapling](https://github.com/D4Vinci/Scrapling) | Fetchers from plain HTTP up to a stealth browser, adaptive selectors | Chromium | BSD-3 | v0.5.1 (Nov 2026) | 243 | Still 0.x, so expect API changes between releases. |
| [Camoufox](https://github.com/daijro/camoufox) | Firefox build with fingerprint spoofing at the C++ level | Firefox | MPL-2.0 | beta.41 (Oct 2026) | 295 | Firefox only. Releases are tagged beta. |
| [SeleniumBase](https://github.com/seleniumbase/SeleniumBase) | Selenium wrapper with UC (undetected Chrome) mode | Chrome | MIT | v4.57.1 (Nov 2026) | 325 | UC mode works best in headed mode, which needs a display or Xvfb on servers. |
| [nodriver](https://github.com/ultrafunkamsterdam/nodriver) | Direct Chrome DevTools control, no WebDriver | Chrome | AGPL-3.0 | 0.50.99 on PyPI (Oct 2026) | 6 | AGPL. Three contributors and few commits. |
| [Botasaurus](https://github.com/omkarcloud/botasaurus) | Framework with anti-detection, caching and parallel runs | Chrome | MIT | 4.0.97 on PyPI (Jan 2026) | 13 | No PyPI release since January 2026. |

## AI and LLM extraction

LLM extraction and agent actions add a model call to each page or step. That handles messy layouts and changing sites, and it costs tokens and seconds per page. Plain markdown conversion (Crawl4AI, Firecrawl, Jina Reader) runs without one. For a stable layout at volume, write selectors.

"Needs a model" means an LLM provider key or a local model (such as Ollama); the open-source tools here accept either.

| Tool | What it does | Needs a model | License | Latest release | Commits (90d) | Watch out for |
|---|---|---|---|---|---|---|
| [Crawl4AI](https://github.com/unclecode/crawl4ai) | Crawler that outputs markdown, with optional LLM extraction | Only for LLM extraction | Apache-2.0 | v0.9.5 (Oct 2026) | 185 | 0.x with breaking changes between versions. 346 open issues. |
| [Firecrawl](https://github.com/firecrawl/firecrawl) | Scrape, crawl, map and search API that returns markdown or JSON | Cloud: no, included in credits. Self-hosted: only for JSON extraction | AGPL-3.0 | v2.11.0 (Jun 2026) | 763 | Self-hosting is AGPL, and the anti-bot engine (Fire-engine) is set up separately. Most users take the cloud. |
| [ScrapeGraphAI](https://github.com/ScrapeGraphAI/Scrapegraph-ai) | Describe the data in plain English, get JSON | Yes | MIT | v2.3.1 (Oct 2026) | 53 | Pays for a model call on every page. Commit pace has slowed. |
| [browser-use](https://github.com/browser-use/browser-use) | An agent that drives a browser to finish a task | Yes | MIT | 1.0.5 (Nov 2026) | 966 | One model call per step makes it slow and costly for bulk scraping. Best for tasks. |
| [Stagehand](https://github.com/browserbase/stagehand) | Playwright plus `act`, `extract` and `observe` in natural language | Yes | MIT | v3.7.7 (Oct 2026) | 260 | TypeScript first. Built around Browserbase, though it runs locally too. |
| [Skyvern](https://github.com/Skyvern-AI/skyvern) | Vision model plus LLM workflows, no selectors | Yes | AGPL-3.0 | v1.0.57 (Nov 2026) | 1,017 | AGPL. Vision calls per step are the most expensive option here. |
| [llm-scraper](https://github.com/mishushakov/llm-scraper) | TypeScript, Zod schema in, typed data out | Yes | MIT | none on GitHub | 0 | No commits since June 2026. |
| [Jina Reader](https://github.com/jina-ai/reader) | Prefix any URL with `r.jina.ai/` to get markdown | No | Apache-2.0 | none on GitHub | 0 | The repo has been quiet since May 2026. Use the hosted endpoint. |
| [Playwright MCP](https://github.com/microsoft/playwright-mcp) | Gives an AI assistant a browser through accessibility snapshots | Uses your assistant's model | Apache-2.0 | v0.0.85 (Nov 2026) | 54 | Snapshots of large pages use a lot of context tokens. |

## Managed APIs: what the first month costs

<sub>We may earn a commission from some links.</sub>

| Service | Free | Cheapest paid plan | Billed per | JavaScript or anti-bot cost |
|---|---|---|---|---|
| [Firecrawl Cloud](https://firecrawl.link/PzR7fd7) | 1,000 credits a month | $19/mo, 5,000 credits | Page (1 credit) | JSON extraction adds 4 credits a page |
| [ScrapingBee](https://www.scrapingbee.com?fpr=edward77) | 1,000 credits once | $19/mo, 75,000 credits | Successful request | JavaScript 5 credits, premium proxy 10, both 25 |
| [ZenRows](https://www.zenrows.com/) | 5,000 credits a month | $19/mo, 45,000 credits | Successful page | JavaScript 5x, premium proxy 10x, both 25x |
| [ScraperAPI](https://www.scraperapi.com/?fp_ref=edward66) | 5,000-credit 7-day trial | $49/mo, 100,000 credits | Request | Rendering 10 credits, premium plus rendering 25, some domains cost more |
| [ScrapFly](https://scrapfly.io/) | 1,000 credits on signup | $30/mo, 200,000 credits | Request | Residential proxy 25 credits, JavaScript adds 5 |
| [Zyte API](https://www.zyte.com/pricing/) | $5 credit for 30 days | $100/mo commitment | 1,000 responses, priced by site difficulty | Easiest tier: $0.13 per 1K plain, $1.01 per 1K browser-rendered |
| [Bright Data Web Unlocker](https://brightdata.com/products/web-unlocker) | 5,000 requests a month | Pay as you go, $1.50 per 1K | Successful request | Browser rendering included |
| [Oxylabs Web Scraper API](https://oxylabs.io/products/scraper-api) | $5 credit | $15/mo, up to 30K results | 1,000 results | Any site: $1.00 per 1K, $1.50 with JavaScript |
| [Apify](https://www.apify.com/?fpr=3nr7v8) | $5 of usage a month | $19/mo of usage | Compute unit ($0.20), or per result on some Actors | Residential proxy $8/GB |
| [Browserbase](https://www.browserbase.com/) | 1 browser hour | $20/mo, 100 browser hours | Browser hour | Proxy: 1 GB included, then $12/GB |
| [Browserless](https://www.browserless.io/) | 1,000 units a month | $25/mo billed yearly, 20,000 units | Unit (up to 30 s of browser time) | Residential proxy 6 units/MB, CAPTCHA 10 units |
| [SerpApi](https://serpapi.com/) | 250 searches a month | $25/mo, 1,000 searches | Successful search | Failed and cached searches are free |
| [Browse AI](https://partners.browse.ai/72ax5sc1epaz) | 50 credits a month | $48/mo, 2,000 credits (monthly billing) | 10 rows or 1 screenshot | Protected sites cost 2 to 10 credits a task |

Credit prices look alike and are not comparable: a "credit" on one service can be 25 on another for the same protected page. Price the pages you actually scrape. Most of these services report the real cost per request in a response header or an account endpoint.

## How this page is checked

- GitHub numbers come from the GitHub API on the date at the top. Latest release falls back to PyPI where a project does not publish GitHub releases.
- Commit counts show activity. A busy repo can still break on your target site, and a quiet one can be finished software.
- Prices come from each vendor's own pricing page, read on the same date. Anything a page did not state is left out.
- Spotted something out of date? [Open an issue](https://github.com/edwardtay/awesome-scrapers/issues/new/choose) or a pull request.

<p align="right">(<a href="#which-scraper-should-i-use">⬆ back to top</a>)</p>
