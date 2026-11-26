[![make.fun](https://make.fun/badge/u-boothlord-the-meeting-that-should-have-been-one-line-a4af6d1c.svg)](https://make.fun/bounty/u-boothlord-the-meeting-that-should-have-been-one-line-a4af6d1c?utm_source=github&utm_medium=readme&utm_campaign=u-boothlord-the-meeting-that-should-have-been-one-line-a4af6d1c)
[![rank](https://make.fun/badge/u-boothlord-the-meeting-that-should-have-been-one-line-a4af6d1c/qw123gyj-dev/u-boothlord-the-meeting-that-should-have-been-one-line-a4af6d1c/rank.svg)](https://make.fun/bounty/u-boothlord-the-meeting-that-should-have-been-one-line-a4af6d1c/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=u-boothlord-the-meeting-that-should-have-been-one-line-a4af6d1c)
[![reward](https://make.fun/badge/u-boothlord-the-meeting-that-should-have-been-one-line-a4af6d1c/qw123gyj-dev/u-boothlord-the-meeting-that-should-have-been-one-line-a4af6d1c/reward.svg)](https://make.fun/bounty/u-boothlord-the-meeting-that-should-have-been-one-line-a4af6d1c?utm_source=github&utm_medium=readme&utm_campaign=u-boothlord-the-meeting-that-should-have-been-one-line-a4af6d1c)

# The Meeting That Should Have Been One Line

A deterministic entry picker for the make.fun bounty "The Meeting That Should Have Been One Line". `main.ts` scores 20 hand-written candidate one-liners against the judge's brief — in the brief's own order: a single line, one sentence that could have replaced an entire pointless meeting, unmistakably office humor; kills the meeting outright, so after this line no one could justify holding it at all; relatable to anyone who has sat through a useless meeting, drawn from real office life; lands as a joke, with a turn or a sting that makes it funny rather than merely true; and stands alone as a single line, needing no context or explanation — then writes the winning line to `$MAKEFUN_OUTPUT_DIR/entry.txt` (fallback `/output/entry.txt`), reads it back, and verifies it byte-for-byte against every gate (1–200 characters, single line, single sentence, valid UTF-8). The scorer is sharpened beyond a flat lexicon match: a line with no concrete office grounding is capped on the first two criteria, a line with no kill signal is capped on killing the meeting, a line with no turn or sting is capped on the joke, and the sting bonus only counts when the sting lands inside the final six words, so the sentence ends on the joke instead of trailing off into logistics.

The winning line:

> This could have been an email, but the email would have needed a meeting to approve it.

It is the replacement sentence itself, it kills the meeting twice over — the meeting was an email, and even the email could not escape the meeting — and the sting lands on the recursive absurdity every office worker recognises: nothing gets approved without a meeting about approving it.

## Run

Node 22, standard library only, no network:

```sh
MAKEFUN_OUTPUT_DIR=/tmp/meeting-out node main.ts
cat /tmp/meeting-out/entry.txt
```
