---
title: "SuperGrok Paid but Still Free: Account and Billing Checks"
description: "If SuperGrok was charged but Grok still shows Free or Upgrade, check the receipt, billing route, original account, Apple Hide My Email, weekly limit and paid plan on the account before paying again."
permalink: /en/guides/supergrok-paid-but-still-free/
lang: en
schema_type: Article
date_published: 2026-07-24
last_modified_at: 2026-08-05
breadcrumbs:
  - name: "Home"
    url: /
  - name: "Guides"
    url: /guides/
  - name: "SuperGrok Paid but Still Free"
    url: /en/guides/supergrok-paid-but-still-free/
faq:
  - question: "Why does Grok still show Free after I paid for SuperGrok?"
    answer: "The payment, active subscription and paid plan shown on the current account are separate states. The purchase may be pending, attached to another login, associated with Apple Hide My Email or X, or active while a weekly usage limit has been reached."
  - question: "Should I buy SuperGrok again if the first payment was charged?"
    answer: "No. Check the original billing channel and account first. A second purchase can create duplicate subscriptions or charges without making the first paid plan appear on the account you are using."
  - question: "Can a weekly usage limit make an active SuperGrok account show an upgrade prompt?"
    answer: "An active subscription can temporarily lose access to some paid usage after a weekly limit is reached. Check Settings and Usage before treating the prompt as an inactive subscription."
  - question: "What should I check for a ChongGrok card-key order?"
    answer: "Use the verification page to check the card key, submitted Grok User ID, target account and processing result. Do not publish the User ID or place a second order while the first one is unresolved."
---

# SuperGrok Was Charged but Still Shows Free: Account, Billing Route and Entitlement Checks

**Short answer:** do not pay again. A bank charge, store receipt, active subscription and paid plan shown in Grok are separate states, so first identify the original purchase route and the exact account that owns it.

If the plan is active but a feature is unavailable, also check the weekly usage limit. A usage cap and a missing subscription are not the same problem.

## Separate the four states

| State | What it proves | What it does not prove |
|---|---|---|
| Bank shows `pending` | The bank recorded the payment request, but has not confirmed a final payment to the provider | That the purchase completed |
| Final receipt | The provider recorded a completed purchase | That the current login is the purchasing account |
| Active subscription | The billing provider considers the plan active | That every feature has remaining usage |
| Paid plan on the account | The current Grok identity shows the paid plan | That another Apple, Google or X login owns the same plan |

## 1. Find the original billing route

Check only the platform that processed the purchase:

| Purchase route | Where to check |
|---|---|
| grok.com | The signed-in Grok account's billing page |
| Apple App Store | Subscriptions and purchase history under the original Apple account |
| Google Play | Payments & subscriptions under the original Google account |
| X Premium+ | Premium settings under the purchasing X account |
| ChongGrok card key | Card-key verification and order processing status |

If you cannot identify the route, search the receipt issuer and transaction description before changing accounts or paying again.

**Expected result:** one billing route shows the order and its final state. If the only evidence is a pending bank record, wait for the final outcome and do not continue to account troubleshooting yet.

## 2. Verify the original account and sign-in method

The xAI consumer FAQ states that subscriptions are tied to the account used to buy them. Confirm:

1. the account email or X identity used at purchase;
2. whether the current session used email, Google, Apple or X sign-in;
3. whether another browser or app is already signed into a different Grok account;
4. whether the active subscription appears inside that exact account.

Similar display names do not establish that two sessions are the same account.

**Expected result:** the account that owns the receipt is the account currently open in Grok. If it is not, return to the original sign-in method before refreshing or reinstalling anything.

## 3. Check Apple Hide My Email

If the purchase used **Sign in with Apple** and **Hide My Email**, continue with the same Apple sign-in method. Typing the Apple relay email into another login method can open a separate Grok identity that does not own the subscription.

Do not create another account to solve this mismatch. Return to the original Apple authentication route.

## 4. Distinguish a weekly limit from an inactive plan

