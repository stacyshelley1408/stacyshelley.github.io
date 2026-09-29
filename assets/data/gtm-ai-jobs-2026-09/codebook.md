# Codebook: how GTM job postings ask people to use AI

Version 1, frozen 24 September 2026 before any held-out posting was labeled. The codes were derived by reading every
AI-related sentence in an exploration sample of 165 postings (15 per job family). That sample is excluded from all
results. Clarifying rules added after the audits are listed at the end; no code definition changed.

## Unit of coding

The sentence. Section headings cannot be trusted to separate company boilerplate from role content, so each
AI-related sentence is coded on its own. A heading that carries the signal on its own ("AI Mindset: Use new
technologies for performance advantage") is coded as a sentence.

A sentence is "AI-related" if it matches: AI, A.I., artificial intelligence, GenAI, generative, LLM, large language,
agentic, agent(s), machine learning, ML, ChatGPT, Claude, Copilot, Gemini, Perplexity, Cursor, prompt(s)/prompting.
"Automation" alone is not an AI term ("marketing automation platform" means Marketo).

## Codes

### Not about the job
- **X1 Company or product.** What the company sells or believes. "the AI-powered platform"
- **X2 Hiring process.** AI in screening, candidate AI policies, legal notices, text addressed to AI applicants.
- **N** Matched the AI filter but is not about AI (for example "insurance agents", a company domain ending in .ai).

### AI as the subject of the job, not something the person uses
- **S1 Sell, position or market AI.** "Articulate the value of AI/agentic capabilities."
- **S2 Know the AI landscape.** "Familiarity with the current AI/LLM landscape."

### Company-wide expectation
- **C1** How everyone at the company is expected to work, not specific to this role. "All team members are expected
  to incorporate AI into their daily workflows." Never counted as role-level usage.

### Role-level usage
- **U1 Disposition only.** Openness, curiosity or fluency with no task named. "Open to using AI to amplify their
  skills."
- **U2 Existing tasks, faster.** A named existing task done with AI. "Use AI tooling to move faster on account
  research, proposal drafting, forecast summaries."
- **U3 Adopt AI vendor tools.** Use or roll out AI features of bought tools (Gong, Clay, conversation intelligence,
  AI writing tools).
- **U4 Build or redesign.** Build AI workflows, agents, automations or tools for yourself or others; lead a team's AI
  adoption; redesign how the function works. "Build lightweight tools, prompts, and workflows ... share them across
  sales, channel, and marketing rather than keeping them personal."
- **U5 Govern AI output or encode standards into AI.** Define how voice, brand or claims live in AI workflows; judge
  AI output against a standard. Each U5 sentence also carries a kind:
  - **self**: the person judges their own AI output ("validate outputs before using them")
  - **org**: sets standards or guardrails for AI systems others use
  - **content**: governs AI-generated content or owns the source material AI generates from ("maintain the core
    'brain' of PMM context that feeds our AI-first approach")
- **U6 Write for AI as the reader.** Answer-engine optimization; being retrieved and cited by AI assistants.

A sentence can carry more than one code.

### Placement (usage sentences only)
responsibility, role summary, required, preferred.

## Posting-level measures used in the analysis
- **Role usage**: any U1 to U6 in the posting.
- **Task named**: any U2 to U6.
- **Build/redesign**: any U4.
- **Retrofit only**: U2 or U3, no U4.
- **Content governance**: U5 with kind "content".
- **Generate with AI** (derived, not hand-coded): a U2, U3 or U4 sentence that matches a keyword filter for producing
  customer-facing material (drafts, copy, decks, proposals, personalization, emails, outreach, landing pages,
  variants, collateral). The filter was checked by hand at about 90% precision.

## Clarifying rules from the audits (applied to all labels through `corrections.csv`)
1. U4 means something is built or a function is redesigned. "Leverage AI and workflows to improve efficiency" is not
   U4; it is U2 if a task is named, U1 if not.
2. U2 needs a named task. "Use AI to work smarter" is U1.
3. A "without compromising quality" clause on its own is U5 self, not content governance.
4. Prototyping with AI tools is U2 (a task done with AI), not U4.
