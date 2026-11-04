> Generic rules for every client's pages. Each rule is written to carry to any client in their own brand and world;
> Ana Calin's "The Exit Plan" pages (registration `index.html`, VIP `vip/index.html`, confirmation `confirmed/`,
> offer `program/` in seeeadd/2026-ana-calin) are the worked example, with exact values and selectors. Her facts live
> in `../clients/ana-calin.md`.

# Page motion and speed

**Purpose:** every page moves like a premium, hand-made piece in the client's own brand (real animation, never pops,
pulses or slides), and still loads fast on every device. Motion and speed are one job: keep every graphic and every
animation, and find the cheaper way to run it.

Read with: `../motion.md` (the house motion rules: banned list, animation principles, GSAP code pattern, characters),
`../graphics.md` (what the pictures look like, §7 seasonal), [registration-page.md](registration-page.md) (§5.9 motion
in the hero), [vip-page.md](vip-page.md) (§17 motion), [ui-kit.md](ui-kit.md) (forms, badges, signature),
[layout-type-spacing.md](layout-type-spacing.md) (§9 never cover text, §12 big monitors), [copy.md](copy.md),
[page-sop.md](page-sop.md) (how a round runs), [evolution-ana.md](evolution-ana.md) (how Ana's pages got here),
[fladlien-on-pages.md](fladlien-on-pages.md) (one focal object per section). This file does not repeat those; it adds
the page-specific detail.

Status words: **final** (Sean approved, or it shipped and stood), **still to do** (known gap), **open** (waiting on
Sean or the client). The latest final decision wins.

---

## 1. The motion standard in one list

- **Banned on pages:** pops, pulses for attention, generic slide-ins and fade-ins, flaps, stop-motion jitter, busy
  motion, slow motion (full list: `../motion.md` §1).
  - Sean: "I don't want pops, pulses, and slides. I don't want any of that. I want it to be smooth".
  - Sean: "Where are the animations? I think these are just slides and flaps. Where are the real animations?"
  - Sean: "some animations are still very generic. And they're just popping and sliding so I want really premium
    animations."
- **Required:** real animation principles (anticipation, easing, arcs, follow-through and settle, overlapping action,
  layers at their own depth). See `../motion.md` §2.
- **Things are placed, not dropped.** A shadow arrives first and tightens as the object settles; ink and underlines
  are drawn at pen speed; any camera move (zoom into an app, push-in) uses long, slow eases.
- **Specific to the concept and the client.** Motion acts out the line it sits beside, in the client's own brand and
  animation style. Generic motion on a custom picture still reads as "made by Claude" (`../graphics.md` §1).
  - Sean: "the graphics you're making right now are too generic, and you didn't put as much effort in as you did in
    the VIP graphics. they are also not specific and not animated premiumly".
- **Animate only what is better animated.** A still that already says it stays still.
- **Fast.** People scroll past slow motion. Speed targets are in section 4.

## 2. Plan the motion with the picture (one moment per section)

- **Plan the animation before drawing.** Write each picture's small story (a state, a turn, a payoff) before painting
  it, so the parts that move are built as separate layers. Never make a static picture and slide it in.
  - Sean: "Probably instead of creating the graphic as it is, I should already plan an animation for it instead of
    just creating static visuals."
  - Ana: the plan was written in `tools/paint/PLAN-v5.md` (VIP) and `tools/paint/PLAN-registration.md`
    (registration) before painting.
- **Animation happens inside the picture.** Props and parts act out the line; the whole picture never pops or slides
  in as a block.
  - Ana VIP: the red pencil arcs in, strikes the weak line, writes "Say the price in the first line.", ticks the good
    line. The WhatsApp line lifts off as paper and flies into the phone as a sent message. "Meeting ran late" slaps
    onto Wednesday, the play button is pressed, ripples, and turns to pause.
- **One moment per section.** One focal picture per section plays one story (Jason Fladlien: one focal object per
  section, [fladlien-on-pages.md](fladlien-on-pages.md)). Never two stories competing in one view.
- **One metaphor object across the funnel.** The same object can carry the motion on every page so the story stays
  consistent.
  - Ana: a door or window that opens on her video. Registration: blue painted shutters swing open. VIP: the pink EXIT
    door swings open (`.door-closed`, `dswing 1.6s`, starting at .55 s).
- **State a benefit literally with a small text animation** when a picture only hints at it.
  - Sean: "I want the graphic to visually convey that a little bit more literally. Maybe you can add it somewhere in
    the text as an animation or something instead of on the graphics."
  - Ana VIP Nº 04: "Your recordings · access expires:" then "never" is written in by hand (a clip reveal over .9 s,
    starting at .5 s) and underlined (.45 s), when `.exp` is 85% down the screen. On phones the line was tightened so
    "never" does not wrap under its pill.
- **Show progress as the reward revealing itself** (game-like, but secondary to the task). Motion plays only right
  after progress goes up, never while people read.
  - Ana confirmation page: a brick wall over the locked calculator (`#cxtb`), 42 bricks in 7 seeded sets of 6, rows in
    `#F9B4D3`, `#FFE680`, `#FFF3C9`. Each answer sends one small ball that knocks out one set in about a second
    (`wallShow(n, lastPow > -1 && n > lastPow)`). Going back restores bricks; returning later shows the wall as they
    left it; at 7 of 7 it unlocks.
  - Sean: "the more they answer, the more the calculator reveals itself. Kind of like that break game ... Same vibes,
    maybe, but not too distracting from the survey."

## 3. How a section plays

- **Plays once, when it is seen.** Each section's timeline starts when the section scrolls into view, and plays once
  (reload to replay). Then only tiny idle loops continue: steam, voice-note bars, a slowly turning sun, falling petals,
  a nodding flower. Nothing pulses or nags.
  - Ana: `when(el, tl, start)` in `assets/reg-motion.js` (default start `'top 65%'`) and `assets/vip-motion.js`
    (default `'top 70%'`), a ScrollTrigger with `once: true`.
  - Exception where it helps: an object animation can replay when scrolled back past (Ana's VIP chair:
    `onLeaveBack: tch.pause(0)`, so it plays again on the way down).
- **Wait for the container.** A section's story starts only after its own block has finished fading in. Nothing moves
  while its card is still appearing.
- **The animation library owns what it animates.** Never put a CSS transition on an element GSAP moves; they fight
  and the motion stalls or lags.
  - Ana VIP chair, three rounds: "I want this seat, this chair, to move faster because there's too much delay right
    now." (a CSS transition was fighting GSAP; the letter had the same bug), then "The chair is still not moving" (it
    moved while the card was fading in, and a leftover style stopped it 60px short), then "where is the animation for
    the chair" (it slid in before people reached it).
  - Final chair (`.seat.two .you`): starts at the card's edge, half out of frame (`xPercent: -24`, `rotation: -7`),
    waits until the card is well in view (`start: 'top 62%'`), slides in (.75 s, `power2.in`), bumps a little closer
    (`xPercent: 5`, .3 s), settles with `elastic.out(1,.45)` (.7 s).
