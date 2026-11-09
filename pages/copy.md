# Page copy: rules and Ana's final copy as the worked example

> **Purpose:** every word on a client's registration, VIP, confirmation and offer pages comes out right the first time,
> in the client's own voice, without Sean re-explaining. Rules first (general, for any client), then Ana Calin's final
> copy for "The Exit Plan", section by section, verbatim from the code, with the pattern each line follows so it can be
> rewritten for the next client. Ana's facts live in `../clients/ana-calin.md`.

Read with: [registration-page.md](registration-page.md) (section order and layout), [vip-page.md](vip-page.md),
[ui-kit.md](ui-kit.md) (button looks, forms, popups, dates and line breaks), [layout-type-spacing.md](layout-type-spacing.md)
(fonts, headline breaks), [motion-and-speed.md](motion-and-speed.md), [fladlien-on-pages.md](fladlien-on-pages.md),
[page-sop.md](page-sop.md), [evolution-ana.md](evolution-ana.md), and the house files `../SOP.md` (section E: never
fabricate), `../graphics.md`, `../video-editing.md`, `../feedback-log.md`.

Status words: **final** (approved or shipped unchallenged), **open** (waiting on Sean or the client), **still to do**
(known gap). Where chat items conflicted, the latest final one is written here.

Ana's code paths: registration `index.html` (live at https://exitplan.howwegrowtoday.com), VIP `vip/index.html`,
confirmation `confirmed/index.html` and `vip-confirmed/index.html`, offer pages `program/index.html` and
`join/index.html`, all in seeeadd/2026-ana-calin. Dates below are the current ones (the event moved from Nov 17 to 19
to Dec 8 to 10; see [ui-kit.md](ui-kit.md) section 15 for moving dates).

---

## 1. Where the words come from

- **Sean's copy doc is the source, word for word.** When he sends page copy, rebuild the page around it inside the
  approved layout. Do not shorten, rewrite or "improve" it. Sean (Nov 1): "heres the new copy".
- **The only edit you make on your own is dashes.** Em dashes become commas, colons or parentheses; en dash ranges
  become "to". Sean: "here's the updated registration copy (dont use em dashes)". Ana examples of the swap: "sell, and
  could it earn enough"; "The work (choosing a problem, shaping an offer, and asking people to buy) applies"; the en
  dash range "Nov 17 to 19" (written with a dash in his doc). His Nov 3 draft still had an em dash after "the order
  I'd follow": remove them every time, he will not repeat it.
- **Keep the client's real spelling of her name** even when Sean's message spells it differently. Sean types "Anna";
  the pages say "Ana" ("I'm in, Ana (it's free)").
- **Use the newest doc.** When Drive holds several docs with the same name (Ana had six called "Registration page
  copy"), open the most recently edited one and send Sean its link. Sean: "I want to try this out with the most updated
  copy. Can you resend the docs for the updated copy as well?" Save a copy in the repo (Ana:
  `tools/copy/registration-copy-2026-11-01.md`).
- **Check every line after it goes in.** Go through the draft line by line and confirm each line is on the page, and
  that nothing banned slipped in (section 4). Report it the way the VIP rounds did: "every visible sentence matches your approved Nov 1 copy word for word".
- **A redesign never changes copy.** Only additions Sean asks for are allowed (Ana VIP: the "Don't close this page"
  strip).
- **A copy update never drops proof.** Keep every existing proof card unless Sean says to remove it. Sean, when the
  Nov 3 update dropped two result cards: "dont remove the other 2 testimonials here". See section 8.
- **Make it skimmable without changing meaning.** Sean (Nov 3): "can you just update the copy real quick? Do the same
  as before, where you make it skimmable, add some bold and highlights, and know which words to emphasize (which words
  are important for them to get to opt in)". Emphasis rules are in section 5.
- **Lines you write in the client's voice are drafts.** Any chat message, question or quote Claude writes as the
  client (a WhatsApp demo, Zoom Q&A questions) is flagged for the client to approve before launch. Open for Ana: the
  VIP WhatsApp demo lines and the Zoom Q&A questions (section 10).
- **When the client's video script cannot be filmed,** move only the lines that say something better than the page;
  leave out warm-up talk meant for video. Keep Sean's step order even when the script orders steps differently. Upsell
  parts go on the upsell page, not the confirmation page. Recommend first, build after his yes, send screenshots before
  publishing. Sean: "You can just tell me which ones deserve to be on the confirmation page."
