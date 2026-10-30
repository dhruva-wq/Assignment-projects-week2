# RTCFR: Role, Task, Context, Format, Restrictions

**Use it for:** any single task where you want consistent, controlled output.

## What it is
A structured prompt with five labeled parts. Each part removes one kind of ambiguity.

| Part | Question it answers |
|---|---|
| **Role** | Who should the model act as? |
| **Task** | What exactly must it produce? |
| **Context** | What does it need to know about the channel, audience, and constraints? |
| **Format** | What shape should the output take? |
| **Restrictions** | What must it avoid or never exceed? |

## Example: Faceless YouTube channel "Unsolved History Mysteries"

```
ROLE: You are a senior YouTube scriptwriter who specializes in faceless
documentary-style channels with 1M+ subscribers.

TASK: Write a 6-minute script on "The Disappearance of the Roanoke Colony."

CONTEXT: The channel is "Unsolved History Mysteries." The audience is
18-35, watches on mobile, and drops off if the first 15 seconds are weak.
The voiceover will be AI-generated, so there is no on-screen host.
Visuals will be stock footage and AI images.

FORMAT: Two-column table. Left: narration (spoken text only).
Right: visual cue (e.g., "aerial shot of dense forest, 3s").
End with a 1-line title, 3 title alternatives, and a thumbnail concept.

RESTRICTIONS:
- Hook in the first 15 seconds with a question or shocking fact
- Max 150 words per minute of narration
- No unverified claims presented as fact; flag theories as "theories"
- No filler phrases like "without further ado"
- Do not exceed 900 words total
```

## Tips
- Be specific in Restrictions; vague limits get ignored.
- Reuse the same Role and Context across every video for a consistent channel voice.
- Some sources define the "R" differently (Result, Rules). The structure is what matters.
- In an automated pipeline, store the template with `{topic}` placeholders.