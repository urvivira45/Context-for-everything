# 2. Measures and Triggers

Last updated: 23 Nov 2026. Urvi asked to save this list so we can add to it and track what the monitoring agent checks. Thresholds are Claude's rules of thumb from research, NOT yet confirmed by Urvi; to be tightened after a week of real data.

## Rhythm
- Check daily, act only at the end of each ₹5,000 spend block. First 3 days: no changes (learning).
- Make changes once a week, on the same day.

## Measures
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
