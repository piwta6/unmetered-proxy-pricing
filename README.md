# Unmetered proxies: how to spot real flat-rate plans, what the fine print hides, and where 9Proxy's per-IP pricing lands

Most people who type "unmetered proxies" into a search box are not browsing. They got burned. A crawl hit image-heavy product pages, the gigabyte meter kept climbing, and the invoice at the end of the month covered traffic nobody had budgeted for. So the question turns into: who sells proxies where traffic simply isn't counted?

The answer starts with a distinction that marketing pages tend to blur. Unmetered is a billing shape, not a promise about speed, concurrency, or how long an IP stays alive. Plenty of providers advertise unlimited bandwidth and then enforce a fair-use threshold, a session cap, or a minimum proxy count buried three pages into the documentation. Below is where those limits actually live, how to check them before paying, and how 9Proxy structures its own unmetered option.

## Unmetered, unlimited, flat-rate: same words, different deals

Three pricing shapes show up in this market, and they behave very differently once you're running real workloads.

**Pay per gigabyte.** Traffic is the product. You top up 50 GB or 500 GB and the meter runs down. 9Proxy's bandwidth packages sit here, from $3.00 per GB at the 5 GB level down to $0.68 per GB at the 10,000 GB level. Costs scale linearly with volume, which is comfortable for small jobs and expensive for heavy ones.

**Flat rate per capacity.** You buy IPs, ports, or throughput, and the provider doesn't count the bytes. 9Proxy's IP-based packages are this model: 100 IPs, 5,000 IPs, whatever the tier, the price is fixed and traffic isn't recorded. This is what most people mean by unmetered.

**"Unlimited," subject to fair use.** Cheap entry price, thresholds in the terms. Cross them and you get throttled, lose concurrency, or get billed at a pay-as-you-go rate for the overage.

Only the middle one removes the meter entirely. The third one removes it until it doesn't.

## The fine print where "unlimited" quietly ends

Bandwidth policies across the big providers are a useful reality check, because the pattern repeats: the marketing word is unlimited, and the enforcement mechanism is something else entirely.

- **Bright Data** sells "shared unlimited" and "dedicated unlimited" ISP proxies, paid per proxy rather than per gigabyte. The published fair-use figure is 100 GB per proxy per month, shared or dedicated. Past that, you get email reminders and the extra data is billed at the current pay-as-you-go rate.
- **Oxylabs** doesn't restrict traffic on dedicated datacenter and ISP proxies, but caps concurrent sessions at 100 for the first 50 GB of an ISP proxy in a month. Once you pass 50 GB, you drop to 10 sessions for the rest of the month. Same gigabyte count, one-tenth the parallelism.
- **Decodo** enforces its fair-use policy only when two conditions stack: more than 10 TB across a subscription term, and more than 25 GB through a single IP. When both hit, concurrent sessions are reduced for the remainder of the term.
- **Webshare** makes unlimited bandwidth a function of proxy count. You need 1,000 premium proxies, 100 private proxies, or 75 dedicated proxies before traffic stops mattering. The free tier is 10 proxies and 1 GB per month.
- **IPRoyal** runs unmetered ISP and datacenter proxies, but its mobile 4G/5G connections carry a daily soft cap of roughly 20–25 GB per day in the countries where they're offered.
- **Live Proxies** counts both directions, ingress and egress, toward your total, and sells metered and unmetered plans side by side.
- **ProxyOmega** takes the capacity model to its logical end: flat-rate residential at a guaranteed speed tier, with unlimited bandwidth and unlimited concurrent connections. Its published rate card runs from $149 for one day at 200 Mbps up to $3,279 for 30 days at 1,000 Mbps.

None of that is necessarily unreasonable — running a real residential network costs money, and traffic per IP is what makes it expensive. The point is that "unmetered" tells you where the invoice stops, not where the limits stop. Concurrency caps, request-rate ceilings, and IP churn are still there, and they're usually the thing that actually breaks a scraping job.

