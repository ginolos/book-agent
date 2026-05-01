---
name: fiction-bedtime-story-collection
description: Create children's bedtime story collections as a complete book package, including collection concept, 15 unique story seeds, introduction, conclusion, compiled markdown, DOCX export, and Amazon KDP marketing assets. Use when the user wants a themed bedtime-story book for children ages 4-8 built around topics like fairies, mermaids, princesses, pets, or similar child-friendly themes, with consistent title patterns, gentle lessons, and non-repetitive short stories.
---

# Fiction Bedtime Story Collection

Create a themed children's bedtime story collection from concept through compiled book.

## Scope

Use this skill for children's bedtime story books aimed at ages 4-8.

Default collection format:

- 1 themed collection
- 1 one-sentence dedication
- 15 short stories
- 1 introduction
- 1 conclusion
- compiled markdown manuscript
- DOCX export via pandoc
- Amazon KDP description
- Amazon KDP keywords

## Collection format rules

### Book title

Use this pattern:

- `[Topic] Tales`

Examples:

- `Fairy Tales`
- `Mermaid Tales`
- `Princess Tales`
- `Pet Tales`

### Subtitle

Use this pattern:

- `15 <adjective> Bedtime Stories for Kids`

Examples:

- `15 Magical Bedtime Stories for Kids`
- `15 Gentle Bedtime Stories for Kids`
- `15 Cozy Bedtime Stories for Kids`

### Story title pattern

Use this pattern for each story:

- `{Topic-singular} {Name} and the {Story Aspect}`

Examples:

- `Fairy Lilac and the Shrinking Garden`
- `Mermaid Pearl and the Singing Shell`

### Audience and tone

Write for children ages 4-8.

Prioritize:

- warmth
- clarity
- gentle wonder
- emotional safety
- simple but vivid language
- reassuring endings

## Workflow

### Step 1: Choose the collection topic

Choose or confirm a child-friendly topic that suits bedtime reading.

Examples:

- fairies
- mermaids
- princesses
- pets
- forest friends
- little dragons
- unicorns
- moonlit animals

If the user already gives the topic, use it.

### Step 2: Create the 15-story seed list

Before drafting stories, create a planning list for all 15 stories.

For each story, define:

- name
- setting
- plot
- conflict
- resolution
- extra element
- lesson

Each story seed should be distinct.

Check the full set before writing to ensure:

- no repeated main character names
- no repeated core plots
- no repeated resolutions used too similarly
- enough variation in setting and emotional situation

If repetition appears, replace the duplicate item before drafting.

## Step 3: Draft each story

Write each story in markdown.

Target length per story:

- 800 to 1000 words

Use this prompt shape when drafting each story:

`You are a children's short story author working on a collection of {topic} bedtime stories. Can you write an 800-1000 word short story for kids about a {topic} {name}. Plot: {plot} with {conflict}, resolved by {resolution} to teach kids {lesson}. Aim for kids ages 4-8. In the output, do not put dividers in the text. Add a title in the format "{Topic} {name} and the...". Limit the use of the em dash, and avoid not this but that sentence structure.`

Incorporate the extra element naturally into the story.

Write in full, natural sentences throughout.

Write each story as finished bedtime-story prose, not as expanded notes. The story should feel calm, continuous, and readable aloud, with a clear setting, a gentle character problem, understandable cause-and-effect, and smooth transitions from one moment to the next. Include concrete sensory details, character actions, emotional reactions, and a reassuring flow that carries the child naturally toward the ending.

Aim for prose that feels warm, cozy, emotionally safe, and complete on the page. The final story should read like a polished bedtime tale rather than a summary of story beats.

Do not leave planning language, outline fragments, shorthand plot summaries, prompt residue, template scaffolding, or broken sentence structures inside the prose.

## Step 4: Write the dedication

Write a one-sentence dedication before the introduction.

The dedication should:

- be warm and gentle
- be directly related to the collection topic
- feel specific rather than generic
- be suitable for children and families

Example pattern:

- `For every little animal lover who finds magic in soft paws, wagging tails, and bedtime cuddles.`

## Step 5: Write the introduction

Write a short introduction after the dedication and before the first story.

Use this prompt shape:

`You are a children's short story author working on a collection of {topic} bedtime stories. Write a short introduction telling children that they will read stories of {topic} to learn lessons about kindness, friendship, family, bravery, and other themes such as {lessons}.`

The introduction should feel welcoming, calm, and suitable for bedtime.

## Step 6: Write the conclusion

Write a short conclusion after the final story.

The conclusion should:

- gently close the collection
- echo the themes and lessons
- leave the child with a warm, settled feeling

## Step 7: Consistency pass

After all stories are drafted, review the full collection for:

- repeated names
- repeated story structures
- inconsistent character names inside stories
- tone drift
- lesson repetition
- title pattern consistency

Fix any repetition or continuity errors before compiling.

## Step 8: Compile and export

Combine the dedication, introduction, all markdown stories, and the conclusion into one markdown manuscript and convert it to DOCX using pandoc.

## Step 9: Create Amazon KDP assets

After the book files are complete, create Amazon KDP marketing files in markdown.

Create:

- one KDP-ready book description
- one keyword list for the 7 Amazon KDP keyword slots

The KDP description should:

- clearly describe the theme, audience, and bedtime tone
- highlight the emotional benefits and story content
- use short paragraphs and scannable benefit bullets
- include a version formatted for Amazon KDP using simple supported markup such as `<br>`, `<b>`, and `<i>`

The KDP keywords file should:

- provide 7 keyword phrases suitable for Amazon KDP backend slots
- avoid repeating the exact full title too heavily
- focus on likely parent and gift-buyer search intent
- include an optional supporting SEO word bank for future metadata use

## File structure

Use this structure for a collection project:

- `books/fiction/<collection-slug>/README.md`
- `books/fiction/<collection-slug>/01-collection-plan.md`
- `books/fiction/<collection-slug>/02-story-seeds.md`
- `books/fiction/<collection-slug>/stories/story-01.md`
- `books/fiction/<collection-slug>/stories/story-02.md`
- `books/fiction/<collection-slug>/...`
- `books/fiction/<collection-slug>/dedication.md`
- `books/fiction/<collection-slug>/introduction.md`
- `books/fiction/<collection-slug>/conclusion.md`
- `books/fiction/<collection-slug>/<collection-slug>.md`
- `books/fiction/<collection-slug>/<collection-slug>.docx`
- `books/fiction/<collection-slug>/amazon-kdp-description.md`
- `books/fiction/<collection-slug>/amazon-kdp-keywords.md`

## Output order in compiled manuscript

1. title
2. subtitle
3. dedication
4. introduction
5. story 1 through story 15
6. conclusion

## References

Read these only when needed:

- `references/story-seed-template.md` — planning format for the 15-story seed list
- `references/bedtime-quality-checklist.md` — final checks for repetition, tone, and child-readiness
