---
name: add-resource
description: Use this skill when the user gives a URL to a robotics-adjacent tutorial, course, textbook, docs site, or GitHub repo and wants it added to this educational-resources repository. Fetches the page, summarizes it, works out proper attribution and free/paid status, checks for duplicates, proposes the right topics/*.md file and section, and — after the user confirms — edits the file to match this repo's entry format.
---

# Add Educational Resource

Adds a new entry to this repo's curated list of free robotics learning resources, following the conventions in `CLAUDE.md`.

## Inputs

The user provides a URL (as the skill argument or in their message). If no URL is present, ask for one before doing anything else.

## Steps

### 1. Fetch the content

Use WebFetch on the URL. Pull out:
- The real title of the resource (not just the `<title>` tag if it's noisy — use what a reader would recognize).
- The author, instructor, or owning institution/organization (e.g. "Andrew Ng, DeepLearning.AI & Stanford Online", "Open Robotics", "Google DeepMind"). For a GitHub repo, this is the org/user that owns it.
- What the resource actually covers and its rough difficulty level (beginner / intermediate / advanced), based on real content, not marketing copy.
- Any license (check for a LICENSE file/badge on GitHub repos — e.g. Apache 2.0, MIT, BSD, CC).

If the fetch fails or the page requires login to view any content, tell the user and stop rather than guessing.

### 2. Check free/paid status

Per `CLAUDE.md`, every listed resource must be free to access.

- If it's a Coursera/edX course, check whether it has a free **audit** option (full video/material access without payment). This is a well-established pattern in this repo — note it in the entry, e.g. "(Coursera, free to audit)".
- If it's a GitHub repo, docs site, personal course page, or similar with no paywall, it's free.
- If it looks paywalled, subscription-gated, or requires payment for the core material (not just a certificate) — flag this clearly to the user and ask whether to proceed. Do not silently add paid content.
- Note any hard requirements that aren't quite "cost" but gate access similarly (e.g. Isaac Sim's GPU requirement, a required free developer account) — mention these the way `topics/simulation.md` does, as a caveat rather than a blocker.

### 3. Check for duplicates

Before proposing anything, grep the repo for signs this resource (or a near-duplicate) is already listed:

```
grep -ril "<domain-or-distinctive-path>" topics/ README.md learning-path.md
grep -ril "<resource-title-keywords>" topics/ README.md learning-path.md
```

If something very similar is already there, tell the user what exists and ask whether they still want to add this one (e.g. as a complementary resource) or skip.

### 4. Draft the summary and citation

Write a 1–2 sentence description in the same terse, information-dense style as existing entries (see any file in `topics/` for examples — e.g. `topics/simulation.md`, `topics/machine-learning-and-ai.md`). State what it teaches and, where useful, its difficulty level or how it compares to similar listed resources. Don't editorialize or use marketing language from the source page.

Format the citation line to match the established pattern:

```
- **<Title>** — <Author/Institution>[, <parenthetical note: e.g. Coursera free to audit, license, hardware requirement>]
  <URL>
  <1–2 sentence description.>
```

### 5. Pick the destination

Read `README.md`'s topic table and skim the relevant file(s) in `topics/` to decide:

- **Which topic file** this belongs in (ROS 2, Software Engineering, Computer Vision, Embedded Systems, Mechanical Engineering & CAD, Machine Learning & AI, Cloud & DevOps, Simulation, or Links to Lectures). Some resources plausibly fit two files — pick the primary one and mention the alternative to the user.
- **Which section within that file** — most topic files are organized into `##` subsections by tool/subtopic (e.g. `simulation.md` has Gazebo / MuJoCo / NVIDIA Isaac Sim / Other Simulators); others use a flat `## Resources` list (e.g. `machine-learning-and-ai.md`). Match the existing structure rather than inventing a new section unless nothing fits.
- **Where in that section** — entries aren't strictly alphabetical; they're grouped by relatedness/progression. Place the new entry near the most similar existing entries (e.g. next to other resources from the same author, or at the point in the beginner→advanced progression where it belongs).

If nothing in the existing 8 topics fits at all, this may warrant a **new topic file**. That's a bigger structural change (new `topics/<name>.md`, a new row in `README.md`'s table, and possibly a `learning-path.md` update per `CLAUDE.md`) — flag this to the user explicitly and confirm before creating a new topic, rather than assuming.

### 6. Confirm with the user before editing

Present, in one message:
- The drafted citation block (title, author, URL, description) exactly as it would appear.
- Free/audit/paid status and any caveats found in step 2.
- Duplicate-check result from step 3.
- Proposed destination: file, section, and position (what it would sit next to).

Ask the user to confirm or adjust any of the above. Do not edit any files until they confirm.

### 7. Make the edit

Once confirmed, use Edit to insert the entry into the target file, matching exact formatting: bold title, em dash before author, URL on its own indented line, description on its own indented line, one blank line between entries. If a new topic file, README.md row, or learning-path.md change was agreed in step 5, make those edits too.

Do not commit. Leave the change for the user to review via `git diff` and commit themselves.
