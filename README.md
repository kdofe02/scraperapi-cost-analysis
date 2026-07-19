# ScraperAPI Review: Is It Worth It in — Honest Look at Pricing, Plans, Credit Multipliers, and Who Should (and Shouldn't) Use It

> I'm going to respond in English, as ScraperAPI's primary language is English.

---

# ScraperAPI Review: Is It Actually Worth the Price? — How Credits Really Work, Which Plan Fits Your Budget, and What No One Tells You Before You Sign Up (Full Plan Breakdown Included)

---

Something funny happens when you sign up for ScraperAPI for the first time. You see "100,000 credits" on the Hobby plan and think: *that should last me a while*. Three days later, half those credits are gone and you've barely scraped a few thousand product pages.

That's not a bug. It's a feature — of the credit multiplier system. And it's the single most important thing to understand before you hand over any money.

This ScraperAPI review covers everything that actually matters: what the platform does, how the credit system really works (including the math most people never run), real performance numbers from independent benchmarks, what users across G2, Capterra, and Trustpilot are actually saying, and a clear breakdown of every plan available right now. By the end, you'll know exactly whether ScraperAPI fits your use case — or whether you're better off going a different direction.

---

## **What ScraperAPI Is (And Isn't)**

ScraperAPI is, at its core, a proxy rendering API. You send it a URL, it routes that request through a massive pool of IPs, optionally renders JavaScript with a headless browser, solves CAPTCHAs, and hands you back the HTML. That's the whole product.

Founded in 2018, the company has grown to serve over 10,000 brands — including Deloitte, Sony, and Alibaba — processing around 36 billion API requests per month. The proxy network covers 40 million+ IPs across 50+ countries. Those are legitimately impressive numbers.

But here's what ScraperAPI is *not*: it's not a full scraping platform. You don't get pre-built scrapers, hosted code execution, dataset storage, scheduling, or workflow automation. If you don't already have scraper code, ScraperAPI is just a fancy proxy. You still have to write all the parsing logic, manage your own infrastructure, and figure out your own data storage.

For developers who just need a reliable proxy layer dropped in front of existing code? It's excellent. For someone starting from scratch who just wants data in a spreadsheet by Thursday? It's the wrong tool.

---

## **The Credit System — The Part Every Review Glosses Over**

The official pricing page says things like "100,000 API credits." What it doesn't say loudly enough is that 1 API credit ≠ 1 page scraped. Not even close, in many common scenarios.

Here's how it actually breaks down.

**Domain-based multipliers are automatic.** The moment ScraperAPI detects which website you're hitting, it applies a base credit multiplier — and you don't get to opt out:

| Target Site Type | Credits per Request |
|---|---|
| Standard HTML pages (blogs, news) | 1 credit |
| E-commerce sites (Amazon, Walmart, eBay) | 5 credits |
| Search engines (Google, Bing) | 25 credits |
| Social media (LinkedIn) | 30 credits |

**Feature flags add more credits on top.** And this is where it gets sneaky:

| Feature | Additional Credits |
|---|---|
| `render=true` (JavaScript rendering) | +10 credits |
| `premium=true` (residential proxies) | +10 credits |
| `ultra_premium=true` | +30 credits |
| Anti-bot bypass (Cloudflare, DataDome, etc.) | +10 credits each (auto-detected) |
| `premium=true` + `render=true` combined | **+25 credits** (not +20) |
| `ultra_premium=true` + `render=true` combined | **+75 credits** (not +40) |

That last column is the killer. Combining features costs *more* than the sum of the individual costs. Ultra-premium plus JavaScript rendering should logically cost +40 extra credits. ScraperAPI charges +75. This non-linear stacking is documented — but you have to dig deep in the docs to find it. It's the primary reason users report credits evaporating faster than expected.

**Credits do not roll over.** Unused credits expire at the end of each billing cycle. And Pay-As-You-Go is only available on the Scaling plan ($475/month) and above. If you exhaust credits on a Hobby, Startup, or Business plan, you're simply cut off until the next billing period.

---

## **Every ScraperAPI Plan, Laid Out Clearly**

Here's the complete current plan lineup, including everything you need to know before choosing one:

| Plan | Monthly Price | Annual (per month) | API Credits / Month | Concurrent Threads | Geotargeting | Pay-As-You-Go |
|---|---|---|---|---|---|---|
| Free | $0 | — | 1,000 | 5 | ❌ | ❌ |
| Hobby | $49 | ~$44 | 100,000 | 20 | US & EU only | ❌ |
| Startup | $149 | ~$134 | 1,000,000 | 50 | US & EU only | ❌ |
| Business | $299 | ~$269 | 3,000,000 | 100 | 50+ countries | ❌ |
| Scaling | $475 | ~$427 | 5,000,000 | 200 | 50+ countries | ✅ |
| Enterprise | Custom | Custom | 5M+ | 200+ | 50+ countries | ✅ |

