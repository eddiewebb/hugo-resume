---
title: "Atlassian Deployment Triggers"
link: "https://bitbucket.org/atlassianlabs/bamboo-after-deployment-trigger/pull-requests/2/fixes-issue-2-eliminate/diff"
image: "/img/deploysonly.webp"
description: "Uses Async call to lucene index for super fast autocompletion to address performance issue loading config."
featured: true
tags: ["Java","jQuery","REST APIs","Bamboo","JSON"]
fact: "Reduce page load time from minutes to instantaneous."
weight: 100
sitemap: 
    priority : 0.8
---

Addressed pretty significant page load performance issue founde in larger deployments. Eliminates uses of intensive backend query, replacing it with an asynchronous API call against a lucene index. This change reduces page load from from 2+ minutes to nearly instant, with an incredibly responsive UI.
