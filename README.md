# AI Resume Analyzer

Compares a resume with a job description, finds missing skills, and suggests improvements.

## Run it

```bash
npm install
npm run dev
```

Open http://localhost:3000.

## Current state (step 1: skeleton)

- Input form for resume and job description
- Shimmer skeleton screen while analysis runs (no spinner)
- `/api/analyze` route with input validation
- `lib/analyzer.js` returns sample data for now

## Roadmap

1. **Skeleton UI**: done
2. **Skill extraction**: pull skills from both texts using keyword lists or an NLP library such as `compromise` or `natural`
3. **Matching**: compare the two skill sets and calculate a match score
4. **LLM suggestions**: send the resume and job description to an LLM API (set the key in `.env.local` as `OPENAI_API_KEY` or `ANTHROPIC_API_KEY`) and get rewrite suggestions
5. **File upload**: accept PDF or DOCX resumes (for example with `pdf-parse` and `mammoth`)