> 👉 [Start your 7-day free trial with 5,000 credits — no credit card required](https://www.scraperapi.com/?fp_ref=coupons)

A few things worth flagging from this table:

- **Geotargeting beyond US & EU requires the Business plan at $299/month.** This is a significant jump. If you need to scrape region-specific content from, say, Japan or Brazil, you can't do it on Hobby or Startup.
- **Concurrent threads scale with the plan** — and this directly affects how fast your scraper runs. Hobby's 20 threads vs. Business's 100 threads is a real operational difference for time-sensitive jobs.
- **Annual plans save roughly 10%** on the effective monthly rate, which is worth it if you know you'll be using the platform consistently.

---

## **What Each Plan Actually Gets You: The Real Math**

That 100,000 credits on the Hobby plan sounds generous. But run the multipliers and it starts looking a lot smaller:

| Scenario | Credits per Request | Hobby (100K credits) | Startup (1M credits) | Business (3M credits) |
|---|---|---|---|---|
| Simple HTML pages | 1 | 100,000 pages | 1,000,000 pages | 3,000,000 pages |
| Amazon product pages | 5 | 20,000 pages | 200,000 pages | 600,000 pages |
| Google SERP results | 25 | 4,000 pages | 40,000 pages | 120,000 pages |
| Amazon + JS rendering | 15 | 6,666 pages | 66,666 pages | 200,000 pages |
| Protected sites (ultra-premium + JS) | 75 | 1,333 pages | 13,333 pages | 40,000 pages |

If your use case involves Amazon with JavaScript rendering, the $49 Hobby plan gives you about 6,600 pages per month. That's meaningful for a side project but nowhere near enough for a real data operation.

The annual discount — around 10% off — brings the effective monthly rates to approximately $44 for Hobby, $134 for Startup, and $269 for Business. If you're planning to use ScraperAPI for more than a few months, the annual plan is almost always the better deal.

> 👉 [See all current plans and pricing](https://www.scraperapi.com/?fp_ref=coupons)

---

## **Where ScraperAPI Performs Well — And Where It Completely Falls Apart**

Real-world performance varies wildly depending on the site you're targeting. Independent benchmarks (Scrapeway, April 2026) paint a sharply bimodal picture:

**Strong performers:**

| Site | Success Rate | Average Speed |
|---|---|---|
| Zillow | 100% | 10.5s |
| Etsy | 99% | 4.8s |
| Amazon | 98% | 6.5s |
| LinkedIn | 95% | 17.8s |
| Walmart | 93% | 11.4s |

**Weak or failed:**

| Site | Success Rate |
|---|---|
| Realtor.com | 12% |
| Instagram | 0% |
| Booking.com | 0% |
| Twitter/X | 0% |

The pattern is clear: ScraperAPI is excellent on major e-commerce platforms and real estate sites. It's useless on social media beyond LinkedIn, and it outright fails on Instagram, Twitter/X, and Booking.com. If your scraping targets fall into that "failed" bucket, ScraperAPI is simply not the tool for you — regardless of which plan you're on.

One additional caveat: ScraperAPI applies a **10-minute forced cache on difficult targets**. If you're scraping time-sensitive data like live pricing or stock levels, you may receive results that are up to 10 minutes stale. That's not mentioned anywhere obvious in the documentation.

---

## **Structured Data Endpoints: Actually Useful, But Know the Cost**

One of ScraperAPI's genuinely strong features is its library of 18 structured data endpoints across five major platforms: Amazon (3 endpoints), Google (5 endpoints), Walmart (4 endpoints), eBay (2 endpoints), and Redfin (4 endpoints). Instead of raw HTML, these return parsed JSON with clean, usable data fields.

The Amazon endpoint is the best of the bunch — returning 18+ fields including price, BSR, ratings, variants, images, seller info, and customer reviews, with support for 21 regional marketplaces. The Google SERP endpoint returns organic results, ads, featured snippets, and People Also Ask — solid for SEO research workflows.

These endpoints cost credits on the same multiplier schedule. Amazon structured data still costs 5 credits per request. But the value is in the time saved: you don't need to write and maintain your own parser. For small teams without dedicated engineering resources, that tradeoff is often worth it.

Structured data endpoints are available on all plans including Free — so you can test them during the 7-day trial.

> 👉 [Try ScraperAPI's structured data endpoints free](https://www.scraperapi.com/?fp_ref=coupons)

---

## **What Real Users Actually Say**

Ratings across the major review platforms:

| Platform | Rating | Reviews |
|---|---|---|
| Trustpilot | 4.5 / 5 | 43 reviews |
| G2 | 4.4 / 5 | 16 reviews |
| Capterra | 4.6 / 5 | 62 reviews |

Capterra's sub-ratings are particularly revealing: **Ease of Use 4.9/5**, **Customer Service 4.6/5**, **Features 4.5/5**, **Value for Money 4.5/5**. The setup experience is consistently praised — users repeatedly mention getting up and running in minutes with clean documentation.

The complaints cluster around a few recurring themes:

- **Credit confusion**: Multiple users mention that the credit multiplier system wasn't clearly explained upfront. "Breakdown of credit costs can be confusing" is a common refrain across Capterra and G2. One Reddit user reported being quoted a rate, then billed at 5× that rate due to an undisclosed domain multiplier.
- **Reliability on harder targets**: On straightforward sites, reliability is strong. On complex, heavily protected targets, reports are more mixed. As one user put it: "ScraperAPI becomes shaky for heavy duty jobs."
- **Cost at scale**: Several users note that for large-scale operations, building custom infrastructure becomes more cost-effective than staying on ScraperAPI long-term.

The positive feedback is genuine — the platform is genuinely easy to integrate and the documentation is above average. The negatives are also genuine and worth planning for.

---

## **ScraperAPI Pros and Cons: A Straight Look**

**What works well:**

- 40M+ IPs across 50+ countries — serious proxy infrastructure
- Only charges for successful requests (HTTP 200 and 404) — failed requests don't count
- Excellent documentation and beginner-friendly setup (Capterra Ease of Use: 4.9/5)
- 18 structured data endpoints for Amazon, Google, Walmart, eBay, Redfin
- 7-day no-questions-asked refund policy
- Available on all plans including Free
- 7-day trial with 5,000 credits, no credit card required

**What to watch out for:**

- Credit multipliers stack in non-linear ways — ultra-premium + JS rendering = 75 credits per request, not 40
- Credits don't roll over between billing periods
- Pay-As-You-Go only on Scaling ($475/month) and above
- 0% success rate on Instagram, Twitter/X, Booking.com
- Geotargeting beyond US/EU requires the $299 Business plan
- Forced 10-minute cache on difficult targets — stale data risk
- Login-required sites are explicitly forbidden by the Terms of Service
- No proactive usage alerts — you have to monitor the dashboard yourself

---

## **ScraperAPI vs. Alternatives: Where It Sits in the Market**

At the ~$300/month tier, here's how ScraperAPI stacks up against the main alternatives for basic HTML scraping:

| Provider | Plan | Cost per 1,000 Requests (Basic HTML) |
|---|---|---|
| ScrapingBee | Business $249 | ~$0.08 |
| ScraperAPI | Business $299 | ~$0.10 |
| Scrapfly | Startup $250 | ~$0.10 |
| ZenRows | Business $300 | ~$0.28 |
| Bright Data | Pay-As-You-Go | ~$1.50 |

For basic HTML, ScraperAPI is competitive. But for JavaScript rendering, the calculus shifts:

| Provider | Plan | Cost per 1,000 Requests (JS Rendering) |
|---|---|---|
| ScrapingBee | Business $249 | ~$0.42 |
| Scrapfly | Startup $250 | ~$0.60 |
| ScraperAPI | Business $299 | ~$1.00 |
| ZenRows | Business $300 | ~$1.40 |

For JS-heavy scraping, ScraperAPI is mid-table. ScrapingBee is notably cheaper per rendered page at this tier, because it bundles rendering into a lower per-request cost.

The short version: ScraperAPI is a solid choice for e-commerce and SERP scraping on the right plan. It's not the cheapest option for JavaScript-heavy targets. And for anything involving social media, travel booking, or login-required pages — look elsewhere.

---

## **The DataPipeline: Great Concept, Expensive in Practice**

ScraperAPI's no-code DataPipeline feature lets you schedule scraping jobs without writing any code — you set it up, point it at a URL, and it delivers results on a schedule with webhook support. For non-technical users, that sounds perfect.

The catch: DataPipeline uses a separate, significantly higher credit schedule. A basic normal request costs **6 credits** in DataPipeline, versus 1 credit via the standard API. E-commerce requests cost 10 credits (vs. 5 via standard API). If you set up pipelines expecting standard API credit costs, you'll burn through your plan in a fraction of the expected time.

| Request Type | Standard API Credits | DataPipeline Credits |
|---|---|---|
| Basic normal request | 1 | 6 |
| E-commerce (Amazon, etc.) | 5 | 10 |
| Google SERP | 25 | 30 |
| Ultra-premium + JS | 75 | 80 |

DataPipeline is genuinely useful for teams that want automated, scheduled scraping without server management. Just factor in the 6× base credit multiplier when planning your budget.

---

## **How to Get the Most Out of ScraperAPI If You Decide to Use It**

A few things that will save you from unpleasant surprises:

**Run your actual use case math before choosing a plan.** Take your target site category, your expected monthly page volume, and the features you'll need (JS rendering? premium proxies?), apply the multipliers, and see which plan actually covers your workload. Don't assume the headline credit number is what you'll get.

**Use the free trial strategically.** You get 5,000 credits over 7 days with no credit card required. Use them specifically on your real target sites — not generic test pages. You want to know your actual credit burn rate before committing to a paid plan.

**Disable premium features unless the target requires them.** JavaScript rendering and premium proxies are opt-in — you have to explicitly set `render=true` or `premium=true`. But domain-based pricing is *not* opt-in. Amazon always costs 5 credits, Google always costs 25. Know this before running batch jobs.

**Set manual calendar reminders to check your dashboard.** ScraperAPI doesn't send proactive usage alerts. There's no email when you hit 80% of your credits. Analytics history is limited to 2 weeks on Hobby and Startup plans. You have to check manually.

**Have a backup plan for sites where ScraperAPI underperforms.** If your success rate on a specific site is below 90%, route those requests through a different provider. If the site requires a login, ScraperAPI is explicitly off-limits per their Terms of Service — you'll need a browser-based solution that operates within your existing session.

> 👉 [Start for free — 5,000 credits, 7-day trial, no credit card needed](https://www.scraperapi.com/?fp_ref=coupons)

---

## **Who ScraperAPI Is Actually Built For**

After everything above, the answer is genuinely simple.

**ScraperAPI makes sense if:**
- You have working scraper code and just need a reliable proxy layer
- Your target sites are Amazon, Google, Walmart, Zillow, or Etsy
- You're scraping under 1 million pages per month at the Startup tier or under
- Your team has at least one developer comfortable with HTTP, JSON, and API calls
- You need structured data endpoints and don't want to build your own parsers

**ScraperAPI probably isn't the right fit if:**
- Your targets include Instagram, Twitter/X, Booking.com, or heavily protected travel sites
- You need to scrape sites behind login (explicitly forbidden by ToS)
- You're a non-technical user in sales, marketing, or ops who needs data in a spreadsheet
- You need real-time data and can't tolerate 10-minute stale results from cache
- You're on a tight budget and need Pay-As-You-Go without committing to $475/month

The credit multiplier system isn't a dealbreaker — once you understand it and budget accordingly, ScraperAPI is genuinely effective at what it does. The dealbreaker is if your use case falls outside the platforms it performs well on, or if you're not set up to work with a raw API at all.

---

## **Frequently Asked Questions**

**Is ScraperAPI free to try?**
Yes. You get a permanent free tier with 1,000 credits per month, plus a 7-day trial with 5,000 credits. No credit card required. The trial gives full feature access including geotargeting, JavaScript rendering, and proxy rotation.

**How much does ScraperAPI actually cost per page?**
It depends heavily on your target. Standard HTML: 1 credit ($0.00049 on Hobby). Amazon product: 5 credits ($0.00245 on Hobby). Google SERP: 25 credits ($0.01225 on Hobby). Amazon with JS rendering: 15 credits. Protected site with ultra-premium + JS: 75 credits ($0.0368 on Hobby). Always run the math for your specific use case.

**Does ScraperAPI offer refunds?**
Yes — 7-day no-questions-asked refund policy. Contact support and they'll process it.

**What happens when I run out of credits mid-month?**
On Hobby, Startup, and Business plans: you're cut off until the next billing period, or you can upgrade to a higher tier. Pay-As-You-Go (overage billing) is only available on the Scaling plan ($475/month) and Enterprise.

**Can ScraperAPI scrape sites that require login?**
No. ScraperAPI explicitly forbids scraping data behind login walls in their Terms of Service. It supports session persistence (same IP across multiple requests) but cannot handle form filling, authentication flows, or two-factor authentication.

**Is there a discount on annual plans?**
Yes, annual billing saves approximately 10% compared to month-to-month pricing — bringing Hobby down to ~$44/month, Startup to ~$134/month, and Business to ~$269/month.

> 👉 [Get started with ScraperAPI — free trial, no credit card required](https://www.scraperapi.com/?fp_ref=coupons)
