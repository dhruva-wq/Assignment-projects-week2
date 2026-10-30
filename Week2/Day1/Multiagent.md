# Multi-Agent Prompting: Collaborate on a Video Package

## Definition

Multi-agent prompting assigns different parts of a task to separate AI roles or agents, then combines their work. Agents may work in parallel on research, audience fit, scripting, and risk review. A coordinator reconciles disagreements and produces one result.

## When to use it

Use it when a project has separable perspectives that benefit from independent review. It may be excessive for a short, simple video; more agents can add cost, repetition, and conflicting advice.

## Workflow

1. Give every agent the same audience, objective, and source packet.
2. Assign narrow, complementary responsibilities.
3. Ask each agent to return evidence, assumptions, and open questions in a common format.
4. Have a coordinator combine compatible findings and flag conflicts.
5. Ask a human to fact-check and approve the final video package.

## Copy-and-paste prompt

Use this as a single prompt when the AI environment supports multiple agents. If it does not, run each role separately and paste the results into the coordinator section.

```text
PROJECT
Prepare a draft video package for Quietly Useful, a faceless YouTube channel for freelancers who want practical, cautious uses of AI.
Topic: using AI to turn fictional client-meeting notes into a clear action list.
Length: 6–8 minutes. Visual style: narration, screen recording, simple graphics.
Use only the supplied research packet: [PASTE SOURCES, NOTES, AND CHECKED DATE].

Assign these independent roles:

AGENT 1 — AUDIENCE EDITOR
Identify the viewer’s likely problem and a specific, realistic promise. Suggest a hook and explain what would make the video useful. Do not predict views.

AGENT 2 — RESEARCH AND CLAIMS REVIEWER
Check every proposed factual claim against the supplied packet. Return supported claims, unsupported claims, and questions requiring additional sources. Do not add outside facts.

AGENT 3 — SCRIPT AND VISUALS EDITOR
Draft a timestamped outline and visual ideas using fictional meeting notes. Make the steps clear for a beginner. Mark any factual statement that needs confirmation as [VERIFY].

AGENT 4 — PRIVACY AND ORIGINALITY REVIEWER
Identify privacy risks, sensitive data that should never appear in a demo, misleading promises, and any generic or derivative creative elements that need revision. Offer practical fixes.

COORDINATOR
Combine the role reports into one proposed package with: title, viewer promise, timestamped outline, visual plan, fact-check list, and privacy checklist. Preserve disagreements as open questions instead of silently choosing a side. Do not invent sources, analytics, or product behavior. Clearly label assumptions. A human editor will verify the package before recording or publication.
```

## Concrete YouTube-channel example

The audience editor might recommend focusing on the pain of forgetting follow-ups; the research reviewer might flag a claim about a tool’s data retention; the script editor can replace real client examples with a fictional scenario; and the privacy reviewer can recommend hiding email addresses and using a test account. The coordinator then creates a draft while keeping the retention question open for verification.

## Expected output

A single proposed video package that benefits from multiple perspectives, along with visible unresolved claims and risks. The reports should be complementary rather than four copies of the same outline.

## Limitations and best practices

- Several agents can repeat the same mistake, especially when they share a weak source packet.
- Role labels do not guarantee real expertise or independent judgment.
- Keep assignments narrow and return formats consistent.
- Make the coordinator retain disagreements and trace factual claims to sources.
- Minimize sensitive information; fictional examples are usually enough.
- Review copyright, permissions, product claims, and platform policies before publication.
- A human creator remains responsible for the finished video and its publishing decisions.

## Summary

Multi-agent prompting is a way to organize distinct editorial viewpoints around one channel task. Use it when the perspectives add value, and keep sources, disagreements, and final approval visible.
