# memo-review

A Claude skill that reviews an early-stage venture investment memo (pre-seed, seed, early Series A), together with its comments and tracked edits. It verifies claims by research and against the data room, then returns a checklist of exact, sourced edits in the order the memo reads, which you can challenge item by item.

## What it does
- Turns each collaborator comment or tracked edit into a concrete edit, after checking it. Every one gets a verdict: Supported, Partly supported, Not supported, or Could not verify.
- Reviews the memo as a skeptical committee member: team, market, product, traction, comps, unit economics, round terms, returns, risks, internal consistency.
- Reconciles the memo against the deck and data room where one exists.
- Recomputes every number it relies on (ownership under pre- and post-money SAFEs, dilution, runway, returns) and shows the arithmetic.
- Never invents data. Anything it cannot verify goes in a closing list.
- You make every edit. The skill only supplies the wording and the evidence.

## Install
Copy `SKILL.md` into a folder named `memo-review` in your Claude skills directory.

## Tested with
A memo in a Google Doc, open in a Chrome tab shared with Claude. It has not been tested with a Word file or the Word app. The method is not tied to one tool, but how comments and tracked edits get read is the part most likely to differ.

## How it was made
I designed and directed this skill and built it with Claude. It started from a review routine I use on my own reviews of early-stage deals. It has been used by me only; I have not measured time saved.

## Example
See [example/](example/) for a review of a fictional memo.

## License
No license: all rights reserved. This repo is public to be read, not reused.