An account can have an active paid subscription while some paid usage is temporarily unavailable.

| Observation | More likely explanation |
|---|---|
| Billing shows no active plan | Missing, expired or wrong-account subscription |
| Billing is active and Settings → Usage shows a reached limit | Weekly usage allowance is exhausted |
| Another login shows the paid plan | Current session uses the wrong account |
| Store subscription is active but app shows Upgrade | App/session synchronization or account mismatch |

Check the current usage screen and reset information. Do not purchase another membership to bypass a weekly usage limit.

If Billing shows an active plan and Usage shows a reached limit, the subscription is working; wait for the reset shown on that account. If Billing shows no plan, continue with account and purchase checks instead.

## 5. Refresh the app or browser state

After confirming the correct account and active subscription:

1. update the Grok app;
2. fully close and reopen it;
3. sign out and back in with the original method;
4. clear the browser cache or test a private window;
5. reinstall the app only after recording the account and purchase evidence.

These actions can refresh local state, but they cannot transfer a subscription between accounts.

The expected result is that the same account now shows the active plan. If it remains Free after one clean sign-in, stop repeating refresh steps and contact the provider that owns the completed receipt.

## 6. Check a ChongGrok order without repurchasing

For an existing ChongGrok card key or order, use [chonggrok.com/verify](https://chonggrok.com/verify?utm_source=github_guides&utm_medium=referral&utm_campaign=supergrok_paid_but_still_free&utm_content=en_verify_existing_order) and confirm:

- the card key was accepted;
- the submitted Grok User ID belongs to the intended account;
- the order is pending, completed or failed;
- the current browser is signed into that same account; and
- the processing record matches the order.

A Grok User ID is an account identifier, not a password, but it is sensitive and must not be posted publicly. Do not place a second order while the first order or payment remains unresolved.

Only after confirming that no active, completed or pending purchase exists should current options at [chonggrok.com/supergrok](https://chonggrok.com/supergrok?utm_source=github_guides&utm_medium=referral&utm_campaign=supergrok_paid_but_still_free&utm_content=en_repurchase_boundary) be considered.

## Completion checklist

- The original billing route and final order state are known.
- The current Grok login matches the purchasing account and sign-in method.
- An active plan has been distinguished from a reached weekly usage limit.
- The correct provider has received the redacted receipt and account evidence when paid access is still missing.
- No second purchase was created while the first charge or order remained unresolved.

## Who should handle the problem?

| Evidence | Contact |
|---|---|
| Direct grok.com receipt but the correct account still lacks the paid plan | xAI consumer support |
| Apple receipt or App Store subscription issue | Apple |
| Google Play receipt or Play subscription issue | Google Play |
| X Premium+ billing or linked X account issue | X |
| Bank authorization or issuer decline | Card issuer |
| ChongGrok card key or processing record | ChongGrok support |

Keep the account email, login method, platform, redacted receipt, date, currency, amount, screenshot, app version and device details. Never publish passwords, codes, full payment details or User IDs.

## Scope and safety

- ChongGrok is not affiliated with xAI, X, Apple or Google.
- Passwords, verification codes and recovery codes are not requested.
- No online service is risk-free, and no fixed recovery time or account outcome is guaranteed.
- This guide covers consumer memberships, not API credits or API billing.
- Ready-made accounts, SMS verification and bulk registration are outside this service.

{% include faq_en.html %}

## Official references

- [xAI Grok consumer FAQ](https://docs.x.ai/grok/faq)
- [X Premium FAQ](https://help.x.com/en/using-x/x-premium-faq)
- [Chinese SuperGrok paid-but-still-Free guide]({{ '/guides/supergrok-paid-but-still-free/' | relative_url }})
- [Weekly limit versus subscription guide]({{ '/guides/supergrok-weekly-limit-vs-subscription/' | relative_url }})

**Fact check:** July 24, 2026. Subscription interfaces and usage limits can change; verify the current official account page.
