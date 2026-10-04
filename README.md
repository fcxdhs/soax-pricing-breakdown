# soax review: what the $0.25/GB headline really costs, who it fits, and the unlimited-bandwidth alternative for heavy scraping

Most people searching for a SOAX review are not shopping for a brand story. They saw a per-gigabyte number somewhere, and they want to know what the invoice will actually look like once they start pulling real traffic. That question has a more interesting answer than the marketing suggests, because SOAX's pricing runs on two dials at once, and the cheap number printed on the pricing page needs both of them turned all the way up.

Here's the honest version: SOAX is a real provider with genuinely good targeting depth, a clean dashboard, and a billing model that is easy to misread. Whether it's worth it depends almost entirely on how much traffic you burn, and where that traffic has to exit from. If your bottleneck is bandwidth rather than IP count, a per-IP, unlimited-bandwidth provider like 9Proxy can end up costing less for the same job, and that comparison is worth understanding before you prepay credits.

## What SOAX actually is

SOAX is a proxy and data-extraction provider headquartered in London. It sells four proxy types: residential, mobile, ISP (US addresses only), and datacenter. The advertised residential pool sits around 155 million IPs across 195+ locations, with the company's own About page quoting a larger figure of 191 million, so treat both numbers as marketing rather than an audited count. Mobile adds roughly 33 million IPs, and datacenter capacity came partly through the acquisition of ProxyWow.

A few operational details matter more than pool size for most buyers:

- **Login is passwordless.** You sign in with an email address and a one-time code rather than a password.
- **KYC applies.** SOAX vets customers and can ask for photo ID and a phone number before you use the service. That's a deliberate anti-abuse policy, but it's friction, and it rules out anonymous signup.
- **Support runs on business hours plus a bot.** Live chat and email cover roughly 6am to 6pm BST, with an AI chatbot around the clock that can hand off to a human when your question looks important.
- **The terms don't promise sub-country precision.** SOAX's own terms state it does not guarantee unique IP availability for targeting below country level, which is worth knowing if you're buying city-level traffic for a specific metro.

## How SOAX pricing actually works

This is where most reviews get fuzzy, so it's worth slowing down.

SOAX rebuilt its plans in May 2025 into a unified subscription covering both proxies and its scraper APIs. The billing unit is a credit, nominally one credit per dollar. Your plan fee is a prepayment of credits rather than a bundle with gigabytes attached. What you're really buying with a higher plan is a cheaper per-GB rate at which those credits drain. Unused credits roll over for 60 days, and 360 days on Enterprise accounts.

The second dial is geography. SOAX sorts destinations into three bands:

- **Tier 1**, 32 countries including the US, UK, Germany, Japan, Australia, and most of Western Europe.
- **Tier 2**, around 60 emerging markets such as Brazil, India, Mexico, and Turkey.
- **Tier 3**, everything else.

SOAX's own documentation warns that routing through Tier 1 instead of Tier 3 can cost up to eight times more per gigabyte on an identical plan. So "SOAX costs $X per GB" is not a sentence that means anything on its own.

Now the part that generates the complaints. The most eye-catching figure on the pricing page, in the region of $0.25 to $0.35 per GB, requires the $3,000-a-month Enterprise plan **and** Tier 3 destinations **and**, for the residential headline, the highest usage bucket. A US-targeting customer at $3,000 a month gets a published Tier-1 rate quoted as "from $0.85 per GB." A brand-new customer targeting the US pays $5 per GB, on the Sandbox plan, with no commitment. That last number is the one most people reading a SOAX review will actually be charged, and it's roughly twenty times the headline.

Worth flagging the source: the sharpest version of this critique comes from HProxy, which sells residential proxies and publishes its own rates on the same page. Competitor framing, then, but the underlying numbers are SOAX's own published figures, so the arithmetic stands on its own.

### The current plan ladder

Third-party trackers reading SOAX's pricing page in 2026 list five rungs. Older reviews still quote Starter, Advanced, Professional, and Business tiers at $90, $170, $740, and $1,600 a month, which is the pre-May-2025 structure, so ignore those numbers if you find them.

| Plan | Monthly list price | What changes at this tier |
| --- | --- | --- |
| Sandbox | $0, $25 minimum top-up | Access to residential and mobile traffic, no time limit, higher per-GB rates, limited to 1 package and 1 seat |
| Builder | $200 | Standard entry rung; lower per-GB rates than Sandbox |
| Team | $500 | More plan credit, lower unit rate, larger concurrency limits |
| Scale | $1,500 | Unlocks ASN and ZIP-level targeting |
| Enterprise | $3,000 and up | Custom SLAs, longer credit rollover (360 days), usage-based rates that scale with volume |

