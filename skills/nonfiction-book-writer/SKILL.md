---
name: nonfiction-book-writer
description: Create a detailed nonfiction book outline from a topic and keywords, then expand that outline into full chapter prose, chapter markdown files, a compiled manuscript markdown file, and a DOCX via pandoc. Use when the user wants a nonfiction book created from a topic, niche, concept, or keyword set and expects the workflow to begin with a 16-20 chapter outline containing subsection dot points for the exact content to be covered.
---

# Nonfiction Book Writer

Create the outline first, then write the book from that outline.

> This skill is for nonfiction books only.

## Canonical prompt for outline generation

When the user gives a topic and keywords, use this exact prompt shape as the basis for outline generation:

`Create a detailed 16-20 chapter book outline for the topic. For each chapter include subsections with dot points talking about the exact content to be covered. Using these keywords:`

Append the user's topic and keyword list after that instruction.

## Workflow

### Step 1: Generate the outline from topic and keywords

Default assumption: the user gives a topic and keywords, and the outline must be created from that input.

1. Identify the nonfiction topic.
2. Identify or extract the keyword list.
3. Generate a detailed 16-20 chapter outline using the canonical prompt shape.
4. Make sure each chapter contains:
   - a clear chapter title
   - useful subsection titles
   - bullet points describing the exact content to be covered
5. Save the result to the project workspace.

Default project structure:

- `books/nonfiction/<book-slug>/outline.md`
- `books/nonfiction/<book-slug>/chapters/`
- `books/nonfiction/<book-slug>/<book-slug>.md`
- `books/nonfiction/<book-slug>/<book-slug>.docx`

If the user already has an outline, you may refine it, but the preferred workflow is to generate the outline from topic + keywords first.

## Step 2: Expand each chapter section by section

Complete all subsections in a chapter before moving to the next chapter.

### Substep 2A: Expand the subsection outline

For each subsection, first expand the outline into a richer subsection plan.

Target output:

- clearer subheadings
- supporting points
- useful examples to include
- practical takeaways
- likely references or evidence needs

### Substep 2B: Convert the subsection to full narrative prose

Then convert the expanded subsection into readable chapter prose.

Required style rules:

- use a professional, grounded, neutral tone
- begin with a grounded, specific opening that states the problem or context
- use cohesive paragraphs with full sentences
- ensure each subsection has at least 2 paragraphs
- ensure each paragraph has at least 3 sentences unless there is a strong craft reason not to
- keep sentence length moderate to long; avoid choppy cadence
- use practical, precise language
- include brief real-world examples where helpful
- integrate bullet points naturally into the narrative flow
- end the subsection with `Section Summary` and `References` in bullet form

Strictly avoid:

- em dashes
- "not this but that" constructions as a stylistic tic
- overblown hype
- rhetorical repetition
- motivational filler

## Step 3: Check chapter word count

After all subsections for a chapter are drafted:

- check total chapter word count
- if the chapter is below 3,000 words, expand usefully rather than padding
- only move to the next chapter once the chapter is substantively complete

## Step 4: Compile the manuscript markdown

After all chapters are drafted:

1. read the chapter files from `books/nonfiction/<book-slug>/chapters/`
2. combine them into `books/nonfiction/<book-slug>/<book-slug>.md`
3. add a table of contents if helpful

## Step 5: Run the editing pass

After the manuscript is compiled, run an editing and polish pass aligned with `nonfiction-book-editor`.

Editing goals:

- improve structural clarity
- remove repetition
- strengthen weak sections
- add practical frameworks, checklists, examples, or failure modes where they genuinely help
- normalize headings, bullets, summaries, and formatting

For a new book, treat the editor skill as the default post-draft stage rather than an optional extra.

## Step 6: Convert the manuscript to DOCX

Use pandoc only after drafting and editing are complete and the manuscript satisfies the final checklist used by `nonfiction-book-editor`.

```bash
pandoc "books/nonfiction/<book-slug>/<book-slug>.md" -o "books/nonfiction/<book-slug>/<book-slug>.docx"
```

## Whole-book expansion pass

If the compiled manuscript is under roughly 40,000 words and the target is closer to 50,000 words, expand with useful additions such as:

- practical application sections
- checklists
- step-by-step procedures
- templates
- case scenarios
- failure modes and fixes
- decision tools
- diagnostics or self-assessment questions
- first-person professional anecdotes when consistent with the author voice

After expansion, recompile the markdown and regenerate the DOCX.

## Output pattern

Preferred project structure:

- `books/nonfiction/<book-slug>/outline.md`
- `books/nonfiction/<book-slug>/chapters/chapter-01.md`
- `books/nonfiction/<book-slug>/chapters/chapter-02.md`
- `books/nonfiction/<book-slug>/<book-slug>.md`
- `books/nonfiction/<book-slug>/<book-slug>.docx`

## Chapter pattern

Use natural headings. Do not literally insert an "Opening Hook" heading unless the user asked for it.

Recommended chapter shape:

- chapter title
- grounded introduction
- section 1
- section 2
- additional sections as needed
- conclusion
- chapter summary in bullet points

## Scope

Use this as the canonical nonfiction book workflow in this workspace.

The expected flow is:
1. receive topic + keywords
2. generate the 16-20 chapter outline
3. save the outline
4. write the book from that outline
5. edit and polish the manuscript
6. export the finished DOCX
