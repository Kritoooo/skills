# Copy calibration and sources

Use these examples to distinguish instructions for the builder from information needed by the person using the product. Judge text in context; these are examples, not banned phrases.

| Builder's requirement | Unhelpful text on screen | Better treatment |
| --- | --- | --- |
| Keep the interface compact and responsive | “高信息密度 · 响应式布局” | Express this through layout; omit the badge. |
| Reveal advanced options progressively | “采用渐进式披露，降低认知负担” | An “高级设置” disclosure that opens the actual options. |
| Support filtering and sorting | “支持多维筛选与排序的数据表格” | Useful filters and sortable column headers. |
| Store data in the browser | “采用 localStorage 本地存储架构” | “保存在此浏览器中”, if location affects the user's expectations. |
| Allow retry after a save failure | “完善的错误恢复机制” | “保存失败，请重试” and a working retry action. |

The reusable methods from the research are:

- Separate design and implementation instructions from product content. Give text a specific role in the user's task.
- Ask for exact original text and a deletion or replacement, rather than a vague judgment about “AI tone”. Inspect the surrounding interaction and each supported language involved in the change.
- Remove repetition and self-describing template labels. Preserve necessary instructions, meaningful accessible names, and consequences; evaluate clarity, not just word count.

These examples assume a task-oriented interface. A design tutorial can legitimately discuss layout; a developer tool can legitimately expose implementation concepts. Explicitly requested marketing, onboarding, and documentation need their own useful content.

## Sources and synthesis

Checked on 2026-11-05. This is an independently written synthesis of the following sources and the user's supplied guidance.

- **[Anthropic frontend-design](https://github.com/anthropics/skills/blob/41bbe19d1a1a7eaab5e7bb9050a417e5c6cffc8f/skills/frontend-design/SKILL.md):** the current `main` file was checked live; its latest file-changing commit was `41bbe19d1a1a7eaab5e7bb9050a417e5c6cffc8f`, dated 2026-09-03. Informed subject-specific direction, typography, restraint, and writing from the user's perspective.
- **[Frontend guidance](https://developers.openai.com/api/docs/guides/frontend-prompt):** supplied in full by the user. Informed task-appropriate controls, usable first screens, layout stability, assets, and local preview delivery. Universal aesthetic bans became contextual defaults; necessary user guidance remains allowed.
- **[Impeccable: clarify](https://impeccable.style/docs/clarify/):** informed reviewing words by their role in an interaction, accurate recovery messages, and preserving meaning while shortening copy.
- **[Developer discussion: auditing 92 screens](https://www.reddit.com/r/SideProject/comments/1x4p7k6/we_had_claude_audit_all_92_screens_of_our_app_for/):** informed requesting exact text and replacements. This is an author-reported practice, not evidence of guaranteed results.
- **[OJO: UI anti-patterns](https://github.com/touchine-ojo/OJO-Design-Skills/blob/main/skills/app-ui-ux-best-practices/references/anti-patterns.md):** identified self-referential template labels as a concrete failure mode. Its broad stylistic ban lists were not adopted.

The skill deliberately avoids mandatory approval rounds, exhaustive copy reports, fixed palettes, and a universal visual formula. Verification stays proportional to the requested change.
