# 4. Tracking and Agent Rules

Last updated: 23 Nov 2026. What the monitoring agent follows once ads are live. The agent never changes anything itself; it reports and Urvi acts.

## Report rhythm (LOCKED)
- Every 2 hours: alerts only (ad spent ₹1,000+ with no sale; spending faster than budget; spend stopped; visits but zero add-to-carts for 4+ hours; Meta purchases vs Razorpay orders mismatch). Otherwise silent.
- Daily 10 pm: today and last 7 days, spend, orders, CAC colour, funnel, offense or defense.
- Every 3 days: small decisions (pause weak ads, swap ads, fix a site step). (LOCKED: Urvi wants 3-day decisions)
- Every 7 days: big decisions on the 7-day average (scale, stop a campaign, launch a new one), progress vs scoreboard, lessons for the test log.

## Decision rules (LOCKED unless marked)
- Decide on 7-day averages; last 3 days show direction only. Never decide on one day.
- Days 1 to 3: no changes. Day 5: safety check. Day 7: first big decision.
- Defense (2+ red days across the whole account): hold position, launch nothing new, cut newest/worst first if needed, protect old winners.
- Offense (2 to 3 green days in a row): launch the next test or raise budget 20%.
- CAC colours (PROPOSED): green ₹300 or less, amber ₹300 to ₹380, red above ₹380.
- Judge an ad after 3 x CAC spend (~₹1,000); an ad set or campaign after 5 x CAC (~₹1,900) and 3+ days. (PROPOSED)
- Frequency is supporting evidence only: CAC decides. (PROPOSED)

## Diagnosis order (PROPOSED)
1. Tracking (Meta purchases vs Razorpay). 2. The ad (hook rate, click rate, cost per visit). 3. The site (visits/clicks, add to cart, checkout, purchase). 4. The offer (average order value, kits per order). 5. Wear-out (frequency and reach cost, only when CAC is red). 6. Account mood (whole account down = defense).

## Formulas (PROPOSED; thresholds tighten after week 1)
| What | Formula | Threshold |
|---|---|---|
| CAC incl. GST | Spend x 1.18 / Razorpay orders | green ≤₹300, red >₹380 |
| Ad sets the budget can feed | Weekly budget / (₹380 x 50) | |
| Min daily budget per ad set | CAC x 1 to 2 | ₹380 to ₹760 |
| Judge an ad | Spend ≥ 3 x CAC | ~₹1,000 |
| Judge an ad set/campaign | Spend ≥ 5 x CAC and 3+ days | ~₹1,900 |
| Expected orders | Spend / CAC | |
| Daily pace needed | Orders still needed / days left | |
| Daily budget left | Budget left / days left | |
| Buy rate needed | Cost per visit / CAC | |
| Cost per visit | Spend / landing page views | ≤ ₹10 |
| Visits per click | Landing page views / link clicks | ≥ 70% |
| Click rate | Unique outbound clicks / reach | ≥ 1% |
| Hook rate | 3-sec views / impressions | ≥ 25% |
| Hold rate | ThruPlays / 3-sec views | ≥ 15% |
| Add to cart rate | Add to carts / visits | ≥ 5% |
| Cart to checkout | Checkouts / add to carts | ~1 in 2 healthy; 1 in 6 = problem |
| Checkout to purchase | Purchases / checkouts | ≥ 40% |
| Average order value | Revenue / orders | > ₹1,100 |
| Kits per order | Kits / orders | higher is better |
| Profit per order after ads | Average keep per order - CAC | positive |
| Break-even CAC | Keep per order (`../finance.md`) | single ₹522, combo ₹668, 3 kits ₹1,145 |
| Break-even ROAS | Average order value / average keep per order | ~1.9 (true break-even) |
| Target ROAS (our ROAS) | Revenue / (spend x 1.18) | ≥3.5 at ₹380 CAC, ≥4.5 at ₹300 (at ~₹1,340 average order) |
| Meta-shown ROAS | Revenue / spend excl. GST (what Ads Manager shows) | divide by 1.18 to get our ROAS |
| Frequency | Impressions / reach | evidence only |
| Tracking check | Meta purchases / Razorpay orders | within ~20% |
| View-through share | 1-day view purchases / all purchases | under ~40% |
| Safe budget change | New / old budget | ≤ 1.2, once per 3 days |
| Week-over-week | (This 7 days - last 7) / last 7 | trend |
| CAC by state, placement, age | Ads Manager breakdowns | vs average |

