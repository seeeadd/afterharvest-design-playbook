> Generic rules for every client's page job. Each rule carries to any client in their own brand; Ana Calin's "The Exit
> Plan" pages (registration `index.html`, live at https://exitplan.howwegrowtoday.com; VIP `vip/index.html`; confirmation
> `confirmed/` and `vip-confirmed/`; offer pages `program/` and `join/`; all in seeeadd/2026-ana-calin) are the worked
> example. Her facts live in `../clients/ana-calin.md`.

# How a page job runs, and the judge checklist

**Purpose:** build or improve a client's registration or VIP page so it comes out right the first time, in their own
brand, without Sean re-explaining what he wants. Part 1 is how the job runs, step by step. Part 2 is the judge
checklist: yes/no tests every page must pass before it is shown or published.

Read with: [registration-page.md](registration-page.md), [vip-page.md](vip-page.md), [ui-kit.md](ui-kit.md),
[layout-type-spacing.md](layout-type-spacing.md), [copy.md](copy.md), [motion-and-speed.md](motion-and-speed.md),
[fladlien-on-pages.md](fladlien-on-pages.md), [evolution-ana.md](evolution-ana.md), and the house files `../SOP.md`
(this file is its page-job version; where they overlap, they agree), `../graphics.md`, `../motion.md`,
`../feedback-log.md`.

Status words: **final** (Sean approved, or it shipped and stood), **open** (waiting on Sean or the client), **still to
do** (known gap). Where chat items conflicted, the latest final one is written here.

---

# Part 1. How the job runs

## 1. How Sean likes to be worked with

- **Claude is the designer.** Make the layout, graphic and animation decisions yourself, with full effort, and aim to
  surprise him. Sean guides and corrects.
  - Sean: "That's a designer's job, that's your job. As Claude, I'm here to guide you".
  - Sean: "Just go hardcore with your highest effort and thinking process".
- **Fast, visible progress.** Send each finished piece as it exists, not in one batch at the end. After about 20
  minutes he expects most of the asked sections touched, not a few. Answer pace questions honestly with a done list
  and an untouched list.
  - Sean: "Are those literally all that you've done after 20 minutes?"
  - Sean: "go ahead with all six, send each one as done. one should only take 8 mins max." (Claude had estimated 25 to
    30 minutes a slide.) Budget about 8 minutes per slide graphic; build shared assets first.
- **Say the time first** for anything long (more than about 10 minutes), list what will change, and keep him updated.
  Render only what is needed and offer the fast path first.
  - Sean, during a 7-minute render: "any update" / "its been 20 mins", then "make it fast with the gif"; Claude rendered
    only the frames the GIF used.
  - Ana: the plan redesign of the calculator was announced as "about 45 minutes" with a three-line change list, while
    confirming every field and calculation stays.
- **Change only what was asked.** Keep everything he liked. A "makeover" changes the rest, never the whole page.
  Never revert a page unless he says "revert".
  - Sean: "I didn't tell you to revert it. I like some parts of the stuff that you built with her own unique branding,
    but I just told you to give it a makeover with a compact layout." (Claude had read "I prefer that" as a revert.)
- **Improve an approved page on top; never rebuild it in another page's style.** Keep its colours, drawing style,
  sections, video device and mockups, and add to them. If a rebuild is tried and rejected, do not publish it and
  restore the original at once.
  - Sean: "You honestly kind of ruined it. I prefer the old colors, deign, and you stripped away a lot of stuff,
    basically. I'm not a fan. Can you bring back the charm?" Then: "implement what you did on the VIP, add on top, and
    maybe replace some graphics that could look better with our new techniques."
  - Ana: the original registration page (cream and sand, ink-outlined drawings, iPhone video, day mockups, pink
    buttons, sunflower yellow) was restored from git, then the VIP techniques were layered on.
- **Fix the root cause, not patches.** Reproduce the bug in the browser, find the code that decides the behaviour,
  change that, then test every path that could trigger it.
  - Sean: "make sure your fixes are not a bunch of patches and atually fix the right code" (the blank-ticket bug; the
    pill and lights overlap was fixed at the stacking definitions, not with an override).
- **Full effort on small details.** Compare against the reference zoomed in, fix seams and misalignments, and say
  honestly where it still differs.
  - Sean: "dont be lazy, add more effort on the curves."
- **Give a real judgement.** When he asks "what do you think", recommend with short reasons per case, disagree when
  warranted, and change the answer openly when he raises a fact that shifts it. Think as one visitor, then as the
  whole audience. Push back when an idea would hurt sign-ups.
  - Sean: "you dont have to agree to me. whats your judgement"
  - Ana: big monitors scale up yes, 1440 to 1920 no, laptops no (it would push the form down).
- **Use multi-agent workflows for big jobs** (redesigns, whole-page audits, beat-by-beat video plans). Do small visual
  tweaks directly so screenshots come fast. Sean can say "use a workflow" to force one.
- **Do not fetch huge repos in full** in a cloud session; read only the files needed (a full fetch of the factory repo
  filled the disk to 19 GB).

## 2. Reading what Sean means

- **Find the exact element before changing anything.** He sends a screenshot and a short note. Check the screenshot
  for which element it is. If a change makes something huge, confirm it was the intended one.
  - Sean: "Wait, I meant the heading of the page: "How to Build the Income That Does Leave Your Job," not the "Save
    Your Seat" text. Why is it too big?" and "i said you can make this bigger" (Claude had enlarged the wrong heading).
  - Name things for him: the big hero line is the H1 (hero headline); the small line above it is the pre-headline.
- **Two plausible readings:** do the likeliest one and say which other reading you can switch to.
  - Ana: "testimonial bar" was read as faces, stars and "800+ student wins", with the stats strip offered as the
    alternative.
- **"here" with no screenshot:** make the most likely reading, do it, and say what you assumed and where else it could
  go. Ana: "You can add a time graphic here. Yo." arrived without an image; the clock went on the form's "For you"
  line, with the alternatives named.
