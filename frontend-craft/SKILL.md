---
name: frontend-craft
description: Design, build, or refine web interfaces with deliberate visual choices, working interactions, and natural product copy. Use for frontend components, pages, applications, and UI reviews.
---

# Frontend Craft

Build for the product, its audience, and the task at hand. Respect explicit user choices and existing design systems. Treat visual suggestions here as defaults to adapt, not a style to impose. Keep focused changes focused.

## Find the direction

Identify who uses the interface, what they need to accomplish, and the primary action. Infer from the brief and existing product; ask only when missing context would materially change the result.

Reuse the project's framework, components, tokens, and conventions. For a new design, briefly settle the palette, typography, layout, and a characteristic detail before building. Small changes need no separate design ceremony.

Let the subject guide the expression. Operational tools favor scanning, comparison, and efficient repeated use. Editorial, brand, and game experiences can be more expressive. Make the actual experience available immediately; create a landing page when the task calls for one.

## Write for the person using it

**Keep construction instructions out of product copy.** Prompts, design briefs, implementation notes, and acceptance criteria guide the work; do not turn them into headings, labels, badges, or explanations to demonstrate compliance. Keep design rationale in developer communication, including for prototypes.

Give text a useful job: identify something, name an action, explain a real state, or support a decision. Remove decorative labels, repeated explanations, and narration of obvious controls. Implement qualities such as responsiveness or progressive disclosure through the interface itself.

Use the audience's vocabulary and natural language. Name buttons after their result, keep terms consistent, and avoid inflated claims or invented product facts. Technical terms are appropriate when the audience needs them.

Keep guidance that prevents mistakes or explains requirements, costs, permissions, consequences, or recovery. Empty and error states should explain the situation and a useful next step. Concision must preserve meaning and personality; do not remove help indiscriminately.

For copy-focused work or suspected instruction leakage, read the short [examples and research notes](references/copy-and-sources.md).

## Compose with intent

- Let content determine structure. Use open layouts for sections and cards for meaningful groups or repeated items. Avoid nested cards, repeated badges, and decorative numbering unless they communicate a real relationship or sequence. Start with modest radii, around 8px or less, unless the design system or subject suggests otherwise.
- Establish a readable type hierarchy. Reserve large display text for genuine focal points; fit headings to their containers. Prefer stable sizes with breakpoint adjustments and neutral tracking over viewport-driven scaling or squeezed text. Wrap long content without collisions or unreadably shrinking it.
- Choose a coherent palette with useful contrast and hierarchy. Challenge habitual gradients, monochromatic themes, and ornamental glow orbs when they add no meaning. A color or style is not wrong merely because AI often uses it.
- Match controls to the task: toggles for binary settings, tabs for views, swatches for colors. Use familiar icons for tools, with accessible names and tooltips where useful; retain text when it improves understanding. Prefer the existing icon library, or Lucide when choosing one.
- Use imagery that reveals the actual product, place, person, or object when that matters. For a new marketing hero, consider unframed media with clear subject identity and a glimpse of what follows. Do not force imagery or a hero into a utility screen, or substitute decorative SVGs for useful visuals.
- Give motion a purpose: feedback, orientation, or a considered focal moment. Respect reduced motion. A distinctive detail can carry the design without decorating every component.

## Build and finish

Make the requested workflow usable, including relevant loading, empty, error, and success states. Reuse established libraries for game rules, parsing, or other domain logic. Prefer Three.js for custom web 3D when appropriate to the stack.

Before delivery, review the changed interface in context:

- **Copy:** inspect labels, hints, placeholders, tooltips, dialogs, and state messages. Identify the exact offending words, then delete or replace them. Do not hide unwanted explanations in tooltips or accessibility text. Keep the audit brief unless a report is requested.
- **Behavior and layout:** check the main action, keyboard access, focus, narrow and wide layouts, long content, and asset loading. Keep fixed-format controls stable as their state changes. Use browser interaction and screenshots where available; for canvas or 3D, also verify nonblank output, framing, and movement. Match verification to the change and honor explicit testing constraints.

Fix what the checks reveal and state any verification limits. If the result needs a dev server, start it and provide the URL; choose another port if occupied. For standalone HTML that works directly, provide a file link. Keep the handoff concise.
