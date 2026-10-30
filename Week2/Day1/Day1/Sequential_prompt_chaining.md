# Sequential Prompt Chaining

**Use it for:** the full pipeline from idea to metadata, one stage at a time.

## What it is
Break a big job into small prompts. The output of each prompt becomes the input of the next. Each step has one job, and you can inspect or fix the output before it moves on.

## Example: Idea to upload package

**Prompt 1: Topic ideation**
```
Give me 10 unsolved history mystery topics with high search interest
and low competition on YouTube. Return as a numbered list with a
one-line hook for each.
```

**Prompt 2: Research** (paste the chosen topic from Prompt 1)
```
Topic: [chosen topic]. Summarize the 5 key facts, 3 leading theories,
and 2 lesser-known details. Mark anything disputed.
```

**Prompt 3: Outline** (paste the Prompt 2 output)
```
Using this research: [Prompt 2 output], create a 6-minute video outline
with: Hook, Context, Evidence, Theories, Twist, Outro + CTA.
```

**Prompt 4: Script** (paste the outline)
```
Write the full narration from this outline: [Prompt 3 output].
Conversational tone, short sentences, built for text-to-speech.
```

**Prompt 5: Scene breakdown** (paste the script)
```
Split this script into scenes. For each: narration line, visual
description, and an image-generation prompt. Output as JSON.
```

**Prompt 6: Metadata**
```
From this script: [Prompt 4 output], generate a title, description
with timestamps, 15 tags, and 3 thumbnail text options.
```

## Flow

```
Topics -> Research -> Outline -> Script -> Scenes -> Metadata
```

## Tips
- Pass structured output (JSON) between steps so parsing never breaks.
- Add a validation step between nodes (word count, required fields).
- In n8n, Make, or Airflow, each prompt becomes one node/task.
- A failure in step 3 does not force you to redo steps 1 and 2.