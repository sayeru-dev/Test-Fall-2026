# Week 04 AI Opportunity [259]

## Section A Lab Reflections

The five labs closest to our problem are Text Generation, Structured Extraction, Audio + Voice, Document Retrieval, and Tool Use, because our problem is an alert email that gets written, sent late, and never becomes a pattern.

**Lab 1 Text Generation.** When I asked the model to write a campus alert it ended with the same "stay aware of your surroundings" line Joe's real emails do, the part [259] called obvious suggestions.

**Lab 2 Structured Extraction.** The model pulled location and type out of a pasted alert into JSON, but set time to null because the email said "early this morning," which is how real alerts are worded.

**Lab 4 Audio + Voice.** Bà Linh [231] hung up on the non-emergency line because the recording was too fast. Transcription was close on clear speech but dropped words when I mumbled, so the phone side is not a free win.

**Lab 5 Document Retrieval.** Joe said 4th and San Fernando is "burned into my head as a spot." Retrieval found the right chunk 3 out of 4 times, which is the memory Joe has that nobody else does.

**Lab 7 Tool Use.** The model called a lookup tool instead of guessing a value. That is the piece that could check CrimeMapping, which only updates once a day, before an alert goes out.

## Section B Raw Idea

The civic problem is students get crime alerts after the fact with no sense of whether the spot is a pattern.
The people most affected are Joe, the UPD analyst who drafts the alerts and is too worn out to tell a one-off from a repeat.
AI could help by reading his draft, pulling the location, checking past alerts, and adding one line like "third incident here since March, last time UPD added a patrol."
The input would be text (the draft email) and the output needs to be one short sentence appended to the draft.
This opportunity draws on Lab 2 Structured Extraction, Lab 5 Document Retrieval, and Lab 1 Text Generation.
The hard part of the harness is the retrieval box, because old alerts spell the same corner five different ways and a miss means the pattern stays invisible.
The assumption I have not confirmed is that Joe would report or word things differently if the draft told him it was a repeat.
