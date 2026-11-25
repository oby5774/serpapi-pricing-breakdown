# SerpApi Pricing: What 1,000, 10,000 and 100,000 Searches Cost, Which Plan You Need, and the Add-Ons That Double the Bill

SerpApi charges $0 for 250 searches a month, $25 for 1,000, $75 for 5,000, $150 for 15,000, $275 for 30,000, $725 for 100,000, $1,475 for 250,000 and $2,750 for 500,000. Above that, Cloud plans run in one-million-search steps from $3,750 to $106,050 a month. At full use the effective rate falls from $25.00 per 1,000 searches on Starter to $1.96 per 1,000 on Cloud 54M.

Three numbers decide what you actually pay: monthly search volume, peak-hour throughput, and speed mode. Getting the first one right still leaves the other two able to double the bill, which is why the plan table alone rarely answers the question people are really asking. What follows covers every public plan, the billing rules buried in the FAQ, the situations where that sticker price doubles, and a credit-priced alternative for teams whose volume is too small or too spiky for a monthly search quota.

> **Quick pick:** Most teams landing between 10,000 and 15,000 searches a month end up on Production at $150, which is also the first plan that includes the U.S. Legal Shield. If your volume swings month to month or your budget sits under $150, a monthly search quota is the wrong shape of purchase and a credit-based scraper will cost less. 👉 [See ScraperAPI's current plans and credit pricing](https://www.scraperapi.com/pricing?fp_ref=coupons)

## Every SerpApi plan, and what each one costs per 1,000 searches

All prices are USD, billed month to month, cancellable at any time. The per-1,000 column assumes you use the full allowance, which matters more than it sounds.

| Plan | Searches / month | Searches / hour | Price / month | Per 1,000 (full use) |
| --- | --- | --- | --- | --- |
| Free | 250 | 50 | $0 | — |
| Starter | 1,000 | 200 | $25 | $25.00 |
| Developer | 5,000 | 1,000 | $75 | $15.00 |
| Production | 15,000 | 3,000 | $150 | $10.00 |
| Big Data | 30,000 | 6,000 | $275 | $9.17 |
| Searcher | 100,000 | 20,000 | $725 | $7.25 |
| Volume | 250,000 | 50,000 | $1,475 | $5.90 |
| Infrastructure | 500,000 | 100,000 | $2,750 | $5.50 |

Two features unlock by tier, and neither shows up in the price. The U.S. Legal Shield, which SerpApi describes as up to $2 million in coverage for scraping and parsing search engine data as long as the use isn't illegal, starts at Production ($150). ZeroTrace, which keeps queries and results off SerpApi's systems and discards each request after completion, only exists on Cloud plans.

Cloud plans continue in 1M steps with the hourly cap rising by 10,000 for every million:

| Plan | Searches / month | Searches / hour | Price / month | Per 1,000 |
| --- | --- | --- | --- | --- |
| Cloud 1M | 1,000,000 | 110,000 | $3,750 | $3.75 |
| Cloud 10M | 10,000,000 | 200,000 | $21,125 | $2.11 |
| Cloud 54M | 54,000,000 | 640,000 | $106,050 | $1.96 |

Cloud 1M allows 110,000 searches an hour, roughly 30 per second. ZeroTrace and Priority Support both start here, which means the privacy option costs $3,750 a month at minimum. There is no add-on for it.

## What the per-1,000 price hides

The rate in those tables is the best case, and a lot of buyers never reach it. SerpApi sells fixed allowances, so a volume that falls between two plan sizes pays for the larger one while using part of it.

| Your monthly searches | Plan you must buy | Monthly cost | Real rate per 1,000 |
| --- | --- | --- | --- |
| 1,000 | Starter | $25 | $25.00 |
| 5,000 | Developer | $75 | $15.00 |
| 10,000 | Production | $150 | $15.00 |
| 15,000 | Production | $150 | $10.00 |
| 20,000 | Big Data | $275 | $13.75 |
| 50,000 | Searcher | $725 | $14.50 |
| 100,000 | Searcher | $725 | $7.25 |
| 500,000 | Infrastructure | $2,750 | $5.50 |

At 10,000 searches you pay the same $150 as someone running 15,000, so the advertised $10.00 becomes $15.00. At 50,000 searches you land on Searcher and pay $14.50 per 1,000, worse than Production's rate at one third the volume. Nothing carries over: unused searches reset at the start of each billing period, so a quiet month costs the same as a peak month.

## Ludicrous Speed doubles or quadruples the bill

Every plan runs on Best Effort by default at the base price. Two paid speed modes sit on top, and they multiply whatever plan you picked rather than adding a fixed fee.

- **Ludicrous Speed** costs 2× the base price and delivers 2.2× faster average response times and 4.2× faster p99.
- **Ludicrous Speed Max** costs 4× the base price, with a further 9.6% improvement on average latency and 35.4% on p99 over Ludicrous Speed.

The conversions are brutal at the low end. Starter at $25 becomes $50 a month. Production at $150 becomes $300. On Searcher, $7.25 per 1,000 becomes $14.50, and $29.00 at Max. Since the speed multiplier applies to the plan fee, not to individual requests, you cannot test it on a handful of calls.

## Five ways a SerpApi bill ends up higher than the sticker price

**1. Unused searches expire every month.** A plan allowance resets each billing month. If your volume varies, you buy for the peak and pay for it year round.

**2. The fee is flat, so small months are expensive.** A month with 100 searches on Starter still costs $25. At 10% usage, every search costs ten times the listed rate.

**3. Throughput forces a bigger plan.** A nightly job that has to finish 2,000 searches within one hour needs Production's 3,000-per-hour cap, even if the monthly total would fit Starter or Developer. SerpApi defines throughput as the guaranteed number of successful searches per hour and recommends spreading requests evenly, so a burst above the cap just waits.

**4. Running out means paying the full plan price again.** When the allowance is gone you can renew manually or switch on Automatic Early Renewal. Both refill fully and both move your renewal date. Two Production renewals inside one calendar month cost $300 for 30,000 searches, and there is no top-up pack priced per search.

**5. Speed mode.** Covered above, and easy to leave switched on after a one-off test.

Two smaller details worth knowing before you commit. Upgrades charge only the difference and keep your renewal date. Downgrades keep the renewal date too, and any leftover searches move into an Extra Credits balance. The refund is full within 7 days of subscribing, but only if you have used 20% or fewer of your searches, which is 200 searches on Starter and 3,000 on Production.

## Which SerpApi plan fits your volume?

Work out two numbers first: total searches per month, and the largest number of searches any single hour must contain. Buy the smallest plan that satisfies both.

- **Testing an integration:** Free, 250 searches a month at 50 per hour. That hourly cap means a month's quota takes at least five hours to burn through.
- **Up to 1,000 searches, no bursts:** Starter at $25. This is the most expensive per-search rate SerpApi sells.
- **1,000 to 5,000 with some burst:** Developer at $75, 1,000 searches an hour.
- **10,000 to 15,000:** Production at $150. The Legal Shield starts here.
- **15,000 to 30,000:** Big Data at $275.
- **30,000 to 100,000:** Searcher at $725, unless you can hold at 30,000.
- **100,000 to 500,000:** Volume at $1,475, then Infrastructure at $2,750.

The one pricing cliff worth planning around sits between Infrastructure and Cloud 1M. Infrastructure gives 500,000 searches for $2,750, or $5.50 per 1,000. Cloud 1M gives a million for $3,750, or $3.75 per 1,000. Paying $1,000 more buys twice the searches and drops the unit price by 32%, and it also brings ZeroTrace and Priority Support. If you are anywhere near 500,000 searches a month, the jump is the better buy.

## When a monthly search quota is the wrong purchase

SerpApi is a sensible purchase for steady, production-level workloads where you can predict next month's volume within 20% and your peak hour is not wildly above your average. It is a poor fit in three situations.

Your volume is genuinely irregular. A team that runs 80,000 searches in January and 5,000 in February pays for capacity it does not use, and no amount of planning fixes a seasonal pattern.

Your job is bursty. A one-hour batch of 20,000 searches needs Searcher at $725 even if the monthly total is 25,000, because the hourly cap, not the total, is the binding constraint.

Your volume is small. At 1,000 searches a month you pay $25, which is $25 per 1,000 and the worst rate on the entire price list. Below a few thousand searches, a prepaid or credit-based provider is almost always cheaper.

## ScraperAPI: the same job priced in credits

ScraperAPI sells API credits rather than searches, and the credit cost per request depends on the target. A standard page costs 1 credit. Amazon, Walmart and eBay cost 5. Google and Bing, including subdomains, cost 25 per request. LinkedIn costs 30. Bot-protection bypass, JavaScript rendering, premium proxies and screenshots each add 10 credits, and Ultra Premium adds 30 (75 combined with rendering). Geotargeting, sessions, device type, output format and auto parsing add nothing.

| Plan | API credits / month | Concurrent threads | Price | Get started |
| --- | --- | --- | --- | --- |
| Free | 1,000 | 5 | $0 | [Start free](https://www.scraperapi.com/?fp_ref=coupons) |
| Hobby | 100,000 | 20 | Listed on pricing page | [See the Hobby rate](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Startup | 1,000,000 | 50 | $149/mo, or $134.10/mo billed annually | [See Startup](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Business | 3,000,000 | 100 | Listed on pricing page | [See the Business rate](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Scaling | 5,000,000 | 200 | $475/mo, or $427.50/mo billed annually | [See Scaling](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Professional | 10,500,000 | 300 | Listed on pricing page | [See the Professional rate](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Advanced | 21,500,000 | 500 | Listed on pricing page | [See the Advanced rate](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Enterprise | 22,000,000+ | 500+ | Custom | [Talk to ScraperAPI about volume](https://www.scraperapi.com/pricing?fp_ref=coupons) |

The SERP rate is what makes the comparison concrete. At 25 credits per Google or Bing request, Startup's 1,000,000 credits cover 40,000 SERP requests a month for $149, which works out to about $3.73 per 1,000 requests. Billed annually that drops to roughly $3.35. Scaling covers 200,000 requests for $475, or $2.38 per 1,000 ($2.14 on annual billing). Compare that with SerpApi at $10.00 per 1,000 on Production with the allowance fully used, or $15.00 at 10,000 searches a month.

Add JavaScript rendering to every SERP call and each request costs 35 credits, cutting Startup to about 28,500 requests, still around $5.22 per 1,000. 👉 [Check what a SERP request costs in credits on ScraperAPI's pricing page](https://www.scraperapi.com/pricing?fp_ref=coupons)

The structural differences matter as much as the rate. ScraperAPI caps concurrent threads (50 on Startup, 200 on Scaling) instead of searches per hour, so a large nightly batch is limited by parallelism rather than by a published hourly ceiling. Hobby, Startup and Business can switch on auto-upgrade so scraping continues when credits run out. Scaling and the tiers above it get pay-as-you-go at a fixed per-credit rate with a monthly spending cap you set yourself, which avoids the full-price early-renewal pattern. Annual plans hand over the full year's credits upfront and can be used on any timeline. Cancelling is free from the dashboard, and the refund policy is 7 days, no questions asked.

The limits worth stating plainly: the free plan's 1,000 credits equal 40 Google SERP requests, enough to test an integration and nothing more, though the first 7 days after signup come with 5,000 credits (200 SERP requests). Hobby and Startup geotarget to US and EU only; country-level targeting starts at Business. And ScraperAPI is a general scraping API, so if you depend on structured per-engine JSON for a dozen verticals rather than the SERP page itself, SerpApi's parsing breadth is the thing you would be giving up. 👉 [Compare ScraperAPI's monthly and annual credit rates](https://www.scraperapi.com/pricing?fp_ref=coupons)

## How SerpApi compares with other SERP APIs on price

For 10,000 searches a month, the spread across providers is wide. These rates were checked against each provider's public pricing in October and November 2026.

| Provider | Cost at ~10,000 searches/mo | Rate per 1,000 | Notes |
| --- | --- | --- | --- |
| DataForSEO | ~$6 (but $50 minimum payment) | $0.60 | Standard queue averages 5 minutes; live mode $2.00 |
| Serper | ~$10 | $1.00 | $50 pack of 50,000 searches, valid 6 months |
| Bright Data SERP API | ~$15 | $1.50 | Pay as you go, no monthly fee |
| SearchApi | $40 | $4.00 | Enhanced speed doubles the price |
| ScrapingBee | $49 | $4.90 | 25,000 searches on the entry paid plan |
| SerpApi | $150 (Production) | $15.00 | Full structured results, Legal Shield included |

Google's own Custom Search JSON API is closed to new customers and existing users can keep it until 1 January 2027, with 100 free queries a day and $5 per 1,000 after that, so it is not a realistic path for a new project.

Reviewer sentiment on SerpApi, for what it is worth, sits at 4.8 out of 5 across G2 reviews updated in mid-2026. Praise clusters around response speed and the number of engines covered; complaints cluster around price and the fact that credits expire at renewal.

## Before you order: two numbers to check

Whatever provider you pick, confirm these before paying.

**Your peak hour, not your monthly total.** On SerpApi, a nightly batch of 2,000 searches needs Production's 3,000-per-hour cap even if your monthly volume fits a $25 plan. On ScraperAPI, check whether your concurrency fits the thread count for the tier.

**What happens when you run out.** On SerpApi the answer is a second full plan price inside the same month. On ScraperAPI, tiers up to Business auto-upgrade, and Scaling and above can use pay-as-you-go against a cap you control.

Final rules by situation. Steady 10,000 to 30,000 searches a month with no sharp bursts: SerpApi Production at $150, or Big Data at $275 if you want headroom. Under 5,000 searches a month: skip SerpApi's per-search premium and price the job in credits. Volume that swings by more than 2× between months: credits, because you cannot un-buy a fixed allowance. Any need for ZeroTrace: only Cloud 1M qualifies, at $3,750.

👉 [Open ScraperAPI's pricing page and check whether a credit tier covers your SERP volume](https://www.scraperapi.com/pricing?fp_ref=coupons)
