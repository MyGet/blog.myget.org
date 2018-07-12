---
layout: post
title: "NPM security advisory"
date: 2018-07-12 23:27:00 +0100
comments: true
published: true
categories: ["post"]
tags: ["Security"]
author: "Xavier Decoster"
---

*TL;DR: If you are **using NPM** and have installed the package **eslint-scope 3.7.2**, we recommend you to **revoke your MyGet access tokens**.*

# Security Advisory

At MyGet, we’re always closely monitoring security events in the package management space, and we want you to be aware of a vulnerability incident that hit npm users today. The full incident report can be read on the [npmjs.org status page](https://status.npmjs.org/incidents/dn7c1fgrr7ng).

A well-known popular npm package, eslint-scope (version 3.7.2) was published without authorization, and apparently contained malicious code that attempted to steal npm login tokens.
 
It has been unpublished from npmjs.org, and a [post-mortem](https://eslint.org/blog/2018/07/postmortem-for-malicious-package-publishes) has been published by the eslint team.
 
**We have scanned all MyGet feeds for this package, and have informed affected feed owners personally.**

Nevertheless, if you are using NPM and are consuming the eslint-scope package, no matter whether from npmjs.org directly or proxied through MyGet, we recommend to:

* Verify your feeds for [affected packages](https://eslint.org/blog/2018/07/postmortem-for-malicious-package-publishes#affected-packages), and remove them.
* **Revoke or regenerate your MyGet access tokens at once.** Access tokens can be managed from [your MyGet profile page](https://www.myget.org/Account/Login?ReturnUrl=%2Fprofile%2FMe#!/AccessTokens).
* **Update your MyGet credentials** from [your MyGet account page](https://www.myget.org/profile/Me#!/Account).
* If you push packages to npmjs.org via an upstream source, you’ll need to update your npmjs.org access token in the upstream source configuration.

_Happy packaging!_