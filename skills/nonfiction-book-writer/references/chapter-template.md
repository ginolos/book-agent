# Chapter Output Template

Use this template when writing completed nonfiction chapters.

```markdown
# Chapter X: [Chapter Title]

[Grounded introduction that names the problem, context, or reader situation. Do not add a literal "Opening Hook" heading unless the project explicitly wants one.]

---

## [Section 1 Title]

 [Full narrative content with cohesive paragraphs. Use integrated bullet points only when they improve clarity and flow.]

Optional practical list:

- [Useful action, diagnostic question, or decision criterion.]
- [Useful action, diagnostic question, or decision criterion.]

Optional compact table:

| Situation | Reader action | Evidence to check |
| --- | --- | --- |
| [Condition] | [Action] | [Evidence] |

### Section Summary
- [Summary 1 as a complete sentence.]
- [Summary 2 as a complete sentence.]

### References
- [Reference 1]
- [Reference 2]

---

## [Section 2 Title]

[Full narrative content with cohesive paragraphs.]

### Section Summary
- [Summary 1 as a complete sentence.]
- [Summary 2 as a complete sentence.]

### References
- [Reference 1]

---

## Conclusion

[Chapter conclusion tying together the practical or conceptual throughline.]

## Chapter Summary
- [Summary point 1 as a complete sentence.]
- [Summary point 2 as a complete sentence.]
- [Summary point 3 as a complete sentence.]
```

## Scanability guidance

Use bullets and tables selectively. A chapter should still read like a book chapter, but dense practical material should not appear only as long blocks of prose. Good table uses include:

- comparing stakeholder groups
- clarifying roles and decision rights
- showing common failure modes and fixes
- summarizing metrics
- listing readiness signals and responses

## Filename convention

Save as `chapter-XX.md` with zero padding, for example `chapter-01.md`.

## Directory structure

```text
books/nonfiction/[book-slug]/
├── outline.md
├── chapters/
│   ├── chapter-01.md
│   ├── chapter-02.md
│   └── ...
├── [book-slug].md
├── [book-slug].docx
└── resources/
```

Use `resources/` for research, notes, supporting references, and background material when needed.
