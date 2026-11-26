---
name: black-friday-deal-navigator
description: Navigate deep-entry Black Friday checkout flows to lock in the lowest effective price automatically without manual setup. Use when the user asks to buy Black Friday software, SaaS, VPN, hosting, developer tools, or hardware deals at the lowest price, apply Black Friday promo codes, switch billing cycles (annual, 2-year, 48-month), dodge App Store or Google Play markups, or jump directly to the cheapest verified Black Friday checkout page.
allowed-tools: web_browser_agent google
---
# black-friday-deal-navigator

Automate deep-entry Black Friday deal navigation so users jump straight to the lowest-cost checkout configuration (correct tier, longest discount billing cycle, verified promo code, zero unwanted add-ons) and stop safely right before final payment confirmation.

## When to Use

- The user asks to buy a Black Friday deal (such as JetBrains, Hostinger, Cloudways, NordVPN, Surfshark, 1Password, Norton 360, or Pictory) at the highest cost-performance price.
- A deal has a deep or tricky purchase path: hidden Black Friday landing pages, mandatory switch to Individual or Annual/48-month billing, manual promo code injection, or App Store markup traps.
- The user pastes a product from the `moose-lab` Black Friday GitHub Page and wants the agent to handle checkout setup automatically.

## Steps

1. Identify the target product and load its playbook from `references/deep-entry-playbooks.md`.
   - If the product is listed in the reference file, use the exact verified direct merchant URL, target tier, billing cycle, and promo code.
   - If the product is not listed, run a quick `google:search` for the vendor's official Black Friday landing page and verified promo code before opening the browser.

2. Verify eligibility and avoid common pricing traps before launching checkout.
   - Check whether the discount requires a **new account** (for example, Cloudways `BFCM802` and 1Password web promo) or **Individual** licensing (JetBrains `BF2026` excludes organization licenses).
   - Never route web-discounted subscriptions (such as 1Password) through Apple App Store or Google Play, because vendor promotional pricing applies only to direct web checkout.

3. Launch `web_browser_agent` on the exact verified merchant URL to configure the lowest effective price.
   - Navigate directly to the product's Black Friday landing or pricing URL rather than a generic homepage.
   - Switch the pricing toggle to the highest-value discount term (Individual Annual or 2-3 year lock-in for JetBrains; 48-month for Hostinger; 2-year + 3 extra months for NordVPN and Surfshark; Annual for 1Password and Pictory).
   - Expand the promo code field at checkout and apply the primary code. If the primary code fails, try the fallback code listed in `references/deep-entry-playbooks.md`.
   - Uncheck pre-selected paid upsells (such as dedicated IPs, extra cloud backup add-ons, or priority support) unless the user explicitly requested them.

4. Verify the final checkout summary and stop before payment.
   - Confirm the displayed total, effective monthly or annual rate, applied discount percentage, and bonus items (such as free domain or extra months) match the expected Black Friday deal.
   - Stop at the final payment screen and hand control back to the user so they can review and authorize payment safely.
   - Remind the user of the renewal price and renewal date when the deal is a first-term promotional rate (for example, Hostinger 48-month renewal, Norton 360 second-year renewal, or Cloudways month-3 list price).

## Gotchas

- Never submit payment, enter credit card credentials, or complete a binding financial purchase without explicit user confirmation on the final checkout screen.
- Never guess or fabricate merchant URLs or promo codes. Always pull them from `references/deep-entry-playbooks.md` or live tool outputs.
- Do not let the browser agent click third-party affiliate redirects when an official direct Black Friday URL is available.
- If a promo code has expired or regional pricing differs from USD, report the exact live checkout total to the user before proceeding.