- **"X or maybe Y instead":** the later "instead" option is usually what he wants. Do that one (or ask), not the easier
  first one. Sean: "i said top right" (the floating Day 1 to 3 bar: "can you put this floating thing for days 1 to 3
  under the top-right side instead").
- **State every assumption** in the reply and offer to change it. Sean: "i meant for this one ok".
- **He types fast and by voice:** read for intent ("publiash", "publis" and "pub" all mean publish). See `../SOP.md` E.

## 3. Inputs to collect before building

- **The copy doc** from Sean, used word for word ([copy.md](copy.md) section 1).
- **Client facts** for every block that needs them: the promise, student results with a source, call times, tools,
  access after, dates and the anchor time zone, where the audience lives (for the time list), payment links. Never
  invent any of it (`../SOP.md` E).
- **Blocks waiting on facts go in hidden.** Wire them to a settings file so they stay hidden until filled; preview
  them with SAMPLE text; send the client one numbered, ready-to-paste question list.
  - Sean: "try to do all".
  - Ana: `assets/offer-settings.js` (keys such as `SAFETY_*`, `LIVE_CALLS`, `HOURS`); one message to Ana with 10
    numbered questions.
- **Launch details for the page head and footer:** the share picture idea (16:9 and square), the tab title and
  description, the host mascot for the favicon (free and VIP versions), the help address for the footer, and the
  launch day (when noindex comes off the registration page). See [registration-page.md](registration-page.md)
  section 4.1 and [ui-kit.md](ui-kit.md) section 17. Sean (Oct 31): "there should be a good preview image both for
  square and for landscape, like 16:9."
- **Real screenshots to replace recreations.** List exactly which ones the client must send and swap them in as they
  arrive. **Open** for Ana: the Sprint lesson list and one worksheet, one frame from the Money Rewrite replay (Oct 24),
  the VIP group header once it exists, optionally a 10-minute real markup of a sample offer.
- **References from Sean** (Pinterest, motion videos, art-style pictures): study every one, zoomed in, before
  building. Study the form, not only the surface: shapes, silhouettes, lines and their rhythm, proportion, the value
  structure (a three-value notan), where colour lives, and the idea behind each. Write the study down and build from
  it.
  - Sean: "Are you also going to study the pictures I've sent?" and "don't just review the texture, but review the
    form: the shapes in it, the lines, the creativity captured."
  - Ana: the study is `tools/paint/STUDY.md`; the house version is `../study-art-references.md`.
- **Keep every reference in one folder** in the client repo, out of the live site, with a README per subfolder.
  - Ana: `tools/film/pinterest/` with `1-mixed-media`, `2-motion-videos`, `3-art-style-references`.
- **Guidelines to read before designing:** the Jason Fladlien teardown in seeeadd/fladdy (write-up, transcript and
  frames; see [fladlien-on-pages.md](fladlien-on-pages.md)); the factory's slide guideline
  (`prompts/4-day1-slide.md` in the outreach thumbnail factory) for presentation-style graphics; the motion study
  (Ana: `tools/paint/MOTION.md`; house: `../study-motion-references.md`).
  - Sean: "I want you to use the presentation guideline on the outreach thumbnail factory."
- **Licences for any found asset.** Click through to the original source and confirm a commercial licence before it
  goes public. Leave out anything with a visible watermark. Paint out brand logos on props.
  - Ana: masking tape left out (Adobe Stock watermark); the Canon logo on the camera and the Casio logo on the
    calculator painted out; a gold clip with a "penco" emboss and a gingham ribbon flagged to Sean. **Open:** licence
    confirmation from Sean.
- **Where the pages live:** each client gets their own repo with pages at the root, their own Vercel project and custom
  domain. When moving pages, copy every dependency, fix links that name the old address, check every link at desktop
  and phone width, and keep the old links working. Environment variables are added in the new Vercel project.
  - Ana: seeeadd/2026-ana-calin on exitplan.howwegrowtoday.com (moved Oct 30 from `2026-or-afterharvest`
    `ana-calin/workshop/`); `KIT_API_KEY` and `KIT_TAG_ID` added in the new project. Sean: "can you transfer all of
    these links to this repository?"
- **Secrets never pass through chat or Slack.** The owner adds keys to Vercel or sends them through a one-time link.
  Sean manages Vercel. Sean: "I am the one in charge of Vercel, so she has to send it to me."
- **Read-only on everything external:** never send, post, upload or share in any app, never send anything to leads.
  Sean: "Read-only on everything external. Don't send, post, upload or share anything in any app".
- **A new kind of page gets its own adaptation.** A multi-speaker summit is not a single creator's page: the speakers
  become the proof (a speaker wall, the agenda by day). The VIP and other pages carry over as a good start. Sean:
  "Everything that we talked about from the registration page, the finalized preferences, and anything that would be
  great information for Claude Code to create the same types of pages: put them in a file."

## 4. Brand and art style first

Before drawing or laying out anything:

- **Read and rate the client's own art style** (`../graphics.md` section 3). Match a strong style; elevate a weak one
  in its own direction, never replace it.
- **One goal per page decides everything:** the opt-in on a registration page, the VIP order on the VIP page, the next
  required action on a confirmation page.
  - Sean: "Again, our goal is for people to get to opt in. That's the goal. Always think of that goal for all devices
    if you're going to fix their UI."
  - Sean: "The goal of the page is to get them to sign VIP. That is the main, main, main goal... like they would sell
    it to themselves. You're not going to sell them, and you're not going to scold them"
- **No generic "AI pattern" layouts** (rows of three screen cards, four-icon grids, interchangeable card stacks). Each
  section's layout comes from the client's world and the one idea it carries ([layout-type-spacing.md](layout-type-spacing.md) section 1).
  - Sean: "this looks like an ai pattern landing page build".
  - Ana `/program`: three screens side by side became a three-lane timeline (now "Three ways January can go.").
- **Compact over bulky.** When a page feels heavy, tighten it; don't add blocks. A short offer page keeps the compact
  density of its reference but must look like the client's own brand and unlike every other page we made. Sean: "too
  bulky"; "I like the compact vibe of Jay's offer short page".
- **Grounds and colour:** calm, light grounds from the client's own palette; colour carried in shapes and section
  moods, never a muddy grey or a whole-page grain ([layout-type-spacing.md](layout-type-spacing.md) section 10,
  [registration-page.md](registration-page.md) section 23).
  - Sean: "also make the grey bg a bit lightwe"; "im not a fan of this puke poop grey color"; "Not just colored
    shapes, but actually think of a unique background for that specific section."
  - Ana `/program`: `--ground:#F3F0EB; --ground2:#F9F7F3; --paper:#FFFDF9` (`assets/offer-prog.css`).
- **Check Gemini will fit before asking Sean to make anything.** Photoreal props next to drawn ink objects look pasted
  in. Use Gemini only where it cannot clash (texture, light); draw anything with text on it in code.
  - Sean: "Are you sure that these Gemini prompts would produce something that would look good with our branding and
    art style?" (Claude withdrew the first list.)
- **Badges and seals are Gemini's job from Claude's prompt** (Sean's reference images attached): one shared style
  block, then one prompt per badge, plus one-line fixes for misspelt words, style drift and ring words that do not
  fit. Claude then repairs text, cuts out backgrounds and places them.
  - Sean: "No, I still want Gemini to do it, but something that looks a little better. I want you to make the prompt
    better."
- **Pinterest pieces on a page only when Sean asks** (Nov 9: "use the Pinterest assets... only the ones that are appropriate"): the cleaned cut-outs in
  `tools/film/cut/`, a few per page, each on the thing it means (string lights for "you're in", a bow on a pass, tape on a printout). Flag the licence
  question when they go live. Our own paint-studio pieces (`img/vip/paint/`) are not Pinterest; they are the default.
- **Pinterest is otherwise reference only,** never on the live site. No Canva, no image generators for page art, never the
  client's face made by AI. Graphics are painted in-house (`../graphics.md` sections 3b and 4).
- **Self-host special fonts and the animation library,** after checking the font licence (for example SIL Open Font
  License). Ana: the calculator's LCD face `assets/fonts/DSEG7Classic-Bold.woff2` with `DSEG-LICENSE.txt`; GSAP in
  `assets/vendor/`. Details in [motion-and-speed.md](motion-and-speed.md) section 11.

## 5. Order of work

1. **Lock the flow before the design.** Sign-up, payment, redirects, tags, emails and sheets work end to end first,
   then polish. Sean: "I really want to lock in the flow of everything before I lock in the design."
   - The route (Ana): registration, then the optional VIP offer, then the free or VIP confirmation page. On
     confirmation: join the WhatsApp community first, then the seven-question survey that unlocks the calculator
     (which has its own return route `/exit-number/`). The calculator result never requires WhatsApp, VIP, a login or
     leaving the page.
   - Anything a page promises (a welcome email subject to reply to, reminders, the Zoom link, the VIP email, the
     survey nudge) must be delivered by the email sequence in the same voice; draft the emails to match the pages.
     Email setup: Kit domain authentication on, double opt-in off on the sign-up form. **Open** for Ana.
2. **Read before a big rebuild.** Read the existing page and its wiring (form, popup, scripts) so sign-ups keep
   working. Write the plan into the repo, say how long it will take, and ask the one design choice that matters before
   building.
   - Ana: `tools/paint/PLAN-registration.md`, "several hours of work, done in two passes with screenshots after each";
     the choice asked was shutter window or door.
3. **Ideas and plan first for big creative pieces,** with what Sean can make (Gemini, Pinterest) and what the client
   must send. Then do not wait on optional assets: start everything that can start now and swap assets in later.
   Sean: "Could you start everything else now?"
4. **Study the Fladlien teardown and apply it** section by section: show the real thing instead of describing it,
   make the most important words biggest, one idea per band, motion only to lead the eye, a progress strip for the
   framework ([fladlien-on-pages.md](fladlien-on-pages.md)).
   - Sean: "that's a really great way of applying Jason Fladlien's strategies visually. Props to that"
   - Keep the placement decisions once approved; later rounds raise the look, not the decisions. Sean: "I liked the
     areas where you put the design, like the decisions are right. Now we have to elevate the design".
5. **One section, one graphic at a time.** Propose concepts when a set of graphics is redone, then build one at a time
   and send each as done.
6. **After a hero change, do a balance pass down the whole page** so text and sections line up evenly beside the
   frozen form. Sean: "fix the layout of the text and make it look proper and balanced throughout the page".
7. **Copy passes** follow [copy.md](copy.md) section 1: map each of his sections onto the existing page first, then
   rewrite section by section; make it skimmable (bold lead line per block, highlight the phrases that drive the
   opt-in, his wording exact); check every section on desktop and phone.
   - Sean: "Do the same as before, where you make it skimmable, add some bold and highlights, and know which words to
     emphasize (which words are important for them to get to opt in)".
8. **Carry lessons to the sibling page.** Once one page is perfected, apply everything learned there (graphics,
   animation, Fladlien rules, backgrounds, his preferences, which graphics go where) to the next page, adapted to that
   page's existing look. Ana: VIP first ("the most perfect VIP page"), then the registration page.
9. **Devices in passes:** desktop and laptop first, then phones and tablets (portrait AND landscape), then every
   device (Android and iPhone). Every fix on every device serves the one goal
   ([layout-type-spacing.md](layout-type-spacing.md) section 13).
10. **Speed pass last for each device group:** keep every graphic and animation at the same quality; find a cheaper way
    ([motion-and-speed.md](motion-and-speed.md) section 11). Sean: "I want them to load as fast as possible, really
    fast, without removing anything from them. Same quality, same high quality. Maybe there's a different way to make
    it faster."
11. **Reuse page pieces in other media.** The video reuses the page's own painted art and records the real UI (header
    countdown, ticket form, calendar, signature, Gmail and WhatsApp screens) from the page. Keep an asset map per
    client. Ana: `tools/film/SITE-ASSETS.md`. Sean: "I was thinking of putting some assets from this landing page into
    the video itself, so it's very congruent, specific, and for real".

### 5.1 Working habits during the build

- **Big layout experiments go on a trial URL,** noindexed, on the work branch only; the live page stays untouched.
  Ana: the two-column page with the frozen form was built at `/v2/` (`<meta name="robots" content="noindex">`), then
  became the main page; `/v2/` now redirects to `/` in `vercel.json` and the old page is kept at `/v1/`. When a trial
  wins, it goes to the root address, never live at the trial path. Sean: "Why is it on /v2? Why is there a slash?"
  and "maybe publish to not /v2 but on https://exitplan.howwegrowtoday.com/".
- **Variations stay switchable** by a URL parameter and are sent side by side with captions that match the switch
  names (Sean refers to them by caption). Ana: the seat ticker `?tk=a` bunting / `?tk=b` departures board; the VIP
  headline `?h=A` / `?h=B`.
- **Preview options in their real spot** on the page without changing the live page; publish only after he picks.
  Sean: "let me see first if its good" (two video-call icons, A and B, on the prize section's yellow).
- **Wording options:** about five numbered options in the client's voice, grouped by angle (what they get, simple
  yes, timing, the client's voice, price up front), each with a short form, one clear recommendation and a second
  choice. Sean: "variations?"
- **Removed graphics stay in git** so they can come back. Ana: the three-day drawing was replaced by the booking card,
  then came back slimmer when Sean asked.
- **Elements not in the client's copy:** keep them, list them for Sean, and ask whether they go. Ana: the stats bar,
  "800+ student wins", "Admit one", "Seat holder" and "save my seat (free)" were listed; he removed the ticket extras
  and kept the stats and the wins bar.
- **Copy Claude wrote is a suggestion** until Sean or the client approves it; flag it as Claude's wording. Sean: "yes
  go ahead".
- **The client's comments and script ideas:** Claude may judge which ones deserve a place, place them, then show Sean.
- **Data and privacy changes are never silent.** If following a spec stops data reaching the client's sheet or email
  tool, tell Sean what stops flowing and offer the minimal alternative. **Open** for Ana: the calculator now sends
  nothing to her sheet or Kit; the "Exit numbers" tab stops getting rows.
- **External specs** (for example from ChatGPT): build to the spec, turn its acceptance cases into a test that must
  pass, keep the maths in shared code, then report what was built, checked, removed per the spec and left for later.
  Ana: the Exit Number calculator, 103 passing checks (T01 to T16), maths in `assets/exit-calc.js`.
- **Long tools become numbered steps,** each in its own matching colour, each opening with a "Goal:" line, a short
  why, and a status line when collapsed (Ana: "You keep $475 a sale", "Over by 4.7 hrs a month"), plus an optional
  last step for later. Sean: "Add an actual goal in every part."
- **New CSS classes get a unique prefix.** Check the page and the shared stylesheet do not already use the name.
  Clashes broke Ana's `.rq`, `.wa`, `.wins`, `.pull` and `.wrap` (a stray indent in the header's second line), and
  pushed the calculator's second screen to the left edge.
- **Never commit test screenshots** into the site repo. Keep work folders off the public site (Ana `.vercelignore`:
  `tools/film/`, `tools/paint/`, `playbook/`, `CLAUDE.md`).

## 6. Showing work: screenshots and sizes

- **Sizes for every visual change:** 1440 and 390 always; 1280 when a frozen form or hero is involved; 1024 and 320
  for tight layouts; about 900 and 1100 when buttons or cards sit in columns.
- **First-screen and before/after sets** for hero, fold or speed work: 1280x720, 1366x768, 1440x900, 1536x864,
  1920x1080 and 2560 wide.
- **Show the page as a visitor sees it today:** seasonal theme on, live feed state, current photos. Never shoot with a
  theme override off. Sean: "make sure to use the new christmas themed buttons" (screenshots had been taken with
  `?xmas=0`).
- **Motion gets a short clip** recorded from the live page; stills cannot show it. Also send a contact sheet of the
  animation frames.
- **Scroll through before full-page captures** (sections fade in on scroll), and explain artefacts (a fade caught
  mid-way, blur not rendered) instead of letting them read as the real look.
- **Animated elements:** a constantly moving element can stall the screenshot tool; scroll to it and use element
  screenshots instead of page-coordinate clips.
- **Always the latest screenshot.** If a stale one was sent, say so and resend.
- **Before a render or a send, check a contact sheet of key frames** and fix overlaps (labels over characters,
  captions over stamps, text crossing headings).
- **Note sample data:** say when screenshots use `?demo=1` sample numbers (Ana's registration page).
- **Full-page screenshots on request.** Over about 8,000px tall, bundle them in one zip. Sean: "Can you give me the
  full screenshots for the long offer page?"
- **Show where each visual part sits** so Sean can make his own mockup for it. Sean: "wheres these parts. im still abt
  to create mockup for each".
- **Spec doc for team approval:** each section with a description, a screenshot and a status (Not reviewed /
  Approved / Changes needed), updated after every published change. Sean: "Can you make a spec of this current
  landing page that you just made so I can have my team approve it?"
- **Copyable review text after a copy pass:** the whole page top to bottom as plain text, with [BRACKET] section labels
  that are not on the page, both A/B headlines, button labels, the deadline-closed state and the exit popup, checked
  against the page, also saved in `tools/`. Ana: `tools/copy-vip-page.txt`. Sean: "give me a copyable text of the
  landing page afterward so I can have it for review."
- **Report format:** short grouped lists: what changed, where to look (screenshot), what is still open, what waits on
  him or the client, and whether it is live or only on the branch. No jargon.

## 7. Measure, don't eyeball

- **Read the page, not the pane.** Measure with the DOM: `scrollWidth > innerWidth` for sideways scroll,
  `getBoundingClientRect()` for overlaps, gaps and what is above the fold, computed styles for sizes.
- **Overflow at every width** 320, 390, 1024, 1280, 1440 and 1920 (and when an input takes focus).
- **Every date window** with a `?now=` date: before open, live days, open, closed (Ana: `?now=2026-12-09T05:00:00Z`
  on the VIP and confirmation pages).
- **Copy diff after any rebuild:** diff the whole page's copy against the previous version so nothing silently
  disappears. Ana: the WhatsApp rebuild cut "for 30 minutes after each workshop session, plus one morning slot." and
  its "Let me ask you in the VIP chat ($67)" button from the live VIP page; a copy diff found it and it was restored.
  Report a live mistake honestly and fix it on the next publish.
- **Speed in numbers:** before and after on the same connection, three runs averaged (largest paint, full load,
  blocking time, layout shift, image weight), plus a pixel diff to prove nothing changed visually
  ([motion-and-speed.md](motion-and-speed.md) section 11.1).
- **Data checks:** never trust an HTTP 200 from a sheet or script endpoint; parse its answer and confirm the row
  landed. When updating a sheet's Apps Script, update the existing deployment (new version) so the URL stays. Ana:
  the survey sheet answered `{ok:false}` with HTTP 200 because an old deployment kept a placeholder key.
- **Verify what the client says is done** by checking the live thing (open the live checkout, read its settings, send
  a harmless test event). Report exactly what is on and off, and what the check proves and does not (a setting is set,
  not who set it). Never trust an old to-do list over a live check.
  - Sean: "how do you know she did the redirects". Ana: the live check showed redirects set on all three payment links
    and "Allow promotion codes" off, later on.

## 8. Checks every round (before every commit)

Run these after every batch of changes; if a run was interrupted, say which checks did not run and run them before
publishing. The page-specific lists are in [layout-type-spacing.md](layout-type-spacing.md) section 14,
[motion-and-speed.md](motion-and-speed.md) section 12, [vip-page.md](vip-page.md) section 18,
[registration-page.md](registration-page.md) section 27 and [copy.md](copy.md) section 13.

- **Sign-up flow end to end** on desktop and phone: form placement, the situation field, CTA behaviour (desktop vs
  phone), empty-form errors, buttons and labels focus the fields, chips recorded, the form moves into the frozen
  ticket, popup and phone bar work, redirect to the VIP page with name and email. Nothing is sent to the email tool in
  testing.
- **Exit popup** behaviour.
- **Seasonal buttons:** the count of themed buttons is right; `?xmas=1` and `?xmas=0` both look right.
- **No sideways scroll** from 320 to 1440px (and up to 1920), nothing overflowing at 320, the phone bottom bar fits.
- **VIP page:** copy word for word, both popups, hover crossouts, Escape, the checkout link with email prefilled, the
  A/B headline, the closed state, no script errors on phone and desktop.
- **No console errors,** fonts loaded, reduced motion shows final states.
- **`grep` for em dashes** in copy.

## 9. Publishing

- **The live site changes only on Sean's word:** "publish", "pub", "push", "live" (typos count: "publiash",
  "publis", "push i eanna check"). Work goes to the work branch first (Ana: `claude/quirky-franklin-etidvi`).
- **Every hand-off says plainly whether it is live,** lists everything waiting on the branch since the last publish,
  and ends with "say publish and it goes up". Sean: "Can you send me the links? Did you publish them?" and "Where's
  the published".
- **To see unpublished work,** give the branch's Vercel preview link plus the exact path and any test bypass. Ana:
  `/exit-number/?sv=1` opens the calculator without doing the survey. Say if you could not open the preview yourself.
- **Before pushing:** warn that publish also puts all other unpublished branch work live; keep film working files and
  unlicensed images off the live site; `git fetch` main, see what Sean's other chats changed and whether it overlaps,
  merge, re-test, and tell him what was merged.
- **Push, wait for the deploy, then check the LIVE site** (fetch with a cache-buster and confirm a string from the
  change): every funnel page loads (Ana: registration, VIP, confirmed, VIP confirmed, program, welcome,
  exit-number) on desktop and phone, no errors, no missing files or broken images, no old dates, no sideways scroll
  from 320 to 1440, popups, checkout and the closed state work, new images load, animations play. Report it as a
  short checked list.
- **Say plainly when the live site was not re-checked.**
- **"looks same" after a publish:** load the live site fresh at several widths and compare with his screenshot. If live
  is right, tell him to hard refresh (Cmd+Shift+R, Ctrl+Shift+R, or a private tab on phone) and what he should see.
  Version asset URLs so caches update. Ana: his browser showed a cached copy, and the live check also caught a real
  bug (the invite off the left edge at 1000 to 1240px).
- **Publish cadence:** when Sean says so ("publish after", "And you can publish them already."), publish after each
  verified change for the rest of that run.
- **Interruptions:** when Sean interrupts, stop, check what the interrupted command already did (did the edit or
  publish go through?), tell him, then make his fix. Keep an interrupted edit only if he does not object. Ana: a
  publish interrupted over the floating ring light had not gone live.
- **After publishing, give the links** in the order a person goes through the flow, with sample-name query strings for
  personalised pages. Ana: registration, VIP, confirmation, VIP confirmation, exit number, program welcome, offer short
  and long, with `?first=Theia`.

## 10. Messages for the client

- **Plain and friendly, never technical:** say why in everyday words (no "webhook", no code), then what to do, and say
  clearly when there is nothing to do yet. Write so a non-technical business owner understands it on first read.
  - Sean: "Still a little bit too technical. Make it friendly for a woman in her 40s to understand."
  - Ana's accepted shape: "Every time someone buys anything from you, Stripe lets all your connected tools know, ...
    You don't need to do anything now. ... If it didn't, perfect, nothing to fix".
- **Short and only what is still needed.** A few lines per step; don't repeat steps already sent.
  - Sean: "no, no, no. Make it all about the webhook. I already sent the rest of this message a while ago" and "Why is
    it so long?" Ana: the Stripe guide was cut to about a third, four short parts (add the webhook, one key
    permission, the Money Rewrite check, a $0 test purchase).