- **An object animation must be clearly visible:** a real travel distance, started when its card is in full view.
- **Content is visible without the script.** Hide things for their entrance only after the script has started.
  - Ana: `[data-r]` blocks are visible by default; the hiding (`opacity:0; translateY(22px)`, revealed over .8 s) only
    applies once the script adds `html.anim-on`.
- **Count-ups start at 0 only when they start.** Never show "$0" or "0" before the count plays; the real number is
  in the HTML.
  - Ana: `count()` in `reg-motion.js` writes 0 in `onStart` and the final value in `onComplete`. The hero stats
    (`.hero .stat b`: "$1.4M", "About 80,000") count once over 1.6 s, starting at .5 s, each .15 s after the last.
- **The end state matches the resting CSS exactly** (same angle, same position), or the element jumps when the
  animation ends.
  - Ana: the flipped Day slide ended its arrival at `rotate(-4deg)` while its CSS rested at `4deg`, and jumped. Fixed
    by using the same angle.
- **Check the first frame, not just the last.** Nothing may look cut or broken before it plays.
  - Sean: "the first frame of the Yes button is just a small, tiny error. The Yes doesn't fit the thing, like it's
    cut or something, but when I check Yes, it looks good." (the "See you Tuesday" Google Calendar invite, `.gi`).
- **Motion stays inside its box at every point.** A section that clips overflow cuts off a bounce or swing that hangs
  past its edge. Check the lowest and widest point of every motion at desktop, tablet and phone.
  - Sean: "the arrow animation is like cutting, so maybe you have to fix that" (the confirmation page arrow).
  - Painted assets and their shadows get room inside their own canvas too ([ui-kit.md](ui-kit.md), `../graphics.md`
    §3b).