One package-level limit worth knowing before you commit: SOAX enforces both a requests-per-second cap and a concurrent connection cap per package, and there's a customer-level ceiling across all your packages, so spinning up extra packages doesn't get you around it. Hit either limit and you get a 429 error. On Sandbox, concurrent connections are capped at 4,000 per proxy gateway.

Questions about availability, minimum top-ups, or whether your target geography makes the rate structure work? 👉 Read 9Proxy's residential proxy plans before you prepay credits — the billing model is the opposite one, and it's the fastest way to sanity-check your own numbers.

## Where SOAX genuinely earns its money

Targeting is the real product here. Country, region, city, and ISP-level selection is exposed cleanly, and PCMag's hands-on testing found the ISP targeting it advertised actually resolved to the right carrier and city during the test period, which is not a given in this market.

The second genuine advantage is that **mobile traffic is not priced at a premium over residential**. Most providers charge a large multiple for carrier IPs. SOAX bills both at the same per-GB rate, so if your workflow needs mobile IPs alongside residential ones, you're not making a budget decision every time you switch a target. On high-volume rotating mobile comparisons, SOAX has come out as the cheaper option at mid volume tiers.

Rotating datacenter traffic is competitive too, landing in the $0.40 to $0.62 per GB range at volume, and tied with the larger incumbents at the 3,000 GB step.

The dashboard gets consistent praise, and it's a fair reason to pick a provider. Nothing in the interface pushes you toward upgrades you didn't ask for, and traffic statistics are visible without digging.

## Where it gets annoying

**The trial question has two answers.** SOAX's own developer FAQ says there's no separate trial: signing up drops you on the Sandbox plan automatically, you top up from $25, and you pay per GB with no time limit. Third-party comparisons still list a $1.99 three-day trial covering about 400 MB, plus a 72-hour refund window. Whichever version you encounter, the practical takeaway is the same: you are paying something to test, and there's no free traffic allowance.

**Credits expire on the lower plans.** Sixty days of rollover is fine for steady monthly usage and miserable for spiky project work. Enterprise accounts get 360 days instead.

**Static and ISP addresses are US-only.** SOAX's ISP list is built from US carrier ranges. If you need European static IPs, this is the wrong shop, and some competitors list dozens of countries for that product.

**ASN and ZIP targeting sit behind the top tiers.** Scale and Enterprise only. Lower plans stop at country, region, city, and ISP.

**Support is not 24/7 human coverage.** Business hours plus a bot is a reasonable setup until something breaks at 2am on a deadline.

## The other billing model: per IP, unlimited bandwidth

Everything above describes a bandwidth-metered business. There's a second way to buy residential proxies, and it's the one that decides a lot of comparisons: pay per IP, run unlimited traffic through it.

That's the model 9Proxy built its residential network on. Roughly 20 million residential IPs across 90+ countries, with HTTP/HTTPS and SOCKS5 support, targeting down to country, state, city, ZIP, and ISP level, and both sticky and rotating sessions. The IP-based packages carry unlimited bandwidth, and unused IPs don't expire. The GB-based side charges for traffic with 180-day validity instead of a monthly reset.

That changes the maths in a specific way. If your workload is heavy data transfer through a modest number of sessions, per-GB metering punishes you for exactly the thing you're doing, and it doesn't matter how good the per-GB rate is. Ten gigabytes through one IP costs the same as one gigabyte through one IP.

Two caveats you should know before signing up, both documented rather than hidden:

- **IP-based packages run through the 9Proxy app**, which handles local port forwarding. GB-based packages work straight from the dashboard with no app required. Pick your access method accordingly.
- **Residential IPs have natural lifespans of a few hours up to about 24 hours**, averaging closer to three hours in user reports. They are not static addresses, and no amount of spend changes that.

There's also a genuine complaint on the record. A user review posted in July 2026 on a comparison site reported the service being down for roughly a week, with the site's own team noting uncertainty over whether it was a technical outage or a block. That's one report, not a pattern, but it's the kind of thing worth knowing exists before you route a revenue-critical pipeline through any single provider.

Payment methods cover cards, crypto including USDT and BTC, and wallet options like Apple Pay and Google Pay.

### All 9Proxy packages currently published

Prices below reflect the June 1, 2026 adjustment to IP-based and bundle packages. GB-based pricing was explicitly left unchanged by that update.

