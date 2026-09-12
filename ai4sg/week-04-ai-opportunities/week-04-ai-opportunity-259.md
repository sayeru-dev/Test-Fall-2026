# Week 04 AI Opportunity [259]

## Section A Lab Reflections

The five labs closest to our problem are Text Generation, Structured Extraction, Audio + Voice, Document Retrieval, and Tool Use, because our problem is an alert email that gets written by hand, sent late, and never checked against the alerts before it.

**Lab 1 Text Generation.** I typed "apple" and the model gave me the fruit and then Apple Inc. too, 407 output tokens for one word. Joe writes alerts by hand, and this shows the model will pad unless you box it in.

**Lab 2 Structured Extraction.** Without a schema the same report came back "High" on run 1 and "Immediate" on run 2. With the schema it was MEDIUM all three runs, but location still said "possibly 123 or 125," so the form fixes the format, not the fuzzy address.

**Lab 4 Audio + Voice.** Bà Linh [231] hung up on the non-emergency line because the English recording was too fast. The cost table put 500 three-minute calls a day at $270 a month, which is cheap next to a call that never gets made.

**Lab 5 Document Retrieval.** The search pulled 8,174 input tokens against 19 without it, and turn 1 mixed a smoke shop raid into an illegal dumping question. Joe's "spot" at 4th and San Fernando is exactly the kind of thing search would get wrong and memory would get right.

**Lab 7 Tool Use.** The log ended with 3 reports and 123 Main St showed up twice, once MEDIUM and once HIGH. Nothing flagged the repeat. That is Joe's problem in one table.

## Section B Raw Idea

The civic problem is students get crime alerts after the fact with no sense of whether the spot is a repeat.
The people most affected are Joe, the UPD analyst who drafts the alerts and is too worn out to tell a one-off from a pattern.
AI could help by reading his draft, pulling the location, checking it against past alerts, and adding one line like "third incident here since March."
The input would be text (the draft email) and the output needs to be one short sentence appended to the draft.
This opportunity draws on Lab 2 Structured Extraction, Lab 7 Tool Use + Integrations, and Lab 1 Text Generation.
The hard part of the harness is the tool box, because the lookup has to match "4th and San Fernando" to "San Fernando & 4th" and a miss means the pattern stays invisible.
The assumption I have not confirmed is that Joe would word or send the alert differently if the draft told him it was a repeat.