- **An endless loop never sits inside a timeline you wait on.** Start a dependent loop at a fixed time instead of on
  the parent's `complete`.
  - Ana: the money in the Google Calendar week (`.gw`, a registration section the Nov 3 copy later removed; the
    lesson stands) did not appear at first because the sun's endless yoyo kept the
    timeline from completing. Fixed with `tl.add(function () { flow.play() }, 3.4)`. The money loop also pauses when
    the calendar is off screen.
- **Floating elements never sit over text people are reading.** On desktop they float over pictures at the side, small.
  - Sean: "can you put this floating thing for days 1 to 3 under the top-right side instead, so it won't block the text
    while we're reading it? I think it's a little distracting. And annoying".
  - Ana: `.dmap` (the sticky Day 1-3 tracker) from 1061px: `justify-content:flex-end; top:96px`,
    `.dm-in{transform:scale(.82)}` (about 20% smaller), over the slide pictures on the right, just under the header.
- **Decorative motion behind content never draws over letters or takes clicks** (`pointer-events:none`, behind the
  content in stacking order). Badges sit below sticky bars.

## 4. Speed of motion (fast starts)

| what | target | Ana's value |
|---|---|---|
| Above-the-fold load animation | main move in about half a second, all done well under 2 s | hero shutters: main swing about .5 s inside a 1.05 s settle |
| A section's story | about 1 to 2.5 s after it is seen; longer stories trimmed | "Bring the part you're stuck on": 8.6 s cut to about 4.5 s |
| A signature or handwritten word | about 1 s | signature: 1,150 ms of writing |
| A highlighter sweep | about 1 s, a beat after the line is seen | 1.2 s, 300 ms after the line is 15% into view (200 ms on VIP) |
| A reveal after a task step | about 1 s, only right after the step | brick wall: one set per answer in about a second |
| An opening sequence on an offer page | about 2 s in total | `/program` hero (below) |

- **Above the fold, speed beats everything.** Sean: "I want the animation faster and smoother than this because they
  might just skip and scroll past it if it loads this slow, so we must really optimize the animation." The shutters
  went from a slow rattle-and-swing to open by about half a second (about three times faster).
- **Section stories are quick too.** Sean: "And make the animation faster on the part you're stuck on." It went from
  about 8.6 s to about 4.5 s (sheet flies in, pencil marks it, the note) and was published.
- **Make the first section exciting, in one short sequence.** The headline rises in, a highlighter sweeps under the
  key phrase, the brand mark grows in the margin, proof numbers count up. On phones the mark peeks over a corner
  instead of taking room.
  - Sean: "Can you make this first section more exciting?"
  - Ana `/program`: highlighter under "your first paid customers"; 771 likes, 82 likes and $120 count up
    (`data-count="771"`, `data-count="120" data-pre="$"`); the sunflower stem grows, a leaf unfolds, the head spins
    open, then it sways, blinks and follows the cursor.

## 5. The signature ink (hand-made marks that write themselves)

The pen is the house signature motion: a line that appears at the speed a hand draws it, never a fade.

- **Drawn ink:** reveal the stroke along its length with a pen or nib on the tip. Speed follows stroke length; tiny
  pauses at pen lifts; ease in and out per stroke.
  - Ana: `draw(path, dur, pen, ease)` and `Pen()` in both motion files.
- **The signature** writes itself once when scrolled into view, in about 1 s, with a soft nib leading, longer strokes
  taking longer, tiny pauses at pen lifts, feathered ink edges and wet-to-dry colour. It writes once and stays.
  Reduced motion shows it finished. Check that it actually finishes.
  - Sean: "make the signature animation faster" (it was about 2 s; the first version was still mid-name at 3 s).
  - Ana (`.hwg-cap svg.sig`, an inline script near the end of `index.html`): `T = 1150` ms shared across strokes by length,
    each stroke at least 45 ms, 8 ms lifts after short strokes and 28 ms after long ones. The ink goes on wet
    (`.wet`, `#A80F55`) and dries to the page pink over a 1.8 s colour transition. Font and placement: [ui-kit.md](ui-kit.md).
- **The highlighter sweep** is the one way to mark a key line, and it is drawn, not faded.
  - Ana: `mark.sk`, a yellow band from 52% to 94% of the line (`rgba(255,212,0,.6)`), `background-size` 0 to 100%
    over 1.2 s, `cubic-bezier(.22,.8,.24,1)`.
