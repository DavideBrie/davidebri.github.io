---
layout: post
title: 2 Factor Authenticator explained
description: What's a 2FA and how it works. 
summary: What's a 2FA and how it works. 
tags: security
minute: 2
---
# 2FA REVERSE ENGENEERING

First of all, let's dive in and talk about what's a 2 Factor Authentication.

Everybody nowadays experienced at least once, after inserting the login credentials to enter a website, the other "tedious" step of writing a temporary code, send via text messages as token or generated via an authentication app (2FA).

This last step can save your accounts to be hacked. Because it's One-Time 6 digit code and expires in less than a minute, can offer a second layer of security.


Thus even if someone knows your login credentials or stole them, they still not be able to enter if they don't have access to your 2FA app.


This, in short, it's how 2 Factor Authentication works.

## Why it's called 2-Factor Authentication

To identify yourself into a system, you could be asked 3 main things:

1. Something you **know**.
2. Something you **are**.
3. Something you **have**.

As can you imagine a two factor, involve 2 of these 3 things. One example, equivalent to 2FA, that we use in our everyday life, is when we go to an ATM to withdraw some money, we **have** a bank card and we know the pin of it.


What about the something we **are**? \
We're talking about biometrics, for example, fingerprint or face recognition, a great method, but still not perfect.

## How a 2FA code it's made

If you're not familiar, here's a screenshot of the Google Auth app. 

![](https://joshmoulin.com/wp-content/uploads/2015/07/Google-Authenticator.png)

As you can see, there is a code for each account and there is a little pie timer that lasts 30 seconds, at the end of it, it will generate a new one.

This it's basically made by an algorithm that randomly outputs a 6 digit code. This can be implemented in different ways, for example, they could be based on TOTP a Time-Based One-time Password.

You may know wondering, since it's random, how the site we are trying to log in is capable of recognizing the right 2FA code.

When you enable this layer of security, the site will give you a QR code or a string, that we have to input in the app so it can start generating codes, for that site.

That string is a secret key, assigned to your account, that it's combined, in case the app used a TOTP-based algorithm, with a timestamp to generate a new code every 30 seconds.


## Can 2FA be reverse engeneered ?

No. If we use a well-known third-party software and someone gets our code, they can't use it to predict the new ones. The only method they have it's to get access to the third-party app that we use to generate codes.


## 2FA Third-party apps - Wich is the best?

As always there are different options to choose from, but by my experience, I can tell that when if you're dealing with multiple accounts, my advice is [Authy](https://authy.com/) since having a lot of feature like:

- Password protection
- Push notifications
- Encrypted **Backup**
- And many more...

And the migration from Google Authenticator was really easy.
