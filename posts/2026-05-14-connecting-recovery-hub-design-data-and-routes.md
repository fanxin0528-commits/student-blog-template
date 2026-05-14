---
title: Connecting Recovery Hub Design, Data, and Routes
date: 2026-05-14
author: Fanxin
summary: A reflection on turning Recovery Hub from high fidelity screens into a data-backed prototype with clear routes and user flows.
tags:
  - advanced web design
  - recovery hub
  - prototype
  - sqlite
  - reflection
---
This week I continued developing Recovery Hub from a high fidelity interface into a working data-backed prototype. Earlier work focused on the concept, wireframes, and visual direction. This stage was about connecting those screens to real content structures, routes, and database relationships so the project could be experienced as a small web application rather than only a set of static designs.

The main challenge was making sure each screen had a clear data purpose. The Home page is not just a visual dashboard. It needs to show the user's current recovery context, latest pain state, relevant logs, and next action. The Explore page is not just a list of content. It needs to support filtering by recovery stage, body area, goal, and tags. The Log page is not just a form. It is the place where changing recovery-state data is created.

Thinking this way helped me connect the interface back to the DDD and ERD work. Each view depends on specific entities: users, recovery contexts, recovery logs, stages, goals, discussion threads, replies, saved items, and reports. Instead of designing pages first and thinking about data later, the prototype now shows how the screen layout and database structure support each other.

One important decision was keeping pain level out of the account settings. My Account can show the latest pain state, but it should not ask users to manually maintain a separate pain field. The more meaningful source is the structured recovery log, because that is where users record pain before and after an activity. This keeps the data closer to lived experience and avoids asking users to update the same information in multiple places.

The routes also helped clarify the user flow. A user can start at Home, review their current state, add a recovery log, and then return to see the latest pain state reflected in the interface. They can also move from Home or Stage Dashboard into Explore, where the focus becomes finding similar users, logs, and discussions. This separates checking in, recording progress, and discovering community content into different but connected actions.

For implementation, I used SQLite as the local database and connected it to server-rendered pages. This made the prototype easier to reason about because each page can be traced back to the query that supports it. For example, Home reads the current context and latest log, while Explore builds its results from filters. This feels appropriate for the current stage because the important goal is to demonstrate the relationship between user flow, data, and rendered interface.

The visual system still matters. The pixel-style blue interface gives Recovery Hub a clear identity, and the high fidelity Home design helped define the style of panels, buttons, icons, and navigation. However, this week reminded me that a polished visual direction is stronger when the information behind it is also structured. A good prototype should not only look like an app; it should also behave like one.

The next step is to keep testing the main journey end to end. I want to check whether a user can understand their recovery context, add a log, see the latest pain state update, and find relevant community examples without confusion. If those flows work clearly, the prototype will communicate the core idea of Recovery Hub much more effectively.

Overall, this week was about connecting layers of the project. The high fidelity design gives the app its visual form. The database gives it structure. The routes connect user actions to data. Together, these parts make Recovery Hub feel more complete as an interactive prototype.