- **Pencil arrows** draw themselves to lead the eye, then idle very gently. A tap scrolls to the target.
  - Sean: "I want an arrow animation on there to make them scroll to the VIP page so it becomes the focus."
  - Ana VIP `.go-vip`: starts at 1.4 s, the line draws in 1.1 s, the head in .3 s, then a slow 7px bob; a tap scrolls
    to `#vsl`. Arrow look: hand doodle, never a default callout (`../graphics.md` §1).
- **Handwritten words** in a line are written in (clip reveal plus a drawn underline), as in "never" (section 2).

## 6. Hero openings (doors, windows, shutters)

- **The hero video sits inside an object from the client's world that opens on load** (door, window, curtain, shop
  shutter), in 3D, with anticipation, overshoot and settle. Adapting it: [registration-page.md](registration-page.md)
  §5.10.
- **It runs on CSS alone from the first paint,** so it never waits for the scripts, and its images are preloaded.
  - Ana (`.iph.win .wn-sh.l` / `.r`): `wnL 1.05s .12s` and `wnR 1.05s .17s` (the right shutter a beat later). Keyframes:
    a small anticipation to 5deg at 9%, the main swing to 81deg by 66% (overshoot), back to 69deg at 84%, rest at
    72deg. The shutter shade fades to .55 as it turns away from the light (`wnShade`), cast shadows on the wall fade in
    over .9 s from .35 s (`wnCast`), four petals drift down from .6 to 1.25 s. When the video plays, the shutters open
    further to 84deg over .5 s.
  - Preloads: `img/o/vip/paint/winh.avif` and both shutter images with `fetchpriority="high"`.
- **Depth is part of the motion.** Shutters have a painted edge, darken as they turn, cast soft shadows; the video sits
  back in the wall (lintel, jambs and sill drawn as a recess). Sean: "I want it to be a little more 3D-looking because
  now it looks flat".

## 7. Attention cues on forms (small, and they stop)

- **The sign-up ticket swings a little now and then, like a ticket hanging from the top, then rests.** It stops for
  good once the visitor clicks into it or types. Off for reduced motion.
  - Sean: "Can you make this one sway sometimes or pulse, maybe?"
  - Ana: `.tkshell{transform-origin:50% 0; animation:tksway 7s ease-in-out 2.5s infinite}`; the swing (-1.3deg, 1.1deg,
    -.6deg, .25deg) happens in the first 16% of each 7 s cycle, then it rests. Stopped by
    `.tkshell:focus-within, .tkshell:has(input:not(:placeholder-shown)){animation:none}`.
- **A soft hint on the next field to fill, then the button.** Never a strong glow that keeps distracting.
  - Sean: "I think it's too strong right now. I keep getting distracted by the light."
  - Ana: first name `fhint 7s` from 2.5 s (a pink border at .75 and a 5px ring at .12 for a moment); the email gets one
    `fhint 2.8s` once the first name is in; the button gets `bglow 2.4s` twice once both are filled. Details:
    [ui-kit.md](ui-kit.md) §8.
- **Badges stamp in once with a small spin** as they scroll into view; with reduced motion they simply show.
  - Ana: `.bdg.in{animation:bdgIn .6s cubic-bezier(.2,1.5,.4,1) both}`, from 1.9x scale and 24deg more turn to the
    badge's resting tilt (`--r`, default -8deg).
- **Small "live" status dots** keep a soft ring that grows and fades (transform and opacity only). They are status
  signals, not attention pulses on content. Ana: `.fb-l i:after`, `.hpill .dot:after` (`dotp 2s`).

## 8. App demos that play (Gmail, WhatsApp, Calendar, Zoom)

What the apps look like is in `../graphics.md` §2 and [vip-page.md](vip-page.md) §8. The motion rules:
- **Zoom in on the exact button, click it with a cursor, show the app's own confirmation, zoom back out.** The text
  beside it names the exact button.
  - Ana confirmation (`assets/gmail-demo.css`, 11 s loops): Spam scene zooms to "Report not spam", toast
    "Conversation marked as not spam. Undo", then the inbox. Promotions scene: the email is dragged to Primary, Gmail
    asks "Do this for future messages from ...?", Yes is tapped. The two scenes take turns; the buttons above
    ("Found it in: Spam / Promotions") keep one playing when tapped.
