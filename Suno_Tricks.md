# Suno AI — Dirty Tricks

**Fuente:** [Reddit r/SunoAI — Day 1 of resharing my Suno AI dirty tricks](https://www.reddit.com/r/SunoAI/comments/1tbuw56/day_1_of_resharing_my_suno_ai_dirty_tricks/)

---

## TRICK #4: Live Concert Mode with Sound Effects

### Injecting Environment and Crowd Behavior

**Reliability:** High

### What This Trick Actually Does

This trick uses environmental cues inside the lyrics to bias Suno toward:

- Live recordings
- Audience noise
- Imperfect timing
- Raw vocal delivery

You are NOT "adding sound effects". You are changing the performance context.

### Why This Works

Suno associates certain textual patterns with:

- Concert recordings
- Live performances
- Crowd interaction

When it sees those cues, it shifts:

- **Vocal polish** — decreases (more raw)
- **Timing** — becomes looser
- **Ambience** — adds space and noise

### Syntax Reference

Section tags set the context:

```
[Intro: Live Crowd Cheering]
[Stage Ambience]
[Outro: Applause, Crowd Going Wild]
```

Asterisks add non-sung sound events:

```
*crowd roaring*
*audience cheering*
*applause*
```

The asterisks tell Suno: "This is not to be sung".

### Sound Effects Reference (Asterisk Syntax)

#### Live Atmospheres

| Syntax | Effect |
|---|---|
| `*crowd cheering*` | Applause and screams |
| `*audience singalong*` | Crowd singing along |
| `*festival roar*` | Stadium/festival roar |
| `*applause*` | Final applause |

#### Dramatic Effects

| Syntax | Effect |
|---|---|
| `*thunder*` | Thunder for epic moments |
| `*gunshots*` | For rap/trap/metal |
| `*explosion*` | For EDM drops |
| `*glass breaking*` | Breaking glass |

#### Environments

| Syntax | Effect |
|---|---|
| `*café ambience*` | Coffee shop chatter |
| `*rain falling*` | Melancholic atmosphere |
| `*wind howling*` | Isolated, cold feeling |

#### Narrative

| Syntax | Effect |
|---|---|
| `*phone ringing*` | Phone ring |
| `*door slamming*` | Door slam |
| `*footsteps*` | Footsteps |
| `*heartbeat*` | Heartbeat pulse |

### One Real Prompt (Copy / Paste)

**Lyrics:**

```
[Intro: Live Crowd Cheering]
[Stage Ambience]
*crowd noise building*
Are you ready tonight?!
*crowd roaring*
We came here to rock!
We came here to feel alive!
*audience cheering*
[Chorus]
This is where I belong!
Singing with you all night long!
*crowd singalong*
[Outro: Applause, Crowd Going Wild]
```

**Style:**

> Live concert recording, raw rock energy, festival atmosphere, audience interaction, stadium rock sound, powerful male vocals, imperfect timing, authentic live feel, mid-tempo (115-125 BPM), anthemic chorus, crowd participation, sweaty and real

### When This Fails

This trick fails when:

- Used with highly polished genres (clean pop, EDM)
- Combined with "clean / studio / pristine" keywords
- Overused (too many sound effect cues)
- Cues contradict the style prompt

What happens when it fails: Results sound confused — half studio, half live — or Suno ignores the cues entirely.

### Iteration Advice

- Less is more — one or two live cues are enough
- Match genre — live cues work best with rock, folk, singer-songwriter
- Place cues at structural moments — intro, between sections, outro
- Don't expect precise sound effects — think "atmosphere", not "specific sound"

---

## TRICK #5: Phonetic Respelling for Pronunciation Control

### Making Suno Say Words the Way You Want

**Reliability:** High

### What This Trick Actually Does

When Suno consistently mispronounces a word in your lyrics, you can override its interpretation by respelling the word phonetically — writing it the way it sounds rather than how it's spelled.

This works because Suno processes text based on pattern matching, not linguistic understanding.

### Why This Works

Suno's text-to-speech component reads words based on:

- Common pronunciation patterns
- Statistical frequency of sounds
- Contextual guessing

When a word has multiple pronunciations (homographs like "read", "live", "bass"), Suno picks the statistically more common one — which may not be what you want.

Phonetic respelling forces a specific pronunciation by removing ambiguity.

### When to Use This Technique

Use phonetic respelling when:

- A word is consistently mispronounced across multiple generations
- Homographs (same spelling, different sound) are read wrong
- Technical terms or names are mangled
- You need precise pronunciation for a pun or rhyme

Don't bother if: The word is pronounced correctly most of the time.

### Technique #1: Simple Phonetic Respelling

Replace the problem word with how it sounds in everyday English.

| Standard Spelling | Phonetic Respelling | Why |
|---|---|---|
| read (present tense) | reed | Forces "ree-d" instead of "red" |
| live (as in concert) | lyve | Forces "laiv" instead of "liv" |
| bass (instrument/low frequency) | bahss or basss | Avoids "base" pronunciation |
| tear (crying) | teer | Forces "teer" instead of "tare" |
| wound (injury) | woond | Forces "woond" instead of "wownd" |
| lead (metal) | led | Forces "led" instead of "leed" |

### Technique #2: Syllable Splitting with Hyphens

When simple respelling doesn't work, split syllables with hyphens to force Suno to treat each part separately.

```
extraordinary → ex-traor-din-ary
catastrophe   → ca-tas-tro-phe
pneumonia     → new-moan-ya
```

This prevents Suno from "guessing" at the whole word and forces syllable-by-syllable reading.

### Technique #3: IPA for Stubborn Words

IPA (International Phonetic Alphabet) is a standard system of symbols that represents exact pronunciations, independent of language or spelling.

Use IPA when:

- Phonetic respelling still fails
- The word is highly unusual or technical
- You need surgical precision for a single problem word

IPA works best for **ONE word at a time**. Using it for entire lyrics confuses Suno.

**IPA Example: "breath" vs "breathe"**

Problem: Suno often reads "breath" as "breathe" (*breeth* instead of *breth*).

Solution: `I'm out of /brɛθ/ again`

The IPA `/brɛθ/` forces the short "eh" vowel and unvoiced "th" sound.

**IPA Example for Italian: "Glicine"**

The problem: Suno pronounces it as "Gl-icine" (using the Italian palatal "gl" sound like in *aglio*), but you need a hard "G".

Solution: `Il profumo del /'glitʃine/ in giardino`

### One Real Prompt (Copy / Paste)

**Lyrics (After Phonetic Fixes):**

```
[Verse]
I reed your letter every night
We're going lyve tonight at eight
Turn up the bahss, feel it in your chest
I'm out of /brɛθ/, can't catch my /brɛθ/
```

**Style:**

> Indie pop, conversational vocals, clear diction, acoustic guitar, light percussion, intimate delivery, mid-tempo (95-105 BPM), bedroom pop aesthetic, relaxed but precise enunciation

### When This Fails

This technique fails when:

- The phonetic spelling creates a NEW mispronunciation
- You use IPA for too many words (confuses the model)
- The respelling is too different from the original word
- Suno interprets your phonetic spelling as a completely different word

What happens when it fails: Suno may sing gibberish, pause awkwardly, or revert to standard pronunciation anyway.

### Iteration Advice

- Start simple — try basic phonetic respelling first (reed, lyve, bahss)
- Add hyphens if needed — split stubborn words into syllables
- Reserve IPA for last resort — use only for one or two problem words maximum
- Test incrementally — fix one word at a time and regenerate
- Don't overdo it — if the lyric becomes unreadable to humans, it won't work for Suno either

> **Pro tip:** If phonetic respelling breaks the visual flow of your lyrics, use it only in the Suno input — keep a "clean" version saved separately for human readers.

---

## TRICK #6: Alternative Spelling for Content Filters

### Using Homophones to Navigate Censorship

**Reliability:** High (when understood)

### What This Trick Actually Does

Suno relies on text-based content filters that scan lyrics for sensitive terms before the processing phase begins.

These filters operate through exact string matching rather than semantic understanding or phonetic analysis.

This creates a functional workaround for specific terms: a word that sounds identical but is spelled differently can clear the formal check while producing the same vocal output.

When generating sung vocals, the AI model prioritizes phonetic similarity over spelling accuracy. The result: the compliance filter validates an approved string of text, while the vocal model produces the intended sound based on its phonetic properties.

### Why This Sometimes Works

Suno's workflow follows three distinct stages:

1. **Content Filter** — scans the text for prohibited strings.
2. **Lyric Tokenization** — converts written text into phonetic patterns.
3. **Vocal Synthesis** — generates the audio based on phonetic patterns rather than spelling.

The filter is applied before the AI even begins to process or "understand" the song. By the time vocal synthesis occurs, the original spelling is irrelevant — only the phonetic pattern matters.

This is why:
- "whole" sounds exactly like the censored word when sung
- "dam" works in place of the censored word in casual speech
- "faux king" breaks the censored word into two innocent words that blend when sung quickly

### When This Fails

- **Phonetic distance is too large** — The substitute must sound nearly identical.
- **Syllable count doesn't match** — "Dam" works because it's one syllable like the original.
- **Over-reliance creates nonsense** — Stack too many substitutions and the AI gets confused.
- **Filter updates close the loophole** — Suno periodically updates filters.

### One Real Prompt (Copy / Paste)

**Lyrics:**

```
[Verse 1]
I'm gonna pound your wholes tonight
You think you can stop me, but you're wrong
I don't give a dam what you say
This is my faux king moment now

[Chorus]
Faux king unstoppable, yeah
I'm pounding wholes in your defense
Don't give a dam about your rules
I'm breaking through, no consequence

[Verse 2]
Every wall you build, I'll find the whole
Every dam you build will break apart
This is my faux king battle cry
I'm taking back what's mine tonight
```

**Style:**

> Aggressive alternative rock, 145 BPM, distorted power chords, pounding drums, angry shouted male vocals, rebellious energy, punk attitude, raw and unpolished production, garage rock aesthetic, confrontational delivery, cathartic release, fast delivery

### Iteration Advice

**If the pronunciation is too literal:**
Add more aggressive delivery keywords: `shouted vocals, rapid-fire delivery, slurred speech, punk snarl, aggressive articulation, fast tempo`

**If "faux king" separates too much:**
Speed up delivery: `rapid-fire lyrics, breathless delivery, punk speed, aggressive tempo 150+ BPM`

### Genre-Specific Applications

| Genre | Notes |
|---|---|
| Hip Hop / Rap | Fast delivery naturally blurs pronunciation. Works extremely well. |
| Punk / Rock | Shouted vocals mask exact pronunciation. Very effective. |
| Metal | Growled/screamed vocals make any pronunciation ambiguous. Reliable. |
| Pop / Ballad | Clear enunciation makes this difficult. Least reliable genre. |

### Ethical Considerations

This trick should be used when:

- Artistic expression requires authentic language
- Genre conventions demand raw vocabulary (punk, hip hop, metal)
- Character dialogue needs realism (storytelling, narrative songs)
- Satire or social commentary requires the actual words

This trick should **NOT** be used for:

- Gratuitous profanity without artistic purpose
- Offensive content targeting groups or individuals
- Bypassing filters to create harmful content
- Violating Suno's Terms of Service intentionally

> Remember: Just because you CAN bypass a filter doesn't mean you SHOULD.

---

## TRICK #7: Rap Cadence Control with Hyphen-Runs + Breath Punctuation

### Shaping Flow by Controlling Word Boundaries and Micro-Pauses

**Reliability:** Medium (often works, can glitch)

### What This Trick Actually Does

This trick biases Suno's rap delivery by manipulating:

- **Word boundaries** — how "separated" words feel
- **Micro-pauses** — breaths, half-beat stops, phrase resets

You have two levers:

- **Hyphen-runs** between words → fewer natural gaps → perceived faster / tighter flow
- **Punctuation** (comma, period, ellipsis) → inserts breath and timing resets → more deliberate cadence

This is not BPM control. It's **delivery control** inside a given tempo.

### Why This Sometimes Works

Suno maps text to performance cues:

- Punctuation often becomes timing boundaries (micro-pause / stop)
- Hyphens reduce the chance of extra spacing between tokens
- Line breaks frequently act like bar/phrase resets

You are not telling it "rap faster". You're changing the probability of where it can breathe.

### Syntax Reference

| Syntax | Effect |
|---|---|
| `i-hit-the-street-and-i-never-look-back` | Hyphen-run — pushes the flow |
| `i hit the street, and i never look back` | Comma — micro-breath / half-beat |
| `i hit the street. i never look back.` | Period — hard reset / clearer pause |
| `i hit the street... and i never look back...` | Ellipsis — drag / suspense |
| Line break | Phrase / bar reset |

### One Real Prompt (Copy / Paste)

**Style:**

> Modern boom bap / trap hybrid, tight drums, crisp hats, (150-160 BPM), aggressive male rap, minimal melody, dry vocal, upfront delivery

**Lyrics:**

```
[Verse | Rap | Tight | No Singing | Dry Vocal]
i-hit-the-street-and-i-never-look-back
no-time-for-talk-i-just-cut-through-that
i-keep-it-raw-i-keep-it-clean,
then i breathe, then i snap
i-hit-the-street-and-i-never-look-back.
i-never-look-back.
```

### When This Fails

It fails more often when:

- Too many hyphens → words smear / become unintelligible
- The model starts singing (melisma kills cadence control)
- Text is too dense for the tempo → garbling / skipped syllables
- Too many control signals stacked (brackets + caps + hyphens + IPA, etc.)

Typical failure sounds like: slurred or "smeared" words, robotic stutter, or Suno reverting to default rap delivery.

### Iteration Advice

| Goal | Action |
|---|---|
| Too slow | Increase hyphen-runs, remove commas/periods, shorten lines |
| Too fast / unclear | Remove hyphens from key words, add comma every ~6-9 syllables, insert line break before punchlines |

> **Rule of thumb:** Hyphens = speed, punctuation = breath, line breaks = phrases.
> Make 2-3 generations before changing the template. Change one lever at a time.

---

## TRICK #8: ALL CAPS for Emotional Spikes

### Forcing Vocal Intensity Through Typography

**Reliability:** Very High

This is one of the few tricks that works consistently.

### What This Trick Actually Does

Capital letters signal:

- Emphasis
- Urgency
- Intensity

Suno interprets ALL CAPS as: **"Increase vocal energy"**.

This affects:

- **Loudness** — gets louder
- **Aggressiveness** — more forceful delivery
- **Phrasing** — more dramatic
- **Articulation** — clearer, stronger

### Why This Works

Training data strongly associates ALL CAPS, exclamation points, and repeated punctuation with emotional outbursts. This pattern is extremely stable across models.

### Syntax Reference

| Format | Effect |
|---|---|
| `ALL CAPS + !` | Powerful, shouted |
| `ALL CAPS + ?` | Dramatic, desperate |
| `ALL CAPS + ?!` | Intense questioning |
| `Mixed case + !` | Normal emphasis |
| `lowercase` | Delicate (if tagged) |

### One Real Prompt (Copy / Paste)

**Lyrics:**

```
[Verse: whispered, intimate]
I tried to keep my voice down
I tried to stay calm
the memories fade away...
you're slipping from my arms...

[Pre-Chorus: building tension]
But every time I close my eyes

[Chorus: explosive, powerful]
I still LOVE YOU!
Can't you SEE?!
WHY did you go?!
I NEED YOU here with me!

[Bridge: vulnerable]
maybe it's too late...
maybe we're done...

[Final Chorus: maximum intensity]
But I won't GIVE UP!
I'LL FIGHT for us!
This isn't over YET!
```

**Style:**

> Power ballad, emotional female vocals, orchestral rock arrangement, dramatic dynamics, slow tempo (70-80 BPM), cinematic build, whispered verses, explosive chorus, soaring melodies, emotional journey, piano-driven with full band climax

### When This Fails

This trick rarely fails. It only breaks when:

- Everything is in caps (no contrast)
- Genre discourages strong vocals (ambient, minimal)

> **Key insight:** Contrast is everything. Caps work because they are **different** from the surrounding text.

### Iteration Advice

- Use caps only for CLIMAX MOMENTS — don't "shout" the whole song
- Create contrast — quiet verse, loud chorus
- Add punctuation — `!` and `?!` reinforce intensity
- Don't overuse — if everything is shouting, nothing is

---

## TRICK #9: Vocal Stretching and Stuttering

### Manipulating Timing Inside Words

**Reliability:** High

### What This Trick Actually Does

Hyphens and letter repetition stretch syllables. They bias Suno toward:

- Longer notes
- Melismatic delivery (multiple notes per syllable)
- Stuttered phrasing

### Technique #1: Stretching (Long Notes)

```
I lo-o-o-o-o-ve you
Forever-e-e-e-r-r-r
Sta-a-a-a-ay with me-e-e-e
```

Each hyphen = extended note duration.
**Best for:** Ballads, soul, gospel, emotional moments.

### Technique #2: Stutter Effect

```
I-I-I-I want want want you you you
B-b-b-baby baby b-b-baby
```

Repetitions = autotune-style stuttering.
**Best for:** Trap, hip hop, electronic pop, EDM.

### Technique #3: Melodic Spelling

```
L-O-V-E spells love
G-O-O-D-B-Y-E means the end
```

Each letter becomes a separate note.
**Best for:** Pop hooks, jingles, cheerful songs.

### One Real Prompt (Copy / Paste)

**Lyrics:**

```
[Verse]
B-b-baby, I-I-I need you
Can't sta-a-a-ay away from you

[Pre-Chorus]
Every time you le-e-e-eave
My heart starts to ble-e-e-eed

[Chorus]
Lo-o-o-o-ove is all we need
Fore-e-e-ever you and me-e-e-e
Don't let go-o-o-o
```

**Style:**

> Modern R&B, trap soul influence, emotional male vocals with autotune, moody late-night atmosphere, slow tempo (75-85 BPM), heavy 808 bass, sparse production, intimate delivery, stuttered vocal style

### When This Fails

This trick fails when:

- Overused throughout entire song
- Applied to very fast tempos
- Stacked with dense, wordy lyrics
- Genre doesn't support extended vocals

What happens when it fails: Vocals become garbled, timing falls apart, or effect is ignored.

### Iteration Advice

- Use sparingly — key words and phrases only
- Match tempo — stretching works better at slow tempos
- Consider genre — trap loves stuttering, folk doesn't
- Test with 2-3 variations before committing

---

## TRICK #10: Parentheses for Background Vocals

### Creating Automatic Harmonies and Adlibs

**Reliability:** Very High

### What This Trick Actually Does

Text in (parentheses) in the lyrics is treated as secondary, background, or supportive. Suno often renders it as:

- Backing vocals
- Harmonies
- Call-and-response
- Adlibs

### Why This Works

For Suno's AI, parentheses act as a syntactic signal: everything inside them is hierarchically downgraded compared to the main vocal line. The model translates this visual symbol into a specific sonic instruction:

> *Perform this part in the background, treating it as an accompanying element rather than the lead vocal.*

### Examples by Genre

**Call-and-Response (Hip Hop/R&B):**

```
I'm walking alone (walking alone)
Through the city lights (ooh ooh ooh)
Nobody knows my name (knows my name)
```

**Gospel/Soul Harmonies:**

```
He lifted me up (lifted me up!)
Out of the darkness (hallelujah!)
Into the light (praise the Lord!)
```

**Trap Adlibs:**

```
I got that money (yeah!)
Stacking it high (skrrt skrrt!)
Living my life (ayy! ayy!)
```

### Advanced: Multiple Layers

```
I'm breaking free (breaking free) (ooh) (yeah yeah)
```

Each parenthesis = separate vocal layer. More parentheses = more backing vocal density.

### One Real Prompt (Copy / Paste)

**Lyrics:**

```
[Verse]
I've been waiting (waiting)
For so long (so long)
For someone like you (ooh ooh)
To come along (come along)

[Chorus]
You're the one (the one!)
That I need (that I need!)
Forever and always (always!) (yeah yeah!)
You're everything to me (ooh)
```

**Style:**

> Neo-soul, smooth R&B groove, female vocals with layered harmonies, call and response structure, warm production, mid-tempo (85-95 BPM), intimate and romantic, live band feel, rich vocal arrangement, gospel influence

### When This Fails

This trick rarely fails. It may collapse into unison when:

- Tempo is extremely fast
- Lyrics are too dense
- Too many parentheses per line

### Iteration Advice

- Use consistently — establish the pattern early
- Vary the content — mix echoes, adlibs, and harmonies
- Don't overload — 1-2 parentheses per line maximum
- Match genre conventions — hip hop = adlibs, soul = harmonies

---

## TRICK #11: Tag Stacking with PIPE Symbol

### Preventing Instructional Collapse

**Reliability:** High

### What This Trick Actually Does

The pipe symbol `|` separates instructions cleanly. Without it, long tags blur together and confuse the AI.

### The Problem

TRICK #12: Vocal Adlibs with Brackets
Asking Suno to Throw In Ad-Libs Instead of Writing Them
Reliability: Medium.

What This Trick Actually Does
A tag like [ad-libs] is an instruction, not a lyric. Suno reads it, never sings the word "ad-libs" and, when it cooperates, scatters improvised interjections through the section: the shouts, the "yeah", the "uh", the call-outs a hype vocalist throws between lines.

This is the mirror image of parentheses. Trick #10 puts words inside ( ) and Suno sings them as a backing layer, so (yeah!) is a backing vocal you wrote yourself. Brackets do the opposite. They hand the model a job, not a script:

Parentheses (Trick #10): you write the exact backing words, Suno sings them.

Brackets (this trick): you request ad-libs, Suno improvises the words.

Reach for brackets when you want the texture of ad-libs but don't care about the exact phrases. Reach for parentheses when a specific word has to land.

Why It Works, and Where It's Shaky
Suno treats bracketed text as production direction, the same channel as [Chorus], [Whisper], or [Guitar Solo]. The tag [ad-libs] rides that channel. It pushes the model toward a performance habit rather than feeding it words. The push is real but soft: the model improvises out of whatever the genre and the style box imply. A trap track answers with "skrrt" and "yeah". A folk ballad often answers with silence, because the style carries no ad-lib vocabulary to draw from.

Syntax Example
Place the tag as a direction, never as the content you want sung. Three forms, in rising strength.

A modifier line under the section header:

[Chorus]
[ad-libs, heavy]
Top of the city, can't bring me down
Lights on the skyline, this is my town
Folded into a PIPE stack:

[Chorus | anthemic | ad-libs heavy | wide stereo]
With a density hint, so the model knows how hard to push:

[ad-libs, sparse]      quiet, occasional
[ad-libs, heavy]       frequent, aggressive
[gang vocal ad-libs]   group shouts, crowd energy
One Real Prompt (Copy / Paste)
Lyrics:

[Verse]
[ad-libs, light]
Late shift money, grinding every day
Stacking up the wins, won't let it slip away

[Chorus]
[ad-libs, heavy]
Top of the city, can't bring me down
Lights on the skyline, this is my town
Style:

Trap, confident male rapper, aggressive delivery, heavy 808 bass, crisp hi-hats, ad-libs throughout, hard drums, 135-145 BPM, dark and energetic, Atlanta influence, modern production
When This Fails
The genre has no ad-lib tradition. Classical, ambient, and most folk give the model nothing to improvise, so the tag does nothing.

The seed ignores it. This is non-determinism, not a syntax error. Regenerate two or three times before changing anything.

You tagged every section. Ad-libs read as emphasis, and constant emphasis stops registering as emphasis at all.

Iteration Advice
Match the intensity to the genre. [ad-libs, heavy] on a trap hook lands; the same tag on an acoustic verse gets shrugged off.

Combine the two systems when it helps. Let Suno improvise the filler with brackets, and reserve parentheses for the one or two call-outs you actually care about.

Treat the tag as a dial you test, not a switch you flip. Two or three runs tell you whether the style will play along.

**WRONG** (9 adjectives, confused AI — too many = AI doesn't know which to prioritize):

```
[Chorus: Anthemic, Powerful, Epic, Orchestral, Dramatic, Climactic, Intense, Explosive, Grandiose]
```

### The Solution: PIPE Operator

**CORRECT** (7 elements, clearly separated — each element is processed as a separate instruction):

```
[Chorus | Anthemic | Stacked Harmonies | Brass Section | Bass Drop | Wide Stereo | Heavy Compression]
```

### Optimal Element Order

```
[Section | Mood/Energy | Vocal Style | Key Instruments | Dynamic/Movement | Spatial/Effects | Production Style]
```

Priority flows left to right. **Most important = first.**

### Genre Examples

**EDM Drop:**
```
[Drop | Explosive | Vocoder Vocals | Synth Lead | Bass Drop | Sidechain Compression | Wall of Sound]
```

**Jazz Ballad:**
```
[Verse | Intimate | Smooth Female Vocals | Piano Solo | Gentle Dynamics | Close Mic | Warm Analog]
```

**Rock Anthem:**
```
[Chorus | Anthemic | Full Band | Distorted Guitars | Building Energy | Wide Stereo | Arena Sound]
```

### One Real Prompt (Copy / Paste)

**Lyrics:**

```
[Intro | Atmospheric | Soft Synth Pad | Building]
[Verse | Intimate | Whispered Male Vocals | Minimal Beat | Lo-Fi Texture | Close and Personal]
I've been lost in the city lights
Searching for meaning every night
[Chorus | Explosive | Full Voice | Layered Synths | Driving Beat | Wide Stereo | Euphoric]
BUT NOW I'VE FOUND MY WAY!
NOTHING CAN STOP ME TODAY!
[Outro | Fading | Reverb Decay | Peaceful Resolution]
```

**Style:**

> Indie electronic pop, emotional male vocals, dynamic contrast between sections, mid-tempo (105-115 BPM), synth-driven, intimate verses, anthemic chorus, modern production, cinematic feel

### When This Fails

This trick fails when:

- More than 7 elements per tag
- Contradictory elements (intimate + explosive together)
- Used without clear section structure

### Iteration Advice

- **MAX 7 elements per tag** — beyond = confusion
- **Prioritize** — put most important elements first
- **Be specific** — "Guitar Solo" not just "Guitar"
- **Match to style prompt** — tags should reinforce, not contradict
