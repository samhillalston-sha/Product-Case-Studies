# AI-Assisted BRD Breakdowns to User Stories and Jira Upload Automation

### End-to-end automation: from a requirements document to fully prepared stories in Jira

As a Senior Product Manager at DTCC, I established a workflow that takes a requirements document all the way through to **fully prepared user stories uploaded to Jira**. Kiro takes a first pass at the document and proposes a story breakdown. I then iterate with it to refine the stories, challenge assumptions, and uncover gaps in the requirements. Once the stories are right, Kiro uploads them to Jira in moments, including their acceptance criteria, required fields, and approved relationships.

**This saves hours of manual work across requirements breakdown, story writing, formatting, and Jira entry.** Product managers focus their time on evaluating the requirements and making decisions throughout the process.

The workflow combines reusable Kiro agent skills with Jira tools connected through Model Context Protocol (MCP). The tools and skills are managed in Bitbucket so the whole product team can use and improve the same process.

## The problem

Turning a Business Requirements Document (BRD) or Product Requirements Document (PRD) into a backlog requires substantial preparation: interpreting requirements, breaking down scope, writing acceptance criteria, identifying dependencies, and entering everything into Jira.

Done manually, this creates repetitive work and inconsistent story quality. Ambiguities can carry into refinement, while context becomes scattered across documents and tickets. My goal was to eliminate as much of the grunt work as possible, leaving more time for thoughtful analysis of the created requirements and of course all the other things product managers do.

## My contribution

I brought the requirements breakdown process, Jira integration, and shared standards into one workflow by:

- Translating story-writing expectations into reusable agent instructions and skills.
- Connecting requirements analysis, iterative story development, and direct Jira upload through MCP server tools.
- Incorporating Definition of Ready checks into story preparation and improvement.
- Establishing product manager review before creating or updating Jira stories.
- Managing the shared tools and skills in Bitbucket so the team can reuse and improve them.

## How it works

**1. Kiro takes the first pass.** A product manager provides a BRD, PRD, mockup, or other requirements source. Kiro reads it and proposes a breakdown into individual stories, with draft descriptions, business value, and acceptance criteria. It also surfaces initial questions and gaps.

**2. The product manager and Kiro iterate together.** We work through the proposed stories, adjust scope, sharpen acceptance criteria, and challenge the underlying requirements. Kiro helps identify contradictions, missing business rules, edge cases, and dependencies. That conversation continues until the stories accurately reflect the intended work, with references back to the source requirements.

**3. Check readiness and approve.** Shared skills guide the writing, while Definition of Ready rules help identify remaining gaps. The product manager reviews the stories and confirms the project, priority, epic, release, and any dependency links before upload.

**4. Kiro uploads the prepared stories to Jira.** Through the MCP tools, Kiro creates the stories directly in Jira in moments, populating descriptions, acceptance criteria, required fields, and approved links. This completes the journey: the backlog is in Jira, ready for team refinement, without the product manager manually copying and configuring each ticket.

The delivery team then discusses implementation, validates scope, and assigns estimates during refinement.

## The building blocks

| Component | Role in the workflow |
| --- | --- |
| **Kiro agents** | Read requirements, ask clarifying questions, propose story breakdowns, and draft or revise content with the product manager. |
| **Agent skills and steering rules** | Supply reusable instructions for story structure, readiness checks, dependency handling, and review before Jira updates. |
| **Jira MCP server tools** | Turn approved drafts into populated Jira stories, including acceptance criteria, required fields, and relationships. They also retrieve and update existing issues. |
| **Shared Bitbucket repository** | Keeps the server tools and agent skills together under version control for team use and continued improvement. |

Existing stories are retrieved before editing, giving the agent context for targeted changes that preserve relevant information.

## Quality standards and product judgment

The **Definition of Ready** is the team's agreed standard for whether a story contains enough information to move into delivery. We translated it into rules that grade readiness and guide the skills used to craft stories, giving product managers a consistent way to identify gaps.

The readiness score uses the following weighted criteria:

| Readiness criterion | Weight | How the workflow addresses it |
| --- | ---: | --- |
| Clear, user-centered description | 20% | States the user, their need, and the intended outcome. |
| Testable acceptance criteria | 16% | Defines independently testable requirements. |
| Dependencies identified | 16% | Checks dependencies and proposes links for product manager approval. |
| Team estimation | 16% | Reserved for the delivery team during refinement. |
| Business value articulated | 10% | Explains why the story matters. |
| Target release assigned | 8% | Confirms and sets the intended release. |
| Linked to an epic | 8% | Connects the story to the agreed parent initiative. |
| Small enough for one sprint | 6% | Flags oversized stories and suggests how to split them. |
| **Total** | **100%** | |

The score helps identify missing information; product managers and the delivery team still validate the substance.

Examples of the reusable skill instructions:

- **Story-writing style:** Use “As a [user], I want [capability], so that [outcome],” followed by a short business-value sentence. Keep the description concise and write in plain business language.
- **Content rules:** Write independently testable acceptance criteria under clear headings. Capture confirmed business rules, flag unknowns, and distinguish assumptions from documented requirements.

Product managers remain responsible for business decisions, resolving ambiguity, and approving what goes into Jira.

## Making it reusable across the team

The server tools and agent skills are managed in a shared **Bitbucket repository**. Product managers reuse a common, versioned set of assets, with story-writing guidance and readiness rules maintained alongside the integration tools that apply them.

This makes changes traceable and lets improvements spread across the team. For example, a skill updated to handle ambiguous requirements more effectively can be reused by other product managers in their own work.

## Practical value

The main value is completing the full journey in one workflow: read the requirements, draft the stories, iterate on their substance, check quality, and upload the finished work directly to Jira. Automating the preparation and administrative tasks saves hours while giving product managers room to scrutinize the requirements along the way.

The finished product is a set of fully prepared Jira stories that the delivery team can pick up for refinement. The same tools also support improvements to existing stories and reconstruction of requirements summaries from Jira issues.

---

*This case study describes my work at a generalized level. Internal project names, document references, and implementation details have been omitted or simplified.*