## Six questions worth asking before you pay

If a plan claims unmetered traffic, these are the questions that separate a genuine flat rate from a quota with better branding.

1. **What exactly isn't counted?** Total traffic across the account, or traffic per IP? Some providers meter per IP and cap that instead of the account.
2. **Is there a fair-use threshold, and what triggers it?** Look for the specific numbers: GB per proxy, GB per IP, TB per term. Then find out whether crossing it means throttling, session reduction, or a charge.
3. **Are concurrent connections or threads capped?** A plan that ignores bandwidth but allows 10 simultaneous sessions is unusable for parallel scraping.
4. **Is the meter one-directional?** If upload and download both count, a plan you thought was free on the outbound side isn't.
5. **How is it billed — subscription or one-off balance?** Non-expiring balance behaves very differently from a monthly reset when your workload is seasonal.
6. **Does it require a client app or a minimum proxy count?** Desktop-app requirements matter if your stack lives on a Linux server, and count minimums matter if you're not ready to commit to 1,000 proxies.

## How 9Proxy sells unmetered traffic

9Proxy's model is the capacity version, applied to residential IPs. IP-based packages are sold as a fixed number of IPs with traffic not counted — the documentation states it as "unlimited during active time," and billing is by IP count rather than by data transferred. You pay once, and unused IPs stay in your balance instead of expiring at the end of a month.

Two details shape what "unmetered" actually means here. First, these are real residential connections, so each IP stays usable for a few hours up to roughly 24 hours, not indefinitely. Second, forwarding an IP counts as one usage — one IP equals one unit when you activate it. So the unmetered part covers the data you push through an active IP, while the IP's own lifespan is the practical resource you're burning. If your workflow needs a fresh IP every few seconds, that's a different product.

There's also a pricing wrinkle worth knowing about, because older reviews are still floating around with stale numbers. 9Proxy adjusted prices for its IP-based and bundle packages on June 1, 2026 — the first change in the company's history, according to its own announcement — while leaving GB-based packages untouched. If you read something quoting 100 IPs at $20, you're looking at pre-adjustment pricing. Any quote you act on should come from the current rate card.