- **Chats play message by message with real app behaviour:** typing indicator, ticks that change when read, time inside
  each bubble. Ana VIP: header switches to "Ana is typing…", ticks turn pink when read.
- **A calendar fills like a real one:** sessions drop into their slots, then the reminder.
  - Ana registration `.gw` (the "life left to enjoy it" calendar, removed with the Nov 3 copy): the card arrives (y 60px, 6deg, .9 s, `power3.out`), the three sessions grow in on Tue to
    Thu, evenings and the weekend light up yellow, the sun turns, then money drifts off the work blocks.
  - Ana "See you Tuesday" `.gi`: the invite drops onto her photo (.8 s, `back.out(1.5)`), a cursor arcs in (.9 s),
    clicks "Yes", Tuesday lights up.
- **A Q&A or chat ends on the visitor's own action** (their question typed, sent, answered live). Ana VIP Zoom Q&A:
  "Can I start selling before my offer is finished?".
- **A device graphic acts like the device.** Ana's Exit Number calculator: keys press in turn before the result shows,
  a receipt tape prints from the top.

## 9. Seasonal motion (Christmas on Ana's page)

Look and placement: `../graphics.md` §7. Motion and switching:
- **One small date-checked script adds every seasonal piece** and switches itself off after the season; `?xmas=0` and
  `?xmas=1` preview either state.
  - Ana: `on = now < new Date('2027-01-01T00:00:00')`, adds `html.xmas`. Nothing seasonal lives anywhere else.
- **Snow only where it adds, never across the page.** It falls behind the content of at most the sections that had
  flakes, never over text, video or forms, never blocks clicks.
  - Sean: "I don't need the snow to fall across the whole page because that might be too distracting. Maybe just the
    parts that you put them in before." (Nov 2: hero and the final "See you" section.)
  - Latest (Nov 4): Ana said the page "looks very christmasy" and Sean asked for "less christmas stuff", so the snow
    now falls in the last section only: `snowIn(document.getElementById('final'))`, behind a `LESS = true` switch.
    What teaches: a seasonal layer is dialled down by removing places, not by weakening each piece.
- **Ana's final seasonal set (Nov 4).** The first cut removed too much; Sean brought two pieces back: "keep the xmas
  sunflower on the buttons lol" and "and the lights on form".
  - Kept: the Santa hat on every button's sunflower, the fairy lights on the frozen side form, the wreath over the
    video window, the footer village lights (trees, stars, wreaths on doors), holly on the Day 1 date tile, snow in the
    last section.
  - Removed: the Santa hat on Ana in the header (`.fb-hat`, now behind `!LESS`) and the hero snow.
  - Rule for any client: when a seasonal layer is too much, cut the pieces on the host and the big moving ones first,
    and keep the small touches on brand pieces (buttons, the form). Show Sean the keep list before cutting.
- **Check the season fits the client and audience.** Ana is Greek; Greek people do celebrate Christmas, so the layer
  stayed. For another client, confirm the holiday is theirs before adding it.
- **How the snow moves:** depth (specks small, slow and faint at the back; crisper crystals in front, about 16 to 42px),
  gentle sway, a slow turn, a shifting breeze. It animates only while its section is on screen, the time step is capped
  (`Math.min(.05, ...)`) so it never jumps after a tab switch, and it is off with reduced motion.
  - Ana: `canvas.snow` inserted as the section's first child, `position:absolute; pointer-events:none; z-index:0`;
    flakes per section `Math.min(40, Math.max(12, W * H / 32000))`.
- **Snowflakes look real** (Bentley crystals; look rules in `../graphics.md` §7). Sean: "i want this snowflake to be
  more glassmorphism and light looking".
- **Lights twinkle slowly in the client's colours** on a fine ink cord. Ana: bulbs `#F72585`, `#FFD400`, `#3C6FB0`,
  `#E0243A`, `#3BAA6B`, 2.4 s twinkle with staggered delays; on the frozen side form `#rcard` (Sean, Nov 4: the lights
  stay on the frozen form) and along the footer village rooflines. Never on the hero form.
- **The seasonal touch on every button stays still:** Ana's sunflower in a Santa hat (`#sfx`) on every button.

## 10. Reduced motion

