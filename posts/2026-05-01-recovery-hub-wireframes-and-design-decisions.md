---
title: Recovery Hub Wireframes and Design Decisions
date: 2026-05-01
author: Fanxin
summary: A reflection on how my Recovery Hub wireframes developed the project concept and how class discussion changed my next design decisions.
tags:
  - advanced web design
  - wireframes
  - interaction design
  - recovery hub
---
This week I turned my Recovery Hub concept into a set of wireframes. In earlier posts, I focused on why a recovery-based community needs to work differently from a general fitness platform. The main problem was not just that users need more information. It was that they need information which matches their current recovery stage, their uncertainty, and the kind of progress they are trying to make.

The wireframes helped me test that idea as an interface. Instead of beginning with a generic feed, I mapped out a hub that includes a home page, recovery context setup, a stage dashboard, structured recovery logs, a discussion detail page, and an explore page. Together, these screens show how the platform could guide users from their current recovery situation toward more relevant community content.

[View the full Recovery Hub wireframe file in Figma](https://www.figma.com/design/A0MZb1NDSbtWS2HBV9BeE2).

![Overview of the Recovery Hub wireframe board](assets/wireframes/recovery-hub-board.svg)

The main design principle behind this version was relevance. A person returning to exercise after an injury is usually not browsing in the same way as someone looking for general fitness inspiration. They may be asking whether an exercise is safe, whether a pain response is normal, or whether other people at a similar stage have experienced the same problem. Because of that, the interface needs to reduce noise rather than simply increase engagement.

In the first wireframe version, the home page included a large area for finding people recovering at the same stage. This made sense because matching similar users is one of the core values of the concept. However, after discussing the wireframes in class, I realised that this search task may not belong on the home page as the main focus.

![Initial Hub Home wireframe](assets/wireframes/hub-home-wireframe.svg)

The home page should probably feel more like a calm entry point. It can show the user's current recovery context, recent relevant content, and prompts to continue logging progress. If the first thing users see is a large search panel, the page may feel like it is asking them to do too much too early. For someone recovering from injury, the interface should create orientation first, then discovery.

This is why one of my next changes will be to move the "find people recovering at your stage" idea into the Explore section. Explore is a better location for active searching, filtering, and comparing experiences. Users who want to look for similar people, similar injuries, or similar recovery goals can still do that, but the behaviour becomes part of a discovery flow rather than the default home page experience.

![Explore Community wireframe](assets/wireframes/explore-community-wireframe.svg)

The class discussion also helped me rethink how pain level should work. In my first model, pain level was part of the user's recovery context, almost like something they would update manually in an account or profile area. That now feels less appropriate. Pain level changes often, and asking users to maintain it separately could create duplicated work.

A better approach is to make structured recovery logs the source of that information. When users create a log, they can record pain before and after an activity, symptoms, confidence, and limitations. Over time, the system can use those logs to reflect the user's current state. This makes the data feel more connected to real activity instead of becoming another profile setting that users might forget to update.

![Structured Recovery Log wireframe](assets/wireframes/structured-log-wireframe.svg)

This change also supports the larger concept of the hub. The value of the community is not just in open-ended posting, but in structured experiences that other people can compare meaningfully. If recovery logs include stage, symptoms, pain response, and progress markers, then the platform can connect users through context rather than popularity.

The next design step is to simplify the home page and make the information architecture clearer. Home should focus on orientation and recent relevant content. Explore should become the main place for finding similar users and discussions. Logs should become the main way that recovery state changes over time. These changes make the design feel more realistic because they separate three different behaviours: checking in, discovering, and recording progress.

Overall, the wireframing process helped me move from a broad concept into a clearer system. Recovery Hub is not just a community with fitness content. It is a community organised around recovery stage, structured self-reflection, and the reassurance that comes from seeing relevant experiences from other people.