- **Script vs page:** when a new video script and the page say different things, list the differences for Sean;
  never choose silently. Every number in a script is confirmed with the client before use (Ana: "16,907 people have
  bought from me" was flagged); drop tool brand mentions ("A short calculator I built in Claude" was dropped); prefer
  the page's softer wording over a stronger script claim ("AI changed the order she teaches in" over "AI flipped that
  order"). Details: `../video-editing.md`.

## 2. Voice

- **The host speaks in first person** on her own page: I, my, me. Sean: "can you make it a little bit more first
  person?" Ana: "From people in my past challenge", "Jill Hart, in my past challenge", "A student in my past
  challenge", "From readers and students who've worked with me", "Individual experiences from my past challenge.
  Results vary.", footer "my own figures".
- **Third person is kept only where it is true to the speaker:** the reader's own buttons ("I'm in, Ana"), quoted
  testimonials ("Jill said Ana helped her ..."), and labels inside app replicas ("Ana is sharing her slides", "Ana is
  answering this live", "Ana Calin is answering this live").
- **Clear for a 40-year-old at a glance.** A clever idea that needs decoding is rejected; simplify until the point reads
  in one look. Sean: "i like the idea but isnt it too confusing especially for a 40 yr old".
- **Everyday words, with the technical name small.** Write questions the way a person asks them ("How many hours does
  each buyer take?"), the technical term in small letters under it, and a plain example below. Sean: "Try to use
  language that's a little bit easier to understand, with more explanation. Don't assume that they already know what
  we mean here."
- **Warm, never a jab.** No line that mocks the visitor. Cut on Ana's VIP page: "Less than the course you bought in
  March and never opened".
- **Never assume an audience.** Copy must not suppose the visitor already has readers or followers. Ana: "You don't
  need a newsletter, an audience or an idea ready." A VIP line "Send it to your readers" became "Put it in front of
  potential buyers and learn from the response."
- **Speak to the edge audiences too**, in one short note each, not a separate page. Ana: "Already self-employed?" and
  "Been to one of my workshops before?" under the hero.
- **Name the reader's pain in their words, from real messages.** Use real student messages to find the true objection
  and answer it in the host's voice, tied to a real fact about the host. Ana: a student's worry that success would be
  "eating me up alive" led to "You want more money. You'd also like some life left to enjoy it." with "I run my
  newsletter business in about two hours a day." (Oct 31 copy; the current page carries the two-hours fact in the host
  story.)
- **Do not add a teaching topic the host has not confirmed.** Answer a pain as an objection (a fit-check row, one
  hero or context line) and check with the client before promising it. Open: Claude proposed a fit-check row "You
  don't have many readers yet, and growing feels slow." for Ana; no answer yet.
- **Ana only:** no exclamation marks in her own lines, no em dashes. The visitor's own button voice may use one where
  Sean's copy does ("See you live, Ana!", "I want out by 2027!"), and students' quotes keep theirs.

## 3. No hype, no false promises

- **No countdown pressure, no slashed prices, no invented per-item values, no fake scarcity.** A deadline is explained
  with its real reason. Ana `/join/` receipt items read "Included", no dollar value per item; doors close because the
  group starts together.
- **Hide a block whose facts are missing** rather than invent them.
- **Never promise what isn't offered.** No promised sales, income, leaving date or personal review for everyone. Ana
  registration FAQ: "I can't promise a leaving date." and "I'll review selected attendees' work during the live
  teaching sessions. I won't be able to review everyone's." VIP: Sean's Nov 1 handoff, "Do not promise an individual
  review for every buyer." So: "selected submissions", "a personal review isn't guaranteed".
- **No fake status:** no progress percentages, temporary seat-hold warnings, green success badges ("Ready to leave",
  "you have enough readers") or probability scores. Label figures plainly: Example, Your estimate, Recorded result.
  Never call an assumed rate normal, safe, cautious or expected. Ana's gift line: "Planning estimates based on the
  figures you enter."
- **Free-event pages never mention replays and never pitch the paid program.** Ana's registration page has no
  "replay" and no "my program". The FAQ may say, honestly and once, that an upgrade and a way to continue exist (Ana:
  "After you register, there's an optional VIP upgrade for lifetime access to the recordings and extra support. During
  the event, I'll also explain how you can continue working with me.").
- **Tools tied to the event** (calculators, surveys) use the configured dates in the visitor's time zone; after the
  event, swap reminder copy for an update prompt, never an expired countdown; no internal method names, no program
  mention, no replay message.
- **Show a zero amount as "$0"**, never "-$0".

## 4. Mechanics: punctuation, case, numbers, breaks

- **No em dashes, no en dashes** anywhere in copy. Ranges: "Dec 8 to 10", "Tue Dec 8 to Thu Dec 10". Ana's pages have
  0 em dashes. The one en dash left on the registration page is inside the Google Calendar replica
  (between "12:00" and "1:30pm"), because it copies the real app's UI.
- **Case:**
  - The hero H1 follows Sean's copy doc, which writes it in title case. Ana: "My Newsletter Business Has Made $1.4M.
    Here's What I'd Do First If I Wanted to Leave My Job in 2027."
  - Section headlines, labels, buttons, eyebrows and the sticky header line are sentence case. Ana: "Here's what we'll
    work through together.", "The Exit Plan · A free 3-day live event with Ana Calin" (switched from capitals to sentence
    case so it fits one line). Small eyebrows may be set in capitals by CSS; the source text stays sentence case.
- **Numerals in brackets after key counts:** word, then the numeral in brackets, kept on one line (Ana
  `<span class="nn">three (3)</span>`). Sean: "make it three (3) just for them to visualize the number 3, not just as a
  word also, anywhere where we say a number, not everything, but you can do this in the most appropriate cases."
  - Ana uses it in: "Join me for three (3) free, live sessions", "Come to all three (3).", "My first workshop sold two
    (2) copies.", "about two (2) hours of work a day", "answer seven (7) quick questions", "All three (3) live sessions
    are free", "Five (5) people will win a 1:1 session with me."
  - Not in: student quotes ("Three emails, launched the same week."), buttons that already have brackets ("I'm in for
    all three (free)"), short labels, minor counts ("one question", "five platforms").
  - Short UI lines use the numeral alone: "Join me for all 3 days (for free).", "3 days live with me".
- **Day labels in numerals:** Day 1, Day 2, Day 3.
- **Dates and times:** weekday never standing alone where the date matters; time with the host's anchor city:
  "12:00 pm New York", "7:00 pm Greece", deadlines "Tue, Dec 8, 11:59 pm New York". Visitor-city rules are in
  [ui-kit.md](ui-kit.md) section 15.
- **No automatic hyphens.** Auto-hyphens split a word inside a highlight ("review" broke inside the yellow mark). Ana:
  justified paragraphs use `hyphens:manual`.
- **No orphans.** No one-word line under a button or in small print (a lone "you" under the form button was fixed).
  Balance short wrapped lines (`text-wrap:balance`) and keep phrases whole with nowrap spans (Ana `.nn`, `.nw`). Full
  line-break rules: [ui-kit.md](ui-kit.md) section 16 and [layout-type-spacing.md](layout-type-spacing.md).
- **Do not crowd coloured emphasis text;** fix breaks line by line. Sean: "whats going on the pink text is overcroded" /
  "fix per line".

- **A new copy doc replaces only what it covers.** Keep every text it leaves out: labels, descriptions, proof lines,
  extra reviews (Sean, Nov 9: "keep those texts... Justin Welsh, solo business, the co-founder of Substack"). Format it
  to this file (sentence-case headings, "Dec 8 to 10 · 12:00 pm New York"), and bold the line to read first in each
  block so the page reads in a skim.

- **New copy is a layout job, not a text swap** (Sean, Nov 10: "make sure you're not just replacing the text... balanced,
  rightly placed"). After a copy change, check every changed block at desktop and phone: headline lines even (no lone
  last line), long runs grouped (a list inside a sentence becomes a ticked list, the closing line joins its paragraph),
  new sections given their own designed visual, never a generic placeholder.

- **A logo for a client's tool starts from the client's own mark** (Sean, Nov 10, three passes on Ana's Offer Flow: a generic
  app-icon tile was "nope"; her own smiling sunflower as the O of "Offer" worked). Her fonts, her handwriting, her colours.

## 5. Emphasis: bold, highlights, the promise line

- **Skimmable pages:** the key sentence in a block gets bold plus a soft marker sweep, and a related sentence nearby can
  be bold too (never highlight alone). One highlight per paragraph at most. Ana `mark.sk`: ink text, weight 700, a
  sunflower band `rgba(255,212,0,.6)` from 52% to 94% of the line height, drawn on as it scrolls in; 12 on the
  registration page, 9 on VIP.
- **Keep it subtle.** Sean, after the first publish: "make the highlight a bit subtler".
- **Pick the words that make people opt in:** free, the dates, the outcome, the proof numbers. Ana: "Join me for
  **three (3) free, live sessions**"; "about **80,000 people**", "**$1.4M**", "**I've never taken a sales call.**";
  highlighted "I want you to start finding out what your experience could earn while your current work still pays the
  bills."
- **Headline highlights:** the key words get a yellow highlighter mark behind dark text, not coloured text. Ana H1:
  `$1.4M` (`.hl`), "I'd Do First" and "to Leave" (`.m`), "in 2027" (`em`).
- **A one-line promise from the host inside a section** is bold sans serif in the page pink, with a minimum size on
  phones. Sean: "make this sans serif. I'll review selected ideas live and show you what I'd change." Ana
  `.bring h2.bring-h .l2 em`: `var(--sans)`, weight 700, `clamp(18px,1.45vw,21px)`, `var(--pink)` (#F72585), max
  26ch.
- **Small accent-coloured text on a light ground** uses a darker shade of the accent so it stays readable (Ana: dark
  gold for small labels; the VIP quote byline `#B0124F`).

## 6. Naming and labels

- **One name per thing, everywhere.** Group vs community vs channel: pick one per thing and use it on every page, and
  say truthfully where a gift lives and how it unlocks. Ana: the free "WhatsApp community" ("Free or VIP, join my
  WhatsApp community on the next page for workshop reminders. You'll also find the next steps for getting your exit
  number there."), the VIP "Private WhatsApp group with me".
- **No unexplained internal labels.** Sean on the offer page: "Why is it called round one?" Say plainly it is a first
  round, but keep "Round 1" only where dates matter (the line under the headline, the receipt title, the deadline
  section); elsewhere use the program name (Ana timeline row: "Join The Exit Lab"). A round number invites people to wait for the next round. Still to do: Ana's `/program/` and `/join/` still show "Round 1" in many body lines; audit them
  against this rule.
- **Define a coined term on first use,** before it appears in a price box.
- **A cute label is used once at most, as a heading;** lists and tables use the plain words. Ana: "Me, in your pocket"
  appeared four times; tables now say "Private WhatsApp group with me".
- **Never tell the same point twice on one page.** When new copy goes in, reword older lines that repeat it, and check
  every A/B headline variant against the lines under it (a variant that repeats skips the duplicate sentence). Ana:
  the "$97" story in "Your week" was reworded. Open: the fix for the second VIP headline variant ("Most people stop on
  Thursday and wait to feel ready") was saved but not confirmed published.
- **Unclear availability wording is confirmed with the client before shipping.** Open: Ana's "one morning slot" (one
  per day or one in total?) still appears twice on the VIP page.
- **No privacy caveats as annotations.** Sean: "Can you also remove the "group members can see each other's phone
  numbers" example annotation?" and later: remove "Other members can see your name and number, the way any WhatsApp
  group works." Neither line is on the VIP page now.

## 7. Buttons: wording

Looks, states, the brand graphic and the hover are in [ui-kit.md](ui-kit.md) section 11. The copy rules:

- **Outcome-led, first person, in the visitor's voice,** about what they get. Never "Join now". Never a phrase that
  belongs to another page's action. Sean on the offer page: "also why is it "save my seat"". "Save my seat" wording
  belongs only to the free registration.
- **Each placement gets its own wording,** tied to the section it closes; often addressed to the host by first name.
  The last button addresses the host ("See you live, Ana!").
- **A long form for page buttons, a short form (about 16 characters) for the header and bars.** Labels fit one line on
  phones.
- **Free pages: say free on every sign-up button,** in the label or in a micro line right under it, worded per section.
  Header, form and bottom bar carry it in the label itself. Sean: "Don't remove for free." (when Claude dropped "(it's
  free)" to narrow the sticky bar; it was kept by tightening other parts). Sean asked on Nov 4: "Should we say "free"
  on all buttons so they won't forget that it's free, so they will always be reminded?" Decision (in
  [ui-kit.md](ui-kit.md) section 11): yes.
- **The free tail is smaller than the action words** (Fladlien: the biggest words are the most important). Ana
  `small.bq`: `.8em`, weight 600, opacity .85.
- **Paid buttons show the price in brackets on every one, never "free".** Same label on every main buy button; each
  section CTA worded for its section.
- **Decline links are warm and keep the free seat:** frame the free path as fine, end with a see-you line and an arrow;
  never guilt or scolding. A "No thanks" under each section CTA is worded for that section.
- **Situation buttons follow the visitor's choice** (Ana `SITGO`).
- **Hidden content needs a button that says what they get.** Sean: "How do I get this section? I am only getting a very
  short one." Ana confirmation: "See my plan at $50 / $150 / $500" and a prompt "Pick a price to see your plan." Never a
  vague "Explore this price".
- **Equal options:** never mark one best, recommended, easiest or most profitable.
- **Before doors open, a click shows a short note with the date,** never a greyed button. Sean: "dont grey out any
  button." Ana offer pages: "Doors open Wed Dec 9, live on Day 2."; after close: "Doors are closed. Thank you."
- **Test discount codes never appear in page copy or links.** Sean: "The discount codes don't apply. These are for
  testing, so we can test the payment gates." (Ana: ExitPlan99 and ExitPlan100 removed.)

### Ana's button sets (verbatim from the code)

**Registration (`index.html`)**, every one opens the popup:

| where | label | micro line under it |
|---|---|---|
| header, form, popup, phone bar | I'm in, Ana (it's free) | none |
| hero booking card, "who" section | I want my exit plan, free | none |
| Day 1 (`data-cta="day1"`) | Show me where to start (it's free) | free · live on Zoom |
| Day 2 | Help me choose what to sell (it's free) | free · live on Zoom |
| Day 3 | Show me the path (it's free) | free · live on Zoom |
| after the days | I'm in for all three (free) | none |
| situation picker (`SITGO`) | job: I want out by 2027! · self: I want to get paid for what I know · both or default: I want the plan | free · live on Zoom |
| host | Show me your numbers, Ana (free) | free · live on Zoom |
| why live | I'll bring mine (it's free) | free · live on Zoom |
| gift | Save my seat and get my number | your exit number comes after you register |
| fit check (after the first tap) | That's me. I'm in. | Free · 3 days live |
| reviews | I want to see the work (it's free) | free · live on Zoom |
| prize | Save my seat for the draw (free) | free · live on Zoom |
| FAQ | Questions answered. I'm in (free) | free · live on Zoom |
| recap | Yes, I'm coming, free | none |
| final | See you live, Ana! | Free · Live on Zoom |

**VIP (`vip/index.html`)**: header "Add VIP $67"; hero and letter "I want VIP, Ana ($67)" (phone bar "I want VIP,
Ana"); table "Give me the VIP column ($67)"; Q&A "Bring my offer to Friday's Q&A ($67)"; chat "Let me ask you in the
VIP chat ($67)"; course "Get the Sprint with VIP ($67)"; recordings "Keep the workshop for life ($67)"; fit check "Yes,
pull my chair closer ($67)"; questions "Questions answered. Add VIP ($67)". Under each: "One payment of $67, added to
your free seat." Declines: "Coming to see what it's like? Keep your free seat. Either way, see you Tuesday →" (hero and
letter), then per section "No thanks, the free seat is enough for me", "No thanks, I'll work on my offer on my own",
"No thanks, I'll keep my questions for the live sessions", "No thanks, I'll skip the course", "No thanks, I'll catch it
live", "No thanks, the free seat suits me", "No thanks, keep my free seat". The decline flow itself is protected
([vip-page.md](vip-page.md) section 13).

**Offer pages:** `/program/` "Start my first paid offer", header "Start my offer"; `/join/` "Start my first paid offer,
$850 today" (switches to "$1,500" on pay in full), pill "Start my offer".

## 8. Proof: wording and labels

How proof looks (raw screenshots, cards, walls) is in [registration-page.md](registration-page.md) sections 8 and 14.
The copy rules:

- **Real, sourced numbers only.** Never invent names, counts, results or quotes (`../SOP.md` E). Numbers whose sources
  conflict stay out (Ana: a 312-subscriber story told as $8,400 and as $1,067 was left out; the prize copy lost its
  "$3,000" value). Unverified or anonymous results are flagged for the client to confirm.
- **Lead with the strongest concrete results.** Sean: "Can you choose better testimonials with better results than
  these?" (52 subscribers was too weak as a lead). Keep the strong figures as the big numbers, and do not swap them for
  weaker ones just because the weaker ones have screenshots. Sean: "Why are those small list testimonials different?
  Where's the 3,000+, 3,200, 2,400? Also, make the text maker show us that these are from the past challenge."
- **Label where proof comes from,** in the host's first person, with a results-vary line under every results block.
  Ana: tag "From people in my past challenge" style captions ("Jill Hart, in my past challenge", "A student in my past
  challenge"), then "Individual experiences from my past challenge. Results vary." Wall: "Individual experiences from my
  earlier teaching and challenge. Results vary." Featured card: "From Jill's experience working with Ana. Individual
  results vary."
- **Raw, not designed.** Use the person's real screenshot or post; when none exists, rebuild the note word for word as
  text or a plain quote and ask the client for the real one. Never drawn mockups as proof. Sean: "make these look more
  like raw testimonials. Are there screenshots for this?"
- **Keep students' original wording,** typos and all (Jill's "because of her advise"; Gustavo's ":)"). Sean's Nov 3
  note: "Keep the existing gallery and original screenshots ... Preserve their original wording."
- **Live counts and names only from the real feed.** Names show only from real sign-ups in the last 3 days (first names
  only); the count replaces the fallback at 50 (`FEED_MIN = 50`). Until then, a true fallback. Ana: "800+ student wins"
  (hero ticket), "800+ wins from my past students" (popup), then "N people registered so far". Never a line that would
  read 0 at launch (the reference's "registered in the last 24 hours" line was left out for that reason).
- **A quote byline is just the name:** small accent capitals after a short rule. No tiny photo, no tag like "in her note
  below". Sean: "also can you change this its so funny". Ana VIP `.pq-by`: 12px, weight 800, `.2em` tracking,
  uppercase, `#B0124F`, a 28px rule before it.
- **Testimonials on a paid page only when the client's copy includes them.** Open: Gustavo's quote was removed from VIP
  because the Nov 1 copy left it out; Sean has not confirmed.
- **Proof of the host's numbers looks like a raw platform screenshot,** compact, with short labels that never cut off,
  no hand-drawn marks on UI replicas. Sean: "I want that to look a little bit more like a raw screenshot instead of
  something like this. It looks Claude-generated if we keep it like that." Ana host card: "Overview / All time / First
  sales 2 / Readers 80K / Revenue $1.4M / Sales calls 0", axis "First workshop" to "Today".
- **A quote says only what the recording or note says.** Take a featured story from the student's own words in the
  transcript; a bigger claim from a post title or a summary stays out. Ana: Marni Battista's "I went from 25 people on
  the wait list to 61 people on the wait list. Pretty much in two days." and "I already paid for my investment." are
  both in the live transcript; the post title's "5x her investment in 7 days" is not, so it was not used. Label where it
  was said: "From Marni's experience in my bootcamp, said live with me. Individual results vary."
- **Credibility lines for people the host has talked with** (collaboration proof): one short line each, the strongest
  fact found on that person's own pages or in their own words, checked. No shaky numbers: when two sources disagree,
  drop the number. Sean: "for micheal why read tens of millions of times" then "first. make sure all of em have the
  best bio here". Ana: "built a $15M solo business" (Justin Welsh's site says one-person business), "photographed the
  Dalai Lama" (Mary Bartnikowski: 725 vs 722 weddings, so no count), "published in TIME, Forbes and HBR" (Michael
  Simmons), "analyzed 75,000 Substack newsletters" (Ciler Demiralp), "board-certified health and wellness coach"
  (Dr. Nicole Pertillar), "Hay House author, coach for 16 years" (Marni Battista). Word them so they never break badly
  (Sean: "fix line").
- **The heading says what the host got from them, not the platform.** Sean: "doesnt have to be on substack, just gotta
  tell ppl she got insights and had a convo from them too". Ana: "People I've sat down with, and learned from." (was
  "I've recorded conversations on my Substack with").
- **A footnote names the source of the host's own figures.** Ana footer: "$1.4M and reader count: my own figures,
  published on howwegrowtoday.com."

## 9. Ana's final registration copy, section by section

Verbatim from `index.html` (Nov 4), with the pattern to reuse. `**` marks bold or highlighted words in the code.

### 9.1 Floating header (`header.fb`)
- "The Exit Plan · A free 3-day live event with Ana Calin · Dec 8 to 10" / "Dec 8 to 10 · 12:00 pm New York";
  countdown label "Starting soon"; button "I'm in, Ana (it's free)".
- Pattern: event name · what it is (free, length, live) · with whom · dates; anchor time and city; short free button.

### 9.2 Proof strip and booking card (`section#hero`)
- Strip: "HOW WE GROW with Ana Calin" · "$1.4M from the newsletter" · "About 80,000 readers" · "0 sales calls".
  Pattern: the brand line, then three hard numbers with two-to-three word labels.
- Booking card: "Free / live on Zoom" · "Join The Exit Plan, free." · "Tue Dec 8 to Thu Dec 10" · "12:00 pm New York /
  7:00 pm Greece" · button "I want my exit plan, free".
- Under it: "You don't need a newsletter, an audience or an idea ready." then two edge notes, bold lead-in plus one
  answer: "**Already self-employed?** Your goal might be to earn without taking on another client. Bring that goal."
  and "**Been to one of my workshops before?** I'll show you which parts of my business I'd build first today, what I'd
  move earlier, and why."

### 9.3 Hero text
- Eyebrow: "The Exit Plan · Free 3-day event live on Zoom".
- H1: "My Newsletter Business Has Made $1.4M. Here's What I'd Do First If I Wanted to Leave My Job in 2027." Pattern:
  the host's hard proof as a pre-headline, then the promise in her voice with the reader's goal and year.
- Lead (`p.hlead`): "I'll show you what I'd sell first, why someone would pay for it when advice is everywhere, and
  where I'd find my first customers." Pattern: three things she will show, in the reader's order of doubt.
- Support: "Join me for **three (3) free, live sessions** to see what AI has changed about the order I'd follow, and
  work out where you could begin with the experience you already have." Then highlighted: "You can start alongside the
  work that pays your bills."
- Form ticket: proof pill "800+ student wins", eyebrow "Free · 3 days live · Dec 8 to 10", heading "Save your free
  seat" + "Join me for all 3 days (for free)."

### 9.4 Opening ("who", `section#who`)
- Partner line (only with a partner ref): "<name> sent you here. Here's who I am."
- H2: "You want to know you could make it on your own." Pattern: the reader's real wish as one statement.
- Lead: "You can be very good at your job and still wonder **what anyone would buy from you directly.**"
- Then: "At work, people rely on your judgement. Friends ask for your help. Then you think about charging for
  something of your own, and suddenly you're back at, "Who would pay me for this?"" / "Imagine having **a customer you
  found yourself.** Then another. Enough experience to start understanding what sells, what it takes to deliver, and
  whether you want more of it." / "That would give you something real to build your next decision around." / "Maybe
  you want to leave your job in 2027. Maybe you want to replace a difficult client or stop depending on one source of
  income."
- Highlighted: "I want you to start finding out what your experience could earn while your current work still pays the
  bills." / "I'll bring examples from my business, including the things that earned very little, and show you what I'd
  take from them if I were starting today."
- Button "I want my exit plan, free"; line "Dec 8 to 10 · 12:00 pm New York / Free and live on Zoom" (elsewhere their
  own line: "Dec 9 to 11 · 1:00 am in Manila / Free and live on Zoom").
- Pattern: pain in their words, a picture of the first win, the range of goals, the host's promise, honesty about her
  own misses.

### 9.5 The three days (`section#days`)
- H2 "Here's what we'll work through together." Lead: "I'll show you where I'd begin, **the decisions I'd make before
  building more,** and what taking this further could look like." Slide wall label: "From my slides for the three
  days". Tracker: "Day 1 Your people / Day 2 What to sell / Day 3 The path".
- **Day pattern** (repeat per day): date tag ("Tuesday, Dec 8" over "12:00 pm New York") · H3 outcome title · italic lede
  question or promise · one or two body lines · 3 to 5 bullets, each a **bold first sentence** plus one explaining
  sentence in "I'd" voice · "You'll leave knowing / with" outcome line · a "next" line that sets up the next day ·
  section button + "free · live on Zoom" · slide window "LIVE Day N · Ana is sharing her slides".
- Day 1 "Find the people your business could serve." Lede "Where I'd find my first audience if nobody knew my name."
  Bullets: "**The topic inside your topic.** ...", "**Where I'd look for my first readers or followers.** ...", "**The
  responses I'd pay attention to before choosing a business direction.** ..." Out: "You'll leave knowing whom you want
  to reach, what you want to be known for, and where to start finding those people." Next: "Then comes the question
  that makes Day 2 matter: **what could you sell that makes this worth building?**"
- Day 2 "Find the part of what you know that could become your business." Lede "What I'd sell first, and what I'd need
  to know before giving it my evenings." Five bullets (what someone has a reason to buy when AI gives information for
  free; which idea gets my time first; what to know before trusting "people seem interested."; what the price means
  for the business; the step I'd move earlier now that AI has changed the work). Out: "You'll leave with a direction
  for what to sell, the result someone would buy it for, and a starting price. ..." Next: "If you've worked on an offer
  with me before, bring it. ..."
- Day 3 "See the path from your first customers to a business of your own." Lede "What would have to happen for this
  to become income you could start making plans around?" Out: "Come with the business you're starting to picture. See
  what taking it further would involve."
- Close: "Come to all three (3). Give yourself time to work through the decisions and see how they fit your
  situation." + "I'm in for all three (free)".

### 9.6 Featured result and results trio (inside `section#days`)
- Featured (`.jill`): ""I was able to monetize a 300ish audience and make over $3K in a month."" · "Jill Hart · World
  Changer" · "Jill said Ana helped her "sort out what was important and where to focus."" · "From Jill's experience
  working with Ana. Individual results vary." Her Substack note is shown word for word.
- Cards: "$3,000+ in a month, from about 300 readers" (Jill Hart, in my past challenge); "$3,200 from 547 subscribers"
  ("First launch ever. Three emails, launched the same week." A student in my past challenge); "$2,400 from 198
  subscribers" ("She almost didn't start because she thought 198 subscribers wasn't enough. It was." A student in my
  past challenge). Footer: "Individual experiences from my past challenge. Results vary."
- Pattern: big number + "from N readers/subscribers" (small lists make it believable), one-line story, source label.

### 9.7 Situation picker (`section#where`)
- Eyebrow "Where are you right now?" H2 "What would you like to change about work?"
- Chips: "**I have a job.** I want **leaving to become a choice I can afford.**" / "I work for myself. I want more
  income without filling every available hour with client work." / "A bit of both. I want to choose one business
  direction instead of squeezing more work around everything else."
- Pattern: "I + situation" then "I want + the change", in the reader's words; the button follows the choice.

### 9.8 Host story (`section#host`)
- H2 "I'm Ana. My first workshop sold two (2) copies." Big line: "I'd built what I wanted to teach instead of what my
  readers kept asking me for." Hand line: "A whole stadium, and I forgot to sell tickets. Or hot dogs."
- Facts: "Today, about **80,000 people** read my newsletter, How We Grow. The business has made **$1.4M** selling
  workshops and programs, and **I've never taken a sales call.**" / "I run it from a village in Greece, on about two (2)
  hours of work a day. It took work to get here."
- Highlighted question: "For this event, I'm asking a practical question: what would I do with everything I know now if
  I still had a job and nobody knew my name?" Then "Some decisions I'd repeat. Some I'd make much earlier. AI has changed
  the order I'd follow, too." / "I'll bring my own examples and explain the choices behind them, ..."
- "People I've sat down with, and learned from.": name, then one checked fact each: "Justin Welsh / built a $15M solo
  business", "Mary Bartnikowski / photographed the Dalai Lama", "Michael Simmons / published in TIME, Forbes and
  HBR", "Ciler Demiralp / analyzed 75,000 Substack newsletters", "Dr. Nicole Pertillar / board-certified health and
  wellness coach", "Marni Battista / Hay House author, coach for 16 years". Pattern: no platform, no links; the
  strongest fact from each person's own pages (section 8).
- Pattern: open on a small failure, then today's hard numbers, then why this event asks a new question.

### 9.9 Why attend live (`section#bring`)
- Eyebrow "Why attend live?" H2 "Bring your business idea." + pink sans promise "I'll review selected ideas live and
  show you what I'd change."
- Three objections in quotes ("What if I have two completely different ideas?" ...), then "Bring those questions."
- "During the teaching sessions, you'll have time to work on your own direction. I'll review selected attendees' work
  on screen and explain what I'd keep, what I'd question, and what I'd change." / "Even when it's someone else's work,
  you'll see how I make the decision." / bold: "Come with the part you haven't figured out. You don't need to tidy it
  up for me first."
- Pattern: why live beats a recording, with an honest limit ("selected").

### 9.10 The gift (`section#gift`)
- Eyebrow "Your gift: the exit number". H2 "How many sales would you need to reach your monthly income goal?"
- "Perhaps you want to replace one client. Cover your bills. Eventually, match your salary." / "After you register,
  answer seven (7) quick questions to get your exit-number calculator." / what to do with it / "Bring those numbers to
  Day 2. ..." / "Come back and adjust the numbers as your idea develops. That's what it's there for."
- Honest label: "Planning estimates based on the figures you enter." Lock: "The full calculator opens after you
  register". Button "Save my seat and get my number" + "your exit number comes after you register".
- Pattern: the question the gift answers, how to unlock it (with the count), when it is used in the event.

### 9.11 Fit check (`section.fit`)
- Eyebrow "Is this for you?" H2 "Wherever you're starting, bring that." Tip "Tap the ones that sound like you."
- Rows: a quoted worry in the reader's words + one answer naming the day that covers it. ""I know my subject. I don't
  know what anyone would buy from me."" / "Day 2 is where we look at what someone could pay you to help them do." (and
  four more, ending with ""I've already worked on an offer with Ana."").
- Button "That's me. I'm in." + "Free · 3 days live".

### 9.12 Reviews and wins (`section#reviews`)
- H2 "Here's what students say about learning with me." Sub "These are their words, from previous workshops and
  programs."
- Featured: ""I went from 25 people on the wait list to 61 people on the wait list. Pretty much in two days."" · "Marni
  Battista · coach for 16 years, Unscripted on Substack" · "After my bootcamp, she ran her offer through the template,
  and we worked on it together. A week later: "I already paid for my investment."" · "From Marni's experience in my
  bootcamp, said live with me. Individual results vary." · frame caption "Live on Substack with Marni".
- Gallery heading "From readers and students who've worked with me", reviews verbatim; "show all reviews". Wins wall
  short labels ("27 → 88 in 15 days", "+3 paid in week 1", "Raised her price", ...), "show all 9 wins", and "Individual
  experiences from my earlier teaching and challenge. Results vary."

### 9.13 Prize draw (`section.prize`)
- H2 "Five (5) people will win **a 1:1 session with me.**" Lead "Bring the idea you're considering, the decision you're
  stuck on, or the question you'd like more time to discuss." / "We'll have a private session to work through it
  together." / "I'll draw five names at random from the people still attending live at the end of Day 3." / "Free to
  enter. Stay until the end to be included in the draw."
- Pattern: who, how they are picked, the honest rule; no dollar value.

### 9.14 FAQ (`section#faq`)
- H2 "A few things you might be wondering." Questions in the reader's words: "Is it really free?", "Do I need an
  audience or something ready to sell?", "Is this only about newsletters or Substack?", "What will I have by the end?",
  "I've attended one of your workshops before. Should I come again?", "How much time do I need?", "What if my subject
  has nothing to do with business?", "Will you review my idea personally?", "Will I be able to leave my job in 2027?"
- Answers start with a plain Yes / No / That's fine, then the honest detail ("Each live session is about 90 minutes",
  "short preparation tasks before the event, about 15 minutes each", "I can't promise a leaving date.").

### 9.15 Recap (`section.sum`)
- H2 "What could you build alongside the work you do now?" Big: "I'll show you what I'd take from my **$1.4M newsletter
  business** if I were starting again: what I'd sell first, where I'd look for customers, and what AI has changed about
  the order." / "Bring your experience. ..." / highlighted "You can work towards having a choice about your job before
  you're ready to leave it."
- Recap tags "Day 1 · your people / Day 2 · what to sell / Day 3 · the path"; "The Exit Plan · Dec 8 to 10 / Three live
  sessions · About 90 minutes each · Free on Zoom"; button "Yes, I'm coming, free". Elsewhere: "The Exit Plan · Dec 9
  to 11" / "Three live sessions · 1:00 am in Manila · About 90 minutes each · Free on Zoom".

### 9.16 Final invitation (`section#final`)
- H2 "See you live." Lines: "Bring the idea you keep coming back to, or come with your experience and no idea what to do
  with it yet." / "You don't need to figure that out before joining. That's part of what we'll work on."
- Times: "Tue Dec 8 to Thu Dec 10" then "12:00 pm if you're in New York", "9:00 am if you're in Los Angeles", "5:00 pm if
  you're in London", "7:00 pm if you're in Greece". Button "See you live, Ana!" + "Free · Live on Zoom".
- Elsewhere: their own row first and highlighted ("1:00 am if you're in Manila"), the date line "Wed Dec 9 to Fri Dec
  11" with "Tue Dec 8 to Thu Dec 10 New York" beside it, then "Also:" with the other cities ("12:00 pm New York",
  "9:00 am Los Angeles", ...).

### 9.17 Popup, form and exit popup
- Eyebrow "FREE · 3 DAYS LIVE · DEC 8 TO 10"; H3 "Save your free seat."; sub "Join me for all 3 days (for free).";
  proof "800+ wins from my past students"; "Seat reserved for you" (fills with the first name); fields "First name",
  "Email"; errors "add your first name", "Almost. Check that email once more."; button "I'm in, Ana (it's free)";
  ticks "Free / 3 days live with me / Come as you are"; meta "12:00 pm New York · About 90 minutes a session"; note
  "You'll get emails from me, including event details and reminders. Unsubscribe anytime."; sign-off "See you there,
  Ana"; thanks "Your seat is saved." / "See you Tuesday, Dec 8." (their own weekday and date elsewhere).
- Exit popup: "Don't go yet. *Your seat's still here.*" / "Put your name on it before you go. It's free."
- Pattern: friendly errors in her voice, the honest email note, the anchor time and length.

## 10. Ana's final VIP copy, section by section

Verbatim from `vip/index.html`, from Sean's full VIP page copy of Nov 1, 2026, plus the additions Sean asked for. Layout and story: [vip-page.md](vip-page.md).

- **Header:** strip "Don't close this page. Your registration isn't finished yet."; "Free 3-day live workshop" / "The
  Exit Plan" / "Dec 8 to 10"; steps "Seat saved / VIP upgrade / Join details", "STEP 2 OF 3"; button "Add VIP $67".
- **Hero:** eyebrow "Your free seat is saved. One more thing before you go"; spam warning "!Important: check your Spam
  and Promotions folders. Your confirmation is on its way from anacalin@howwegrowtoday.com. If it's there, tap "Not
  spam" or move it to your inbox, or you'll miss your Zoom link and reminders."
- **H1:** "Keep the workshop for life, and work through the hard parts with me." (A/B variant B: "Get my help putting
  this to work, and keep every lesson for life.") Sub: "You've saved your free seat. For $67, add lifetime workshop
  recordings, a live VIP Q&A and group review, private WhatsApp access to me during the workshop, and my Offer Clarity
  Sprint course." Pattern: what they keep + the help they get; the sub names the price once and every part.
- **Under the video:** "A minute with me before you decide. Here's what VIP adds to your free seat." H2 "Use what you
  learn to work toward your first sales", three items with a bold verb lead ("Keep the teaching beside you.", "Ask me
  while you're working on it.", "See what I'd change before someone buys."), then "You also keep my Offer Clarity Sprint
  course. ..."
- **Order card:** "VIP · one payment", "$67", H2 "Get the full VIP package.", four plain items ("Lifetime recordings,
  all three workshop sessions", "Live VIP Q&A and review with me, 90 minutes, plus the recording", "Private WhatsApp
  access to me, Dec 8 to 11", "The Offer Clarity Sprint course, yours to keep"), "On sale until Tue, Dec 8, 11:59 pm New
  York", "Total today $67.00", button, "Live review covers selected submissions. Secure checkout with Stripe. All sales
  are final.", decline link; closed state "VIP is closed. See you live."
- **Your week:** "Your week, Dec 8 to 11", H2 "Work toward the sale that makes this feel possible.", body explaining
  VIP as the step after the free days ("The workshop helps you work toward that. VIP gives you the lessons to revisit
  and access to me while you put them to use."). Days: "Find what you could sell and who could buy." / "Give people a
  reason to pay your price." / "Get ready to invite people to buy." / Fri "See what I'd improve in selected
  submissions." / "Keep going" / "Put it in front of potential buyers and learn from the response."
- **Free vs VIP table:** "Your free seat and VIP, side by side"; plain row names with a small detail line ("VIP Q&A and
  group review with me / Your questions, selected submissions · 90 minutes · Dec 11"); "no" or a tick. Note: "Free or
  VIP, join my WhatsApp community on the next page for workshop reminders. ..."
- **What's in VIP:** H2 "Help while you do it. The lessons to come back to." Each item: number, H3 in her voice, a meta
  line with date and length, a story paragraph, a short list, an honest limit, CTA, decline.
  - 01 "Let's look at it the way a buyer would." · "Fri, Dec 11 · 90 minutes · VIPs only" · limit "I'll cover as many
    submissions as fit into 90 minutes; a personal review isn't guaranteed. You can submit ahead if you can't attend,
    and everyone gets the recording."
  - 02 "Ask me while the question is in front of you." · "Dec 8 to Dec 11 · Ana in the chat" · "I'll be there for 30
    minutes after each workshop session, plus one morning slot. The free community has your reminders. This separate
    group is where we talk about the work."
  - 03 "The Offer Clarity Sprint." · "Bonus · yours to keep" · "You don't have to finish another course before the
    workshop. Already own the Sprint? Bring the work you've started."
  - 04 "The workshop is yours to keep for life." · "Lifetime access · all three sessions in full" · "Your recordings ·
    access expires: never".
- **Demo lines written for Ana (open, awaiting her OK):** WhatsApp: "Morning, VIPs. I'm here for the next 30 minutes.
  Send me what you're working on", visitor "Do I need more subscribers before I sell anything? I only have 212", Ana
  "No. Start with the 212 who already read you", "Post your one sentence here and I'll help you tighten it", visitor
  "Posting it now. Thank you!!". Zoom Q&A: "Is $149 too much for my first workshop?", "Where should the price go in my
  email?", "What if nobody replies to my first email?", "Can I start selling before my offer is finished?"
- **Pull quote and fit check:** ""That first customer matters. It gives you something to learn from, improve and sell
  again."" · ANA CALIN. Eyebrow "Honest fit check", H2 "Would you like me a little closer while you do this?", "Get VIP
  if" (three) vs "Keep the free seat if" (three, said kindly: "You'd prefer to work through your questions
  independently."), then "You don't need an idea or subscribers ready today. Start with the workshop and bring the
  questions that come up."
- **Letter beside the price:** "A note from Ana": "I want you to find out whether people will pay for what you know,
  while you still have the income you rely on." / "That first customer matters. ..." / "That's what VIP is for. ..." ·
  signed "Ana". Price box: "Get the full VIP package for one payment of $67.", the four items, "Lifetime access to the
  workshop recordings. Support while you put the teaching to use.", "Secure checkout with Stripe. All sales are final.
  On sale until Tue, Dec 8 at 11:59 pm New York."
- **Questions:** "Do I need VIP to come live?" ("No. Your free seat includes the full three-day live workshop. ..."),
  "Will you review everyone's work?", "What if I'm just starting?", "Do I keep the recordings?", "I already own the
  Sprint. Is VIP still useful?", "When is the Friday VIP Q&A?", "What happens in the VIP WhatsApp group?", "What if I
  can't make it on Friday?", "Can I get a refund?" ("No. All sales are final. Please check what's included and the
  group-review format before you buy.").
- **Decline popups:** "Wait, before you go." / "Your VIP spot for Friday, Dec 11 is still open." ... "No thanks, Ana.
  I'll do the three days on my own and decide when I'm ready. Take me to my join details." Then "Are you sure?" / "Your
  free seat stays saved either way." / "Yes, I'm sure. Take me to the free version."

## 11. Confirmation pages (`confirmed/`, `vip-confirmed/`)

- **Top:** H1 = seat saved + number of quick steps: "Your seat is saved. Four quick steps before you go." (VIP: "You're
  VIP[, first]. Four quick steps before you go.", lead "Your receipt is in your email. Join the VIP WhatsApp group,
  move my emails to your inbox, add all four days to your calendar, then answer seven quick questions. Your answers
  power your exit number calculator."). Lead lists the steps in order and what the last one powers: "Join my
  WhatsApp group, move my emails to your inbox, add the three days to your calendar, then answer seven quick
  questions. Your answers power your exit number calculator." Ana's video-script ideas were tried at the top and
  reverted. Sean: "ok i like the before".
- **"Do this now"** above the steps: "Do this now If you only have a minute, do the first one."
- **One plain reason per step card, in the host's voice:** WhatsApp "That's where my reminders go, so you don't miss
  Tuesday." · email "Then find my welcome email (subject: "You're in.") and reply with one word: in. That one word makes
  sure the Day 1 link reaches you." · calendar "Treat it like a meeting you can't move."
- **Survey:** say how many questions, what they unlock, why it stays locked, the effort. H2 "Answer 7 quick questions
  to unlock your exit number calculator." Lead "Your exit number: my calculator that shows the sales, audience and
  hours behind your income goal. It opens when all seven are in. All taps, about a minute."
- **"Come live!"** asks directly, no "if you can": "Live is where I fix people's work on screen. Yours could be one of
  them. Most people who sign up for a free workshop never come live, and the ones who do are the ones who leave with
  something written." Then "Bring a laptop, a pen and your Head start page, and close the door."
- **Still to do:** the regular confirmation page still carries claims the registration page dropped: "If you miss a
  day, its replay stays up for 48 hours.", "At the end I show my program, and you can leave before it.", the 1:1
  "worth $3,000" and "$3,000" prize tickets, and "Treat it like a flight you can't move." Check them with Sean against
  the no-replays, no-program-pitch and no-unverified-value rules (section 3).

## 12. Still to do and open (copy)

- **Open:** the VIP decline popup still uses older copy that the Nov 1 page dropped: "Your ready check, live with me",
  "Me, in your pocket for four days", "Yes, check mine on Friday ($67)", and "the Friday where I tell you, live, whether
  your offer is ready to sell" (close to promising a personal review). Ask Sean before touching the protected flow.
- **Open:** "one morning slot" (twice on VIP) to confirm with Ana.
- **Open:** Gustavo's quote on VIP; the Ana-voice demo lines (section 10).
- **Open:** anonymous $3,200 and $2,400 results waiting for Ana's OK; her real screenshots (771-like and 82-like posts,
  the two-sale workshop's sales page) still asked for.
- **Open:** the "audience growth feels slow" objection (section 2).
- **Still to do:** "Round 1" audit on `/program/` and `/join/` (section 6); the leftover VIP labels "Free, for everyone"
  and "From the Offer Clarity Sprint" ([vip-page.md](vip-page.md) section 20).
- **Still to do:** confirmation page claims (section 11).

## 13. Copy checklist before saying done

1. Every line of Sean's newest doc is on the page, word for word; nothing from older copy is left.
2. `grep` finds no em dash and no en dash in copy (UI replicas of real apps excepted), no "replay", no "my program" on
   free pages, no exclamation mark in the host's own lines, no test codes.
3. Every number on the page has a source the client gave; every results block has its results-vary line. Every
   credibility line is found on that person's own pages, with no number whose sources disagree; every featured quote
   is in the recording or note it came from.
3b. Every date and time line has its visitor version (their dates, time and city) and the anchor version.
4. Every sign-up button says free (label or micro line); every paid button shows the price; no button greyed.
5. Host speaks in first person; one name per thing across all pages; no cute label twice; no point told twice.
6. Numerals in brackets on the key counts only; phrases whole at 320 to 1440px; no orphan words; no auto-hyphens.
7. Highlights subtle, one per paragraph, bold with them.
8. When a claim changes, every later page (VIP, confirmation, emails) is checked for the old claim.
9. Corrections logged in `../feedback-log.md` and promoted here (`../SOP.md` D).