- **Every scene shows its finished frame.** Nothing is hidden waiting for motion that will not come.
  - Ana: GSAP timelines `tl.progress(1)`; CSS `@media (prefers-reduced-motion:reduce)` turns off all transitions and
    animations and sets `[data-r]` visible; the signature script returns before hiding its strokes; snow is never
    created; badges show without the stamp; the Day windows show their first slide finished (`?still=1`).
- **Idle loops and attention cues are off** (ticket sway, field hints, petals, twinkles).

## 11. Speed: fast pages with nothing removed (still in progress)

**Status: still in progress.** Desktop and laptop are done and live on Ana's registration page (Nov 4). Sean: "We're
still not done with the optimizations, so we're going to update that still." Tablets, phones, Android and iPhone, and
the other pages are next (section 13).

### 11.1 The rule

- **Load as fast as possible, keep every graphic and animation at the same quality.** Find a cheaper way to do the
  same thing; never remove or downgrade a piece to gain speed.
  - Sean: "I want them to load as fast as possible, really fast, without removing anything from them. Same quality,
    same high quality. Maybe there's a different way to make it faster."
- **Measure before and after** on the same connection: hero image on screen (largest paint), full load, time the
  browser is too busy to respond (blocking time), page jumping while it loads (layout shift), total image weight.
  Average over three runs. Measure again on the live site after publishing.
- **Prove nothing changed visually:** a pixel diff of before and after screenshots. Ana: only tiny edge-smoothing
  pixels differed.
- **Order of work:** the biggest effect on sign-ups first (the form on the first screen), then images, fonts, caching,
  animation cost.

### 11.2 Images

- **Resize every image to the sharpest size it is ever shown at,** on any screen (including 2x screens). Ana: about
  4.8 MB of images loaded and many were 3 to 13 times bigger than shown.
- **Painted art as AVIF with a WebP fallback;** photos and UI as WebP. Ana: `<picture><source type="image/avif"
  srcset="img/o/vip/paint/winh.avif"><img src="img/vip/paint/winh.webp" ...></picture>`.
- **Web copies live in their own folder; originals stay full size** for other uses (the page video, print). Never use
  the web copies in a video. Ana: web copies in `img/o/`.
- **Lazy-load small decorative images below the fold** (`loading="lazy"`). Ana: the review stars
  (`img/o/vip/paint/star-a.webp` and siblings) load only when scrolled near.
- **Preload what the first screen needs,** with `fetchpriority="high"` on the hero art (section 6), and every `<img>`
  carries `width` and `height` so nothing jumps.
