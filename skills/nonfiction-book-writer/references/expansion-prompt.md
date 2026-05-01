# Nonfiction Book Writer Prompt Flow

Use this workflow to create the outline first and then expand each subsection into full narrative text.

## Step 1: Outline generation prompt

When the user provides a topic and keywords, use this exact prompt shape:

`Create a detailed 16-20 chapter book outline for the topic. For each chapter include subsections with dot points talking about the exact content to be covered. Using these keywords:`

Append the user's topic and keyword list after the prompt.

## Expected outline qualities

The generated outline should:

- contain between 16 and 20 chapters unless the user explicitly requests a different number
- give each chapter a useful, specific title
- include subsections for each chapter
- include bullet points that describe the exact content to be covered
- reflect the supplied keywords in a natural, relevant way
- create a progression that can support a full-length nonfiction book

## Step 2: Section expansion prompt

After the outline exists, use this workflow to expand each subsection into full narrative text.

This process has two steps:

1. Expand the original subsection outline into a more detailed plan.
2. Convert that detailed plan into full narrative prose.

### Step 2A: Outline expansion prompt

You are a professional non-fiction author and an expert in [TOPIC]. You are working on a book called [BOOK TITLE].

Please expand the subsection below into a more detailed outline. Add useful subheadings, supporting bullet points, practical takeaways, likely examples, and any references or evidence this section may need.

## Section to expand

**[Section Title]**

[Section description/content from outline]

## Output goals

- create a more detailed outline with subheadings and bullet points
- identify where examples should appear
- identify likely evidence or references to include
- keep the structure practical and draftable

### Step 2B: Narrative expansion prompt

You are a professional non-fiction author and an expert in [TOPIC]. You are working on a book called [BOOK TITLE].

Please expand the following detailed outline into full narrative-style text. Maintain the structure while turning the points into flowing paragraphs.

Requirements:
- Use a professional, neutral tone.
- Start with a grounded, specific opening that states the problem or context.
- Use full sentences and cohesive paragraphs.
- Each subsection must have at least 2 paragraphs.
- Each paragraph should have at least 3 sentences unless a strong writing reason justifies otherwise.
- Keep sentence length moderate to long and avoid choppy cadence.
- Use practical, precise language rather than abstract generalities.
- Add brief, relevant real-world examples where useful.
- Integrate bullet points naturally into the narrative flow when they improve clarity.
- End the section with `Section Summary` and `References` in bullet format.

Strictly avoid:
- em dashes
- habitual "not this but that" sentence structures
- hyperbolic language
- rhetorical repetition
- motivational filler

## Detailed outline

**[Section Title]**

[Expanded outline from Step 2A]

## Output format

```markdown
## [Section Title]

[Full narrative prose...]

### Section Summary
- [Summary bullet 1 as a complete sentence.]
- [Summary bullet 2 as a complete sentence.]

### References
- [Reference 1]
- [Reference 2]
```

## Variables to replace

- `[TOPIC]` - the subject matter of the section
- `[BOOK TITLE]` - full title of the book
- `[Section Title]` - title of the subsection from the outline
- `[Section description/content from outline]` - the original outline material
- `[Expanded outline from Step 2A]` - the detailed plan produced in the first expansion step
