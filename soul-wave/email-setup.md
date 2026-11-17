# Email Setup (soulwave.co.in + Gmail)

Last updated: 17 Nov 2026

## Current setup (as Urvi described it)
- Order emails and bills go out from `orders@soulwave.co.in`.
- Customer queries come in through `hello@soulwave.co.in`.
- Every bill is Bcc'd to `soulwave.support@gmail.com`, the main inbox.
- Replies Urvi sends from `soulwave.support@gmail.com` should go out as `hello@soulwave.co.in`.

## Decisions (18 Oct 2026)
- No third Gmail account for orders. One inbox: `soulwave.support@gmail.com`.
- New, cancelled and failed order alerts move to `soulwave.support@gmail.com` (previously the old `Soulwavekits@gmail.com`). Change is in WooCommerce → Settings → Emails, recipient field of each alert.

## Open (Claude suggestions, not confirmed)
- Check in MilesWeb mPanel whether `orders@` and `hello@` are mailboxes (Email Accounts) or forwarders to the Gmail (Forwarders). Claude's server check showed both addresses exist and accept mail; it can't tell which type.
- Gmail "Send mail as" `hello@` (so replies show hello@) is not confirmed as set up.
- Gmail labels and filters: Orders, Orders/Problems (failed and cancelled, starred), Bills (skip inbox), Customers (to hello@), each with "Never send to Spam".
- Phone notifications only for Orders/Problems and Customers labels.
- Weekly cleanup: delete promotions older than 30 days, unsubscribe from unread newsletters, keep Bills forever for GST.
- Optional: Priority Inbox, Gmail templates for common customer questions.