- **Page video:** `preload="none"` until played (Ana's window video). Keep it light: a few MB at full HD, static grain
  (per-frame grain wrecks compression), and a 720p copy for phones. Ana's film motion test: 89 MB with per-frame grain,
  6.2 MB with static grain and motion blur at 1920x1080; the full draft was 29 MB at 1080p, then a 720p copy.
- **Slides and stills as WebP around 30 to 60 KB each** (Ana's Day slides: 34 to 61 KB).
- **Flag heavy single images and offer to shrink them.** Ana: her painting as an SVG sticker is about 210 KB
  (**still to do**).
- Result on Ana's registration page: images 2.7 MB to 1.8 MB.

### 11.3 Fonts

- **Self-host the fonts.** No trip to Google before text shows. Latin subset only, `font-display:swap`, one file per
  face (a variable font carries its weights in one file), preload the two faces the first screen uses.
  - Ana: `assets/fonts/g/`, preloads `manrope-normal-b222d8.woff2` and `instrument-serif-normal-c008db.woff2`; Manrope
    as one file for weights 400 to 800.
- **Drop font families nothing uses,** except where a mock needs the real app's font. Ana: Roboto kept only for the
  Google Ads mock.
- **Special display fonts must be free to use** (check the licence, for example SIL Open Font License) and self-hosted
  with their licence file. Ana: `assets/fonts/DSEG7Classic-Bold.woff2` plus `DSEG-LICENSE.txt` for the calculator's LCD.

### 11.4 Caching and what is public

- **Browsers keep images, scripts and fonts between visits.** Long cache only for files that get a new name when they
  change (hashed font names, versioned libraries); give a changed image a new name or a `?v=` so visitors do not keep
  the old one.
  - Ana `vercel.json`: `/img/` and `/assets/` 1 hour plus a day of stale-while-revalidate; `/img/o/` 30 days;
    `/assets/fonts/` and `/assets/vendor/` one year, immutable.
- **Keep work folders off the public site.** Ana `.vercelignore`: `tools/film/`, `tools/paint/`, `playbook/`,
  `CLAUDE.md`. Draft page videos stay out of Git until publish.
- **Host the animation library on the client's site.** GSAP 3.13 (free for commercial use) in `assets/vendor/`, not
  from another server.

### 11.5 Cheap animations

- **Animate only transform and opacity** (move, rotate, scale, fade), which the graphics card runs. Anything that
  repaints every frame (box-shadow pulses, glows, `left` or `width` changes, shine sweeps on `left`) is rebuilt to look
  the same on transform and opacity. Idle page CPU should be near zero.
  - Ana, before: the page kept the processor about 30 to 40% busy while sitting still. Rebuilt with the same look: the
    pink pulsing dot and the "Starting soon" dot glow (a pseudo-element that scales and fades instead of a growing
    box-shadow), the play-button ring (`ringp`, scale and opacity), the Christmas light twinkle (a glow layer that
    fades instead of an animated box-shadow), the button shine (`shine` moves with `translateX(475%) skewX(-20deg)`
    instead of `left`).
- **Never redraw a detailed drawing every frame.** Pre-render it once, then move the bitmap.
  - Ana's snow: each crystal is an SVG with drop-shadow filters; drawing it every frame cost about 60 ms a frame. Now
    each of the 7 crystals is drawn once to a small canvas and the flakes move those. Script time on load went from
    about 2.6 s to about 0.5 s in a test with the CPU slowed 4x, and it looks the same.
- **Pause what is off screen or in a hidden tab** (IntersectionObserver, `visibilitychange`, ScrollTrigger toggles).
- **Load-critical motion in CSS,** so it starts from the first paint (the shutters, section 6).

### 11.6 Measured on Ana's registration page (Nov 4)

Local test, old against new, same connection:

| | before | after |
|---|---|---|
| Hero painting on screen | 1.58 s | 0.86 s |
| Page fully loaded | 2.35 s | 1.70 s |
| Time the browser is too busy to respond | 151 ms | 17 ms |
| Page jumping while it loads | 0.10 | 0.02 |
| Images over the whole page | 2.7 MB | 1.8 MB |

Live site, against that morning, same connection, three runs averaged:

| | this morning | now |
|---|---|---|
| Hero painting on screen | 2.0 s | about 1.1 s |
| Page fully loaded | 3.2 s | about 1.9 s |
| Page jumping while it loads | 0.06 | 0 |
| Time the browser is too busy to respond | 0.7 s | about 0.3 s |
| Total downloaded | 5.3 MB | 4.6 MB |

## 12. Checks before saying done

- Watch every animation from its first frame to its last at 1440, 1024, 390 and 320 wide: nothing cut, nothing
  clipped by its section, no jump at the end, nothing over text.
- Scroll at normal speed: each story starts when its card is fully in view and finishes before people move on.
- Turn on reduced motion: every scene finished, nothing hidden.
- Performance panel with the page idle: no repaint every frame, CPU near zero.
- Before and after numbers (section 11.1) and a pixel diff for any speed change; measure the live site after publish.
- Seasonal: `?xmas=1` and `?xmas=0` both look right.

## 13. Still to do and open

- **Still to do:** speed on tablets and phones, checked on real Android and iPhone (Sean's order: desktop and laptop,
  then mobile and tablets, then all devices). Re-measure idle CPU after the animation rebuild.
- **Still to do:** the same speed pass on Ana's VIP, confirmation and offer pages. They still load fonts from Google
  (`fonts.googleapis.com` in `vip/index.html`, `confirmed/index.html`, `program/index.html`) and have no AVIF copies.
- **Still to do:** the holly the Christmas script adds to the Day 1 date tile (`xmas-holly.webp`) is created with
  `new Image()` and loads at once; set it to load lazily.
- **Still to do:** shrink the 210 KB SVG sticker of Ana's painting.
- **Still to do:** big monitors are scaled with CSS zoom from 1800px; tested in Chrome only, Safari not yet checked
  ([layout-type-spacing.md](layout-type-spacing.md) §12).
- **Open:** when a client cannot record videos, replace the registration and confirmation videos with a strong
  graphic, ideally animated, that does the video's job (explains what is happening on the page and what each part is
  for). Sean: "I was thinking for us to explore and think of ways to make a graphic, maybe an animated one, that really
  does the same thing as the video does".
