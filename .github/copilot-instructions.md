# GitHub Copilot instructions — study-notes

## Quick context
- This is a **single-page static notes site**. Key files: `index.html` (content), `index.css` (styles, currently holds backlog in comments), and `README.md` (project roadmap and notes).
- There is **no build system**, no package.json, and no automated tests; changes are validated by opening `index.html` in a browser or using a VS Code Live Server preview.

## Goals for an AI agent
- Make small, focused edits (add a note, improve markup, or style) and keep PRs minimal and self-contained.
- Prefer conservative, visible changes — avoid introducing frameworks, tooling, or external services unless the user explicitly requests it.

## Editing patterns & examples
- Add content: edit `index.html` directly using semantic HTML. Example: to add an "Edge functions" note, add:

```html
<section id="edge-functions">
  <h2>Edge functions</h2>
  <p>Notes about edge functions go here.</p>
</section>
```

- Add styles: append rules to `index.css` (remove backlog comments only when converting them into actual styles). Example:

```css
#edge-functions { max-width: 800px; margin: 1rem auto; }
#edge-functions h2 { font-size: 1.25rem; }
```

- Update project state: when work is completed, update the checklist in `README.md` using the markdown task list format (e.g. change `- [ ] Start Next.js project` to `- [x] Start Next.js project`).

## Conventions and constraints specific to this repo
- Keep HTML/CSS simple and dependency-free. Do not add build tooling (webpack, bundlers, etc.) unless instructed.
- Preserve the `README.md` roadmap as the source of truth for tasks and progress; reflect completed work there after making substantive changes.
- The CSS currently contains backlog comments — treat them as TODOs, not active code. Remove or convert them only when implementing the corresponding feature.
- Documentation changes should be explicit and minimal: update or add a short line in `README.md` describing the change.

## Integration points & checks
- The `README.md` lists services and learning notes (Firebase, MongoDB, Next.js, etc.) — these are notes only. Before adding integrations, verify that configuration or credentials files exist (they do not in this repo presently).
- If you add external dependencies, include a short justification in the PR and instructions to reproduce (how to run/preview locally).

## Testing & validation
- Validation is manual: open `index.html` in a browser or use VS Code Live Server. If adding JS behaviors, include a brief manual test plan in the PR description.
- Do not add automated tests unless the user asks; there is no test harness present.

## Commit / PR guidance
- Commit messages: short imperative form (e.g., `Add edge functions note`, `Style edge functions section`).
- PRs should be small and include: description of change, files modified, and how to preview (open `index.html` or use Live Server).
- Tag the user for review and ask for clarification for any non-trivial UI or content changes.

## When to ask questions
- When a change would introduce tooling, new frameworks, or external services.
- When a large content restructure is proposed (e.g., converting to a multi-page site or adding a build system).
- When there are ambiguous roadmap items in `README.md` that affect implementation.

---

If anything is unclear or you'd like more/less strict rules (for example, a preference about formatting or commit style), tell me and I will update this file.