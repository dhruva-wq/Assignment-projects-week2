# ReAct Prompting: Research, Act, and Reassess

## Definition

ReAct combines reasoning with actions. An AI alternates between deciding what information it needs, using an available tool or source, observing the result, and deciding what to do next. In a channel workflow, actions might include searching official documentation, opening a source, or checking a creator-provided analytics export.

## When to use it

Use ReAct when the task depends on current or external information and the AI has tools that can retrieve it. Do not use it as a substitute for tools or sources the model does not actually have.

## Workflow

1. Set the question, audience, and trusted source types.
2. Have the assistant identify a specific information gap.
3. Use a permitted research tool to check that gap.
4. Record the observation with a source and date.
5. Repeat only if a material gap remains, then report supported findings and uncertainty.

## Copy-and-paste prompt

```text
You are a research assistant for a faceless YouTube channel that publishes practical AI tutorials for freelancers.

Question: What privacy controls should a freelancer check before using an AI meeting-notes service with client calls?

Use the web search/browser tools available in this session. Prefer official product privacy documentation, help centers, and applicable primary sources. Do not infer a control from marketing language. If a source is unavailable, say so.

For each research step:
1. State the specific question you need to check.
2. Search or open a relevant source using the available tool.
3. Summarize only what the source says, with a direct link and date checked.
4. Note what remains unknown or differs by plan, region, or settings.

Return a creator-facing fact-check table with columns: statement suitable for a script, source, checked date, confidence/limitations, and wording to avoid. Then suggest a 30-second demonstration using fictional meeting data. Do not upload, submit, or share any client information. Do not log into accounts or change settings. If you cannot browse, provide a research checklist instead of pretending you checked sources.
```

## Concrete YouTube-channel example

The assistant may discover that a service’s documentation describes retention and training controls but leaves region-specific details unclear. The creator can use a cautious script line such as “Check the current settings and terms for your account,” while flagging the unresolved detail for manual verification. Any screen recording should use a test account and fictional content.

## Expected output

A source-linked fact-check table that distinguishes what was observed from what remains uncertain, plus a safe demonstration idea. The action trail makes it easier for a producer to revisit sources before publication.

## Limitations and best practices

- Search results and pages can be stale, incomplete, promotional, or misread.
- Tool access may be unavailable; the prompt explicitly asks the model to say so.
- Prefer primary sources and record when they were checked.
- Keep human data private; use fictional examples and test accounts.
- Give tools only the permissions needed for the research task.
- A page visit does not prove a product behaves as described; hands-on testing may still be needed.
- Review links and claims before publishing, since policies and features can change.

## Summary

ReAct is useful for research tasks where an assistant can take real, bounded actions and report what it observes. Its value depends on reliable tools, trustworthy sources, and human verification.