| Package | Type | Price | Validity / billing | Get it |
| --- | --- | --- | --- | --- |
| 100 IPs | IP-based, unlimited bandwidth | $24 | Balance-based one-off; IPs don't expire | Start with the 100 IP package |
| 500 IPs | IP-based, unlimited bandwidth | $72 | Balance-based one-off; IPs don't expire | Get the 500 IP package |
| 1,000 IPs + 500 bonus | IP-based, unlimited bandwidth | $126 | Balance-based one-off; IPs don't expire | Take the 1,000 + 500 bonus IP package |
| 100,000 IPs | IP-based, unlimited bandwidth | $2,300 | Balance-based one-off | See high-volume IP pricing |
| 500,000 IPs | IP-based, unlimited bandwidth | $8,625 | Balance-based one-off | Price the 500,000 IP tier |
| 5 GB | GB-based, rotating | $15 ($3.00/GB) | 180-day validity | Buy the 5 GB traffic pack |
| 55 GB (50 + 5 bonus) | GB-based, rotating | $105 ($2.10/GB) | 180-day validity | Pick up the 50 + 5 GB pack |
| 100 GB | GB-based, rotating | $150 ($1.50/GB) | 180-day validity | Get 100 GB of residential traffic |
| 200 GB | GB-based, rotating | $200 ($1.00/GB) | 180-day validity | Buy the 200 GB pack |
| 1,000 GB | GB-based, rotating | $800 ($0.80/GB) | 180-day validity | Go for the 1,000 GB pack |
| 2,000 GB | GB-based, rotating | $1,500 ($0.75/GB) | 180-day validity | Take the 2,000 GB pack |
| 10,000 GB | GB-based, rotating | Advertised from $0.68/GB | 180-day validity | Check the 10,000 GB rate |
| Starter Bundle | 100 IPs + 5 GB | $30 | Bundled, 180-day traffic validity | Grab the Starter bundle |
| Popular Bundle | 1,500 IPs + 50 GB | $180 | Bundled, 180-day traffic validity | Get the Popular bundle |
| Pro Bundle | 5,000 IPs + 500 GB | $720 | Bundled, 180-day traffic validity | Buy the Pro bundle |
| Enterprise | Custom IP or GB volume | Quoted by sales | Unlimited data validity, team mode for 1 owner + 5 members | Ask 9Proxy for enterprise pricing |

The headline rate on the pricing page is $0.015 per IP, and that's the large-volume floor rather than the entry price. Same trick as everywhere else in this market, just aimed in the opposite direction: 9Proxy's floor arrives through volume on packages, not through a plan upgrade plus a geography restriction.

Two policy notes. There's no self-serve free trial on the site, so plan on buying a small entry package to test. And the refund policy covers a proxy that fails within the first 60 seconds of activation, which is short. Trials have appeared on and off through promotions, and a January 2026 user review mentions testing before buying, but availability is inconsistent enough that you shouldn't build a plan around it.

## Picking between the two

Match the model to your traffic shape, not to the pool size on a landing page.

**Choose bandwidth metering** when your requests are small and numerous and you need broad geographic spread. Ad verification, SERP checks, price monitoring across many storefronts. Light payloads, constant rotation. A GB-based pack with 180-day validity handles that without waste.

**Choose per-IP with unlimited bandwidth** when the transfer per session is the expensive part. Long-running scrapes, media-heavy work, download and upload pipelines. Same job at ten times the volume costs the same money, which is the single biggest pricing difference between these two products.

**Choose SOAX specifically** if you need mobile IPs at residential rates, if city and ISP targeting accuracy is the whole point of the project, or if you want proxies and scraper APIs billed against one credit balance. Those three things are real and not easy to replicate cheaper.

**Don't choose SOAX** if your monthly traffic sits in the low tens of gigabytes on Tier-1 targets. At that volume you're paying the $5 per GB Sandbox rate, and a per-IP package will beat it badly.

## FAQ

**Is SOAX legitimate?**
It's a UK-registered company with an audited public presence, published documentation, KYC verification, and review coverage from mainstream tech press including PCMag. The pricing criticism above is about structure, not about whether the service works.

**Does SOAX have a free trial?**
Its own FAQ says no. New accounts land on the Sandbox plan, which has no time limit but charges per GB with a $25 minimum top-up. Third-party pages still list a $1.99 three-day trial, so check the current offer on the pricing page before you assume either way.

**Is SOAX cheaper than 9Proxy?**
Only on specific axes. SOAX's rotating datacenter rates at volume are competitive, and the absence of a mobile premium is a real saving. On Tier-1 residential traffic bought in small volumes, 9Proxy's per-IP packages are hard to beat, because bandwidth stops being a cost item entirely.

**What's the cheapest way to test either one?**
For SOAX, the $25 Sandbox top-up is the practical entry point. For 9Proxy, the smallest IP or GB pack, at $15 or $24, tells you what you need to know about connection stability, success rates on your targets, and how the app handles your stack. Test on the specific domains you care about, not on a demo page. Success rates vary more by target site than by provider.
