---
title: "Grok User ID / UUID: How to Find and Verify It"
description: "Find the Grok userId used for ChongGrok account verification, distinguish it from an email, X handle or xUserId, and submit only the minimum required identifier."
permalink: /en/guides/grok-user-id/
lang: en
schema_type: Article
date_published: 2026-07-23
last_modified_at: 2026-07-23
breadcrumbs:
  - name: "Home"
    url: /
  - name: "Guides"
    url: /guides/
  - name: "Grok User ID"
    url: /en/guides/grok-user-id/
faq:
  - question: "Is a Grok User ID the same as an email address or X username?"
    answer: "No. For ChongGrok verification, the requested value is the userId account identifier. An email address, display name, X handle and xUserId are different fields."
  - question: "Is a Grok User ID a password?"
    answer: "No. It is an account identifier, but it should still be treated as private account data and submitted only through the verified service flow."
  - question: "Why do people search for a Grok UUID?"
    answer: "The userId commonly appears in UUID form, so users often call it a Grok UUID. Do not rely on appearance alone; copy the exact userId field requested by the verification flow."
  - question: "Is Grok User ID required by xAI to buy SuperGrok?"
    answer: "No. Grok User ID is used by ChongGrok to verify the target account during fulfillment. It is not presented as an xAI requirement for a normal official subscription purchase."
---

# Grok User ID / UUID: How to Find and Verify the Correct Account Identifier

**Short answer:** for ChongGrok account verification, use the exact `userId` value from the currently signed-in Grok account. Do not submit an email address, X handle, display name, `xUserId`, password, verification code or recovery code instead.

This identifier is part of **ChongGrok's fulfillment process**, not an xAI requirement for purchasing SuperGrok directly. A Grok User ID is not a password, but it remains private account data and should not be posted publicly.

## Which value is the correct one?

| Value you see | Is it the requested Grok User ID? | Action |
|---|---:|---|
| `userId` | Yes | Copy only this field |
| Email address | No | Do not use it as the User ID |
| X username or handle | No | It identifies an X profile, not this field |
| `xUserId` | No | Do not substitute it for `userId` |
| Password, code or recovery data | Never requested | Do not share it |
| Full session response | Contains more data than needed | Do not publish or submit the whole response |

## Safe verification sequence

1. Sign in to the **Grok account that should receive the membership**.
2. In the same signed-in browser, open the current session view used by the ChongGrok instructions:

   ```text
   https://grok.com/api/auth/session
   ```

3. Locate the field named exactly `userId`.
4. Copy only its value and check that no spaces or surrounding quotation marks were added.
5. Return to the verified ChongGrok flow and confirm that the target account is your own before submitting.

This session response is an internal account view and may change without notice. The current Chinese walkthrough documents the service-side method and screenshots: [Grok User ID 怎么找]({{ '/guides/grok-user-id/' | relative_url }}).

> **Minimum-data rule:** never paste a complete session response into a public post, support forum, shared document or screenshot. If the page contains several account fields, expose only the exact identifier required by the verified form.

## Grok UUID versus Grok User ID

Search queries such as `grok uuid` and `grok user id` often describe the same practical task because the `userId` value commonly looks like a UUID. The visual format is not the deciding factor, however. The safe rule is to copy the field explicitly named `userId`, not another UUID-shaped value from the page.

Do not assume a permanent prefix or length beyond what the current account page displays. xAI may change internal presentation, and this guide does not claim an undocumented xAI subscription interface.

## When the User ID cannot be found

Use this order:

1. confirm that `grok.com` is signed in rather than showing a logged-out or expired session;
2. confirm that the browser account is the intended target account;
3. reopen the current verification instructions instead of using an old bookmark or screenshot;
4. avoid switching among Google, Apple, X and email sign-in methods without checking whether they open different Grok accounts;
5. contact ChongGrok support through the service page if the current form no longer matches the guide.

Do not guess a value or submit an identifier from another account.

## Privacy and service boundary

- ChongGrok does not need your account password, email verification code or recovery code.
- A User ID is less sensitive than a password, but it is not public profile content.
- Submit it only through the verified service workflow and only for your own account.
- ChongGrok is not affiliated with xAI or X.
- No online service is risk-free, and this guide does not promise a guaranteed account outcome.
- This knowledge base covers membership subscriptions, not API credits, ready-made accounts, SMS verification or bulk registration.

## If the account already has a charge or pending order

Do not buy again. First verify the original billing channel and account status using the [SuperGrok charged-but-still-Free guide]({{ '/guides/supergrok-paid-but-still-free/' | relative_url }}).

Only after confirming that there is no active or pending subscription should a new membership path be considered. Current service details are available at [chonggrok.com/supergrok](https://chonggrok.com/supergrok).

## Official and service references

- [xAI consumer Grok FAQ](https://docs.x.ai/grok/faq)
- [Chinese Grok User ID guide]({{ '/guides/grok-user-id/' | relative_url }})
- [AI membership safety checklist](https://he20000405-pixel.github.io/en/resources/ai-membership-safety-checklist/)

**Fact and procedure check:** July 23, 2026. Product interfaces and sign-in behavior can change; use the current official pages and ChongGrok verification instructions.
