# Chain of Thought (CoT): Ask for a Useful Rationale

## Definition

Chain of Thought is a way to encourage a model to work through a multi-step problem. For everyday prompting, request a concise, checkable rationale, assumptions, and conclusion rather than private hidden reasoning. A rationale should help a person inspect the answer; it is not evidence that the answer is correct.

## When to use it

Use this approach when a decision involves several criteria, such as choosing which video concept best serves the channel. It is less useful for simple tasks with an obvious answer.

## Workflow

1. Define the decision and its criteria.
2. Provide the candidate options and any evidence available.
3. Ask for a short comparison against each criterion.
4. Ask the model to state assumptions and uncertainty.
5. Verify important claims and make the decision yourself.

## Copy-and-paste prompt

```text
You are an editorial analyst for a faceless YouTube channel about practical AI for freelancers.

Choose which video idea to produce next from the options below. Do not reveal private step-by-step thoughts. Instead, give a concise decision rationale that a person can check.

Audience: freelancers who are curious about AI, short on time, and cautious about sharing client data.
Channel capacity: one 6–8 minute video per week; screen recordings and narration are available.

Ideas:
A. “Use AI to summarize a long client brief”
B. “Five AI tools that will change your business”
C. “A privacy-safe way to turn meeting notes into action items”

Score each idea from 1–5 on:
- Specific viewer problem
- Ability to demonstrate the value in 6–8 minutes
- Evidence and fact-checking feasibility
- Privacy and safety considerations
- Distinctiveness from generic tool lists

Return:
1. A compact table with scores and one-sentence evidence-based rationale per criterion.
2. The recommended idea and why it fits the stated audience.
3. Assumptions and unknowns that could change the recommendation.
4. One low-cost validation step before scripting.

Do not invent search-volume data, audience analytics, or product features. Treat scores as editorial judgments, not measured facts.
```

## Concrete YouTube-channel example

The comparison may favor idea C because it targets a clear problem, supports a short demonstration, and gives the video a natural privacy discussion. That is a planning judgment, not proof that C will earn more views. A creator could validate it by checking audience comments and testing whether the workflow can be demonstrated safely with fictional notes.

## Expected output

A compact decision record: criteria, comparative scores, a recommendation, assumptions, and a way to validate the choice. The requested rationale makes the recommendation easier to review without needing a long stream of internal reasoning.

## Limitations and best practices

- A model can give confident but arbitrary scores. Treat them as a prompt for discussion.
- Provide real channel evidence if you have it; do not invite made-up analytics.
- Ask for concise reasons tied to stated criteria, not an unbounded “think harder.”
- Separate subjective editorial judgments from verifiable factual claims.
- Verify claims about products, audience behavior, or current trends independently.
- Keep the final decision with the creator, who understands the channel and its audience.

## Summary

For channel planning, CoT-style prompting is most useful as structured, inspectable reasoning: compare options, show concise justifications, name uncertainty, then validate. More generated reasoning does not automatically mean a better answer.
