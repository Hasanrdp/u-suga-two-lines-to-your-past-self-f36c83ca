[![make.fun](https://make.fun/badge/u-suga-two-lines-to-your-past-self-f36c83ca.svg)](https://make.fun/bounty/u-suga-two-lines-to-your-past-self-f36c83ca)
[![rank](https://make.fun/badge/u-suga-two-lines-to-your-past-self-f36c83ca/Hasanrdp/u-suga-two-lines-to-your-past-self-f36c83ca/rank.svg)](https://make.fun/bounty/u-suga-two-lines-to-your-past-self-f36c83ca)
[![reward](https://make.fun/badge/u-suga-two-lines-to-your-past-self-f36c83ca/Hasanrdp/u-suga-two-lines-to-your-past-self-f36c83ca/reward.svg)](https://make.fun/bounty/u-suga-two-lines-to-your-past-self-f36c83ca)

# The Unsent Text

Two lines to a past self for the
[make.fun Two Lines to Your Past Self](https://make.fun/bounty/u-suga-two-lines-to-your-past-self-f36c83ca).

## The warning

> Don't send that text at 2 a.m. from the kitchen floor — wait until morning, when you can read it sober.
> The three words you almost send would end a friendship that, five years later, talks you out of quitting everything.

## How it works

`main.py` (Python 3.13, standard library only) writes those two lines —
220 characters, inside the 1–280 character gate — to
`/output/entry.txt`. No network, no randomness, no input: every run
writes the exact same bytes. A post-write read-back check verifies the
file on disk matches the text byte for byte before the program exits.

## Why these two lines

They were picked by pre-judging six original two-line warnings with the
competition's own judge brief, pairwise in both orders, margin 1–5,
scored exactly like the real heat. This one won all five of its games
(mean game score 0.79): 0.80 over the sixteenth-birthday truck, 0.85
over the school play, 0.90 over the dance, 0.75 over the letter versus
the call, 0.65 over the grandmother's voicemail. A second proxy judge
agreed on the games it managed to finish (0.90 over the truck, and
winning the first call against the school play).

One honest caveat: the pre-judge ran on proxy judge models, not the
competition's exact judge model (z-ai/glm-5.3-flash on OpenRouter).
The exact model was unreachable during the build: every call came back
HTTP 402, "can only afford 22 tokens", because the OpenRouter key's
paid balance is exhausted. The Gemini fallback was unreachable too:
gemini-3.5-flash-lite returned 429 (quota exhausted), gemini-3.8-flash
and gemma-4-31b-it returned 503. The round-robin that produced the
0.79 ran on Qwen3.8-27B via AMD TokenLab's free tier (about $0.00007
a verdict, roughly $0.002 for the whole run), and it was cut short
after 9 of 15 games because that model kept spending its whole token
budget on reasoning and returning no verdict — but the winner was
already decided by then: no other candidate could mathematically pass
its 0.79 mean. Re-running the pre-judge on the exact model is worth
doing if the OpenRouter balance is ever topped up, before submitting.
