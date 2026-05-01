---
name: nonfiction-book-editor
description: Edit, expand, and polish nonfiction book manuscripts in markdown with consistent structure, stronger examples, practical enhancements, and formatting cleanup. Use when the user has an existing nonfiction manuscript, compiled markdown book, or chapter set that needs developmental editing, expansion, practical additions, structural cleanup, style normalization, or final polish before export.
---

# Nonfiction Book Editor

Edit and enhance nonfiction books after drafting.

## Scope

Use this skill after a nonfiction book outline has already been turned into draft chapters or a compiled manuscript.

Typical inputs:

- `books/nonfiction/<book-slug>/<book-slug>.md`
- `books/nonfiction/<book-slug>/chapters/`
- a partial or complete nonfiction markdown manuscript

## Workflow

### Phase 1: Assessment and editing plan

1. Read the manuscript or target chapters.
2. Identify the current state:
   - structural gaps
   - weak sections
   - repetition
   - missing examples or practical material
   - formatting inconsistencies
3. Decide what kind of edit is needed:
   - developmental edit
   - expansion edit
   - structural cleanup
   - style cleanup
   - final polish
4. Produce a concise editing plan before large changes.

### Phase 2: Content editing and expansion

Prefer meaningful improvements over decorative additions.

High-value editing moves:

- add missing chapters only when the book genuinely needs them
- strengthen weak chapters with clearer progression
- add practical frameworks, templates, checklists, or exercises when they increase usefulness
- add case studies or examples where abstraction is hurting clarity
- add failure modes, common mistakes, or troubleshooting sections where appropriate
- sharpen transitions and chapter endings
- remove repetition and topic overlap

### Phase 3: Formatting and consistency cleanup

Normalize the manuscript after content decisions are stable.

Check for:

- heading consistency
- spacing consistency
- bullet formatting
- chapter summary consistency
- reference formatting consistency
- paragraph readability
- chapter numbering consistency

Do not run broad automated rewrites that might distort meaning unless the user specifically wants bulk normalization and the file is backed up or versioned.

### Phase 4: Quality check

Before finalizing:

- read representative sections for flow and consistency
- verify chapter order still makes sense
- confirm the table of contents if present
- confirm new additions fit the book's tone and purpose
- flag any sections that still need author review

## Editing priorities

Use this order unless the user asks otherwise:

1. structural clarity
2. usefulness to the reader
3. examples and practical depth
4. style and rhythm
5. formatting polish

## Expansion options

When a nonfiction manuscript is too thin, expand with useful material such as:

- practical application sections
- checklists
- templates
- step-by-step procedures
- case snapshots
- failure modes and fixes
- diagnostic questions
- brief reflective exercises

Avoid filler, motivational padding, and repetitive emphasis.

## Output pattern

When making substantial edits, preserve a clear trail:

- update the manuscript or chapter files
- add a short edit summary in `notes/` when useful
- mention what changed and what still needs review

## Relationship to nonfiction-book-writer

`nonfiction-book-writer` is the primary creation workflow.

Use this editor skill after the writer skill has:
1. generated the outline
2. drafted the chapters
3. compiled the markdown manuscript

Default sequence for a new book:
- generate outline
- draft chapters
- compile manuscript
- edit and polish with this skill
- export final DOCX

## Done criteria before export

A nonfiction manuscript is ready for export only when:

- structure is coherent
- repetition has been reduced
- weak sections have been strengthened or flagged
- formatting is consistent enough for clean DOCX conversion
- the manuscript meets the shared quality bar in `references/final-manuscript-checklist.md`