👉 [Open a 9Proxy account and check today's IP rates](https://bit.ly/9-Proxy)

## Every 9Proxy package and price in one place

All four product families are listed below: flat-rate IP packages, high-volume business IP tiers, metered GB packages, enterprise GB packages with no expiry, and the IP + GB bundles that mix the two. IP-based and bundle prices reflect the post-June adjustment; GB prices are unchanged.

| Category | Package | What you get | Price | Billing / validity | Get it |
| --- | --- | --- | --- | --- | --- |
| IP-based (unmetered) | 100 IPs | 100 residential IPs, traffic not counted | $24 | One-off, unused IPs never expire | [Get 100 IPs](https://bit.ly/9-Proxy) |
| IP-based (unmetered) | 500 IPs | 500 residential IPs | $72 | One-off | [Get 500 IPs](https://bit.ly/9-Proxy) |
| IP-based (unmetered) | 1,000 + 500 bonus IPs | 1,500 IPs total | $126 | One-off | [Get 1,500 IPs](https://bit.ly/9-Proxy) |
| IP-based (unmetered) | 2,500 IPs | 2,500 residential IPs | $210 | One-off | [Get 2,500 IPs](https://bit.ly/9-Proxy) |
| IP-based (unmetered) | 5,000 IPs | 5,000 residential IPs | $360 | One-off | [Get 5,000 IPs](https://bit.ly/9-Proxy) |
| IP-based (unmetered) | 15,000 IPs | 15,000 residential IPs | $720 | One-off | [Get 15,000 IPs](https://bit.ly/9-Proxy) |
| IP-based (unmetered) | 25,000 IPs | 25,000 residential IPs | $863 | One-off | [Get 25,000 IPs](https://bit.ly/9-Proxy) |
| IP-based (unmetered) | 50,000 IPs | 50,000 residential IPs | $1,438 | One-off | [Get 50,000 IPs](https://bit.ly/9-Proxy) |
| Business IP | 100,000 IPs | High-volume IP pool | $2,300 | One-off | [Get 100,000 IPs](https://bit.ly/9-Proxy) |
| Business IP | 200,000 IPs | High-volume IP pool | $4,140 | One-off | [Get 200,000 IPs](https://bit.ly/9-Proxy) |
| Business IP | 500,000 IPs | Highest-volume IP pool | $8,625 | One-off | [Get 500,000 IPs](https://bit.ly/9-Proxy) |
| GB-based (metered) | 5 GB | Unlimited endpoints | $15 | 180-day validity | [Get the 5 GB plan](https://bit.ly/9-Proxy) |
| GB-based (metered) | 50 GB + 5 GB bonus | Unlimited endpoints | $105 | 180-day validity | [Get the 55 GB plan](https://bit.ly/9-Proxy) |
| GB-based (metered) | 100 GB | Unlimited endpoints | $150 | 180-day validity | [Get the 100 GB plan](https://bit.ly/9-Proxy) |
| GB-based (metered) | 200 GB | Unlimited endpoints | $200 | 180-day validity | [Get the 200 GB plan](https://bit.ly/9-Proxy) |
| GB-based (metered) | 1,000 GB | Unlimited endpoints | $800 | 180-day validity | [Get the 1 TB plan](https://bit.ly/9-Proxy) |
| GB-based (metered) | 2,000 GB | Unlimited endpoints | $1,500 | 180-day validity | [Get the 2 TB plan](https://bit.ly/9-Proxy) |
| Enterprise GB | 3,000 GB | Unlimited endpoints, team access | $2,160 | No expiry | [Get the 3 TB enterprise plan](https://bit.ly/9-Proxy) |
| Enterprise GB | 6,000 GB | Unlimited endpoints, team access | $4,200 | No expiry | [Get the 6 TB enterprise plan](https://bit.ly/9-Proxy) |
| Enterprise GB | 10,000 GB | Unlimited endpoints, team access | $6,800 | No expiry | [Get the 10 TB enterprise plan](https://bit.ly/9-Proxy) |
| Bundle | 100 IPs + 5 GB | IPs plus metered traffic | $30 | 180-day traffic validity | [Get the starter bundle](https://bit.ly/9-Proxy) |
| Bundle | 1,500 IPs + 50 GB | IPs plus metered traffic | $180 | 180-day traffic validity | [Get the mid-tier bundle](https://bit.ly/9-Proxy) |
| Bundle | 5,000 IPs + 500 GB | IPs plus metered traffic | $720 | 180-day traffic validity | [Get the Pro bundle](https://bit.ly/9-Proxy) |

Two things missing from that table that you might look for. There's no free tier, only a limited trial 9Proxy says it hands out to new users depending on availability — ask support whether an IP trial or a GB trial is open before you plan around it. And there's no monthly subscription anywhere: everything is prepaid balance, which is why unused IPs don't expire and GB validity stretches to 180 days.

## The per-IP math, and when it's actually cheaper

Per-IP prices fall steeply with volume: $0.24 per IP at the 100 IP tier, $0.084 at 1,500, $0.048 at 15,000, and roughly $0.017–0.018 at 500,000.

The number that matters for choosing between unmetered and metered is how much traffic a session pushes. Take the 1,500-IP package at $126, or $0.084 per IP. At the 100 GB rate of $1.50 per GB, that $0.084 buys you about 56 MB of metered traffic. At the 5 GB rate of $3.00 per GB, it buys about 28 MB. Push more than a few tens of megabytes through a single IP session and the unmetered route is already ahead of paying by the gigabyte.

That single ratio explains most of the buying decision. Crawling image-heavy pages, watching video, running long authenticated sessions, or moving bulk data through a handful of endpoints — all of that punishes a per-GB meter, and per-IP pricing doesn't care. Firing off thousands of tiny API requests that each pull a few kilobytes is the opposite case: 100 GB of metered traffic costs $150, which buys a lot of small requests, and buying 1,500 unmetered IPs for $126 would be paying for capacity you never use.

👉 [Compare the GB-based plans side by side](https://bit.ly/9-Proxy)

## Setup details that catch people out

The two product families are not interchangeable in how you plug them in, and that difference matters more than the pricing for some teams.

IP-based packages require the desktop app, which handles local port forwarding and optional proxy authentication on Windows, Mac, or Linux. That's a real constraint if your crawlers run on headless cloud boxes with no GUI. Rotation doesn't happen naturally on these plans either — you get an Auto Rotation Proxy that rotates on selected ports at intervals you configure, which is a different thing from an IP that changes on every request.

GB-based packages skip the app entirely. Everything runs from the dashboard: generate endpoints, choose sticky or rotating sessions, target down to country, state, city, ZIP, or ISP, and authenticate with username/password or by whitelisting your device IP. Endpoint generation is unlimited; only the purchased GB is deducted. Enterprise adds no-expiry traffic, a team mode with one owner and up to five members, per-member traffic controls, and activity logs.

The network itself covers 20M+ residential IPs across 90+ countries with HTTP, HTTPS, and SOCKS5 support, plus API access and crypto payments alongside standard card options. Independent comparison directories list 9Proxy at around 3.9 out of 5 with a reported success rate near 97% and average response times around 1.3 seconds. Those figures come from a directory that aggregates vendor specs and published data, not from a controlled test, so treat them as a rough signal rather than a benchmark result.

## Practical notes on stretching an unmetered balance

A few usage habits make an IP balance last longer, and they're documented rather than folklore. The "Today List" in the dashboard lets you reuse IPs from the previous 24 hours at no cost, which cuts down how many fresh IPs a repeat-visit workload burns. Auto-refresh detects offline IPs and swaps them within about a minute, so a scrape doesn't stall on a dead residential connection. Neither feature changes the traffic model — they just reduce IP consumption, which is the resource you're actually paying for.

## FAQ

**Is 9Proxy unmetered or metered?**
Both, depending on which package you buy. IP-based and business IP packages are flat rate with traffic not counted. GB-based packages are metered and billed by data volume. Bundles give you both in one purchase.

**Do unused IPs expire?**
No. Unused IPs stay as balance until you forward them. Once you forward an IP, that counts as one used IP.

**Is "unlimited bandwidth" the same as unmetered?**
Not always. Plenty of providers offer unlimited bandwidth that falls under a fair-use policy, with thresholds of 100 GB per proxy per month or 10 TB per term before concurrency drops or overage billing starts. Unmetered means no meter runs at all.

**Can I get unmetered traffic with automatic IP rotation?**
Not by default on IP packages — those are built for stable sessions, with rotation available through the Auto Rotation Proxy. Frequent rotation with small payloads is what the GB-based plans are designed for.

**What's the cheapest way to test the water?**
The 100-IP package at $24 and the 5 GB package at $15 are the entry points. 9Proxy also runs a limited new-user trial subject to availability, so it's worth asking support which type is open before you buy.

**Which plan is cheapest per unit at scale?**
The 500,000-IP business tier works out to roughly $0.017–0.018 per IP, and the 10,000 GB enterprise tier lands at $0.68 per GB. Neither is worth buying until your volume genuinely reaches that range.

## Where to start

If your proxy bill has ever surprised you because of traffic rather than IP count, the unmetered route is worth pricing out before your next renewal. Pull up the current packages, work out how many megabytes a typical session pushes, and compare that against what you'd pay per gigabyte. The crossover is usually obvious once you have the number.

👉 [See the current 9Proxy packages and start with a balance](https://bit.ly/9-Proxy)
