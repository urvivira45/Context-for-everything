# Soul Wave Website (soulwave.co.in): How It's Built and How It Works

Last updated: 9 Nov 2026. Built with Claude Code. This file is the non-code context: what exists, why, and the rules.

## Stack and infrastructure
- WordPress + WooCommerce. Elementor + Astra (header/footer). Novamira plugin lets Claude Code build native, editable Elementor pages.
- Built first locally in LocalWP (soulwave.local), reviewed through screenshots, then launched.
- Hosting: MilesWeb (12-month plan; plan to move to Shopify after those 12 months). Domain and DNS stay with Dynadot, do not move them.
- Plugins: RankMath (SEO and schema), testimonial carousel, Meta Pixel with ecommerce events, Razorpay (Magic Checkout), abandoned cart. Tracking: GA4, Microsoft Clarity, Meta Pixel.
- Sections are built as reusable blocks so I can add products, reorder, change colours and swap content myself. Only new section types or deep design changes need Claude Code.

## Email setup
- orders@soulwave.co.in: website sends bills and order confirmations from here, with Reply-To set to hello@.
- hello@soulwave.co.in: customer replies land here.
- Both forward to soulwave.support@gmail.com, where I actually work. Replies go out "as hello@" using Gmail Send mail as.
- Store bills, tracking and past-buyer emails via Brevo.
- Gmail labels: Orders, Orders/Problems, Bills, Customers.

## Design language
- Waves and curves, not just rounded corners. Coloured section bands start and end with a wave.
- Palette teal #2A9D8F plus lighter versions of brand colours. No beige or off-white sections, no two sections in the same colour.
- Fonts: Libre Baskerville + Jost.
- References: old soulwave.co.in (waves/feel), knotyourtype.in (overall vibe, carousels, lean policy pages).
- Carousels show a half card on BOTH ends with full cards in the middle.
- Buttons: all primary CTAs say "Get My Kit", navbar says "Buy Now". No new buttons without my approval.

## Site structure
- Homepage, Punch Needle Kits page, a page per design ("Single Punch Needle Kit - [Design]"), Combo page (pick any 2), About Us, Contact, FAQ, Blog, policies (Shipping, Returns & Refunds, Terms, Privacy, Contact).
- Ads land on product pages or the craft page (money pages), not the homepage.
- Future: one brand-level homepage for all crafts, each craft with its own page. Visitors must reach products without wading through a long landing page.

## Homepage (current order, do not reorder)
Hero → Reviews → Why Soul Wave Over Others → What's Inside → Choose Your Kit → Real People, Real Kits (reels) → Founder's note → FAQ → Closing.
- Hero headline: "Punch Needle is as easy as it looks..." / "Until it isn't" (capital U, italics, own line).
- Hero trust ticks sit below the button, one line on desktop, stacked on mobile.
- Why Soul Wave Over Others: one worry question at a time, "Others" (red cross) vs "Soul Wave" (tick) side by side, auto-moving carousel. Must keep the competitor comparison, it justifies ₹999.
- Choose Your Kit order: Combo first.
- Reviews: real only, emoji avatars (👸/🤴), never label the whole section "Google reviews". Google rating 5.0.

## Product pages
- Gallery: kit-contents photo is the 2nd image on every product page.
- Single design pages: "You May Also Like" panel (Combo first + 2 other singles). Combo page: pick-2 circles, You May Also Like shows 3 singles.
- Tabs: Who is it for / What's inside / Why Soul Wave over others / Why are we prepaid only / Product description / Shipping / Returns. One-line summary + "read more", no full stop before "...read more". Opened tab shows only the full answer.
- Picture tags (e.g. "Most ordered") stay. Combo badged "Most ordered" by my choice.
- Without-needle popup: two buttons ("Yes, I have the same needle" / "Keep the needle in my kit") + WhatsApp line. Uses my "Punch needle.jpg", not zoomable.
- FAQ is the last section, in coral, ending with WhatsApp us + See all FAQs. No closing picture section on product pages.
- WhatsApp float button bottom-left on kit pages.

## Cart
- Add to cart goes straight to cart. Buy now goes straight to checkout.
- Crossed-out price must always be the kit's real original price.
- "Add more to your cart" band lower down, centred, with a wave and yellow colour pop.
- Empty cart: "Your cart is empty for now. Pick a kit below to get started." plus the kits. No "Return to shop", no "removed. Undo?" notice.

## SEO / AEO / GEO
- Goal: first Indian brand for "punch needle", "punch needle kit", "punch needle kit India". Long term: new hobby and stress-relief searches.
- ChatGPT already recommends Soul Wave. Load benefit and persona content ONTO pages (AI reads them fastest), blogs supplement.
- Keep FAQ, Product, Organization, Article schema. Why-Soul-Wave circles open keyword-rich popups.
- Commitment: 1 hour daily for 30 days on SEO/AEO/GEO (from Oct 2026).

## Rules for any website round
- Nothing added, removed or rewritten without asking me.
- Agree all changes first, then one complete Claude Code prompt.
- Tell me upfront which pages still need design work.
- Decided, do not re-raise: with/without needle price display, flat-lay photo, scissors in photos, review preview cut-off, Combo-first order, top bar dispatch wording, "₹999 a design" line.
