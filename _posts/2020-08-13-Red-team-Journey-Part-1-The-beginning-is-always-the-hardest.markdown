---
layout: post
author: "Tony"
permalink: 2020/08/Red-team-Journey/Part-1-The-beginning-is-always-the-hardest
title:  "Red team Journey - Part 1 - The beginning is always the hardest"
date:   2020-08-13 22:00:00 +0700
categories: Redteam
description: "I just finished building my little red team with a lot of results after more than a year of work, and now I’m starting with building a second red team. Why do I need two red teams? What difficulties have I encountered and what experience have I gained from it? These will be the questions that I will answer in this article, the first in a series of articles about my work and study journey with red team role."
cover: "assets/img/2020/08/redteam.jpg"
tags:
  - Redteam
  - Journey
  - Talk
---

I have been busy this year, a year with many changes. Fortunately, today I had time to write down the first few lines of my blog.
I just finished building my little red team with a lot of results after more than a year of work, and now I'm starting with build a second red team.

- Why do I need two red teams?
- What difficulties have I encountered?
- What experience have I gained from it?

These will be the questions that I will answer in this article, the first in a series of articles about my work and study journey with the red team role.

<!--more-->

## The first mission

At the end of 2018, I accepted an offer for a new job. From being a red team member, I became a leader of the red team. My initial mission was to build a small group of people with the skills to `actively` and `continuously` detect threats `from outside` for my clients. Possible tasks include: warning about data breaches, warning about serious vulnerabilities that exist on the external application, up to early warning of any threats we may know.

What is the problem here? In addition to working with limited resources in the early days, I also need to recruit the first members of the red team. Because we have to complete the mission of quickly localize and identify major potential threats first. I do not want to face an incident as soon as I take over, which is why we have to detect and resolve them early.

In the beginning, we also had only the right to monitor public systems. Public systems consisted of hundreds of web applications and mobile applications from large to small, a lot of public servers with many services direct exposure to the Internet. We can also only monitor a small number of internal applications and systems. But we are not nearly allowed to run any internally targeted red teaming operations.
So how did I solve those problems?

### Identify immediate threats

During the first year, I realize that we will probably have to deal with three main threats:

- `Threats come from weak management of public IT assets`. This vector can pull up to lots of vulnerabilities. For example, exposure of sensitive path from web applications, exposure of staging environment, exposure of weak web app from an un-known subdomain. Any hacktivist can find and exploit them.
- `Threats come from data breaches`. This threat can be divided into two categories, first of which are employees sharing passwords that have been leaked for sensitive accounts. The second is information leaked from administrators or developers to the Internet. For example, exposure of source code containing credentials on Github, administrative information posted to PasteBin or Google Group, etc.
- `Threats come from weak passwords and weak authentication`. For example, a lack of a multi-factor authentication layer or the application has vulnerabilities that allow bypassing authentication.

It is one of the big problems that we need to address immediately. By solving these problems, my clients will also gradually trust us and allow us to initiate red team campaigns to look for more complex vulnerabilities. For example allowing us to target internal systems, conduct a security awareness assessment for the user, and adversary emulation.

### Recruitment

With big problems that need to be resolved immediately, I decided to hire two employees to focus on web applications. The characteristic of these two employees is that they are not too excellent. They are not the type of employees that often appear in the hall of fame boards, discover 0day or write 1day. They don’t even like coding. However, they have a lot of experience to work as a hacktivist. With a lot of resources, practical experience, and especially sources of information, that makes it possible for them to quickly find major problems in the first year. Finding these 02 employees is very easy and fast, save me a lot of time from search for senior staff and interviews. I will need seniors, but not now.
Over the next few months, I recruited a senior mobile-centric employee. He works for the Penetration testing team, which is an independent group from the red team. However, because I was the one who trained him in mobile apps, so he joined me in the mobile offensive segment on some projects. I also recruited another senior employee. He is a researcher with the mission is to research for 0day, develop 1day PoCs.

So my team has 03 permanent members along with 01 non-permanent members. We worked with this squad for almost a year.

### Action

During the first year, I encourage members to hunt which is not limited to scope. The red team's mission is to work as bounty hunters to look for any weaknesses that could be exploited from outside. In less than a year we discovered and warned thousands of critical security vulnerabilities for our clients, quickly reducing the attack surface. A large number of critical security warnings were sent out to my customers that will help increase security awareness for my clients. My clients will come to pay more attention to establishing security processes and regulations, especially the management of public IT assets, or building security vulnerability management measures.

From my company, we have an internal bug bounty program where any other team in the company can report if a security issue related to the client was found. All such reports will be verified by the red team and alerted to clients. With that said, we also have a Penetration testing team that is independent of the red team. The penetration testing team makes it possible for our clients to use the penetration testing service to take a closer look at each of their systems.

### Defect

Of course, with the use of human resources above, the strategy focusing on the perimeter will not be a long-term solution. Threats don’t just come from outside. Most APT attacks come from exploit user awareness (social engineering) or internal threats. The goal that I set for my second year is to start implementing red teaming campaigns in the internal network, focusing more on infrastructure. Perform adversary simulation campaigns to test the defense system. Perform advanced persistent threat simulation, regular security awareness assessment, and other types of operations.

If you remember, I said that the first year I encouraged the members to work as bounty hunters. What do you think is acting as a bounty hunter in a very large scope? That is the omission of vulnerabilities. They can only focus on a few goals at a time, and they will miss the rest. If they don’t want that to happen, they have to develop automated scanning and tracking systems, which we call bots. However, I remind you that they don’t like programming even when I keep encouraging them.

### Roadmap

Fortunately, in the first year besides implementing my first plan, I also prepared a plan for the next year, which I am working on.
In the second year, I quickly built a second red team, second red team focused more on what the first red team couldn’t do. The second red team consists of more skilled individuals who can solve complex problems. They focus on `advanced persistent threat simulation and malware research`. Members of the second red team are too familiar with the development of security applications, so they are also tasked with `developing tools and systems to automate jobs`.

As for the first red team, I kept them preparing for new clients. For old clients, the first red team will work as a reconnaissance team. The first red team is especially useful when with their experience they often make it easy for us to complete an initial compromise phase.

## Conclusion

In the first year, I have built a red team that has the strength of scouting, working as bounty hunters focused on finding any possible outside threat against a business. In the second year, I continued to build a second red team to address the weaknesses of the first red team. The second red team focuses on solving complex issues like malware research or simulation advanced persistent threat and adversaries, more focus on infrastructure offensive and internal corporate threats, security awareness of users, weaknesses in defense systems.

`I think both of my red teams also represent the current 02 red team building trends in the world. Most red teams in the West are very concerned with malware and emulation of adversaries, while red teams in Southeast Asia are more focused on web and mobile applications as well as network perimeter.`

Anyway, I think a business should maintain both of these aspects. If you are a business providing security services, you should maintain both capabilities for the red team. If you are a normal business, you should also maintain both. However, you can choose between maintaining an internal red team or using a third-party service. For example, you could maintain an internal red team to run internal red team campaigns in conjunction with using a third-party service to track public IT assets, data breaches or early warning of̀ outside threats. Building a bug bounty program is also a good plan.
