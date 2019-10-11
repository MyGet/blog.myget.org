---
layout: post
title: "Webinar Recap: Secure DevOps Starts with Secure Packaging"
date: 2019-08-01 14:00:00 -0500
comments: true
published: true
categories: ["post"]
tags: ["Community news"]
author: "Matthew Caponigro, Marketing Manager"
---
Earlier this month, MyGet Team Lead, Konrad Zuwala, joined us for a live webinar to talk DevOps, secure package management, and best practices for implementing secure package management in your DevOps toolchain.

In the webinar, we discussed why demand for better binary artifact management and private package repositories has grown significantly over the last few years, driven by three industry trends.

## 1. Open-source libraries, frameworks, and packages are changing the way modern software gets developed.

OSS has always propelled software innovation, but the growing popularity of a number of open-source libraries, frameworks, and packages across a variety of industries and applications has contributed to making modern software development faster and easier than ever before. These boilerplate frameworks save dev teams from “reinventing the wheel” and allow them to hyper-focus on the value streams associated with their products in order to deliver greater benefits to customers.

However, the proliferation of open-source packages and frameworks has also introduced new security and compliance challenges for enterprise development organizations (e.g. the widely-publicized exploitation of a vulnerability in the open-source package Apache Struts used in Equifax’s application, that gave hackers access to [143 million Americans’ information ](https://www.forbes.com/sites/thomasbrewster/2017/09/14/equifax-hack-the-result-of-patched-vulnerability/#7e5b75335cda) in 2017). Centralized package repos give security teams a chance to review open-source packages for security threats and license compliance before they enter your code base, and simplify dependency management for developers across multi-functional teams.


## 2. Orchestration and containerization are changing the way applications are built.
More and more organizations are replacing their monolithic applications with applications based on microservices, an approach to application architecture that [makes applications higher-performing, more resilient, and significantly easier to code]( [https://developer.ibm.com/articles/why-should-we-use-microservices-and-containers/). Whereas monolithic apps are typically deployed from a single executable binary artifact, microservices rely on containers composed of a myriad of dependencies, libraries, and packages built at various stages of development. This methodology puts pressure on organizations to find ways to efficiently and securely share and retrieve artifacts developed by multiple teams across an organization.

## 3. DevOps is important; security is nonnegotiable.
Over the last ten years, DevOps has gone from a bleeding-edge “nice-to-have” to a modern development standard—a requirement for high-performing development teams. Meanwhile, the number of security vulnerabilities and threat vectors faced by modern development organizations has grown exponentially.

Maintaining application security is paramount to the success of any software-driven business. While security-focused [testing tools](https://blog.assembla.com/new-integration-shift-security-left-with-the-all-new-assembla-kiuwan-static-code-analysis) and methodologies are important to AppSec, more and more organizations are recognizing the value of shifting their entire [security paradigm to the left](https://blog.assembla.com/the-future-of-source-code-security-is-consensus-based), addressing the [root causes of vulnerabilities at their source](https://www.csoonline.com/article/3226766/security-starts-at-source-code-in-the-cloud.html).

To learn more about building a layer of security around your dev team and the frameworks, packages, and libraries you use to build your application, watch a recording of our webinar (or download a PDF of the slides) here: [Secure DevOps Starts with Secure Packaging: An Introduction to MyGet](https://www.brighttalk.com/webcast/11505/362226).

--- 
MyGet provides private, hosted NuGet, npm, Bower, Maven, PHP Composer, VSIX, and PyPI package registries (with more on the way!) for individuals and enterprise software development teams. [Start a free 14-day trial and see for yourself.](https://www.myget.org/Account/Register)
