# Website QA sample: Toolshop demo store

A QA pass on the guest storefront of a **public practice shop built for testers**
([Practice Software Testing](https://with-bugs.practicesoftwaretesting.com), "with bugs" edition).
It's not a client project. It was run the way I run a client job, so the format and depth match what a client receives.

**14 bugs and 19 UX improvements** found on desktop (1280 px) and phone (390 px) in Chromium. Each bug was reproduced twice, recorded,
compared with the bug-free edition of the same shop, and re-checked on 30 Oct 2026: all 14 still reproduce.

| | |
|---|---|
| **Bug log and Improvement log (Google Sheets)** | [Toolshop QA - Bug log and Improvement log](https://docs.google.com/spreadsheets/d/1sZXeA56UETC9EpoKeyy4eC71b_q9LRgy6ZMJSp66n1A/edit?usp=sharing): steps, expected, actual, severity, priority with a reason, evidence, status, retest date. Two tabs: Bug log (14) and Improvement log (19) |
| **Issues** | [One issue per bug and per improvement](../../issues): bugs #1–#14 (label `bug`), UX improvements #15–#33 (label `improvement`), each with its recording or screenshot and labels for priority and severity or impact |
| **Same logs as CSV** | [bug-log.csv](bug-log.csv) · [improvement-log.csv](improvement-log.csv) |

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

## UX improvements (19)
A bug is something that breaks. An improvement is something that works but costs the shop customers or sales. These came
from walking four customer journeys (first visit, find a tool and pay, ask a question, rent a machine) as a first-time
visitor, asking five questions at each step: is it clear, can I trust it, can I find it, can I take the next step, can I finish.
Phone findings come from a 390 px window, not yet confirmed on a real phone.

| # | Page | Improvement | Priority |
|---|---|---|---|
| [UX-01](../../issues/15) | Rentals list | Give each rental a price, availability and a button | High |
| [UX-02](../../issues/16) | Product page | Show stock, delivery and returns next to Add to cart | High |
| [UX-03](../../issues/17) | Product page, phone | Move Add to cart up on phones | High |
| [UX-04](../../issues/18) | Home, first screen | Say what the shop is on the home page | High |
| [UX-05](../../issues/19) | Checkout, step 2 | Offer guest checkout | High |
| [UX-06](../../issues/20) | Whole site | Add delivery, returns, privacy and about pages | High |
| [UX-07](../../issues/21) | Product page | Hide the placeholder brand tag | Medium |
| [UX-08](../../issues/22) | Menu, phone | Close the phone menu after a choice | Medium |
| [UX-09](../../issues/23) | Cart | Show delivery costs and Continue shopping in the cart | Medium |
| [UX-10](../../issues/24) | Messages | Make every message say what to do | Medium |
| [UX-11](../../issues/25) | Contact | Add contact details beside the form | Medium |
| [UX-12](../../issues/26) | Cart, new tab | Keep the cart across tabs and visits | Medium |
| [UX-13](../../issues/27) | Cart, phone | Fit the cart to a phone screen | Medium |
| [UX-14](../../issues/28) | Cart and product page | Suggest a matching add-on in the cart | Medium |
| [UX-15](../../issues/29) | Rental item | Let renters pick dates and day rates | Medium |
| [UX-16](../../issues/30) | Home, Sort | Show the current sort order | Low |
| [UX-17](../../issues/31) | Every page, browser tab | Name each page in the browser tab | Low |
| [UX-18](../../issues/32) | Product grid | Align product names the same way | Low |
| [UX-19](../../issues/33) | Every page, phone | Keep the chat button off the page's buttons | Low |

## Not covered
Signed-in flows, checkout and payment (there's no test account on a public site), browsers other than Chromium, and security and load testing.

---
Pham Ninh, QA Engineer · web and mobile app testing, including pre-launch checks for apps built with AI tools.