## Block rules per ₹5,000 (PROPOSED)
16+ orders: raise budget 20% (if offense). 13 to 15: hold. 8 to 12: swap the 2 weakest ads, check the site. 7 or fewer twice in a row, or 16 or fewer after ₹10,000: pause and fix.

## Measures (detail)
| # | Measure | Healthy | If bad, the problem is |
|---|---|---|---|
| 1 | CAC incl. GST (spend x 1.18 / purchases) | ₹300 to ₹380 | Overall |
| 2 | Average order value, share of 3-kit/combo orders | Average over ₹1,100 | Offer visibility |
| 3 | Hook rate (3-sec views / impressions) | 25%+ | First 3 seconds of the ad |
| 4 | Link click-through rate | 1%+ | Message or offer |
| 5 | Cost per website visit | ₹10 or less | Ads or reach cost |
| 6 | Visits / link clicks | 70%+ | Site speed |
| 7 | Add to cart / visits | 5%+ | Product page or price |
| 8 | Purchases / checkouts started | 40%+ | Checkout, payment, shipping |
| 9 | Visitors who buy | 2.5%+ | Steps 6 to 8 |
| 10 | Frequency (7-day, cold) | Under 2.5 | Same people seeing ads too often |
| 11 | Cost per 1,000 reached | Steady | Ads wearing out or auction busier |
| 12 | Learning status per ad set | Exits within ~7 days | Too little budget per ad set |
| 13 | Meta purchases vs Razorpay orders | Within ~20% | Tracking |
| 14 | Attribution split: 1-day view share of purchases | Under ~40% | Meta claiming sales it did not cause |
| 15 | Cost per add to cart | ₹60 or less | Early signal before purchases come in |
| 16 | Hold rate (ThruPlay / 3-sec views) | 15%+ | Ad loses people after the hook |
| 17 | CAC by state (region breakdown) | Each state vs average | Which regions to keep, cut or add |
| 18 | CAC by placement (Reels, Feed, Stories) | vs average | Where ads work |
| 19 | CAC by age band | vs average | Who buys |
| 20 | Event Match Quality (Events Manager) | 6+ out of 10 | Tracking quality |
| 21 | Profit per order after ads (keep per order minus CAC) | Positive | Whether scaling makes money |
| 22 | Payment failures (Razorpay) | Low, steady | Checkout friction |

## Triggers
1. Ads wearing out: CAC, frequency and reach cost all rise for 3 days AND average CAC over ₹380. Refresh (under ~30 purchases: new ads in the same ad set; after: new campaign).
2. Weak ad: ~₹1,000 spent, no sale. Pause that ad only.
3. Funnel problem: visits ₹10 or less but few sales. Fix the site step (7, 8 or 9), not the ads.
4. Room to grow: CAC ₹300 or less for 3 days. Raise budget 20% or stack a new campaign.

## Block rules (per ₹5,000 spent)
- 16+ orders: raise budget 20%. 13 to 15: hold. 8 to 12: swap the 2 weakest ads, check the site. 7 or fewer twice in a row, or 16 or fewer after ₹10,000: pause and fix.

## Status
- Measures 1 to 13: proposed 23 Nov. Measures 14 to 22: proposed 23 Nov, pending Urvi's lock.
- Weekly: check "Compare attribution settings" (1-day click vs 1-day view vs incremental).
