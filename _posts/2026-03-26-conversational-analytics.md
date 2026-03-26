---
layout: post
title: How Google integrates Conversational Analytics across its tools and why this matters
date: 2026-03-26 09:00:00
description: A look at conversational analytics across GA4, BigQuery and Looker, and what it means for the future of analytics as a discipline
tags: Analytics, AI, Google
categories:
---

*This blog was originally written for the [Relevant Online](https://www.relevant.online) website.*

---

LLMs do not know the answer. They make a guess. The most statistically likely guess, based on everything they have been trained on. The guesses are becoming remarkably good. Good enough to automate work that once required real expertise.

That shift has not gone unnoticed. Tool vendors across the board are integrating LLMs into their existing products. Google is no exception. From Gmail to Google Drive, conversational AI has been woven into the fabric of the tools millions of people use daily. But Google went further than productivity tools alone. They brought LLMs into the world of analytics and business intelligence.

The result is what is increasingly being called conversational analytics: the ability to ask your data a question in plain language and receive an answer without writing a single line of SQL or building a single dashboard.

That sounds powerful. But is it?

In this blog we explore conversational analytics across three layers of the Google stack: Google Analytics 4 as the data source, BigQuery as the database and Looker as the BI layer. For each we look at what is actually possible, where conversational analytics adds genuine value and where it falls short. We close with our broader take on what this means for the future of analytics as a discipline.

## Google Analytics 4: Analytics Advisor

GA4 has never been the most intuitive platform. Since Universal Analytics was retired, analysts and marketers have been trying to navigate the tool. Getting to a specific insight often requires knowing exactly where to look.

Analytics Advisor is Google's answer to that problem: a conversational AI assistant built directly into GA4, powered by Gemini, designed to give you personalised answers about your property through natural language. It was rolled out to all English-language accounts in December 2025.

In practice, it does three things. It answers data questions directly by returning metrics, trends and visualisations. It points you to the most relevant report when a deeper dive is needed. And it provides guidance on how GA4 itself works, drawing on Google's documentation.

Is it an improvement? Yes. The standard GA4 analytical tools were a low bar to clear, and the Advisor clears it. But there is a catch. When you outsource the analysis to an algorithm, you lose the ability to verify whether the analysis is correct. The Advisor does show its reasoning, which helps. But interpreting that reasoning still requires the same analytical instinct you needed before. Someone who lacks that instinct will not know when the answer is wrong. And occasionally, it will be wrong.

## Google BigQuery: conversational analytics

BigQuery is where things get more interesting. The conversational analytics functionality here operates on two levels: direct conversations and data agents.

Direct conversations allow you to chat with a single table. You can create conversations to answer basic, one-off questions about a data source. The response includes a summary, the underlying data, an automatically generated chart where appropriate, and suggested follow-up questions. It is fast, and for exploratory analysis it works well.

Data agents go further. Agents are built on one or more knowledge sources: tables, views, or functions. They can be configured with custom context, business glossary terms, and instructions that help the agent interpret questions correctly. Where a direct conversation gives you a quick answer, an agent gives you a consistent and context-aware one. The agent can work across multiple datasets at once and is better suited for recurring use cases where business definitions matter.

To give confidence in the results, the agent surfaces its reasoning and the generated SQL behind every answer, then synthesises the insights into a concise summary explaining the "why" behind the numbers.

That last point is where we have to be honest. The fact that BigQuery shows you the SQL is often presented as a feature and it is. But it also exposes the fundamental limitation of the tool. To verify the outcome, you still need SQL experience. You are not removing the need for analytical skills; you are just moving them one step downstream. Both functionalities feel like a well-built shortcut that will save you time reaching the insights you need. The question is what you are sacrificing in exchange. Every time the agent writes the query for you, you lose a small opportunity to sharpen your own understanding of the data. For organisations where analytics maturity matters, that is a trade-off worth thinking about carefully.

## Looker: conversational analytics

Looker is where conversational analytics is most mature and most trustworthy. The reason comes down to one thing: the semantic layer.

Conversational Analytics in Looker is built on top of Looker Explores and uses LookML for fine-tuning and output accuracy. This means every metric, every field, every calculation is centrally defined. When you ask a question, the answer is grounded in the same definitions your entire organisation uses. There is no ambiguity about what "revenue" means, because that definition already exists in the model.

The interface supports multi-turn questions, so you can iterate on findings: ask for total sales, then follow up with "now show me that as an area chart, broken down by payment method.". You can work across up to five Explores simultaneously, covering multiple business areas in a single conversation.

A "How was this calculated?" feature provides a clear, natural language explanation of the underlying query that generated the results. That transparency makes a real difference in practice. You are not just getting an answer; you are getting a verifiable answer.

For more advanced analysis, the Code Interpreter goes beyond SQL. It translates natural language questions into Python code and executes it, expanding the range of possible analysis to include period-over-period comparisons, outlier detection, cohort analysis and compound growth rates.

The trade-off at this level is access. Looker is an enterprise tool, and conversational analytics here assumes a well-maintained LookML model and a properly governed data environment. If the underlying model is poorly defined, the conversational layer will faithfully reproduce those inaccuracies. The quality of the answer depends entirely on the quality of what it is built on. For most organisations Looker is not a feasible tool in their stack due to its high costs.

## Is conversational analytics the future of analytics?

The short answer is: partly. And that "partly" matters more than it might seem.

Conversational analytics will absolutely become a standard part of the toolkit. The time savings are real. What once required an analyst to build a query, check the output, refine the logic and package the result into something a stakeholder could understand can now be done in seconds. For straightforward questions, that is genuinely valuable.

But time saved is not the same as value created. And there is a cost buried in the convenience that is easy to overlook.

When you stop doing the analysis yourself, you stop owning the process. The algorithm writes the query, generates the chart and serves up the conclusion. You receive the answer. What you do not receive is the experience of working through the problem: the wrong turns, the unexpected patterns, the moments where the data forces you to rethink your assumptions. That process is not inefficiency. It is how analytical instinct is built.

The consequence is straightforward: the less you do yourself, the less equipped you become to judge whether the answer in front of you is right. Conversational analytics tools do show their reasoning, as we have seen. But reading a SQL query you did not write and evaluating whether it correctly captures your business question are two different skills. The first requires literacy. The second requires experience. One of those cannot be outsourced.

There is also a structural shift happening that is worth naming directly. Conversational analytics makes data more accessible to people who would previously have needed an analyst to answer their questions. That is presented as pure democratisation, and in some ways it is. But it also means that a layer of analytical work is being automated away. The entry-level tasks that build expertise are disappearing precisely when that expertise is most needed to supervise the tools replacing them.

So what does this mean in practice?

Use conversational analytics for what it is genuinely good at: speeding up exploration, answering recurring questions, and making data accessible to teams who would otherwise be stuck waiting in a queue. But do not let it replace the habit of doing analysis yourself. The organisations that will get the most from these tools are the ones with analysts who understand the data well enough to know when the machine is wrong.

Conversational analytics is not the future of analytics. It is a feature of it. The future still requires people who know what they are doing.
