# bandwagonhost amsterdam plan: $39/Year Specs, Real China Routes, and What to Buy When It's Out of Stock

The Amsterdam Plan is BandwagonHost's limited-run VPS: **$39 per year** for 1 AMD core, 1 GB RAM, 20 GB SSD, 1 TB of monthly traffic on a 2.5 Gbps port, hosted in Amsterdam DC1 with premium China routes — CTGNet/CN2 GIA for China Telecom, plus China Unicom Premium (AS10099) and China Mobile CMIN2 baked into the routing. That price with those routes is why this specific plan has a following.

It also has two catches worth knowing before you chase it. First, stock is genuinely scarce — as of May 2026 it was effectively unavailable without an invitation code, with restocks arriving in small batches. Second, it's the one BandwagonHost plan that **cannot migrate between datacenters**, ever. This guide covers the full spec sheet, the three Amsterdam datacenters behind the plan, every BandwagonHost package that can actually run in Amsterdam, and the fallback route most people end up taking.

> **Quick take:** If the Amsterdam Plan is in stock and you want China-optimized Amsterdam for $3.25/month, grab it — it's refundable within 30 days even if the IP gets blocked. If it's sold out, the CN2 GIA-E line still reaches Amsterdam (EUNL_9) from $169.99/year, and Basic plans cover Amsterdam from $49.99/year. 👉 [Check The Amsterdam Plan stock and price](https://bwh81.net/aff.php?aff=77528&pid=159)

## What the $39 Amsterdam Plan actually includes

Here's the full spec sheet as listed on the order page:

| Item | Spec |
| --- | --- |
| CPU | 1x AMD core |
| RAM | 1024 MB |
| Storage | 20 GB SSD (RAID-10) |
| Transfer | 1000 GB/month |
| Port speed | 2.5 Gbps |
| Location | Amsterdam, Netherlands — DC1 (EUNL_1) |
| Virtualization | KVM (KiwiVM panel) |
| IP | 1 dedicated IPv4, routed /64 IPv6 subnet |
| Price | $39.00/year, single billing cycle |

Beyond the raw numbers, the plan ships with free automatic backups, free snapshots, instant OS reload, manual ISO installs, full root access, and instant rDNS updates from the control panel. Supported operating systems cover CentOS, Debian, Ubuntu, Rocky Linux, and AlmaLinux. Uptime is guaranteed at 99.9%, and the refund window is 30 days — with the unusual condition that you can get a refund even if the IP has been blocked by the GFW. That last point matters a lot for the China-focused buyers this plan targets.

On real-world performance: a January 2026 hands-on review measured the host running an AMD EPYC Genoa processor at around 2.4 GHz, scoring roughly **1066 in Geekbench 5 single-core**. Disk performance was strong — about 155 MB/s on 4K mixed read/write and around 3 GB/s on large sequential reads. The machine sits on AS25820 (IT7 Networks), which is BandwagonHost's parent network. One caveat from that same review: IPv4 was online and working, but IPv6 showed offline at test time, even though the plan spec includes a /64 IPv6 subnet. If IPv6 is critical for your use case, treat it as something to verify after setup rather than assume.

The fine print you won't see on the sales page summary: this plan **does not support datacenter migration**. Every other BandwagonHost family lets you move between locations for free without data loss; the Amsterdam Plan is locked to DC1 for life. Buy it because you want Amsterdam specifically, or don't buy it.

## One European location, three Amsterdam datacenters

Amsterdam is BandwagonHost's only European location, and it's split into three datacenter IDs with noticeably different networks. The old EUNL_3 has been retired and folded into EUNL_2, so those are the only three IDs you'll encounter:

| Datacenter | Network character | Which plans land here |
| --- | --- | --- |
| EUNL_1 (DC1) | Premium legacy European routing with CN2 GIA/CTGNet for China Telecom; integrates AS10099 and CMIN2 | The Amsterdam Plan only |
| EUNL_2 (DC2) | Standard international routing on AMD hardware; no deep China optimization | Basic KVM plans; also selectable for CN2 GIA-E |
| EUNL_9 (DC9) | China Unicom Premium AS9929/AS10099 return routes; strong performance across all three mainland carriers | CN2 GIA-E plans only |

A common mix-up worth flagging: EUNL_9 refers to Amsterdam DC9. It has nothing to do with the Los Angeles DC9 that shows up in BandwagonHost's US lineup. Among the three, EUNL_9 currently offers the best mainland China connectivity in Europe — low latency, minimal packet loss, and a particularly good experience for China Unicom users. EUNL_1 matches it on paper but is only reachable through the Amsterdam Plan's scarce stock. EUNL_2 is the workhorse: stable AMD performance for European traffic, fine if you don't care about China routing.

## Every BandwagonHost plan that can run in Amsterdam

Two regular plan families include Amsterdam as a hosting location — Basic VPS and E-Commerce VPS (CN2 GIA-E) — which together cover 15 plans. Add the limited-edition Amsterdam Plan and that's the complete menu. Here's the full breakdown.

### Basic VPS — Amsterdam on standard routing, from $49.99/year

The Basic family is BandwagonHost's budget line, available in six locations including Amsterdam. All plans run on a 1 Gbps port and can migrate between locations free of charge. In Amsterdam they land on EUNL_2 with standard international routing.

| Plan | vCPU / RAM | SSD / Traffic | Price by billing cycle | Order |
| --- | --- | --- | --- | --- |
| 20G KVM PROMO | 2 / 1 GB | 20 GB / 1 TB | $49.99 / year | [Order](https://bwh81.net/aff.php?aff=77528&pid=44) |
| 40G KVM PROMO | 3 / 2 GB | 40 GB / 2 TB | $52.99 semi-annual · $99.99 year | [Order](https://bwh81.net/aff.php?aff=77528&pid=45) |
| 80G KVM PROMO | 4 / 4 GB | 80 GB / 3 TB | $19.99 month · $59.99 quarter · $107.99 semi-annual · $199.99 year | [Order](https://bwh81.net/aff.php?aff=77528&pid=46) |
| 160G KVM PROMO | 5 / 8 GB | 160 GB / 4 TB | $39.99 month · $112.99 quarter · $213.99 semi-annual · $399.99 year | [Order](https://bwh81.net/aff.php?aff=77528&pid=47) |
| 320G KVM PROMO | 6 / 16 GB | 320 GB / 5 TB | $79.99 month · $227.99 quarter · $432.99 semi-annual · $799.99 year | [Order](https://bwh81.net/aff.php?aff=77528&pid=48) |
| 480G KVM PROMO | 7 / 24 GB | 480 GB / 6 TB | $119.99 month · $341.99 quarter · $649.49 semi-annual · $1,199.99 year | [Order](https://bwh81.net/aff.php?aff=77528&pid=49) |

Note the entry plan is actually more generous than the Amsterdam Plan in one spot: 2 vCPU instead of 1, for $49.99 versus $39. What you give up is the 2.5 Gbps port and the premium China routes.

### E-Commerce VPS (CN2 GIA-E) — Amsterdam EUNL_9, from $169.99/year

The E-Commerce family is where the premium China connectivity lives. Nine plans, and Amsterdam can be selected as either EUNL_9 or EUNL_2 at setup — with free migration between locations afterward, so you can start in Los Angeles and move to Amsterdam later if your needs change.

| Plan | vCPU / RAM | SSD / Traffic | Port | Price by billing cycle | Order |
| --- | --- | --- | --- | --- | --- |
| CN2 GIA-E 20G | 2 / 1 GB | 20 GB / 1 TB | 2.5 Gbps | $49.99 quarter · $89.99 semi-annual · $169.99 year | [Order](https://bwh81.net/aff.php?aff=77528&pid=87) |
| CN2 GIA-E 40G | 3 / 2 GB | 40 GB / 2 TB | 2.5 Gbps | $89.99 quarter · $169.99 semi-annual · $299.99 year | [Order](https://bwh81.net/aff.php?aff=77528&pid=88) |
| CN2 GIA-E 80G | 4 / 4 GB | 80 GB / 3 TB | 2.5 Gbps | $56.99 month · $149.99 quarter · $289.99 semi-annual · $549.99 year | [Order](https://bwh81.net/aff.php?aff=77528&pid=89) |
| CN2 GIA-E 160G | 6 / 8 GB | 160 GB / 5 TB | 5 Gbps | $86.99 month · $239.99 quarter · $459.99 semi-annual · $879.99 year | [Order](https://bwh81.net/aff.php?aff=77528&pid=90) |
| CN2 GIA-E 320G | 8 / 16 GB | 320 GB / 8 TB | 5 Gbps | $159.99 month · $459.99 quarter · $869.99 semi-annual · $1,599.99 year | [Order](https://bwh81.net/aff.php?aff=77528&pid=91) |
| CN2 GIA-E 640G | 10 / 32 GB | 640 GB / 10 TB | 10 Gbps | $289.99 month · $799.99 quarter · $1,499.99 semi-annual · $2,759.99 year | [Order](https://bwh81.net/aff.php?aff=77528&pid=92) |
| CN2 GIA-E 1280G | 12 / 64 GB | 1.28 TB / 12 TB | 10 Gbps | $549.99 month · $1,559.99 quarter · $2,979.99 semi-annual · $5,499.99 year | [Order](https://bwh81.net/aff.php?aff=77528&pid=93) |
| CN2 GIA-E 1280G HIBW 15T | 12 / 64 GB | 1.28 TB / 15 TB | 10 Gbps | $679 month · $1,935 quarter · $3,670 semi-annual · $6,790 year | [Order](https://bwh81.net/aff.php?aff=77528&pid=160) |
| CN2 GIA-E 1280G HIBW 20T | 12 / 64 GB | 1.28 TB / 20 TB | 10 Gbps | $899 month · $2,562 quarter · $4,860 semi-annual · $8,999 year | [Order](https://bwh81.net/aff.php?aff=77528&pid=161) |

### The rest of the catalog, briefly

The full BandwagonHost catalog runs to 48 plans across four families. The fourth family, E-Commerce + SLA, adds a 99.99% service level agreement on top of the premium China routes — but it's currently restricted to a single location, USCA_5 in Los Angeles. The smallest SLA tier (2 vCPU, 1060 MB RAM, 20 GB SSD, 1 TB) runs $239.99/year. Since SLA plans can't be hosted in Amsterdam at all, they're irrelevant to this search and I've left them out of the tables above. The remainder of the catalog is limited-edition plans that appear and sell out in batches — The Amsterdam Plan is one of them.

## Which Amsterdam plan makes sense at your budget

Match the plan to what you actually need, not to the one with the best story:

- **You want the cheapest possible China-optimized Amsterdam box, and you're patient.** The Amsterdam Plan at $39/year works out to $3.25/month — nothing else in the catalog touches that price with CN2 GIA routing. The trade-offs: single core, no migration ever, and you may wait weeks or months for a restock.
- **You want Amsterdam now and don't care about China routes.** Basic 20G KVM at $49.99/year is the sensible buy. You get a second vCPU, EUNL_2's stable AMD platform, and full migration freedom. 👉 [See the Basic 20G KVM plan at $49.99/year](https://bwh81.net/aff.php?aff=77528&pid=44)
- **You want China routes, Amsterdam, and flexibility.** CN2 GIA-E 20G at $169.99/year (or $49.99 quarterly if you'd rather test the waters) puts you on EUNL_9 with the option to relocate later at no cost. It's the most expensive route to Amsterdam, and the one most people actually take when PID 159 is empty. 👉 [Order CN2 GIA-E 20G and pick Amsterdam EUNL_9](https://bwh81.net/aff.php?aff=77528&pid=87)

## Before you order: stock, support, and the refund window

Three things trip people up with this plan.

Stock first. The Amsterdam Plan is not kept continuously available. In May 2026 it required an invitation code and was listed as unavailable through normal checkout — restocks happen in batches and sell through quickly. If the order page shows stock, that's the moment to decide, because the 30-day refund policy (which holds even with a blocked IP) makes the initial purchase low-risk.

Support second. BandwagonHost VPS plans are strictly self-managed. There's no hand-holding, no ticket-based config help — you get the KiwiVM control panel, root access, and documentation. If you need managed hosting, this entire catalog is the wrong product category.

IPv6 third. The spec includes a routed /64 IPv6 subnet, but the January 2026 review found IPv6 offline on a live unit. If your deployment depends on IPv6, plan to verify it early in your refund window.

## FAQ

**Is the Amsterdam Plan really $39/year?**
Yes — $39.00 for a 12-month cycle, with no monthly or quarterly options. It's a single-price plan, so there's no renewal-price jump to worry about either.

**Can I migrate the Amsterdam Plan to Los Angeles later?**
No. It's the only BandwagonHost plan family that doesn't support datacenter migration. Basic and CN2 GIA-E plans can move between locations anytime, free, without data loss.

**What if the Amsterdam Plan is out of stock?**
Buy a CN2 GIA-E plan and choose Amsterdam EUNL_9 as the location — same premium China routing, immediate availability. If China routing doesn't matter to you, the Basic line's Amsterdam (EUNL_2) starts at $49.99/year.

**Does the Amsterdam Plan have a money-back guarantee?**
Yes. 30 days, and it applies even if the IP address gets blocked by the GFW — a specific accommodation for users accessing it from mainland China. Uptime is guaranteed at 99.9%.

**Is EUNL_9 the same as the famous LA DC9?**
No. EUNL_9 is Amsterdam DC9 in the Netherlands. The name overlap with the Los Angeles DC9 is a recurring source of confusion in forum threads, so double-check the location dropdown when ordering.

## Picking a plan, in one pass

In stock and you want the cheapest China-route Amsterdam available → the Amsterdam Plan, no hesitation, since the refund window covers you. Need Amsterdam today with premium routes → CN2 GIA-E on EUNL_9. Just need a solid European VPS → Basic on EUNL_2 and pocket the difference. Whatever you choose, check the Amsterdam Plan's stock status before settling for a pricier alternative — at $39/year it remains the best value in the entire catalog when it exists. 👉 [Grab The Amsterdam Plan at $39/year while stock lasts](https://bwh81.net/aff.php?aff=77528&pid=159)
