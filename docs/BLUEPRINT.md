# Veltrix Portfolio — Product and Technical Blueprint

**Document status:** Draft baseline  
**Owner:** Veltrix  
**Last updated:** 2026-10-30

## 1. Product vision
Create a credible, professional public portfolio and engineering hub for Veltrix. It should communicate what Veltrix builds, demonstrate how the work is engineered, and provide verifiable evidence of progress and outcomes.

The portfolio covers multiple disciplines:
- Software products and applications
- Artificial intelligence and AI-enabled systems
- Workflow automation and agents
- Cybersecurity and security engineering
- Creative technology, CGI, and digital media systems
- Digital ventures and experiments

## 2. Audiences
1. **Clients and partners** — understand capabilities, products, and ways to collaborate.
2. **Employers and collaborators** — assess practical skills, engineering quality, and ownership.
3. **Users and communities** — discover products, documentation, demos, and updates.
4. **The founder and contributors** — maintain a reliable public record of work.

## 3. Product principles
- Evidence over claims.
- Clear separation between concepts, prototypes, beta products, and live products.
- Documentation-first engineering.
- Privacy and security by default.
- Fast, accessible, mobile-first experience.
- GitHub as the source of truth.
- Curated presentation rather than indiscriminate publication of every experiment.

## 4. Proposed information architecture
| Route | Purpose |
|---|---|
| `/` | Overview, positioning, featured work, latest verified updates |
| `/about` | Veltrix mission, approach, and team/founder information |
| `/products` | Product directory |
| `/products/[slug]` | Individual product detail |
| `/projects` | Experiments, tools, and engineering projects |
| `/case-studies` | Evidence-led project narratives |
| `/engineering` | Engineering principles, architecture, and practices |
| `/writing` | Articles, technical notes, and updates |
| `/ventures` | Business and creative initiatives |
| `/contact` | Contact and collaboration channels |

Routes are proposed, not implemented. Final sitemap and content priorities will be confirmed in Phase 1.

## 5. Recommended technology direction
- **Framework:** Next.js App Router
- **Language:** TypeScript with strict type checking
- **Styling:** Tailwind CSS
- **UI primitives:** accessible components, with shadcn/ui considered where useful
- **Content:** Markdown/MDX for editorial content and case studies
- **Hosting:** Vercel is the preferred candidate; final deployment decision is pending
- **Source control:** GitHub
- **Analytics:** optional, privacy-conscious analytics only after review

Use stable, compatible versions at implementation time. Do not treat this proposed stack as installed or deployed until verified.

## 6. Content and data model
Each public project entry should include:
- Name and concise summary
- Category
- Explicit status: Idea, In development, Prototype, Beta, Live, or Archived
- Public repository URL, if approved
- Demo URL, if verified
- Documentation URL
- Technology tags
- Featured flag
- Last verified date
- Evidence links and known limitations

A case study should include:
- Context and problem
- Scope and role
- Approach and key decisions
- Implementation details
- Evidence (commits, tests, screenshots, demo, release)
- Results, clearly distinguished from expectations
- Limitations and next steps

## 7. GitHub integration strategy
- Begin with manually curated project metadata in the portfolio repository.
- Add GitHub API integration only after the public/private visibility rules are defined.
- Cache or build content at deploy time where practical; avoid depending on live GitHub API calls for every page request.
- Never request or display private repository data on a public page.
- Use approved public repository links and verified release/commit information.
- Handle API rate limits, missing metadata, and unavailable repositories gracefully.

## 8. Security and privacy requirements
- Keep secrets server-side and outside source control.
- Validate all external data and escape untrusted content.
- Do not expose private project names, source, issues, or internal notes without approval.
- Minimize personal data and third-party tracking.
- Add security headers and dependency scanning as part of application hardening.
- Provide a clear process for reporting vulnerabilities.

## 9. Non-functional requirements
- Responsive from small mobile screens upward.
- Keyboard navigable and semantic.
- Target WCAG 2.2 AA practices.
- Optimize images, fonts, and client-side JavaScript.
- Good Core Web Vitals and meaningful metadata/SEO.
- Reliable error, loading, and empty states.
- Maintainable content model and automated checks.

## 10. Delivery phases
- **Phase 0 — Foundation:** repository governance, scope, blueprint, security and contribution policies.
- **Phase 1 — Identity and experience:** brand positioning, sitemap, content model, visual direction, design tokens.
- **Phase 2 — Application:** scaffold Next.js, implement shared layout and priority pages.
- **Phase 3 — GitHub integration:** curated data pipeline, safe metadata sync, caching.
- **Phase 4 — Proof:** case studies, screenshots, demos, tests, and verified project records.
- **Phase 5 — Launch:** deployment, domain, analytics review, monitoring, accessibility and performance checks.

## 11. Out of scope for the initial release
- User accounts or public user-generated content
- Payment processing or ecommerce
- Admin CMS unless a demonstrated content workflow requires it
- Live private-repository synchronization
- Claims of real-time operational status without monitoring evidence

## 12. Launch acceptance criteria
- All public project claims have supporting evidence.
- Every project has an accurate status and known limitations.
- No secrets or private data are exposed.
- Core pages work on mobile and desktop.
- Accessibility, lint, type-check, tests, and production build pass.
- Domain, deployment, contact path, and monitoring are verified.
