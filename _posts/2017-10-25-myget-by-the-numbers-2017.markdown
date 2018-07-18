---
layout: post
title: "MyGet by the numbers 2017"
date: 2017-11-17 13:00:00 +0200
comments: true
published: true
categories: ["post"]
tags: ["Development", "Stories"]
author: "Xavier Decoster"
---

Since our [previous MyGet by the numbers](https://blog.myget.org/post/2016/07/28/myget-by-the-numbers.html) post in July 2016, MyGet has grown a lot! We've added support for two additional package managers: [Maven](https://blog.myget.org/post/2017/02/09/maven-packages-just-arrived-on-myget-early-access-preview.html) and [PHP Composer](https://blog.myget.org/post/2017/09/11/php-composer-packages-on-myget.html), bringing the total number of support package managers to 6 (*NuGet, npm, Bower, Visual Studio Extensions, Maven, PHP Composer*), and debugger symbols, of course.

As MyGet has been growing, we've also been facing various challenges in terms of scalability. In the face of those challenges, we're proud on our uptime numbers and have been working hard on improving MyGet's scalability and reliability. We still have work to do to further improve performance which will receive great attention going forward. We figured it'd be an interesting story to share with you. Of course we can’t share all of our statistics, but it’s always fun to look at them. 

## Shared Infrastructure

MyGet is hosted on Microsoft Azure and has regional deployments in Europe and US. MyGet has a shared tenant, [www.myget.org](https://www.myget.org), home of the personal subscription plans (Free, Starter and Professional subscriptions). [MyGet Enterprise](https://www.myget.org/enterprise) tenants run on their own dedicated infrastructure, which may differ from what is outlined below.

The shared tenant has its primary deployment in the West Europe region, and a secondary in US East. We use Azure Cloud Services to deploy both Web and Worker roles, and apply auto-scaling policies on both to ensure the service scales as needed.

On average, the shared tenant has 4 Web roles and 4 Worker roles deployed in each region, and scales in and out multiple times (minimum 2 instances per role, up to 8 during peak moments). Judging by the observed peak moments, all of us restore most packages in the morning (which is multiple times a day when running a global service, but mostly EU CET morning and US PST morning).

## Reliability

Being developers ourselves, we know how frustrating it is when a service you use on a daily basis goes down. Even though we cannot offer an official SLA just yet, we can demonstrate historical uptime data on our [status page](https://www.myget.org/status). We invite you to go take a look if interested (and it lists uptime data for other endpoints too). 

The most interesting data point for package consumers is likely the following one: package download uptime. We're happy to share that, in 2017, we're currently on track to exceed the 99.99% uptime goal we set ourselves!

Currently, the package download endpoint has an uptime percentage of **99.991%**! In other words, the endpoint has been down for 40 minutes in 2017, spread out over 6 different days, so that's 6 days this year with an average interruption of less than 6 minutes and 40 seconds. If you didn't do a restore during those brief interruptions, you likely haven't noticed this interruption at all. If you did, we're very sorry, and please know that we'll continue to work hard to further improve on this metric.

## Scalability: storage, traffic and bandwidth

The below numbers include all supported package types.

Our shared tenant currently hosts **over 20 million packages** (in comparison, that's 20x nuget.org, or 40x npmjs.com!), consuming **770GB of blob storage**. This does not include back-ups to cover for human error, and does not include metadata extracted during upload to facilitate querying. That is significant growth compared to July last year, when we hosted 1 million packages in total. 

**On a monthly basis, over 550K packages are pushed to this tenant**, with an average success rate of **98.05%**. Success means: the package actually ends up on the feed. So 1.95% of packages are rejected because they fail server-side validation.
Wednesday and Thursday seem to be the most productive days of the week with around **45K packages pushed on a single day**!

In terms of bandwidth, MyGet's shared `www.` tenant serves around **10M requests a day** with an **average response time of 93.58ms**, accounting for **220GB egress, and 40GB ingress per day**. If we add CDN egress to those numbers, we end up with **410GB egress per day**. On a monthly basis, this single MyGet tenant accounts for **12TB egress traffic**!

MyGet currently handles approx. **200 requests / second on average**, with regular peaks up to **500 requests / second**, and every now and then we experience a **burst of 2000 requests / second** hammering our service.

And these are just the numbers for our shared tenant. We have MyGet Enterprise customers exceeding these metrics with ease.

One of those other tenants, which many of you may know and use, is the .NET Foundation tenant (hosted at [dotnet.myget.org](https://dotnet.myget.org)).
This tenant is the home of e.g. the [`dotnet-core`](https://dotnet.myget.org/gallery/dotnet-core) NuGet feed, which in itself already consumes **over 3TB of blob storage**. 

![](../Images/2017/10/dotnet-core.png)

Hosting **over 840K package versions not evenly distributed over just 2000 unique package id's** is something that NuGet clients do not like, and the NuGet protocols can't handle very efficiently today. This is a unique scalability challenge that is likely to surface on nuget.org too at some point (or maybe [already has for some packages with many versions](https://github.com/NuGet/NuGetGallery/issues/4859#issuecomment-337455878), e.g. Fake and RavenDb.Client). In fact, [we reported a very detailed issue](https://github.com/NuGet/Home/issues/4448) discussing this.

We have a few ideas on how MyGet can potentially deal with such scenarios better going forward, but until we handled that, we strongly recommend you to apply some [retention policies](https://docs.myget.org/docs/reference/package-retention), or archive the package versions you no longer need (on a different feed, on a tape drive, whatever works for you).
You can in fact automate this today leveraging our [webhooks](https://docs.myget.org/docs/reference/webhooks) support. We even have a sample [custom retention policy implementation using webhooks](https://docs.myget.org/docs/reference/package-retention#Custom_package_retention_rules_using_webhooks) for you to build upon.

This recommendation is not only applicable to NuGet, but applies to all package types. Ensuring a smooth experience is much easier when only retaining the packages you actually need. And, as it turns out, some package manager protocols are much more efficient in dealing with this than others.

## Customer satisfaction

This is what really drives us: customer success! 
MyGet can only be successful when you are, our customers. 
Customer satisfaction (also known as CSAT) is a good indicator for how successful you are in using our services.

We're conducting another Net Promotor Score (NPS) survey to keep in touch with *your* experience, and we're really happy with the feedback we got from you so far! 
Thank you all who already provided feedback, and thank you for your continued trust and support!

If you like what we're doing at MyGet and didn't get a chance to respond to the survey, we'd really appreciate if you could spend 10 seconds to let us know how we're doing: **[How likely are you to recommend MyGet?](https://www.surveybuilder.com/s/1bV59)**! 
And if there's anything we can and should improve, let us know!

*Happy packaging!*