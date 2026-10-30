# Website QA sample: Toolshop demo store

A QA pass on the guest storefront of a **public practice shop built for testers**
([Practice Software Testing](https://with-bugs.practicesoftwaretesting.com), "with bugs" edition).
It's not a client project. It was run the way I run a client job, so the format and depth match what a client receives.

**14 bugs** found on desktop (1280 px) and phone (390 px) in Chromium. Each was reproduced twice, recorded,
compared with the bug-free edition of the same shop, and re-checked on 30 Oct 2026: all 14 still reproduce.

| | |
|---|---|
| **Bug log (Google Sheets)** | [Toolshop QA - Bug log](https://docs.google.com/spreadsheets/d/1sZXeA56UETC9EpoKeyy4eC71b_q9LRgy6ZMJSp66n1A/edit?usp=sharing): steps, expected, actual, severity, priority with a reason, evidence, status, retest date |
| **Issues** | [One issue per bug](../../issues), with the recording and screenshots attached and labels for priority and severity |
| **Same log as CSV** | [bug-log.csv](bug-log.csv) |

## How the work ran
1. **Read-only sweep:** a slow crawl, one page every 2 to 3 seconds, for broken links, broken images, console errors and error pages.
2. **Hands-on checks:** 32 checks of the menus, sorting, filters, search, product pages, cart and contact form.
3. **Proof:** every bug re-run in a fresh browser, compared with the bug-free edition, and recorded.
4. **Ranked report:** severity plus a priority with its reason, and a Top 5 to fix first.

## Top 5 to fix first
1. **"Add to cart" shows an error message although the item is added** (Product page). Major severity, Critical priority: Every shopper who adds an item is told it failed; expect repeat clicks, duplicate items and abandoned carts. ([#6](../../issues/6))
2. **The cart shows $00.00 as every line total** (Cart). Major severity, Critical priority: Every order shows $00.00 per line on the last screen before paying; shoppers can't check what they pay for. ([#7](../../issues/7))
3. **Contact form can't be sent — every subject is rejected** (Contact form). Major severity, Critical priority: No visitor can send a message at all; order, return and payment questions never arrive. ([#2](../../issues/2))
4. **"Home" in the header opens the Contact page** (Navigation). Major severity, High priority: Visitors who use Home to get back to the products land on the contact form instead. ([#1](../../issues/1))
5. **"Add to cart" and "Add to favourites" overlap on product pages** (Product page). Medium severity, High priority: The main button on every product page is half hidden; it still works when clicked. ([#13](../../issues/13))

## All bugs
| # | Area | Bug | Severity | Priority |
|---|---|---|---|---|
| [BUG-01](../../issues/1) | Navigation | "Home" in the header opens the Contact page | Major | High |
| [BUG-02](../../issues/2) | Contact form | Contact form can't be sent — every subject is rejected | Major | Critical |
| [BUG-03](../../issues/3) | Product list | Every sort option sorts in the opposite direction | Medium | Medium |
| [BUG-04](../../issues/4) | Product list | The default $1–$100 price filter is shown but not applied | Medium | Medium |
| [BUG-05](../../issues/5) | Product page | The + and − quantity buttons do nothing | Medium | Medium |
| [BUG-06](../../issues/6) | Product page | "Add to cart" shows an error message although the item is added | Major | Critical |
| [BUG-07](../../issues/7) | Cart | The cart shows $00.00 as every line total | Major | Critical |
| [BUG-08](../../issues/8) | Navigation | The Categories menu has an "UNDEFINED" entry that opens an empty page | Medium | Medium |
| [BUG-09](../../issues/9) | Navigation | "Chainsaws" in the Categories menu opens a "Page Not Found" error | Medium | Medium |
| [BUG-10](../../issues/10) | Contact form | The contact form doesn't flag an invalid email address | Medium | Medium |
| [BUG-11](../../issues/11) | Images & text | The shop logo and the Search icon don't load | Medium | High |
| [BUG-12](../../issues/12) | Images & text | Spelling errors in the interface | Minor | Medium |
| [BUG-13](../../issues/13) | Product page | "Add to cart" and "Add to favourites" overlap on product pages | Medium | High |
| [BUG-14](../../issues/14) | Contact form | The subject list offers two error messages as subjects | Minor | Low |

## Not covered
Signed-in flows, checkout and payment (there's no test account on a public site), browsers other than Chromium, and security and load testing.

---
Pham Ninh, QA Engineer · web and mobile app testing, including pre-launch checks for apps built with AI tools.
