---
title: "Plan First, Act Later: How to Stay in Control of an AI Agent"
date: 2026-11-12 09:00:00 +0800
lang: en
categories: [Guides]
tags: [plan mode, AI Agent, human in the loop, AnBoWork]
image: /assets/images/covers/plan-before-you-approve.webp
excerpt: "The scariest thing about an AI agent is not that it is wrong. It is that it is wrong after touching your files. Here is how a plan-first workflow keeps you in charge."
description: "How a plan-first AI agent workflow works: clarifying questions, read-only exploration, a plan you can edit or reject, and no action until you approve. Shown with AnBoWork."
---

> In short: with a plan-first agent, the AI reads and thinks before it writes anything. You review a plan, change it or throw it out, and only an approved plan gets carried out.

## The problem with "just do it"

Most of us have typed a one-line request into an AI tool and watched it start changing things straight away. When the request is small, that is fine. When it is "reorganize this project" or "turn these twelve documents into a report", a wrong guess early on gets built on for the next twenty steps, and by the time you notice, the result is hard to untangle.

The issue is not that AI makes mistakes; people do too. It is that the **first mistake happens before you had a chance to see it**.

## What a plan-first workflow looks like

AnBoWork builds its agent workflow around a different order of events. For a complex task it goes through these steps:

1. **Clarify the goal.** The AI asks questions instead of guessing what you meant.
2. **Explore in read-only mode.** It looks at your files and material to understand the situation, without changing anything.
3. **Submit a plan.** You get a written plan, not a finished result.
4. **You decide.** You can add comments to the plan, adjust it, or reject it outright.
5. **Carry out the work.** Only after you approve does the AI start. It chooses its tools and can hand parts of the job to several sub-agents running in parallel.
6. **Review and deliver.** The output comes back for you to check.

Nothing is implemented until step 5, and step 5 only happens because you said so.

## What makes a good plan to approve

A plan is only useful if you can judge it quickly. When you read one, check four things:

- **Scope:** Does it touch only what you expected? A plan that mentions files you did not mention deserves a question.
- **Order:** Are the steps in a sensible sequence, with the risky ones (deleting, overwriting) clearly marked?
- **Inputs:** Is it working from the material you actually meant, or did it pick a similar-looking folder?
- **Output:** Does the end result match the format you need, such as a spreadsheet, a slide deck or a code change?

If any of these is off, comment on the plan rather than approving it and fixing things afterwards. A correction at the planning stage costs one sentence; a correction after execution can cost an hour.

## When you can skip the plan

Not every request needs one. Asking for a rewrite of a paragraph, a quick explanation or a short translation is faster done directly. The plan-first flow earns its keep on tasks that involve **many files, several steps or things that are hard to undo**: refactoring across a codebase, cleaning and analyzing a data set, building a multi-section document, or researching and compiling sources.

## Plans and plugins use the same rule

The same "ask first" principle shows up elsewhere in AnBoWork. When the AI wants a plugin, such as an Office toolkit or a Git diff viewer, it shows a confirmation card in the chat and installs it only after you click Install. The pattern is consistent: the AI proposes, you decide.

## A habit worth building

Treat the plan as the real deliverable of the first round. If you get into the habit of reading it for a minute before approving, you will catch most misunderstandings while they are still cheap to fix, and you will learn what kind of instructions lead to good plans.

Product details here were checked against the [official website](https://www.anbowork.com) in November 2026. The website is the source of truth for features and downloads.

## Related reading

- [What Is AnBoWork? A Desktop AI Agent Workbench, Explained]({% post_url en/2026-10-20-what-is-anbowork %})
