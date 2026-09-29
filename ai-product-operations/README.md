# AI-Assisted BRD Breakdowns to User Stories and Jira Upload Automation

### From requirements documents to refinement-ready Jira stories

As a Senior Product Manager at DTCC, I established a shared workflow that uses **Kiro agents, Jira tools connected through Model Context Protocol (MCP), and reusable agent skills** to turn business and product requirements into structured user stories. It combines AI drafting, consistent quality checks, and product manager review, with tools and skills managed in Bitbucket for team use.

## The problem

Turning a Business Requirements Document (BRD) or Product Requirements Document (PRD) into a backlog requires substantial preparation: interpreting requirements, breaking down scope, writing acceptance criteria, identifying dependencies, and entering everything into Jira.

Done manually, this creates repetitive work and inconsistent story quality. Ambiguities can carry into refinement, while context becomes scattered across documents and tickets. My goal was to improve story preparation and give product managers more time for decisions and stakeholder conversations.

## My contribution

I brought the requirements breakdown process, Jira integration, and shared standards into one workflow by:

- Translating story-writing expectations into reusable agent instructions and skills.
- Connecting drafting and review to Jira through MCP server tools.
- Incorporating Definition of Ready checks into story preparation and improvement.
- Establishing product manager review before creating or updating Jira stories.
- Managing the shared tools and skills in Bitbucket so the team can reuse and improve them.

## How it works

**1. Understand and clarify the requirements.** A product manager provides a BRD, PRD, mockup, or other requirements source. Kiro reads the material and surfaces unclear requirements, contradictions, overlapping scope, and open questions. The product manager resolves these through a conversation with the agent.

**2. Break the work into stories.** The agent proposes discrete pieces of work with clear user value. It drafts descriptions and testable acceptance criteria, captures business rules, and flags oversized stories or possible dependencies. Stories retain references to their source requirements so reviewers can follow how the backlog was derived.

**3. Assess readiness and improve the draft.** Shared rules grade stories against the team's Definition of Ready. The agent uses those same expectations when drafting, identifies gaps, and helps the product manager address them before refinement.

**4. Review and publish to Jira.** The product manager reviews the content and confirms the relevant project, priority, epic, and release information. Once approved, the agent uses the Jira connection to create or update stories, populate the required fields, and add approved dependency links.

**5. Refine with the delivery team.** The team uses the prepared stories to discuss implementation, validate scope, and assign estimates.

## The building blocks

| Component | Role in the workflow |
| --- | --- |
| **Kiro agents** | Read requirements, ask clarifying questions, propose story breakdowns, and draft or revise content with the product manager. |
| **Agent skills and steering rules** | Supply reusable instructions for story structure, readiness checks, dependency handling, and review before Jira updates. |
| **Jira MCP server tools** | Let the agent retrieve existing issues and their history, create or update stories, and manage supporting fields and relationships. MCP provides the connection between the agent and these tools. |
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

The agent is instructed to flag missing information and distinguish assumptions from confirmed requirements. Product managers remain responsible for business decisions, resolving ambiguity, and approving what goes into Jira.

## Making it reusable across the team

The server tools and agent skills are managed in a shared **Bitbucket repository**. Product managers reuse a common, versioned set of assets, with story-writing guidance and readiness rules maintained alongside the integration tools that apply them.

This makes changes traceable and lets improvements spread across the team. For example, a skill updated to handle ambiguous requirements more effectively can be reused by other product managers in their own work.

## Practical value

The workflow has been applied to breaking requirements into multi-story backlogs, improving existing Jira stories, and reconstructing requirements summaries from existing issues.

It reduces manual re-entry, supports consistent story preparation, and preserves the connection between requirements and delivery work. The product operations benefit is a repeatable process the whole PM team can use, with human judgment built into the points where decisions matter.

---

*This case study describes my work at a generalized level. Internal project names, document references, and implementation details have been omitted or simplified.*