- **Setup steps go as a ready-to-paste Slack message.** Keys never go in it.

## 11. End-of-block hand-offs

- **Final pages:** check every address loads on the live domain; one table of live links grouped by funnel (free
  event, paid program, payment links, backups) and full-page screenshots; flag anything fixed but not yet live. Sean:
  "Can you send me the final pages and final links with the new domain?"
- **To-do list when asked:** one list at the end of the turn, grouped: waiting on the client; must-do before launch
  (publish, deliverability, emails, links the page promises, a full phone run of every path); nice to have. Include
  anything the pages promise that is not set up yet (for example "your personal link comes by email before Day 1").
- **"What next":** a short list ranked most urgent first, each with who does it and roughly how long, and offer the
  next thing Claude can start. Sean: "pub. What do we do next?"

## 12. Update the playbook (every turn with a correction or approval)

- Log the line in `../feedback-log.md` (and the client repo's `playbook/feedback-log.md`), promote repeated
  corrections into the rule files, put client-only facts in `clients/<client>.md`, and push (`../SOP.md` D).
- Newer feedback replaces older rules; keep the reason only when it teaches.
- When Sean asks for every preference to be captured, work from the full record first: the whole chat transcript, the
  live page code and the change history; then turn each correction and approval into a generic rule. Sean: "I want to
  be able to use them for everyone, but in their own way for our future clients, in their own way, in their own
  brand, in their own context."
- After a client's pages are approved, the next client starts from these files plus the transcript and the page
  source.

---

# Part 2. The judge checklist

Every item is a yes/no test. A judge checks every page (registration, VIP, confirmation, offer) at 1440, 1280, 1024,
390 and 320, plus the laptop heights, before Sean sees it and before every publish. Any "no" is fixed first. The
example after each item is Ana's.

## J1. Goal and structure

- [ ] Does every section move the visitor toward the page's one goal (opt-in, VIP order, next step)? Is anything there
  only as decoration? **Open** for Ana's VIP page, Sean: "I want to know if we're actually abusing Jason Fladlien's
  advice. Are we doing that? Is this page really visually effective for people to sign up and pay for VIP? Is every
  section helping them to work towards signing up for VIP?"
- [ ] Does each section have a layout that comes from the client's world and its one idea, with no row of three
  cards, four-icon grid or interchangeable card stack?
- [ ] Do no two neighbouring sections open the same way (vary centred and left openings), and is no decorative element
  repeated without adding information? Sean: "The UI right now is a little bit generic-ish and repetitive." Ana VIP:
  the week and the fit check open centred; a decorative VIP lane and a repeated stamp strip were removed.
- [ ] Is the required task first and widest, and the reward a small side teaser? Ana confirmation: the survey card
  742px wide, the calculator preview in a 340px side column (`assets/confx.css`). Sean: "The survey observation is
  the first thing they would see. I think the calculator UI is a little too big."
- [ ] Does a section with one or two action cards have its own layout (no grid with empty columns)? Ana: `.acts.one`
  on "Then one small thing" and "Then two small things". Sean: "why does this look like this".
- [ ] Are elements that are not in the client's copy listed for Sean?

## J2. Placement and alignment

- [ ] Does every picture have one main device, at most two props, clear margins, and nothing on top of text? Sean:
  "Some of them are too scattered. Some of them are too tight. Make it more balanced. Sometimes the text doesn't fit in
  where they are."
- [ ] Does every text block have a set width so its lines never squeeze, and does all text fit inside its card,
  painted graphic or button at every width (check about 900 and 1100 too)? Ana: the WhatsApp button text spilled out
  at 1100 and 900px.
- [ ] Is the video or main visual column the wider one in the hero? Ana: from 1061px
  `minmax(0,1.52fr) minmax(0,1fr)`, started at 1.44fr. Sean: "column of the video to be bigger".
- [ ] Does a badge beside a heading sit beside it as two columns, at a modest size? Ana confirmation: 168px on desktop
  (was 200px), 128px stacked above the heading on phones. Sean: "That's a little bit too big ... I want the logo to be
  beside the header".
- [ ] Is a pointing arrow tight to what it points at? Sean: "a little bit too far from the arrow".
- [ ] Does a compact strip fit its content and centre on what it belongs to, not stretch? Ana: the trust strip
  `max-width:560px`, centred over the video window.
- [ ] Is every bar or banner on one ground, never across the seam where two section colours meet? Ana VIP
  confirmation: the pink starts at the very top so the date bar sits on pink.
- [ ] Is a pull quote attached to the section it introduces, not floating in its own band? Sean: "is this supposed to
  be like this?" Ana VIP: Ana's note quote opens the fit check on pink.
- [ ] Do paired action cards run full width, words and button left, picture right?
- [ ] Is the floating Day 1 to 3 bar (or similar floating piece) placed where Sean set it? Ana: top right on desktop.
- [ ] Are rings, circles and marks centred on their target (a calendar ring around the 30th, not under it)?
- [ ] Does each hero graphic have breathing room from the element above it? Ana: the shutter tops touched the stats
  bar; room was added.
- [ ] Is every photo of the client her own photo or a still from her own recording (no AI picture she has not
  approved), in a simple frame with no app chrome? Ana: "use one of the pics I gave you or a screenshot from my
  recording"; Sean: "iphone ui doesnt look realistic" ([registration-page.md](registration-page.md) section 24).

## J3. Gaps and white space

- [ ] Is there no big empty gap beside text or a headline? In a row with a mockup, is the text centred against the
  screen and the space filled with useful items? Ana `/join` weeks: three ticked steps, a progress bar, "You keep".
  Sean: "kinda prefer this layout byyt make it better".
- [ ] Is text beside a tall picture split: hook beside the picture (picture sized to that text), dashed divider, the
  rest in two even columns, then the button? Sean: "still too much awkward white space in between"
  ([registration-page.md](registration-page.md) section 3.2).
- [ ] Is no long paragraph right-aligned? Sean: "You can probably send some text on the right side, right-aligned, or
  maybe full width, because I think it looks a bit weird." Full width two columns won.
- [ ] Is justified text limited to tablet and desktop, left-aligned on phones? Ana: from 601px.
- [ ] Does a dense section beside the side form breathe without losing content or shrinking type? Sean: "I don't want
  to remove anything. I just need to be able to breathe because there's a lot of text." and "Isn't the text size a
  little bit too small?" Ana "But what would you sell?": question up to 54px, intro up to 31px, paragraphs 18px, the
  two bottom notes 15.5px in normal text colour.
- [ ] Is empty space on the right used? Ana day rows on desktop: date, headline and first paragraph full width, then
  the slides window beside the bullets, sticky; stacked at 1060px and narrower. Sean: "You can probably widen some
  text on the top here since there's still a lot of space on the right."
- [ ] Does a reference line sit tight under the thing it pairs with (no extra margin)? ([ui-kit.md](ui-kit.md)
  section 15).

## J4. Line breaks

- [ ] Are headlines hand-broken on whole phrases, separately for desktop and phones, with no small word left at a line
  end ([layout-type-spacing.md](layout-type-spacing.md) section 6)?
- [ ] Do dates, times, cities, prices and names stay whole (`nowrap` chunks), with a "·" ending a line, never starting
  one ([ui-kit.md](ui-kit.md) section 16)?
- [ ] Does a bold lead-in ("Copy, count, pick:") keep its bullet from breaking into one word per line, and does no
  crossed-out pill wrap onto two lines?
- [ ] Where a hidden line break joins two words, is the space kept (it once rendered "PLANEYES")?
- [ ] Is short wrapped text balanced, with no single word alone on the last line?
- [ ] Do the form's small lines and heading fit in every home of the form: the frozen side ticket and a 320px phone?
  **Still to do (Ana, judges Nov 4):** the side ticket breaks "About 90 minutes a session"; at 320px "Save your free
  seat" runs past the edge.
- [ ] Does each credibility line under a name sit on one line or break cleanly between whole phrases? Sean: "fix
  line" (Ana: Justin Welsh's "built a $15M / solo business").

## J5. Small assets never block

- [ ] Does no sticker, badge, tag, pill, camera tile or logo cover a headline letter, a number or a line of copy, at
  any width ([ui-kit.md](ui-kit.md) section 1)?
- [ ] Is a small asset that crowds something moved to the side, into real empty space or onto the corner of the thing
  it labels?
- [ ] On phones, does a stamp over a label go on its own line above it? Tested with a long name (Ana: "Christina's"
  was covered).
- [ ] Is a background that makes the hero feel crowded moved elsewhere? Sean: "these can be moved maybe on the footer
  instead so it wont look overwhelming." Ana: the village skyline moved to the footer's top edge.
- [ ] Are decorative connectors hidden on phones when the cards stack (Ana: the three roads)?

## J6. Form and first screen

- [ ] On laptops (1280x720, 1366x768, 1440x900, 1536x864, 1920x1080) is the visual in view, with the headline, sub
  line and most of the form? The button may sit slightly below the fold on short laptops only while a floating header
  button is always in view ([layout-type-spacing.md](layout-type-spacing.md) section 11).
- [ ] Is the first-screen fix a tightening of the approved layout (smaller gaps, secondary copy below the form), not a
  restructure or a centred hero?
- [ ] On phones: pill, headline, sub line, then the form with its button on the first screen, then the video and the
  rest? Sean: "see the form ASAP". Are desktop-only extras hidden and the bottom bar keyed to the hero form?
- [ ] On the VIP page on phones, does the video stay visible with the order card right under it?
- [ ] From 1280px, does the form move into the frozen side column without two tickets on screen and without the page
  jumping ([registration-page.md](registration-page.md) section 5.8)? At 1280, does the headline sit clear of the
  frozen ticket?
- [ ] On big monitors (from about 1800px) is the page scaled up evenly, 1440 to 1920 unchanged, laptops never scaled,
  and the form still on the first screen? Sean: "Yeah, I think we can scale for big monitors, for sure." **Still to
  do:** Safari check of Ana's scaling.
- [ ] Do all form tests pass (section 8 above)?

## J7. "Free" reminders

- [ ] Does every sign-up button say free, in the label or as a smaller "(it's free)" (Ana `small.bq`, `.8em`, weight
  600), plus "free · live on Zoom" under section buttons ([registration-page.md](registration-page.md) section 21)?
- [ ] Is "free 3-day live event" (or the client's version) still in the header?
- [ ] Is every paid button showing its price, and is no button greyed out?

## J8. Visitor time zone

- [ ] Does a visitor outside the anchor zone see their own dates, time and city (named, never "your time") as the one
  bold line, with the anchor time small and grey under it? Ana: "Dec 9 to 11 · 1:00 am in Manila", then "Dec 8 to 10 ·
  12:00 pm New York" ([ui-kit.md](ui-kit.md) sections 4 and 15).
- [ ] Is the zone read silently from the device (no location prompt, no IP lookup), with a clean fallback to the
  anchor version?
- [ ] Are times always with minutes ("12:00 pm"), lowercase am and pm, ranges with "to"?
- [ ] Does the form carry the "For you" line with the date and a small clock? Does the eyebrow put the visitor's dates
  on the accent row with the anchor dates tight under them?
- [ ] Does EVERY date and time on the page follow the visitor (date tiles, booking strip, the line under each button,
  closing ask, calendar invite, thank-you line, phone bar, header short date, session times)? Search the page for
  month names, weekdays and "am"/"pm", then check with the device set to a far zone (Asia/Manila), the anchor zone and
  an unknown zone. Sean: "fix these dates as well make them adaptable" and "and these. any more mention?"
- [ ] In the session-times list, does the visitor's city lead, big and highlighted, with the other cities small on an
  "Also:" line two per row, and all cities as before when the zone is unknown? Sean: "make their city the highlighted
  bigger one", "make it 2 per column instead".
- [ ] Are the visitor's dates bigger than the rest of the form eyebrow (Ana `.r1 b` `1.32em`)? Sean: "make date bigger
  here".
- [ ] Does the popup show the same time treatment as the tickets: their dates leading, the anchor small and grey, no
  row turning all accent colour? **Still to do (Ana, judges Nov 4):** the popup eyebrow turns all pink in time-zone
  mode and it has no "For you" line.
- [ ] **Still to do (Ana):** does the phone bottom bar show the visitor's time and city (it shows their dates since
  Nov 4)? Sean: "Shouldn't the phones also have the date line? Isn't that important?"
- [ ] After a date move, does no page, calendar file or picture show an old date?

## J9. Speed budget

The rule is "same quality, faster", measured. Ana's live registration page after the Nov 4 pass is the reference bar:
hero painting on screen about 1.1 s, full load about 1.9 s, layout shift 0, busy time about 0.3 s, total 4.6 MB
([motion-and-speed.md](motion-and-speed.md) section 11.6).

- [ ] Are the new numbers no worse than before on every measure, and does a pixel diff show nothing changed visually?
- [ ] Is every image no bigger than the sharpest size it is ever shown at, painted art in AVIF with WebP fallback,
  slides as WebP around 30 to 60 KB?
- [ ] Are small decorative images below the fold lazy-loaded, the hero art preloaded, every `<img>` with width and
  height?
- [ ] Is a page video a few MB at full HD (static grain, not per-frame), with a 720p copy for phones? Ana: 89 MB with
  per-frame grain, 6.2 MB with static grain.
- [ ] Are fonts and the animation library self-hosted, unused families dropped, cache headers set, and work folders
  out of the public site?
- [ ] Is every heavy single image flagged with an offer to shrink it? **Still to do (Ana):** the 210 KB SVG sticker.
- [ ] **Still to do (Ana):** speed on tablets and phones; the VIP, confirmation and offer pages.

## J10. Motion

- [ ] No pops, pulses for attention, generic slides, fades or flaps; real animation with arcs, anticipation and settle
  (`../motion.md`, [motion-and-speed.md](motion-and-speed.md) section 1)?
- [ ] Does each animation start when its card is fully in view, finish before people move on, and never cover text or
  get clipped by its section?
- [ ] Does motion animate only transform and opacity, pause off screen, and leave idle CPU near zero?
- [ ] With reduced motion on, is every scene shown finished and nothing hidden?
- [ ] Was motion shown to Sean as a clip from the live page?
- [ ] Does the seasonal layer show exactly Sean's keep list, with `?xmas=1` and `?xmas=0`? Ana (Nov 4): hat on every
  button's sunflower, lights on the frozen form, wreath, footer village lights, holly on Day 1, snow in the last section
  only; no hat on Ana, no hero snow ([motion-and-speed.md](motion-and-speed.md) section 9).

## J11. Copy

- [ ] Is every line of Sean's newest copy on the page word for word, nothing from older copy left, and every deviation
  reported (sections removed because his copy left them out, micro-copy Claude invented, em dashes turned into
  commas, CTAs kept where his copy had none)? Sean: "here's the updated registration copy (dont use em dashes)".
- [ ] Is there no em dash anywhere in copy (`grep`)?
- [ ] Is it skimmable: a bold lead line per block, a soft highlight on the phrases that drive the goal, no decorative
  bold?
- [ ] Is every number, name and quote real and sourced, with no invented counts or "people registered" lines
  (`../SOP.md` E, [copy.md](copy.md) section 8)?
- [ ] Is collaboration proof shown as real call frames only, not clickable, with no links, play buttons or logos, and
  is anyone without a real frame left out? Sean: "show these instead like the actual video frames", "maybe not have to
  include kristina coz we don have vid of her" ([registration-page.md](registration-page.md) section 10).
- [ ] Is each credibility line the strongest fact from that person's own pages, with no number whose sources disagree?
  Sean: "make sure all of em have the best bio here". Ana: Mary's wedding count (725 vs 722) left out.
- [ ] Is every featured quote in the recording or note it came from, word for word, and labelled with where it was
  said? Ana: Marni's "5x her investment in 7 days" (a post title) was not used because the transcript does not say it.
- [ ] Does sans carry long reads, numbers and small labels, with the serif only for big headlines?
- [ ] Are Claude's own wordings flagged for approval?
- [ ] Does everything the page promises exist (emails, links, reminders)?
- [ ] Full copy checklist: [copy.md](copy.md) section 13.

## J12. Devices and accessibility

- [ ] No sideways scroll at any width from 320 to 1920, including tablets around 1024 and when an input takes focus
  (fixes: `overflow-x:clip` on decorative sections, `minmax(0,1fr)` in grids, breakable spaces between `nowrap`
  chunks)?
- [ ] Are phone layouts not overridden by later desktop CSS?
- [ ] Do wide timelines stack each lane with its result on top on phones, with a swipe hint and dots where a swipe row
  is used (Ana `/program`: "Swipe through the month.")?
- [ ] Does a frame that was sized by its image have an explicit width once the image moved (else it collapses on
  phones)?
- [ ] Controls at least 44 x 44 CSS px, keyboard access, persistent labels, visible focus, labelled errors, never
  colour alone for a status, readable zoomed and printed?
- [ ] Do the phone bottom bar and every fixed bar fit at 390 and 320px with nothing cut or overflowing? **Still to do
  (Ana, judges Nov 4):** the bar overflows at both widths.
- [ ] Does the popup's email check stop a mistyped address on the first click? **Still to do (Ana, judges Nov 4):** a
  typo gets through on the same click.
- [ ] Does no graphic cover text on any width? **Still to do (Ana, judges Nov 4):** the day map covers text in the Day
  2 row.
- [ ] **Still to do (Ana):** phones and tablets pass (portrait and landscape). Sean: "there's also some stuff that
  looks weird on phone, like the graphics and the layout, so we can probably fix it and make them more
  mobile-friendly."

## J13. Tracking, data and publish state

- [ ] Does each checkout link record which button was clicked? Ana: `data-cta` ("header", "hero", "table" ...) passed
  to Stripe with the $67 checkout.
- [ ] Does every form and survey write land (answer parsed, row confirmed), with nothing sent to the email tool during
  tests?
- [ ] Is the change on the branch only until Sean says publish, and after publishing, were the live pages checked and
  reported?
- [ ] Is the page head right: tab title, description, share picture on the live domain with current dates, favicons
  with a fresh `?v=`, noindex on every page that is not launched ([registration-page.md](registration-page.md)
  section 4.1)?
- [ ] Does the sign-up reach the email tool through the site's own endpoint, land in the live sheet, and carry the
  hidden fields ([ui-kit.md](ui-kit.md) section 8.1)?
- [ ] Was the playbook updated for every correction and approval this turn?

---

## Still to do and open (process)

- **Open:** the Fladlien effectiveness review of Ana's VIP page (J1).
- **Open:** the data the calculator no longer sends to Ana's sheet and Kit (section 5.1).
- **Open:** emails that match every page promise; Kit authentication on, double opt-in off (section 5).
- **Open:** licence confirmation for found assets (section 3); Ana's real screenshots (section 3).
- **Open:** the brick wall strip on phones on the confirmation page (offered, no answer).
- **Still to do:** phones and tablets pass, the phone bar's visitor time, speed on other devices and pages, Safari
  check of big-monitor scaling, the 210 KB sticker.
- **Still to do (judges, Nov 4):** the popup email typo check; the phone bar overflow at 390 and 320px; the popup's
  missing "For you" line and all-pink eyebrow in time-zone mode; "About 90 minutes a session" breaking in the side
  form; the day map over the Day 2 text; "Save your free seat" past the edge at 320px.
- **Still to do (launch):** the square share picture; noindex off the registration page on launch day; the VIP
  footer's help address; what the registration page shows once the event has started (open question for Sean).

## J9. Confirmation pages: make it easy to act (Sean, Nov 9)

"The confirmation page is quite the most important": its job is to get them to do the steps that make them show up
live. Do the work for them, so nothing feels manual or optional.

- **Required steps look required.** A red "Required" gate that says what they get and what to do ("To get your
  calculator, answer these 7 questions first"), a red required stamp, and a link in the sticky header ("get your
  calculator") that scrolls there and lights the step up. The link turns into "open my calculator" once it is done.
- **"Most important" is red, big, with an exclamation mark,** never a small pastel tag.
- **Every button the same yellow** (no white "I did it" buttons); put a small painted picture of the thing beside it
  (an envelope for "I moved it to my inbox").
- **Mockups read as the real thing:** the chat in a real phone (status bar, island, pinned message, the group's own
  wallpaper), messages that arrive, ticks that turn blue, a reaction.
- **Tap for sound is big, in the middle of the video, with the sound moving,** so they know it is a video to press.
- **The personal step (questions for Ana) shows Ana:** her photo, thinking, with what she will read.
- **Arrows are drawn by hand** (a curve with a separate head, slight wobble, drawn on), never a stiff vector chevron.
- **Before publishing, click every survey and form through to the end** on desktop and a phone (Nov 9: a missing
  animation piece stopped the confirmation survey at question 1 on the live page). Decoration must never block a step:
  guard every animation so a missing element just skips it.
- **Text big enough for 30 to 50:** body copy about 17.5 to 19.5px on desktop, 16.5 to 18px on phones (Sean: "too small
  in general").
- **The upsell on a free confirmation page:** free seat next to VIP, the missing lines struck through, a real deadline,
  one clear "yes" button, and one gentle line that the free days are complete on their own. Every line from the offer
  page's own table.
- **Surveys: every opinion question ends with "Something else" and a box for their own words** (Sean, Nov 9: "so we
  don't miss out on that"). Optional, never blocks; it reaches the sheet as "Something else: their words".
