---
layout: post
title: "Restarting Mudipu with one agent test"
date: 2026-09-28
category: Tech
description: "A small experiment in testing what an AI agent does, beyond its final answer."
---

I paused Mudipu for a while. My current work at SAP has got me thinking about it again. I’ve noticed better ways to approach evaluation, and that inspired an idea I want to explore in Mudipu: evaluations as tests for AI agents, with observability built into the testing process.

The question I keep coming back to is simple: how do I know an agent actually did the right thing?

A reasonable answer doesn’t tell me much about how it got there. An agent could explain a refund policy correctly without ever looking it up. It could also call a tool it shouldn’t have access to and still give a helpful reply.

Mudipu already started with observing agent behavior. I want to use those traces as evidence in a test: which tools ran, what they returned, and how that shaped the final answer.

## Start with one test

The first experiment is small: define a test in YAML, run an agent, capture its tool calls and output, and check what happened.

Take a customer asking to return something after 45 days. I’d want to check whether the agent looked up the return policy, then whether its answer matched what the tool returned.

The first check can be a straightforward assertion. For the second, I want to give an LLM judge a clear rubric, the answer, and the relevant tool calls and results. That makes observability part of the evaluation itself: the judge has evidence to check whether the answer is supported by what the agent actually retrieved.

I’m also curious how consistently the judge will score the same run. That’s something I’ll need to test too.

The goal is a local command that produces a readable result and a JSON report. There’s no implementation of this new test runner yet. Getting one test to run end to end is the next step.

## Keep a record of what happens

Once that works, I’d like to try forbidden-tool checks and prompt-injection cases. But I’ll let the first experiment shape what comes next.

I also want to write about the work as I go. After this starting note, each entry should have something concrete behind it: code I built, a test that failed, or a result I’m still trying to understand.

For now, one agent and one test is enough to get moving again.
