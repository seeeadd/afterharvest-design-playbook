# afterharvest-design-playbook

Claude's playbook for Sean's client work: **design, graphics, motion, video and editing**. One generic set of rules for
every client, plus a short file per client. It learns: every chat that gets feedback writes it back here.

## How a chat uses it

1. The client repo's `CLAUDE.md` says "read seeeadd/afterharvest-design-playbook first" (template in `templates/CLAUDE-client.md`).
2. The chat reads: this README → `SOP.md` → the job's files (for any page job: `pages/page-sop.md` first) →
   `clients/<client>.md` → the newest 40 lines of `feedback-log.md`.
3. After every round of feedback, the chat logs it in `feedback-log.md` and promotes repeated corrections into the rule
   files (`SOP.md` section D), then commits and pushes here.

## Files

| file | what it holds |
|---|---|
| `SOP.md` | how a job runs, how to talk to Sean, and the learning loop |
| `graphics.md` | the "does it look made by Claude?" test, real vs painted, the painted look, badges, UI pieces, seasonal |
| `motion.md` | banned motion, animation principles, page motion code patterns, characters |
| `video-editing.md` | talking head as anchor, framing, captions, transitions, sound, render pipeline, QA |
| `feedback-log.md` | every correction and approval, dated, with the rule it became |
| `study-art-references.md` | the 20 reference images, studied (texture, form, materials, process) |
| `study-motion-references.md` | the 12 motion references, studied |
| `clients/` | one file per client: facts, brand, world, assets, pages |
| `templates/` | a new client file and the client repo's `CLAUDE.md` |
| `pages/` | **registration (opt-in) and VIP pages**: start with `pages/page-sop.md` (how a page job runs + the judge checklist) |
| `pages/registration-page.md` | the registration page section by section: purpose, layout, alignment, gaps, copy pattern, assets, motion |
| `pages/vip-page.md` | the VIP upsell page, section by section |
| `pages/ui-kit.md` | header, forms, buttons (and "free" on every button), popup, phone bar, tickets, badges, time zones, line breaks |
| `pages/layout-type-spacing.md` | alignment, type scale, gaps, balance, laptops, big monitors, devices |
| `pages/copy.md` | page copy rules, with Ana's final copy as the worked example |
| `pages/motion-and-speed.md` | page motion and the speed work (still being extended) |
| `pages/fladlien-on-pages.md` | how Jason Fladlien's advice is used on pages, plus an ideas bank that grows with each job |
| `pages/evolution-ana.md` | how Ana's pages went from first version to final, and why |

## Rules at a glance

1. It must not look made by Claude: real, specific, in the client's world and in the client's own art style
   (graphics section 3). A weak brand is elevated in its own direction, never replaced.
2. Real where proof is needed, painted metaphor where a feeling is. Decide per graphic and say which.
3. Every graphic means one specific thing; no two sections share a layout.
4. Real animation (arcs, anticipation, settle). Never pop, pulse, generic slide or fade. Fast.
5. Balance: even, calm spacing; text always fits; nothing cramped or scattered.
6. Sans for reading and numbers, serif for big headlines; key lines bold with a soft highlight; no em dashes.
7. Keep the charm: improve on top, never strip a page to rebuild.
8. Fix root causes, not patches.
9. Show progress fast: screenshots, short updates, estimates for anything long.
10. Publish only when Sean says "publish".

## New client

1. Copy `templates/brand-template.md` to `clients/<client>.md` and fill it in from their brand kit and site.
2. Put `templates/CLAUDE-client.md` in the client repo as `CLAUDE.md` and fill in the repo, branch and site.
