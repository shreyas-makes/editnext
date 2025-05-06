---
title: Blind reading codebases, and databases
date: 2025-02-14
slug: codebase-diagrams
tags:
  - rough-notes
  - llm
  - programming
---
Analysing codebase and understanding the patterns followed at a top level has become surprisingly easier nowadays with the help of tools such as Gemini (for larger context windows), Gitingest (to convert codebases to simpler markdown), and Mermaid.js (for visualising mermaid diagrams).

This is how I would approach understanding a fresh new codebase in order to take a cursory look:

Use [Gitingest](https://gitingest.com/) to convert github repositories into markdown. Markdown format could then be added to any of your AI chats so that you could ask any question. What I like about this tool is that I just have to replace the URL. So for instance, if I have this URL — https://github.com/ryanckulp/speedrail, I just have to replace this with https://gitingest.com/ryanckulp/speedrail for using the tool. I don't have to think twice on which tool to even use, the switch of context is quite easy and not so difficult for you to remember.

![](Attachments/shreyas-15-02-2025%20at%2009.02.49.jpg)

Once I upload the github repository, I can tweak the file size in case there are specific file size limitations across various LLMs. So far, Gemini has the highest context window, so it could easily take the markdown file as it is. In case you're using in Claude projects, you might run into some errors.

![](Attachments/shreyas-15-02-2025%20at%2008.57.21.jpg)

Once I've downloaded the markdown, I then go to [Gemini Flash](https://gemini.google.com/app/92de35898c1c8237) and then upload this markdown for it to generate a mermaid diagram.

![](Attachments/shreyas-15-02-2025%20at%2008.57.28.jpg)

I then copy this to the clipboard, and then paste it into any online mermaid diagram visualiser such as [Mermaid Live Editor](https://mermaid.live/).

![](Attachments/shreyas-15-02-2025%20at%2008.57.09.jpg)

I follow a similar approach while jumping head first into a new codebase on [Cursor AI](https://cursor.sh/). 

In the same way, I've started doing some sensemaking on the codebases, I've also used a similar approach towards sensemaking databases. Mermaid diagrams are a great tool for also visualising ERD diagrams (Entity Relationship diagrams). Especially when your app is connected to a database, Cursor hallucinates midway on what this database might look like. It's helpful to have a specs sheet, say `specs.md` which holds this ERD diagram for it to provide contextual code.