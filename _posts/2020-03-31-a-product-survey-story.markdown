---
layout: post
title: "A Product Survey Story: What We learned"
date: 2020-04-02 10:37:03 -0600
comments: true
published: true
categories: ["post"]
tags: ["Community news", "Development", "NuGet", "Stories", "Feature", "Python"]
author: "Cat Richardson"
---

# A Product Survey Story: What We Learned 🧐 


A little while back we invited the MyGet community to participate in our first annual product survey! We wanted to learn more about you, our customers, and about how you have been using MyGet to store, manage, and distribute your packages.

Thanks to your candid participation, we learned a tremendous amount about what you value most about MyGet and what we need to change. We are eager to share the results with you too, to help us all better understand the community that makes up MyGet! Here are our top takeaways from the results.


## Built by developers, for developers

First off, we learned more about you! As we think about continuing to build out the functionality of MyGet, it's so important to understand who actually uses our platform and what challenges you face. (In a world that is growing more and more remote, it’s important to stay connected as a community!)

Of the more than 750 folks that participated, more than 85% of you self-identified as having a technical role on your team, whether that be as a developer/software engineer (58%), architect (12%), DevOps/IT engineer (12%) or a Tester/QA team member (3%).

![Who uses my get?](/images/2020/Who-uses-MyGet.jpg "Who-uses-MyGet")


## .NET, JavaScript, HTML: The Top 3
In its early days, MyGet was lovingly introduced as  “NuGet-as-a-service”. That was the need it was built to solve—an easy way for you to get the benefits of a private NuGet server without the headache of managing installation or infrastructure. So it’s not surprising to see Microsoft .NET languages used most by MyGet community members.


![What programming language is most widely used?](/images/2020/What-programming-language-used.jpg "What-programming-language-used")


What _**IS**_  interesting is the percent of Python users that have joined MyGet over the last year. Python developers represent the largest percentage of the MyGet community outside of .NET, JavaScript and plain HTML/CSS, outdoing Java developers by 2%. We’re no longer just a NuGet family; the MyGet tent has grown and some of you have spread your programming wings. 😭

On one hand, it might be expected to see a fair number of responses from Python developers in our survey results, given Python’s ever-growing popularity. (According to [RedMonk Programming Language Rankings](https://redmonk.com/sogrady/2020/02/28/language-rankings-1-20/) Python has climbed into the number two spot in terms of most widely-used programming languages.)

But on the other hand, our Python PyPI support is one of the most recent functionalities we have added to MyGet. It’s reassuring to see how many members of the MyGet community benefitted from the addition of Python packages alongside their NuGet, npm, Bower, Maven, and Composer packages. In less than six months, Python PyPI packages climbed to the number 5 spot in our list of most-used package formats, surpassing other package manager types that we’ve supported for much longer and knocking on Maven’s doorstep for the number 4 spot.


![What package manager do you use?](/images/2020/What-Package-manager-does-your-team-use.png "What-Package-manager-does-your-team-use")



## How does MyGet fit into your DevOps lifecyle?  

Over 98% of you responded that you are currently using source control for the proprietary code you write, which is a good thing: source control is a must-have for modern software development. Almost 100% of you who use source control are using Git, with Github, Azure DevOps (split between cloud and server), Bitbucket, GitLab, and Assembla coming in as your top five hosting platforms.


![What tools do you manage your source code with?](/images/2020/Whats-source-code-do-you-use.jpg "Whats-source-code-do-you-use")


One of the most effective ways to leverage the artifacts you store in MyGet is to integrate MyGet with your CI/CD processes. More than 85% of you responded that you have already embraced the continuous delivery and integration, using a myriad of tools such as Azure DevOps, Jenkins, TeamCity, GitLab, Bamboo, Appveyor, and Travis CI to run your builds and push build artifacts to MyGet.


![What do you use for CI/CD?](/images/2020/What-do-you-use-CI-CD.jpg "What-do-you-use-CI-CD")


## Why do you use MyGet?

Because of its nature as a hub between multiple spokes of the SDLC, the number of different use cases for MyGet can be quite varied. That said, over 68% you reported using MyGet to share your private packages within your internal team. The next three most-reported use cases each had about the same number of responses:  23% of you use MyGet to store build artifacts, 21% responded that you use MyGet to control the open source packages used in your dev environment, followed closely by the 20% of you using MyGet to host open-source packages you have built and shared with the community/public. 


![What's your primary use?](/images/2020/What-is-your-primary-use.png "What-is-your-primary-use")


## What did you ask us to prioritize next?

MyGet’s success depends on our ability to continually improve features that make your lives easier and help you ship better products. Despite the rise and adoption of 3rd-party CI/CD platforms across the MyGet Community, more than 75% of you said that updating MyGet’s build services to support .NET Core 3 and C# 8 was still important to you. Improving uptime and availability, your second-most requested improvement, has been high on our priority list for a while as well, so we are glad to see that this aligns with the concerns you have. Your feedback has been enormously helpful as we’ve been culling down our roadmap for this next fiscal year. Thank you again for your candid input—we are going to be able to be much more focused on delivering the improvements that matter to you because of it!


![What should we do next?](/images/2020/What-should-we-do-next.jpg "What-should-we-do-next")



## Wrapping things up!

We’re glad we could share these insights with you. The more we can connect and learn how you like using MyGet, the better we can help you manage your packages and ship better products. 

Please reach out! We love hearing your stories and suggestions. You can reach us at [support@myget.org,](mailto:support@myget.org) start a chat with us at [https://myget.org,](https://myget.org) or connect with us on [Twitter](https://twitter.com/mygetteam) or [Facebook](https://facebook.com/mygetteam). And be sure to regularly check out our [UserVoice](https://myget.uservoice.com/forums/135675-general) page to vote on our roadmap and stay up to date with our most recent releases (like our [NuGet Symbol Server update](http://blog.myget.org/post/2020/03/05/myget-nuget-symbols-snupkgs.html), which was your top-voted request on UserVoice)!  
 
