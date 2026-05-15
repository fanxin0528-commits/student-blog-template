---
title: Turning Recovery Hub Design into a Course-Aligned SQLite Prototype
date: 2026-05-14
author: Fanxin
summary: A reflection on moving Recovery Hub from high fidelity design into a course-aligned SQLite web prototype with clear routes, data, and validation.
tags:
  - advanced web design
  - recovery hub
  - sqlite
  - mojo
  - prototype
---
This week I focused on turning Recovery Hub from a high fidelity design direction into a working A2 prototype that follows the course workflow more clearly. The goal was not only to make the interface look like the Figma screens, but also to make the app behave like a small data-backed web prototype that can be tested through real pages, forms, and SQLite queries.

The main idea of Recovery Hub is still the same: it is a BlaBla community hub for people who want recovery-stage relevant support. It is not a general fitness feed and it is not trying to become a medical tracking product. The prototype is organised around recovery context, structured logs, similar community content, and a clearer separation between checking in, exploring, and recording progress.

One important decision was keeping Home simple. Home now works as a recovery snapshot. It shows the current recovery context, the latest pain state, recent relevant content, saved items, and a clear next action. It does not make similar-user discovery the main task. That discovery behaviour belongs in Explore, where users can filter by stage, body area, goal, tags, and search terms.

This distinction makes the user flow easier to explain. A user can log in as a seeded BlaBla test member, land on Home, check their current state, add a structured recovery log, then see the latest pain state update from that log. If they want to find people or examples that match their situation, they move into Explore. If they open a detail page, they can read the discussion, reply, save the item, or report it.

On the technical side, I kept the implementation close to the course starter structure. The app uses Mojo routes, controller classes, model classes, server-rendered templates, SQLite, and `better-sqlite3` prepared statements. I also used small HTMX partial updates for Explore filtering and discussion replies, while keeping normal GET and POST fallbacks. This feels appropriate for the assignment because the implementation stays readable and directly connected to the database design.

The database structure also supports the design decisions. Pain level is not manually edited in My Account or Recovery Context. Instead, the latest pain state comes from the newest structured recovery log. This makes the data more meaningful because it is connected to an actual recovery activity, including pain before, pain after, confidence, symptoms, and what helped.

I also added validation around the main prototype behaviour. The test checks that Home can read the current context and derive pain from logs, Explore can return similar members, logs, and discussions, a new recovery log updates the latest pain state, and the detail flow supports reply, save, and report actions. This helped me confirm that the prototype is not only showing static mock content.

The visual system still follows the high fidelity direction from Figma: light blue pixel UI, square buttons, panel blocks, icon-supported navigation, and clear sections. However, this week was more about making the design work through the course implementation structure. A strong visual direction is useful, but for this assignment the prototype also needs to show a clear relationship between wireframes, DDD, ERD, SQLite tables, routes, templates, and user actions.

The next step is to keep testing the full journey with another person. I want to see whether the flow is understandable without explanation: choose a test member, understand the Home snapshot, use Explore for similar experiences, submit a recovery log, and notice that Home and Account update from that log. If that journey feels clear, Recovery Hub will communicate both the product concept and the technical structure more successfully.
