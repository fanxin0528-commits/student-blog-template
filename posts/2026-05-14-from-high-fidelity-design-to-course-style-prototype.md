---
title: From High Fidelity Design to a Course-Style Prototype
date: 2026-05-14
author: Fanxin
summary: A reflection on adapting Recovery Hub from a polished interface direction into a course-aligned SQLite and Mojo.js prototype.
tags:
  - advanced web design
  - recovery hub
  - prototype
  - sqlite
  - reflection
---
This week I focused less on adding new screens and more on making the project fit the course requirements properly. After working on high fidelity design, front-end structure, and database planning, I realised that the next important step was not simply to make the app feel more professional. It was to make the prototype clearly show the skills and workflow taught in class.

At one point, the Recovery Hub prototype was moving in a more production-style direction, with a separate front end, API layer, and modern app structure. That approach can be useful for a real client project, but for this assignment it risked becoming too far away from the course. A2 is not only about building something that looks finished. It is also about showing a clear path from wireframes to data design, SQLite tables, routes, and rendered views.

Because of that, I changed the implementation direction to match the class examples more closely. The current prototype now uses Mojo.js routes, `better-sqlite3`, server-rendered templates, and normal form submissions. This makes the code feel simpler and easier to explain. Instead of hiding the application behind a large front-end framework, each route connects more directly to the data it needs.

This also helped me understand the relationship between the design and the database. The main views in the app are still the same: Home, Recovery Context Setup, Stage Dashboard, Structured Recovery Log, Detail, Explore, and My Account. However, each page now has a clearer responsibility. Home shows the current recovery snapshot. Explore handles discovery. Logs update the latest pain state. Account shows recovery context and preferences without asking the user to manually maintain pain level.

The most important product rule stayed the same: pain level should come from structured recovery logs, not from a separate account field. This decision matters because it makes the data feel connected to real user behaviour. If a user records pain before and after an activity, that log becomes evidence of their current state. The interface can then reflect that state without asking the user to update the same information twice.

Another useful change was simplifying the technical ambition. A more advanced architecture is not always better for a course prototype. In this case, using a simpler server-rendered approach makes the project easier to review, easier to run locally, and easier to connect back to the weekly learning content. It also makes the database work more visible, which is important because the assignment is partly about showing how the app is supported by real data rather than static mockups.

This week made me think more critically about what "good enough" means in an academic project. I still want the visual design to feel polished, especially because the pixel-style interface is part of the identity of Recovery Hub. But the technical side needs to communicate learning, not just complexity. A prototype can be successful if it clearly demonstrates the concept, supports the main user flows, and matches the expected course methods.

The next step is to keep testing the prototype as a complete flow. I want to check that a user can understand their current recovery state, add a structured log, see the latest pain state update, and then explore similar experiences. If those flows are clear, the project will be much stronger than if it only looks good as separate screens.

Overall, this week was about alignment. The design direction, database structure, and course implementation now feel more connected. Recovery Hub is still the same concept, but the prototype is now better shaped for the assignment context.
