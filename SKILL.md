---
name: "memo-review"
description: "Review an early-stage venture investment memo, its comments and tracked edits: verify claims by research and the data room, then give document-ordered sourced edits in a checklist you can challenge."
---

# Memo review

Use when the user asks to review, redline or "suggest changes" to an investment memo on an early-stage venture (pre-seed, seed or early Series A), or to act on its comments. The skill assumes the investor is writing for an investment committee deciding on a first check into a young company with little revenue history, so claims about team, market, technology and round terms carry most of the weight. Three jobs, merged into one checklist:

1. Collaborator comments and in-line (suggested/tracked) edits: turn each into a concrete edit, after verifying it. Comments and suggestions can be wrong, stale or unsupported; check them, do not just transcribe them.
2. Independent investor-lens review: find what is wrong, stale, missing or unsupported in the memo itself, even where nobody commented.
3. Data room check, where one exists: reconcile the memo against the underlying documents.

The human reads the memo and makes every edit. Claude supplies verified, exact wording. Never edit the memo unless asked. The human can argue with any item and Claude must engage on the evidence.

## Output the user wants (do not deviate)

- Walk the document top to bottom. Items follow the order of the lines in the memo, never the comment sidebar order and never grouped by topic or author.
- Each item gives: the memo section; a FIND string copied verbatim from the memo so a text search lands on it; the exact NEW WORDS; a source right next to the suggestion; a tick box.
- Label each item's origin: a named collaborator's comment, a tracked edit, or Claude's own research.
- Show a verdict on every collaborator comment or tracked edit: Supported, Partly supported, Not supported, or Could not verify, with the evidence.
- If one item needs edits in more than one section, say so at the top (how many edits, which sections), give each edit its own section label and FIND string, and state the logic before the edits.
- Mark items Apply, Decide first (needs a team call), or Check if already done.
- Deliver as a checklist page or document, not a long chat message. The chat reply is a short summary: what the checklist is, what changed from the draft, what could not be verified.

## Process

1. Read the memo text. Comments and tracked edits often do not come with the body text, so read them separately and confirm both come from the same version of the memo.
2. Read the comments and suggested edits in full. Some tools show only the sidebar or collapse long comments; check that the full text of each comment was captured.
3. Map each comment to its memo line. Anchor labels and comment text can be offset by one entry when read out of a sidebar, so confirm the mapping by meaning, not adjacency. Comments whose anchor text was deleted have no searchable anchor: place them by topic where the edit lands and say the anchor was deleted. Note resolved threads and ask whether they were already applied. Note suggestions already in the memo and fix typos.
4. Data room. Check the deal record (CRM, pipeline tracker or deal notes) and any data room folder. Read the deck and every available document. Reconcile deck vs memo vs data room: round size, cap and instrument type, committed money, prior raises, team and titles, locations, dates, patents, customers. Record conflicts in the memo's source reconciliation section. If a document cannot be opened, say so; never describe contents you did not read.
5. Verify by research. For every comment, tracked edit and memo claim that states a fact, figure, date, comp, market size, regulation or competitor fact, run a web lookup (and the data room) and recompute every number (ownership under pre- vs post-money SAFEs, dilution, break-even, MOIC, IRR, share of fund, runway, use of funds). Show the arithmetic. Prefer primary sources (government pages, filings, company releases) and check the version and as-of date of any report. If a comment cites numbers that match no published version, say so.
6. Investor lens. Read the memo as a skeptical committee member judging an early-stage company, and check each area, adding edits where the memo is silent, stale or unsupported:
   - Team: founder-market fit, full-time status, equity and vesting, key-person dependency, advisors, hiring plan against cash, references to run.
   - Problem and market: bottom-up sizing with sources, how addressable and serviceable figures are filtered, why now, who pays, who the first customer really is.
   - Product and tech: stage versus claims, what is proven versus modeled, defensibility, IP ownership and assignment, freedom to operate, university or prior-employer claims.
   - Traction: revenue quality, retention, concentration, pilots versus signed contracts, letters of intent, grants versus demand. At this stage traction is often thin; say what exists and do not dress up what does not.
   - Competition and comps: real competitors, exit comps with deal structure (upfront versus milestones, acquisition versus license) and dates.
   - Business model and unit economics: pricing basis, margins, cost of goods assumptions and what they rest on.
   - Financials and round: use of funds, burn and runway in months, cap table, existing instruments, SAFE caps and discounts, MFN, lead and commitments versus the round minimum, working capital, next-round milestones and who funds them.
   - Returns: ownership at entry and exit, dilution path through later rounds, base, downside and bull cases, probability weighting, horizon versus fund life, concentration in the fund.
   - Risks and terms: contract or grant mechanics, side letter and information rights, regulatory path, key dependencies.
   - Fit and process: mandate fit, check size, tracking stage, deadlines, owners for open diligence items.
   - Internal consistency: the recommendation, executive summary and risk sections must name the same binding constraint and the same conditions.
   Add sector checks as needed. Biotech and deep tech: regulatory path and timeline, trial design authorship, manufacturing scale-up, grant payment mechanics and cash float, dose translation. Software: net revenue retention, CAC, payback. Hardware: bill of materials, certification, supply chain.
7. Never invent data. Opinions, probabilities and assumptions stay labeled as the investor's judgment or the commenter's view. Where nothing could be verified, say so in the item and in a closing "What I could not verify" list. Do not soften the memo's key points when adopting a comment's wording.
8. Write each edit as an exact replacement or insertion that reads correctly in place. Use bracketed placeholders such as [founder to supply] when a number is not in any source. When several items edit the same bullet, give distinct FIND strings and say which to apply first.
9. Build the checklist. Page features where the format allows: copy buttons for FIND and NEW WORDS; a tick box per item that is saved; a per-item discussion panel; a verdict badge; section jump links; a progress counter; filters (All, To do, Decide first, Done, Disputed); light and dark themes; a phone-width layout; a What I could not verify list. Title: a short noun phrase naming the memo, for example "Company Memo Edit Checklist".

## Arguing back and forth

The user must be able to challenge any item and get a real answer.

- On the page: each item has a discussion panel that sends the item's full context (comment, memo line, proposed edit, evidence and sources) plus these instructions: concede when the user's point is right and say what changes; hold the position with the cited evidence when it is not; separate what is sourced from what is judgment; never cave to pressure alone; state that the page cannot search the web. The user can mark an item Accepted, Disputed or Revised, and the stance plus a one-line note is saved.
- In the session: when the user brings a disagreement back to the chat, re-run the research the point calls for (web, deal record, data room), answer with the evidence, and update the item's wording or verdict. Read saved stances and notes before updating. Do not change an edit just because the user objects; change it when the evidence changes.

## Preferences to honor

- Citations next to every suggestion.
- Plain, unhurried wording; no emojis; ask at most one question.
- Keep the user informed with a short message if a step takes long.

## After the run

Offer to update this skill with anything the user corrected during the session.
