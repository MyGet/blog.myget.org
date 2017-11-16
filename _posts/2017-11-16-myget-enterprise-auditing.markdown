---
layout: post
title: "Inspecting audit logs in MyGet Enterprise"
date: 2017-11-16 07:43:03 +0100
comments: true
published: true
categories: ["post"]
tags: ["Community news", "Development", "Feature", "Enterprise"]
author: "Maarten Balliauw"
---

A couple of weeks back, we released an audit log viewer on [MyGet Enterprise](https://www.myget.org/enterprise). Administrators of a MyGet Enterprise plan can inspect every action that happens on their MyGet instance and see who did what, when, and where.

From the [MyGet Enterprise administration dashboard](http://docs.myget.org/docs/reference/myget-enterprise), all actions performed on the Enterprise installation can be consulted:

<img src="/images/2017/11/audit-entries.png" title="Audit entries" />

The list of audit entries is searchable and can be exported to a CSV file so additional querying can be done in, for example, Excel. Details for each audit entry can be consulted and display the action that was performed, who performed it, and where it as executed. We can also see the location the user performed the action from, including the IP address (last octet always 0 for privacy reasons).

<img src="/images/2017/11/audit-entry-details.png" title="Audit entry details" />

With audit logs available on [MyGet Enterprise](https://www.myget.org/enterprise), we are confident MyGet can help larger teams and enterprises with auditing and dependency lifecycle management.

*Happy packaging!*