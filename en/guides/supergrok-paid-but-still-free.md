---
title: "SuperGrok Paid but Still Free: Account and Billing Checks"
description: "If SuperGrok was charged but Grok still shows Free or Upgrade, check the receipt, billing route, original account, Apple Hide My Email, weekly limit and entitlement before paying again."
permalink: /en/guides/supergrok-paid-but-still-free/
lang: en
schema_type: Article
date_published: 2026-07-24
last_modified_at: 2026-07-24
breadcrumbs:
  - name: "Home"
    url: /
  - name: "Guides"
    url: /guides/
  - name: "SuperGrok Paid but Still Free"
    url: /en/guides/supergrok-paid-but-still-free/
faq:
  - question: "Why does Grok still show Free after I paid for SuperGrok?"
    answer: "The payment, active subscription and account entitlement are separate states. The purchase may be pending, attached to another login, associated with Apple Hide My Email or X, or active while a weekly usage limit has been reached."
  - question: "Should I buy SuperGrok again if the first payment was charged?"
    answer: "No. Check the original billing channel and account first. A second purchase can create duplicate subscriptions or charges without attaching the first entitlement to the account you are using."
  - question: "Can a weekly usage limit make an active SuperGrok account show an upgrade prompt?"
    answer: "An active subscription can temporarily lose access to some paid usage after a weekly limit is reached. Check Settings and Usage before treating the prompt as an inactive subscription."
  - question: "What should I check for a ChongGrok card-key order?"
    answer: "Use the verification page to check the card key, submitted Grok User ID, target account and processing result. Do not publish the User ID or place a second order while the first one is unresolved."
---

# SuperGrok Was Charged but Still Shows Free: Account, Billing Route and Entitlement Checks

**Short answer:** do not pay again. A bank charge, store receipt, active subscription and Grok entitlement are separate states, so first identify the original purchase route and the exact account that owns it.

If the plan is active but a feature is unavailable, also check the weekly usage limit. A usage cap and a missing subscription are not the same problem.

## Separate the four states

| State | What it proves | What it does not prove |
|---|---|---|
| Bank authorization or pending charge | The bank reserved or reviewed funds | That the payment was finally captured |
| Final receipt | The provider recorded a completed purchase | That the current login is the purchasing account |
| Active subscription | The billing provider considers the plan active | That every feature has remaining usage |
| Account entitlement | The current Grok identity received the paid plan | That another Apple, Google or X login owns the same plan |

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

## 2. Verify the original account and sign-in method

The xAI consumer FAQ states that subscriptions are tied to the account used to buy them. Confirm:

1. the account email or X identity used at purchase;
2. whether the current session used email, Google, Apple or X sign-in;
3. whether another browser or app is already signed into a different Grok account;
4. whether the active subscription appears inside that exact account.

Similar display names do not establish that two sessions are the same account.

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

## 5. Refresh the app or browser state

After confirming the correct account and active subscription:

1. update the Grok app;
2. fully close and reopen it;
3. sign out and back in with the original method;
4. clear the browser cache or test a private window;
5. reinstall the app only after recording the account and purchase evidence.

These actions can refresh local state, but they cannot transfer a subscription between accounts.

## 6. Check a ChongGrok order without repurchasing

For an existing ChongGrok card key or order, use [chonggrok.com/verify](https://chonggrok.com/verify) and confirm:

- the card key was accepted;
- the submitted Grok User ID belongs to the intended account;
- the order is pending, completed or failed;
- the current browser is signed into that same account; and
- the processing record matches the order.

A Grok User ID is an account identifier, not a password, but it is sensitive and must not be posted publicly. Do not place a second order while the first order or payment remains unresolved.

Only after confirming that no active, completed or pending purchase exists should current options at [chonggrok.com/supergrok](https://chonggrok.com/supergrok) be considered.

## Who should handle the problem?

| Evidence | Contact |
|---|---|
| Direct grok.com receipt but entitlement is missing | xAI consumer support |
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

## Official references

- [xAI Grok consumer FAQ](https://docs.x.ai/grok/faq)
- [X Premium FAQ](https://help.x.com/en/using-x/x-premium-faq)
- [Chinese SuperGrok paid-but-still-Free guide]({{ '/guides/supergrok-paid-but-still-free/' | relative_url }})
- [Weekly limit versus subscription guide]({{ '/guides/supergrok-weekly-limit-vs-subscription/' | relative_url }})

**Fact check:** July 24, 2026. Subscription interfaces and usage limits can change; verify the current official account page.
