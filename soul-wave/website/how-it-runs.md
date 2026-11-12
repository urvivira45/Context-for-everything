# How soulwave.co.in Runs (system summary)

Source: "revise website SOP.pdf" (live-site state, verified 9 Nov 2026) in the Soul Wave Claude Project. The full SOP and the full email/WhatsApp copy ("Website email message pattern.pdf") live there. This file is the short version for any chat.

## Basics
- WordPress + WooCommerce on MilesWeb (LiteSpeed). Theme: Astra + child theme `soulwave-child` with ~36 custom PHP files that do the real work. Changing behaviour usually means editing code, not a setting.
- Payments: Razorpay Magic Checkout, live. Prepaid only. No COD, no international shipping, no customer passwords (email codes only).
- Email: WP Mail SMTP via Brevo, from orders@, reply-to hello@, Bcc soulwave.support@gmail.com.
- Code: theme repo `urvivira45/soulwave-theme`. Edit in LocalWP only (one working copy), push to GitHub, deploy with `./tools/deploy.sh --go`, then purge LiteSpeed cache.

## Catalogue (live, verified 9 Nov)
- 8 products: Combo (any 2 different designs) ₹1,349 / ₹1,249 without needle (regular ₹1,449), and 7 singles at ₹999 / ₹899 (regular ₹1,099).
- Designs: Butterfly Bloom, You Got This, Mountain Escape, Dino-mite, Lovebug, Purrfectly, Cosmic Dreams. Last four published 9 Nov with 50 panels each.
- Combo designs are line data, not variations, so the Combo always has just 2 variations. Combo gallery: kit contents, every design photo, Combo photo last; picking a design moves the gallery.
- You May Also Like: Combo first, then Lovebug, Purrfectly, Butterfly Bloom, skipping the current page.
- Adding a design: 5 steps (photo, Design attribute, duplicate a single, set panel count, check). See "Soul Wave - Adding a design.pdf".

## Stock
- Counted in printed design panels at WooCommerce → Design stock, not WooCommerce stock fields.
- Panels deducted on payment, returned on cancel/refund. A kit goes unavailable when any design it needs hits zero.
- "Only X left" launch counter is a separate marketing number in Settings.

## Offers
- Buy 2 Get 1 Free: live, no end date. Applied automatically as the coupon `buy2get1free` (nobody types it) so the Razorpay popup shows the saving. Don't edit or delete that coupon. Combo = 1 unit. Top strip: "Buy 2 Get 1 Free | Free Shipping Across India".
- Store credit: flat ₹150 earned on the order, used on the next one. Created when E4 sends (previously at delivery), valid 90 days, can't combine with B2G1. Checkout applies whichever saves more.

## Order flow and statuses
- Processing (paid) → E1 + invoice. Dispatched (custom status, needs tracking link) → E2. Completed = DELIVERED, not posted → E3 (delivery and support, no coupon), then E4 (thank-you, review, coupon) 24h after E3 if no complaint (previously 48h), then W4 by hand, then 4 Saturday WhatsApp check-ins.
- Complaint hold box pauses E4, W4 and check-ins until unticked (resolved).
- E4 must always send: remove the rule that blocks E4 when the Google review link is empty. Review link lives in Settings → General and must stay filled.
- Gift recipients: check-ins and review ask go to the recipient.

## Messages
- Emails E1 to E8, abandoned cart A1 (1h), A2 (24h), A3 (72h, carries B2G1). A3 must be edited by hand when the offer ends.
- WhatsApp W1 to W9, all sent by hand from prepared buttons; Saturday queue at WooCommerce → Check-ins (16:00).
- Message log + customer list in a Google Sheet (report, not a backup).

## Tracking and SEO
- GA4, Meta Pixel, Clarity, all gated behind cookie consent. Events: ViewContent, AddToCart, InitiateCheckout, Purchase, Lead.
- Schema (Product, FAQ, Breadcrumb, Organization), llms.txt, 15 AI crawlers allowed. FAQ copy edited only in `inc/faq-data.php`.
- Ignore Rank Math red dots on product pages (it only reads ~90 words).

## Backups
- MilesWeb daily backups, kept 7 days only. Take own weekly backup to laptop (/Applications/Soul Wave Backups).
- GitHub holds code only. Database (orders, pages, settings) and uploads are not in GitHub.

## Known gaps (7 Nov 2026)
1. Homepage Instagram reel links are placeholders (most visible broken thing).
2. Admin order alerts go to the old Soulwavekits@gmail.com.
3. No real order placed yet; full path untested end to end.
4. Shadowfax dispatch process not written down.
5. Razorpay keys not rotated since a partial secret appeared in a chat (13 Oct).
6. Theme .git folder and ._ files on the live server need deleting.
7. Abandoned cart A1 to A3 new copy (see `soul-wave/customer-messages.md`) to paste in the plugin, with first-name fallback "there".
8. Astra PHP warning flooding the error log (4MB on 9 Nov).

For the latest gap list, check the revised SOP in the Soul Wave project.
