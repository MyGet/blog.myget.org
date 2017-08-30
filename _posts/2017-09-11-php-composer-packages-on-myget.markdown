---
layout: post
title: "PHP Composer packages just arrived on MyGet"
date: 2017-09-11 07:42:02 +0100
comments: true
published: true
categories: ["post"]
tags: ["Community news", "Development", "Feature", "PHP", "Composer"]
author: "Maarten Balliauw"
---

<img src="/images/2017/09/logo-php-composer.png" alt="MyGet supports hosting private PHP Composer packages" align="right" />

Good news everyone! We just shipped <a href="https://www.phpcomposer.org/" target="_blank">PHP Composer</a> support (preview)! If you are building PHP applications and libraries, you can now package them and add these to your MyGet feeds.

PHP Composer support is still in preview and **[must be enabled on your MyGet subscription](https://www.myget.org/Home/GiveMeComposer) - click [here](https://www.myget.org/Home/GiveMeComposer) to do so**. Once enabled, you will have access to the <a href="https://docs.myget.org/docs/walkthrough/getting-started-with-php-composer" target="_blank">PHP Composer features described in our documentation</a>

## Which features are available?

We currently support almost all features we have available for other package managers. Of course you can upload your own packages (via the web UI as well as via a [<code>curl POST</code>](https://docs.myget.org/docs/walkthrough/getting-started-with-php-composer)) or packages from upstream repositories like [Packagist](https://www.packagist.org).

Packages can be consumed in any PHP Composer-based project. It's possible to proxy upstream repositories into your MyGet feed. You can manage permissions and users, inspect package licenses and vulnerabilities, ...

Build services are supported as well: as long as there is a `composer.json` in your repository, we'll run tests against it, package it up and make it available as a PHP Composer package on your Myget feed.

## Sounds great! How do I get started?

Quite easy: head over to [www.myget.org](http://www.myget.org), sign in (or register), and make sure to **[enable PHP Composer on your MyGet subscription](https://www.myget.org/Home/GiveMeComposer)**. Once done, you can create a feed and start adding packages. Our [getting started documentation](https://docs.myget.org/docs/walkthrough/getting-started-with-php-composer) has some more details on how to upload your first PHP Composer package to MyGet.

We're really excited about introducing PHP Composer support on MyGet! You can now use MyGet to securely host and collaborate on NuGet, symbols and sources, Chocolatey, PowerShell, NPM, Bower, Maven, PHP Composer and VSIX packages.

*Happy composing!*
