# Suno AI — Dirty Tricks & Creative Missions

**Fuente:** [Reddit r/SunoAI — Day 1 of resharing my Suno AI dirty tricks](https://www.reddit.com/r/SunoAI/comments/1tbuw56/day_1_of_resharing_my_suno_ai_dirty_tricks/)

---

# PARTE 1: DIRTY TRICKS


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

You are NOT "adding sound effects". You are **changing the performance context**.

### Why This Works

Suno associates certain textual patterns with concert recordings, live performances, and crowd interaction. When it sees those cues, it shifts:

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

This works because Suno processes text based on **pattern matching**, not linguistic understanding.

### Why This Works

Suno's text-to-speech component reads words based on common pronunciation patterns, statistical frequency of sounds, and contextual guessing. When a word has multiple pronunciations (homographs like "read", "live", "bass"), Suno picks the statistically more common one — which may not be what you want.

**For Italian:** also useful for ambiguous words like "ancora", "subito", "circuito", "principi", "seguito".

### When to Use This Technique

Use phonetic respelling when:
- A word is consistently mispronounced across multiple generations
- Homographs (same spelling, different sound) are read wrong
- Technical terms or names are mangled
- You need precise pronunciation for a pun or rhyme

Don't bother if: The word is pronounced correctly most of the time.

### Technique #1: Simple Phonetic Respelling

| Standard Spelling | Phonetic Respelling | Why |
|---|---|---|
| read (present tense) | reed | Forces "ree-d" instead of "red" |
| live (as in concert) | lyve | Forces "laiv" instead of "liv" |
| bass (instrument) | bahss or basss | Avoids "base" pronunciation |
| tear (crying) | teer | Forces "teer" instead of "tare" |
| wound (injury) | woond | Forces "woond" instead of "wownd" |
| lead (metal) | led | Forces "led" instead of "leed" |

### Technique #2: Syllable Splitting with Hyphens

When simple respelling doesn't work, split syllables with hyphens:
```
extraordinary → ex-traor-din-ary
catastrophe   → ca-tas-tro-phe
pneumonia     → new-moan-ya
```

### Technique #3: IPA for Stubborn Words

Use IPA (International Phonetic Alphabet) when phonetic respelling still fails. Works best for **ONE word at a time**.

**IPA Example — "breath" vs "breathe":**
`I'm out of /brɛθ/ again`

**IPA Example — Italian "Glicine":**
`Il profumo del /'glitʃine/ in giardino`

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

- The phonetic spelling creates a NEW mispronunciation
- You use IPA for too many words (confuses the model)
- The respelling is too different from the original word

> **Pro tip:** If phonetic respelling breaks the visual flow of your lyrics, use it only in the Suno input — keep a "clean" version saved separately for human readers.

### Iteration Advice

- Start simple — try basic phonetic respelling first (reed, lyve, bahss)
- Add hyphens if needed — split stubborn words into syllables
- Reserve IPA for last resort — one or two problem words maximum
- Test incrementally — fix one word at a time and regenerate

---

## TRICK #6: Alternative Spelling for Content Filters
### Using Homophones to Navigate Censorship

**Reliability:** High (when understood)

### What This Trick Actually Does

Suno relies on text-based content filters that scan lyrics through **exact string matching** rather than semantic understanding or phonetic analysis. A word that sounds identical but is spelled differently can clear the formal check while producing the same vocal output.

### Why This Sometimes Works

Suno's workflow follows three distinct stages:
1. **Content Filter** — scans the text for prohibited strings
2. **Lyric Tokenization** — converts written text into phonetic patterns
3. **Vocal Synthesis** — generates audio based on phonetic patterns rather than spelling

By the time vocal synthesis occurs, the original spelling is irrelevant — only the phonetic pattern matters.

This is why:
- "whole" sounds exactly like the censored word when sung
- "dam" works in place of the censored word in casual speech
- "faux king" breaks the censored word into two innocent words that blend when sung quickly

**For Italian:** "cat-zo", "m'erda", "vaffan-cool-o" follow the same logic.

### When This Fails

- **Phonetic distance is too large** — "Nice" will never sound like "knife"
- **Syllable count doesn't match** — multi-syllable substitutes sound forced
- **Over-reliance creates nonsense** — too many substitutions confuse the AI
- **Filter updates close the loophole** — Suno periodically updates filters

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
```

**Style:**
> Aggressive alternative rock, 145 BPM, distorted power chords, pounding drums, angry shouted male vocals, rebellious energy, punk attitude, raw and unpolished production, garage rock aesthetic, fast delivery

### Genre-Specific Applications

| Genre | Notes |
|---|---|
| Hip Hop / Rap | Fast delivery naturally blurs pronunciation. Works extremely well. |
| Punk / Rock | Shouted vocals mask exact pronunciation. Very effective. |
| Metal | Growled/screamed vocals make any pronunciation ambiguous. Reliable. |
| Pop / Ballad | Clear enunciation makes this difficult. Least reliable genre. |

### Combining with Other Tricks

**With Trick #8 (ALL CAPS):**
```
I don't give a DAM what you think
Gonna pound your WHOLES tonight
This is FAUX KING amazing
```

**With Trick #4 (Live Concert Mode):**
```
[crowd cheering]
Are you ready for some FAUX KING rock and roll?!
[crowd roars]
I said I don't give a DAM!
```

**With Trick #15 (Vocal Register Control):**
```
[Growled vocals] Don't give a dam about your rules
[Shouted vocals] This is faux king war
[Belted vocals] Pound your wholes to the ground
```

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

### Future-Proofing Your Approach

Build a **substitution library** — save successful combinations with a note of the date they worked. When a substitution stops working: increase tempo and delivery speed, add more aggressive vocal style keywords, or modify surrounding context.

**Expected success rate: 70–80%** with well-chosen homophones.

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

### Syntax Reference

| Syntax | Effect |
|---|---|
| `i-hit-the-street-and-i-never-look-back` | Hyphen-run — pushes the flow |
| `i hit the street, and i never look back` | Comma — micro-breath / half-beat |
| `i hit the street. i never look back.` | Period — hard reset / clearer pause |
| `i hit the street... and i never look back...` | Ellipsis — drag / suspense |
| Line break | Phrase / bar reset |

> **Rule of thumb:** Hyphens = speed, punctuation = breath, line breaks = phrases.

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

- Too many hyphens → words smear / become unintelligible
- The model starts singing (melisma kills cadence control)
- Text is too dense for the tempo → garbling / skipped syllables
- Too many control signals stacked (brackets + caps + hyphens + IPA, etc.)

### Iteration Advice (Use It Like a Knob)

| Goal | Action |
|---|---|
| Too slow | Increase hyphen-runs, remove commas/periods, shorten lines |
| Too fast / unclear | Remove hyphens from key words, add comma every ~6-9 syllables, insert line break before punchlines |

Make 2-3 generations before changing the template. **Change one lever at a time.**

---

## TRICK #8: ALL CAPS for Emotional Spikes
### Forcing Vocal Intensity Through Typography

**Reliability:** Very High

This is one of the few tricks that works **consistently**.

### What This Trick Actually Does

Capital letters signal emphasis, urgency, and intensity. Suno interprets ALL CAPS as: **"Increase vocal energy"**.

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

> **Key insight:** Contrast is everything. Caps work because they are **different** from the surrounding text.

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
Each hyphen = extended note duration. **Best for:** Ballads, soul, gospel, emotional moments.

### Technique #2: Stutter Effect

```
I-I-I-I want want want you you you
B-b-b-baby baby b-b-baby
```
Repetitions = autotune-style stuttering. **Best for:** Trap, hip hop, electronic pop, EDM.

### Technique #3: Melodic Spelling

```
L-O-V-E spells love
G-O-O-D-B-Y-E means the end
```
Each letter becomes a separate note. **Best for:** Pop hooks, jingles, cheerful songs.

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

- Overused throughout entire song
- Applied to very fast tempos
- Stacked with dense, wordy lyrics
- Genre doesn't support extended vocals

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

Text in (parentheses) in the lyrics is treated as secondary, background, or supportive. Suno often renders it as backing vocals, harmonies, call-and-response, or adlibs.

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

**WRONG** (9 adjectives — AI doesn't know which to prioritize):
```
[Chorus: Anthemic, Powerful, Epic, Orchestral, Dramatic, Climactic, Intense, Explosive, Grandiose]
```

**CORRECT** (7 elements, clearly separated — each processed as a separate instruction):
```
[Chorus | Anthemic | Stacked Harmonies | Brass Section | Bass Drop | Wide Stereo | Heavy Compression]
```

### Optimal Element Order

```
[Section | Mood/Energy | Vocal Style | Key Instruments | Dynamic/Movement | Spatial/Effects | Production Style]
```
Priority flows left to right. **Most important = first.**

### Genre Examples

| Genre | Example Tag |
|---|---|
| EDM Drop | `[Drop \| Explosive \| Vocoder Vocals \| Synth Lead \| Bass Drop \| Sidechain Compression \| Wall of Sound]` |
| Jazz Ballad | `[Verse \| Intimate \| Smooth Female Vocals \| Piano Solo \| Gentle Dynamics \| Close Mic \| Warm Analog]` |
| Rock Anthem | `[Chorus \| Anthemic \| Full Band \| Distorted Guitars \| Building Energy \| Wide Stereo \| Arena Sound]` |

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

- More than 7 elements per tag
- Contradictory elements (intimate + explosive together)
- Used without clear section structure

### Iteration Advice

- **MAX 7 elements per tag** — beyond = confusion
- **Prioritize** — put most important elements first
- **Be specific** — "Guitar Solo" not just "Guitar"
- **Match to style prompt** — tags should reinforce, not contradict

---

## TRICK #12: Vocal Adlibs with Brackets
### Injecting Non-Lyrical Vocal Events

**Reliability:** High

### What This Trick Actually Does

Square brackets `[...]` placed **inside** a line (not as section headers) often produce adlibs, interjections, and non-melodic vocal sounds.

### Syntax Example

```
I'm on top [yeah!] of the world [uh!]
Living my life [let's go!] no regrets [ayy!]
Can't stop me now [woah!] I'm unstoppable [skrrt!]
```
Each `[...]` = separate adlib vocal layer.

### Adlibs by Genre Reference

| Genre | Common Adlibs |
|---|---|
| Hip Hop/Trap | `[yeah!]`, `[uh!]`, `[ayy!]`, `[skrrt!]`, `[woah!]`, `[let's go!]` |
| R&B/Soul | `[ooh]`, `[ahhh]`, `[mmm]`, `[oh yeah]`, `[baby]` |
| Rock/Metal | `[hey!]`, `[go!]`, `[yeah!]`, `[whoa-oh]`, `[come on!]` |
| Pop | `[oh oh oh]`, `[na na na]`, `[la la la]`, `[hey hey]` |
| Latin | `[dale!]`, `[oye!]`, `[vamos!]` |

### One Real Prompt (Copy / Paste)

**Lyrics:**
```
[Verse]
Making moves [uh!] every day [yeah!]
Getting paid [money!] in every way [let's go!]
Haters mad [hah!] but I don't care [nah!]
I'm the king [boss!] everywhere [ayy!]

[Chorus]
We on top [woah!]
Never gonna stop [skrrt!]
Living life [yeah yeah!]
Doing it right [let's get it!]
```

**Style:**
> Trap, confident male rapper, aggressive delivery, heavy 808 bass, crispy hi-hats, ad-libs throughout, hard-hitting drums, fast tempo (135-145 BPM), dark and energetic, Atlanta trap influence, modern production

### When This Fails

- Used too frequently (every word)
- Lyrics are already overcrowded
- Genre doesn't use adlibs (classical, ambient)

### Iteration Advice

- Adlibs = punctuation, not sentences
- Match genre — use appropriate adlibs for the style
- Don't overload — 2-3 per verse is plenty
- Place strategically — end of lines, between phrases

---

## TRICK #13: "Broadway" as a Clarity Override
### Forcing Intelligible, Story-First Enunciation

**Reliability:** High

### What This Trick Actually Does

Using "Broadway" in the style prompt biases Suno toward:
- **Hard consonants** (T/D/K/P/S land clean)
- **Fully formed vowels** (less swallowing / smearing)
- **Tighter rhythm** (syllables align to the grid)
- **Dry, forward vocal presence** (less wash, more speech-band clarity)

**What you are NOT doing:** You aren't asking Suno to turn the track into a show tune, add Jazz hands choreography, or roll out a full Big Band orchestration. It is strictly a **clarity multiplier** for the vocals.

### Why This Sometimes Works

In the AI training data, "Broadway" acts as a powerful shorthand for dialogue-like intelligibility, vocal projection, and impeccable diction even during high-emotion moments. The model stops "smearing" and starts treating your lyrics like actual sentences delivered with intent.

### When This Fails

- Your genre prompt is extremely anti-theatrical ("grunge", "lo-fi mumble", "shoegaze", "washed ambient")
- You stack "Broadway" with heavy vocal FX keywords ("cavernous", "smeared", "drowned", "massive reverb")
- The lyric density is too high (hyper-fast syllables)
- You also demand distortion / screaming (clarity + distortion conflicts)

### One Real Prompt (Copy / Paste)

**Lyrics:**
```
[Verse 1: Intimate, Controlled, Clear]
I said I'm fine like it meant something
But my mouth lied clean
And the truth stayed in my teeth

[Pre-Chorus: Building, Precise]
If you miss one line you miss the wound
So listen close

[Chorus: Confessional, Forward, Dry]
I don't want the echo of you
I want the sentence
I want it true
Say it straight, don't blur the proof
I need the words to cut right through

[Bridge: Low, Dangerous, Still Clear]
Don't drown me in the reverb
Don't hide me in the smoke
I'm not asking for forgiveness
I'm asking you to choke on what you wrote
```

**Style:**
> Dark electronic pop, alt-pop noir, 95-105 BPM, Broadway musical clarity (story-first enunciation, hard consonants, centered vowels), controlled emotion (intense but articulate), dry forward lead vocal, close mic, minimal reverb and delay, deep sub bass, tight drums, cold synth textures, cinematic tension

### Prompt Variants (Keep Broadway, Change Texture)

**Variant A — Broadway clarity + industrial dark pop:**
`Broadway clarity, dry forward vocal, industrial pop, dark electro, distorted synth bass, minimal reverb, tight drums, cinematic low-end`

**Variant B — Broadway clarity + cinematic trip-hop noir:**
`Broadway clarity, close-mic vocal, minimal reverb, trip-hop, noir cinematic, vinyl crackle, slow tension, sub bass, sparse drums`

**Variant C — Broadway clarity + hyperpop precision:**
`Broadway clarity, crisp consonants, dry vocal, hyperpop textures, bright synths, tight quantized drums, lyrics must be intelligible`

### Iteration Advice

- If it sounds too theatrical: reinforce your texture with genre keywords ("dark electronic", "alt-pop noir")
- If it's still murky: add "dry vocal, close mic, upfront" and remove reverb-heavy words
- If it becomes emotionally flat: add "controlled anger / restrained grief / contained intensity"
- If consonants get harsh: add "smooth sibilance"
- If it ignores the trick: move "Broadway" **earlier** in the style line and delete conflicting tags

---

## TRICK #14: Forced Multi-Voice Duets
### Creating the Illusion of Multiple Singers

**Reliability:** High (but fragile)

### What This Trick Actually Does

This trick biases Suno into generating two distinct vocal roles, alternating delivery, and gender contrast (male voice vs. female voice).

> **Heads up:** Vocal identity can "shapeshift" halfway through the track. A character's timbre might not stay consistent from start to finish.

### Critical Requirement

**You MUST specify "Duet" in the Style prompt!** If you don't clearly include "Duet" in the Style prompt, Suno is likely to flatten everything into a single voice.

### Available Vocal Tags

| Tag | Function |
|---|---|
| `[Male Vocal]` | Male voice |
| `[Female Vocal]` | Female voice |
| `[Both Vocals]` | Both together |
| `[Male Lead, Female Backing]` | Male front, female background |
| `[Female Lead, Male Harmony]` | Female front, male harmony |
| `[Duet]` | Both voices, balanced |

### One Real Prompt (Copy / Paste)

**Lyrics:**
```
[Verse 1: Male Vocal]
I walked away from everything we had
Left you standing in the rain
I thought that I could make it on my own
But nothing's ever been the same

[Verse 2: Female Vocal]
You let me go without a fight
Didn't even say goodbye
Now I'm standing here alone tonight
Wondering why, wondering why

[Chorus: Both Vocals, Harmony]
But we still love each other
Can't deny what we feel inside
Maybe we should try again
And let our broken hearts heal

[Bridge: Female Lead, Male Backing]
If you come back to me (come back to me)
I promise I won't leave (won't leave)
We can start again (start again)
```

**Style:**
> Emotional Pop Ballad Duet, Male and Female Vocals, romantic and heartfelt, piano-driven arrangement, slow tempo (70-80 BPM), cinematic build, orchestral swells, intimate verses, powerful harmonized chorus, modern adult contemporary

### When This Fails

- "Duet" is missing from Style (critical!)
- Both roles have identical lyrics
- Section labels are unclear
- There are too many voice switches (confuses AI)

### Iteration Advice

- Always include "Duet" in style — this is non-negotiable
- Clear section labels — be explicit about who sings
- Contrast the lyrics — different perspectives help differentiation
- Limit voice switches — 4-6 per song maximum

---

## TRICK #15: Vocal Register Control per Section
### Biasing Range and Physical Effort

**Reliability:** High

### What This Trick Actually Does

Vocal register tags guide:
- The **pitch range** (how high or low it goes)
- The **breathiness** (the amount of air in the delivery)
- The **vocal effort** (the physical intensity of the performance)

They do NOT enforce correct technique — they **suggest performance energy**.

### Available Registers

| Register | Character | Best For |
|---|---|---|
| Falsetto | Light, airy, high, head voice | Ethereal moments, vulnerability |
| Chest Voice | Full, powerful, grounded | Confident delivery |
| Head Voice | Clear, light, high but full | Pop brightness |
| Mixed Voice | Balanced, versatile | Modern pop/R&B |
| Whispered | Soft, intimate | Secret, vulnerable |
| Spoken Word | Narrative, non-melodic | Rap verses, intros |
| Raspy | Hoarse, gritty | Rock, blues, raw emotion |
| Belted | Maximum power, full volume | Climax moments |

### Emotional Mapping

| Register | Emotion |
|---|---|
| Falsetto | Vulnerability, dream, longing |
| Chest | Strength, determination, confidence |
| Whispered | Intimacy, secrets, fragility |
| Belted | Climax, liberation, triumph |
| Raspy | Pain, experience, authenticity |

### One Real Prompt (Copy / Paste)

**Lyrics:**
```
[Intro: Falsetto, Ethereal]
Ooh... floating above the clouds...
drifting away...

[Verse 1: Chest Voice, Conversational]
But then I woke up to reality
The dream was gone, just a memory
Walking through these empty streets
Searching for what I need

[Pre-Chorus: Mixed Voice, Building]
And I can feel it rising up inside

[Chorus: Belted, Powerful]
I WON'T GIVE UP, I'LL CARRY ON!
EVEN WHEN THE HOPE IS GONE!
I'LL FIGHT UNTIL THE BREAK OF DAWN!

[Bridge: Whispered, Intimate]
(Maybe if I close my eyes...)
(I can find my way back home...)

[Final Chorus: Belted, Maximum Intensity]
I WON'T GIVE UP!
```

**Style:**
> Alternative rock, dynamic male vocals, emotional journey, building intensity, mid-tempo (95-105 BPM), anthemic chorus, raw and vulnerable verses, explosive climax, guitar-driven, modern rock production

### When This Fails

- Tempo is very fast (no time for register shifts)
- Lyrics are too dense
- Too many register changes
- Registers contradict the genre

### Iteration Advice

- Focus on structural shifts — apply changes between verses and choruses
- Build a performance arc — start soft, ramp up the intensity
- Match emotion to technique — whispered or falsetto for vulnerable moments
- Keep it simple — 3 or 4 register shifts per song are plenty

---

## TRICK #16: Emotional Register Change per Section
### Programming Emotional Arcs

**Reliability:** High

### What This Trick Actually Does

Instead of a global mood, you assign different emotions to different sections. This influences melody shape, intensity, harmonic tension, and rhythmic delivery.

### How the AI Responds to Emotional Tags

| Emotional Tag | AI Adjustment |
|---|---|
| Sad | Minor key, slower, sparse |
| Angry | Aggressive voice, faster, louder |
| Desperate | Sparse instruments, raw voice |
| Explosive | Full band, maximum energy |
| Melancholic | Slower tempo, minor harmonies |
| Euphoric | Faster, major key, bright |
| Defiant | Powerful, strong delivery |
| Reflective | Gentle, reflective delivery |
| Triumphant | Full arrangement, victorious |

> **Key insight:** Emotion only works when it **changes**. Contrast is everything.

### One Real Prompt (Copy / Paste)

**Lyrics:**
```
[Verse 1: Sad, Melancholic, Slow, Resigned]
I lost you in the autumn rain
The leaves fell down like tears
Everything we built together
Disappeared with all those years

[Verse 2: Angry, Bitter, Rising Tension]
But now I see you never cared
You played me like a fool
I gave you everything I had
And you broke every rule

[Chorus: Triumphant, Defiant, Explosive]
But I'M FREE NOW! I'M FINALLY FREE!
NO MORE CHAINS HOLDING ME!
I'M STRONGER THAN I'VE EVER BEEN!
THIS IS MY VICTORY!

[Bridge: Reflective, Bittersweet, Gentle]
Maybe someday I'll forgive...
Maybe time will heal these wounds...
But right now I'm just grateful
That I finally found the truth
```

**Style:**
> Emotional rock ballad, powerful female vocals, dynamic journey from soft to explosive, piano to full band arrangement, slow-mid tempo (80-90 BPM), cinematic build, cathartic release, strong emotional arc, modern rock production

### When This Fails

- Emotions contradict the tempo (e.g., "sad" + "fast")
- Everything is tagged as emotional (no contrast)
- Emotions change too frequently
- Tags are too subtle or similar

### Iteration Advice

- Draw a coherent emotional arc — guide the listener through an evolving journey
- Play with contrasts — try pairing a melancholic verse with an explosive chorus
- Don't overdo the tags — limit to 3 or 4 indications per song
- Sync with the lyrics — the chosen emotion should reinforce the meaning of the text

---

## TRICK #40: Acoustic Space Specification
### Defining Physical Recording Environment

**Reliability:** ★★☆☆☆ Low (Experimental)

> **SPECULATIVE:** In Suno, "space" language tends to behave more like a production/effects hint (reverb/ambience/room-mic vibe) than a physically accurate acoustic simulation.

### What This Trick Actually Does

When you write "recorded in a cathedral / bathroom / warehouse" in your prompt, you are steering a cluster of associations:

- **Reverb & Decay** — balance between wet/dry signal and decay character
- **Early Reflections** — difference between a tight boxy room and a massive hall
- **Mic Distance** — close-mic intimacy vs. the "wash" of a distant room mic
- **Room Tone** — intentionally introducing hiss, air, or live environment feeling
- **Performance Vibe** — mimicking the bleed and imperfections of a one-take capture

### How To Make It Less Random

Layer your instructions with four elements:
1. **Space** (where)
2. **Surfaces** (what it's made of)
3. **Capture** (mic style / distance / bleed)
4. **Mix instruction** (dry vs wet, reverb type)

### Space Reference

| Space / Capture | What You Are Hinting At |
|---|---|
| Vocal booth / dead room | Very dry, intimate, minimal reflections |
| Small bedroom | Boxy short reflections, DIY closeness |
| Rehearsal room / garage | Mid-size slap, raw, imperfect |
| Jazz club | Short warm room, close audience feel |
| Concert hall | Wide stereo, long smooth tail |
| Cathedral | Massive tail, slow bloom, sacred scale |
| Tiled bathroom / stairwell | Bright, hard reflections, "wet" vocal |
| Warehouse / parking garage | Metallic smear, gritty reflections |
| Car interior | Tight, close, muffled highs, compressed feel |
| Telephone / AM radio | Narrow band, lo-fi filtering |

### High-Signal Tokens Users Report Working

- `small room acoustics`
- `room tone (air, faint hiss)`
- `close mic presence`
- `off-axis mic placement`
- `proximity effect`
- `single-mic capture`
- `one-take performance`

> If you're struggling with too much vocal echo, add **"dead room"** and **"dry vocal"** to your style prompt.

### One Real Prompt (Copy / Paste)

**Style:**
> Recorded in a 12th century stone cathedral, 7 second reverb decay, microphone 30 feet from source, choir vocals, pipe organ, sacred atmosphere, slow tempo (55-65 BPM), massive holy space, transcendent and ancient, spiritual

**More Prompts:**

1. **Dry intimate singer-songwriter:**
`Dead room vocal booth, close-mic presence, dry vocal mix, single-mic capture, audible breath detail, intimate acoustic guitar, one-take performance, natural room tone only`
*(Exclude: reverb, delay)*

2. **Bathroom indie rock:**
`Tiled bathroom acoustics, bright hard reflections, room mic bleed, raw garage band, spring reverb splash, slapback delay on vocal, messy one-take energy, tape saturation vibe`

3. **Warehouse techno:**
`Industrial warehouse space, metallic early reflections, wide stereo room ambience, cavernous hall reverb, pumping compression feel, mechanical percussion, cold air and distance, late-night rave atmosphere`

4. **Cathedral choir:**
`Stone cathedral space, massive cathedral reverb, long decay, distant stereo pair capture, choir vocals with slow bloom, pipe organ weight, sacred atmosphere, minimal close-mic, huge sense of height`

5. **Jazz club:**
`Small jazz club room, warm short room reverb, close audience feel, intimate stage mic, light room tone, upright bass and brushed drums, natural dynamics, live take with subtle bleed`

6. **Telephone memory intro:**
`Telephone bandpass lo-fi, narrow mono, distant and muffled, subtle room tone hiss, recorded on a cheap handheld, then opens into full mix, nostalgic and imperfect`

### Where to Put Space Instructions

- Put the "space stack" **early** in `Style:`
- Use the Exclude field for things like "echo" or "long reverb tail" if the mix gets too muddy

### When This Fails

- You expect physically accurate acoustics (it's more "vibe steering" than simulation)
- The arrangement is too dense (space cues get masked)
- You give ultra-specific measurements (feet, milliseconds) and the model shrugs

---

## TRICK #41: Mathematical / Scientific Descriptors
### Using Abstract Concepts for Structure

**Reliability:** ★★☆☆☆ Low (Experimental)

> **SPECULATIVE:** These are metaphorical. AI interprets through associated content, not math. Suno cannot compute Fibonacci sequences or apply golden ratios.

### What This Trick Actually Does

You use mathematical or scientific terms as structural and textural descriptors in your style prompt. These terms work (when they work) because of training data association, semantic clustering, and indirect genre steering toward progressive rock, IDM, ambient, generative electronic, and avant-garde classical.

### Extended Reference Table

#### Growth & Structure Patterns

| Term | Musical Association | Best Paired With |
|---|---|---|
| Fibonacci | Natural growth, expanding intervals, organic development | Progressive rock, art rock, ambient |
| Golden ratio | Balanced proportions, climax placement at ~61.8% | Classical-influenced, cinematic, post-rock |
| Fractal | Self-similar patterns at different scales, recursive motifs | IDM, generative electronic, minimalism |
| Logarithmic | Gradual scaling, compression of change over time | Ambient, drone, slow-building compositions |

#### Energy & Dynamics

| Term | Musical Association | Best Paired With |
|---|---|---|
| Exponential | Rapid build, dramatic crescendo | EDM, cinematic, post-rock climaxes |
| Asymptotic | Approaching a limit, tension without resolution | Ambient tension, post-rock, shoegaze |
| Parabolic | Rise and fall, arc shape | Ballads, cinematic arcs |

#### Waveform & Texture

| Term | Musical Association | Best Paired With |
|---|---|---|
| Sine wave | Pure, clean, fundamental tone | Ambient, minimal electronic, meditation |
| Sawtooth | Bright, buzzy, harmonically rich | Synthwave, EDM, electronic |
| Pink noise | Balanced frequency spectrum, natural-sounding | Lo-fi, ambient, organic textures |
| White noise | Equal energy across frequencies, hiss, static | Industrial, noise, glitch |
| Harmonic series | Natural overtones, resonant, rich | Drone, ambient, acoustic |

#### Chaos & Unpredictability

| Term | Musical Association | Best Paired With |
|---|---|---|
| Entropy | Increasing chaos, disorder | Noise, industrial, experimental |
| Stochastic | Controlled randomness, probability-driven | Avant-garde, contemporary classical |
| Quantum | Unpredictable, superposition of states | Experimental, glitch, ambient |
| Fractal | Complex from simple rules | Math rock, progressive, experimental |

#### Geometry & Space

| Term | Musical Association | Best Paired With |
|---|---|---|
| Symmetry | Mirror patterns, palindromic structures | Classical, progressive, math rock |
| Tessellation | Interlocking repeating patterns | Afrobeat, gamelan, minimalism |
| Crystalline | Geometric, precise, faceted, clear | Ambient, IDM, minimal, post-rock |

### Tier List: Which Terms Actually Do Something

**Tier 1 — Likely Understood** (use confidently):
`Crystalline`, `Sine wave`, `Sawtooth`, `Harmonic series`, `Symmetry`, `Exponential build`

**Tier 2 — Plausible Association** (use alongside strong genre anchors):
`Fractal`, `Fibonacci`, `Golden ratio`, `Pink noise`, `White noise`, `Spiral`, `Recursive`

**Tier 3 — Mostly Vibes** (treat as mood words):
`Entropy`, `Quantum`, `Stochastic`, `Logarithmic`, `Parabolic`

**Tier 4 — Almost Certainly Ignored** (don't bother):
`Riemann`, `Euler`, `Fourier`, `Bayesian`, any formula or equation

### Real-World Precedents

- **Fibonacci:** Bartók's "Music for Strings, Percussion and Celesta"; Tool's "Lateralus" (syllable counts: 1, 1, 2, 3, 5, 8, 13...)
- **Golden ratio:** Debussy's "La Mer" uses golden ratio to place climaxes; Billboard top hits frequently climax at ~61.8% of total duration
- **Fractal:** Bach's Cello Suite No. 3 exhibits Cantor-set-like structural scaling; Steve Reich's phasing compositions

### One Real Prompt (Copy / Paste)

**Prompt 1 — Progressive Electronic:**
> Fibonacci sequence arrangement, golden ratio dynamics, fractal melody patterns that evolve and repeat at different scales, exponential energy build, mathematical precision, electronic composition, (115-125 BPM), structured yet organic, algorithmic beauty, crystalline textures

**Prompt 2 — Fractal Ambient (Strongest Use Case):**
> Fractal ambient soundscape, self-similar patterns at different time scales, recursive evolving motifs, 1/f noise distribution, pink noise texture, logarithmic dynamics, slow tempo (60-70 BPM), generative electronic, deep listening, minimalist, Brian Eno influence, natural mathematical beauty

**Prompt 3 — Math Rock:**
> Math rock, asymmetric time signatures, tessellating guitar patterns, Fibonacci rhythmic subdivisions, fractal polyrhythm, angular melodic intervals, precise and complex, (140-155 BPM), technical but groovy, interlocking patterns, crystalline guitar tones, tight drums

### The Core Rule

> Mathematical terms work best when they **REINFORCE** a clear musical prompt, not when they **REPLACE** one.

**Bad:** `Fibonacci golden ratio fractal exponential mathematical composition`

**Good:** `Progressive electronic, fractal-like evolving arpeggios, exponential build to climax, crystalline synth textures, (120-130 BPM), IDM influence, precise yet organic`

### When This Fails

Most of the time, when mathematical terms are the only descriptors. Success rate by term type:

| Category | Estimated Success Rate |
|---|---|
| Waveform terms (sine, sawtooth, pink noise) | ~40-50% |
| Texture terms (crystalline, fractal, organic) | ~30-40% |
| Structure terms (Fibonacci, golden ratio) | ~15-25% |
| Abstract terms (quantum, entropy, stochastic) | ~10-15% |
| Pure math (Riemann, polynomial) | ~5% |

### Iteration Advice

- Never lead with math — always establish genre, tempo, and instruments first
- Pick ONE mathematical concept per prompt — stacking dilutes all of them
- Generate 10+ variations — this is the most unpredictable trick in the book
- A/B test — generate WITH and WITHOUT the mathematical term, compare results

---

## TRICK #42: Error Injection
### Simulating Imperfection Through Deliberate Prompt Chaos

**Reliability:** ★☆☆☆☆ Very Low (High Risk)

> **EXTREMELY SPECULATIVE & HIGH RISK:** This technique intentionally introduces chaos into your prompt. Results are completely unpredictable. May produce unusable output.

### Before You Try This

If you want imperfect, lo-fi, raw, or demo-quality output, try standard descriptors first:
`lo-fi, raw recording, demo quality, tape hiss, bedroom production, DIY aesthetic, cassette 4-track, imperfect timing, unpolished`

These are well-understood terms that work reliably. **Error Injection is for when those descriptors are too clean, too predictable, too intentional.**

### What This Trick Actually Does

You deliberately break your own prompt by including:
- Typos and informal language ("likee," "idk," "lol")
- Uncertainty markers ("??", "maybe," "kinda")
- Conversational hedging ("but like... more vibes???")
- Self-contradiction ("fast but slow," "clean but dirty")
- Incomplete thoughts ("something like... you know")
- Non-standard punctuation (excessive question marks, ellipses)

You are not writing instructions. You are writing **anti-instructions**.

### Types of Error Injection

**Type 1: Conversational Chaos**
> Rock but likee... more ?? vibes??? idk kinda unfinished feeling lol, demo recording, bedroom production, imperfect but real, DIY aesthetic, maybe (95-105 BPM)?? raw and messy but genuine, mistakes included

**Type 2: Self-Contradictory Instructions**
> Fast but slow, heavy but light, polished but raw, professional demo, beautiful disaster, organized chaos, precise sloppiness, (100-110 BPM), lo-fi high-fidelity

**Type 3: Incomplete Thought Stream**
> Something like... indie? but not really, more like if you recorded a band in a kitchen at 2am and the tape was running out and nobody really... you know, (90-100 BPM), that FEELING when a song is almost good but not quite and that's what makes it

**Type 4: Wrong Vocabulary on Purpose**
> Sounds like the color of a rainy Tuesday, wobbly, tastes like cold coffee, the musical equivalent of an unmade bed, comfortable ugly, (85-95 BPM), if nostalgia had bad posture

**Type 5: Technical Gibberish**
> Reverse sidechain on the feelings, 3dB of sadness, detuned emotions, the kick drum is existential, hi-hat anxiety, (105-115 BPM), mix buss melancholy, master bus regret

### Genre Compatibility

| Genre | Why It Works | Best Error Type |
|---|---|---|
| Bedroom pop | Imperfection IS the genre | Conversational chaos, incomplete thoughts |
| Lo-fi hip hop | Degradation is aesthetic | Self-contradiction, wrong vocabulary |
| Garage rock/punk | Rawness is ideology | Conversational chaos |
| Shoegaze | Blur and noise expected | Self-contradiction |
| Vaporwave | Corrupted/decontextualized | Technical gibberish, glitch |
| Noise/experimental | Chaos is the point | Any type, go wild |
| Indie folk | Intimacy, vulnerability | Incomplete thoughts, scene descriptions |

Almost never works with: Modern pop, EDM/House, Classical, Metal (needs tight execution), K-pop.

### When This Fails

Most of the time. Specific failure modes:
- AI ignores the chaos entirely and produces clean, polished output
- Complete gibberish — no musical structure, unusable noise
- Wrong kind of imperfect — you wanted charming lo-fi, you got bad mix with no character
- Literal interpretation — AI tries to generate actual phone buzzing or fridge humming

### Iteration Advice

- Generate at LEAST 5 variations — success rate is very low, volume is your only lever
- Save anything remotely interesting immediately — you will not reproduce it
- **Embed 2-3 real keywords in the mess** — "bedroom production," "demo recording," "raw"
- Keep a "chaos journal" — when something works, save the exact prompt
- Accept the failure rate — this trick exists for the 1-in-10 (or 1-in-100) surprise

### The Fundamental Truth

> You are not controlling imperfection. You are **inviting randomness** and hoping it's beautiful.

Use this trick when you have exhausted everything else, when you are bored of your own competence, when you want to be surprised. **Don't use it when you need results.**

---

# PARTE 2: CREATIVE MISSIONS

---

## Creative Mission #1: Morning Coffee Soundtrack
### Genre: Acoustic Folk

**Micro-story:** You unlock the shop at 5:45, before the espresso machine has stopped hissing at you. The room smells like yesterday's coffee grounds and something floral you can't place. You want a close-mic'd voice and a guitar that sounds like the player is sitting across from you on a stool, not performing, just filling silence the way a person does. The first customer arrives, pauses in the doorway, and asks, "What is this?" You say, "I don't know the name." That's the brief: make something people don't know the name of.

**Story behind the story:** The intimate, confessional style we recognize today grew in the 1960s and 70s through artists like Joni Mitchell and James Taylor. The genre emphasizes storytelling, minimal production, and the human voice. This "living room" aesthetic — close-mic'd vocals, natural reverb, minimal overdubs — became the blueprint for modern indie folk and bedroom pop.

### STYLE prompt

> Indie folk, Singer-songwriter, Acoustic Coffeehouse, Unhurried and conversational, intimate, early morning stillness, 95 BPM, steady 4/4, fingerpicked nylon-string acoustic guitar, close-mic'd female vocal completely dry, natural room ambience only, no drums no percussion no bass, open-tuned chord fills between phrases, hook enters within first 8 bars, warm analog recording, minimal compression to preserve natural breath and finger noise, song feels like overhearing someone think out loud, [Verse] fingerpicking carries the rhythm, voice sits right on top like a conversation, [Chorus] open chord swells, vocal lifts slightly but never breaks the intimacy, [Production] close mic on vocal capturing room air and string resonance, narrow stereo, tape warmth only, organic imperfection welcome

### NEGATIVE prompt

> intro, reverb, delay, EQ-polish, electronic, drums, pop, orchestral

### Version 2 — Strummed guitar

Swap `fingerpicked nylon-string acoustic guitar` → `strummed acoustic guitar with palm muting`

### Version 3 — Half-time with percussion

Swap `95 BPM, steady 4/4` → `80 BPM, half-time feel` and add brushed snare and hand percussion *(remove "drums" from the NEGATIVE prompt)*

### Results

- https://suno.com/s/JGKrwQVC77OSQj6k
- https://suno.com/s/jo0i45BAahUJ0pmz
- https://suno.com/s/U2SxamkBaAr5DY16

### Reference listening

- Joni Mitchell — "A Case of You"
- Nick Drake — "Northern Sky"
- José González — "Heartbeats"
- Bon Iver — "Holocene"

---

## Creative Mission #2: Saturday Night Energy
### Genre: Classic 1970s Disco, Funk Soul

**Micro-story:** The folding tables are up, the extension cord runs across the wet grass, and your neighbor Ricardo is standing next to the speaker looking at you like you are personally responsible for the mood of everyone he has ever met. Forty people will be here in fifteen minutes. He says, "Something that works right away". The mirror ball rents by the hour. Pick something with a four-on-the-floor kick and a bass that moves before the melody does, or Ricardo will put on his salsa playlist and this will be a different party.

**Story behind the story:** Disco emerged in the early 1970s in New York City clubs like Studio 54 and Paradise Garage. The genre brought together funk rhythms, orchestral strings, and four-on-the-floor kick drums to create music designed purely for dancing. The "four-on-the-floor" kick pattern — a kick drum hit on every beat: 1-2-3-4 — became the foundation of nearly all dance music that followed.

### STYLE prompt

> Classic 1970s Disco, Funk Soul, 124 BPM, steady four-on-the-floor kick, syncopated funky bass guitar leading before the melody, tight 16th-note rhythm guitar, punchy brass stabs, lush orchestral strings, celebratory and danceable, euphoric dancefloor energy, female lead vocal warm and powerful, call-and-response chorus with backing vocals, falsetto ad-libs on chorus peaks, hook enters immediately, [Verse] bass and kick lock in first, rhythm guitar chops, strings enter as texture, [Chorus] full arrangement explosion, brass punches, unison backing vocals, [Production] saturated analog warmth, punchy low end, wide stereo on strings and brass, centered vocal, vintage mastering with controlled dynamics

### NEGATIVE prompt

> intro, slow-build, ballad, synth-leads, electronic, lo-fi, bedroom-pop

### Version 2 — Synth strings

Swap `orchestral strings` → `synth strings with slight chorus effect` *(smaller room, slightly more plastic 70s feel)*

### Version 3 — Hi-NRG (crosses genre border)

Swap `124 BPM, steady four-on-the-floor kick` → `145 BPM, harder four-on-the-floor kick` and add `hi-NRG energy, more aggressive synth stabs`

### Results

- https://suno.com/s/CGLwb3VhzD6zFn6h
- https://suno.com/s/gHdwYda9xDbU8PVM
- https://suno.com/s/a7D5TVc0bNwri7LB

### Reference listening

- Chic — "Le Freak"
- Sister Sledge — "We Are Family"
- Earth, Wind & Fire — "September"
- Donna Summer — "I Feel Love"

---

## Creative Mission #3: Late Night Drive
### Genre: Synthwave, Outrun Retrowave

**Micro-story:** It's 2002 and the GPS doesn't work this far out. You've been driving for two hours on a road that your phone shows as a thick gray line going nowhere, and the only decision you've made since the on-ramp was not to change the station. Something came on: no lyrics, no drop, just a synth line moving at the same speed as the road; switching it off now would feel like an act of aggression. Make music that doesn't ask for attention but holds it anyway.

**Story behind the story:** Synthwave emerged in the mid-2000s as a nostalgic revival of 1980s electronic music, film scores, and video game soundtracks. Artists drew inspiration from composers like John Carpenter and Vangelis. The genre uses vintage synthesizers like the Roland Jupiter-8 and Yamaha DX7 to recreate the neon-soaked, futuristic optimism of 80s pop culture.

### STYLE prompt

> [Synthwave], outrun retrowave, (108-112 BPM), cinematic 80s night-drive. Jupiter-8 analog poly synth (sustained chord stabs), expressive CS-80-style wide stereo pad layer (long evolving tails, lush cinematic sustain, melancholic futuristic glow), gated reverb snare (sharp transient, long decay), four-on-the-floor kick (tight 808-style punch), mono synth bass (locked step with kick, no slides). Nocturnal, hypnotic, solitary. Instrumental, no vocals. Sparse pad intro (8 bars), main riff enters bar 9, breakdown strips to kick and bass only at midpoint, full arrangement re-entry with added synth layer for final section. Wide stereo pads, dry punchy kick center, long reverb tails on snare, audible sub-bass, controlled clean master.

### NEGATIVE prompt

> vocals, chillwave, lo-fi, downtempo, soft drums, tape saturation, acoustic instruments

### Version 2 — Club energy

Swap `(108-112 BPM)` → `(126-130 BPM)` *(crosses out of outrun territory into something that could anchor a club set)*

### Version 3 — Arpeggio bass

Swap `mono synth bass (locked step with kick, no slides)` → `mono synth bass (ascending 16th-note arpeggio, no slides)` *(busier, more mechanical, closer to a video game than a highway)*

### Results

- https://suno.com/s/hS9IkCgR3nE4kTCj
- https://suno.com/s/X7yUGuejCBrVEWh4
- https://suno.com/s/jNDQJt1iup8XE05t

### Reference listening

- Kavinsky — "Nightcall"
- College — "A Real Hero"
- Gunship — "Tech Noir"
- Carpenter Brut — "Turbo Killer"

---

## Creative Mission #4: Sunday Morning Gospel
### Genre: Gospel

**Micro-story:** Your aunt sings third alto and she has been calling this the most important Sunday of the year since February, so you are in the third pew with your back straight and your good shoes on. The Hammond player runs a chord and holds it, and four voices come in above it like they already knew. Your aunt isn't looking at the sheet music. She's looking at the space above the congregation, which means she's about to do the thing with her voice that makes people cry. Make something that sounds like it matters this much.

**Story behind the story:** Gospel music has roots in African American spirituals, hymns, and the call-and-response traditions of the Black church. By the 1930s and 1940s, artists like Mahalia Jackson and Thomas A. Dorsey shaped modern gospel. The Hammond B3 organ — an electric organ invented in 1935, famous for its warm, sustained tones — became central to the sound.

### STYLE prompt

> [Gospel], 80 BPM, Southern Black church gospel, call-and-response structure, 1960s–70s soul-gospel feel. Hammond B3 organ (slow Leslie rotation, full lower register swell), four-part SATB choir (close blend, no vibrato on lead), powerful female lead vocal (chest voice, mezzo-soprano), handclaps on beats 2 and 4, tambourine (shaker pattern), acoustic upright piano (comping chords). Reverent, weight-bearing, surrendered. Lead vocal, female, powerful and close-mic, chest voice with gospel runs in upper register; four-part choir behind, tight unison moving to open harmony. Sparse organ intro; verse restrained; build begins when choir enters full; final third erupts into full-choir fortissimo, organ Leslie opens to fast rotation, handclaps double. Small Baptist church interior, wooden room, short warm reverb, mic bleed between voices, natural room tone, vocal-forward, tight low end.

### NEGATIVE prompt

> intro, slow-build, ballad, synth-leads, electronic, lo-fi, bedroom-pop

### Version 2 — Fast Leslie throughout

Swap `slow Leslie rotation` → `fast Leslie rotation throughout` *(loses the sense of something being held back before the final third)*

### Version 3 — Large stone church

Swap `Small Baptist church interior, wooden room, short warm reverb` → `large stone church, wide stereo, long reverb tail, choir bloom` *(lifts voices into the abstract; "you're inside a feeling" vs "you're inside a room")*

### Results

- https://suno.com/s/iPq2clSJ5JjZRNKt
- https://suno.com/s/YVttvLLWKrt0aao5
- https://suno.com/s/iZlDus3R4MVgvS2t

### Reference listening

- Mahalia Jackson — "Take My Hand, Precious Lord"
- The Staple Singers — "I'll Take You There"
- Aretha Franklin — "Amazing Grace" (live album)
- Kirk Franklin — "Stomp"

> **Ethics note:** Gospel is deeply tied to African American cultural and spiritual history. Use these references to understand the genre's vocal power and communal energy, not to mimic sacred practices.

---

## Creative Mission #5: Basement Jam Session
### Genre: Funk

**Micro-story:** Your drummer has to leave at nine. It is currently eight forty-three. Everyone knows this, so the session has stopped being casual and started being something else; nobody wants to be the person who called it early. The guitar player locks into a riff, the bass player finds the one, and there are exactly seventeen minutes to get something tight enough that people remember it on the drive home. Make something with that clock running.

**Story behind the story:** Funk emerged in the mid-1960s when artists like James Brown and Sly Stone shifted the focus from melody to rhythm. The bass and drums became the lead instruments, and the guitar played percussive "chicken scratch" chops — short, muted, rhythmic guitar strokes that sound like scratching. The genre emphasized the "one" — the first beat of every measure, where the bass and kick drum lock together.

### STYLE prompt

> [Funk], 105 BPM, mid-60s funk energy, tight pocket groove. Syncopated electric bass locked to kick on beat 1, tight snare on 2 and 4, dense 16th-note closed hi-hats, chicken-scratch rhythm guitar (wah-filtered short muted strokes), staccato brass stabs (2-3 hits only, no sustain), no melodic solos. Urgent, coiled, sweaty. Lead vocal, gender-neutral, close-mic, clipped phrasing with adlib call-outs, no long melisma. Sparse verse groove locks into dense full-band pocket by the second section, then sustains without release — no breakdown, no fade, only tightening. Rehearsal room acoustics, mid-size slap, single-mic bleed, dry vocal upfront, punchy kick and snap snare, tight low end, no reverb wash, clean master.

### NEGATIVE prompt

> neo-soul, R&B ballad, lo-fi hip-hop, smooth jazz, horn solo, sustained horns, reverb heavy, slow build

### Version 2 — No room (direct DI)

Swap `Rehearsal room acoustics, mid-size slap, single-mic bleed` → `direct DI capture, no room, dead studio` *(the "basement, 8:43 PM, clock running" feeling collapses — the same notes and groove land in a clinical space)*

### Version 3 — Standard structure

Swap `Sparse verse groove locks into dense full-band pocket ... only tightening` → `verse-chorus structure, chorus breakdown, final chorus return` *(the groove becomes comfortable instead of urgent; the 17-minutes-left feeling evaporates)*

### Results

- https://suno.com/s/8TO4ctZnFstsI2Cp
- https://suno.com/s/vV2aBTIAbQSAFTlL
- https://suno.com/s/m7lcQa1sPov7aFjg

### Reference listening

- James Brown — "Get Up (I Feel Like Being a) Sex Machine"
- Parliament — "Flash Light"
- The Meters — "Cissy Strut"
- Sly and the Family Stone — "Thank You (Falettinme Be Mice Elf Agin)"

---

## Creative Mission #6: Rainy Afternoon Loop
### Genre: Lo-Fi Hip-Hop

**Micro-story:** The notebook has been open to the same page for forty minutes. The rain on the window is doing more work than you are. The tea went cold while you were staring at a sentence that turned out to be wrong. This is fine. You have put on music that asks nothing: a loop that cycles through the same warm intervals, the same soft drum hit, the same vinyl crackle that sounds like someone in the next room turning pages. Make that music. Dusty, deliberate, content to repeat.

**Story behind the story:** Lo-fi hip-hop became a recognizable genre in the 2010s through YouTube channels and streaming playlists designed for studying and relaxation. The sound draws from 1990s boom-bap hip-hop, jazz samples, and intentional audio degradation: vinyl crackle, tape hiss, and bit-crushing. The result is nostalgic, warm, and intentionally imperfect, designed to be non-intrusive background music.

### STYLE prompt

> [Lo-Fi Hip-Hop], 85 BPM, 1990s boom-bap, dusty loop aesthetic. Boom-bap kick (soft attack, prominent thud), snare with slight swing, filtered jazz piano chopped into 2-bar loop, warm Rhodes chords, walking electric bass, vinyl crackle and tape hiss throughout, pitch wobble on melodic elements. Still, melancholic, resigned. Instrumental, no vocals. Loop-based: main groove establishes, sparse breakdown strips to kick and crackle, loop re-enters with Rhodes higher in mix, gradual fade. Warm tape saturation, lo-fi coloring, bass-forward mid-focus, dry room, soft transients.

### NEGATIVE prompt

> upbeat, energetic, vocals, singing, bright production, trap hi-hats, EDM drop, reverb-heavy wash

### Version 2 — Nylon-string guitar

Swap `filtered jazz piano chopped into 2-bar loop, warm Rhodes chords` → `filtered nylon-string guitar sample chopped into 2-bar loop, light fingerpicked texture` *(keyboard palette reads as jazz café; guitar reads as someone's living room)*

### Version 3 — Slower, more patient

Swap `85 BPM` → `72 BPM` and `sparse breakdown strips to kick and crackle` → `long breakdown strips to crackle and bass only, extended silence between hits` *(a loop can be dusty at 85 BPM or 72 BPM — but the slower version with more silence stops being wallpaper)*

### Results

- https://suno.com/s/SR38jaTCRF6mmiom
- https://suno.com/s/MlT3jdobrsu0nSYh
- https://suno.com/s/JnaeiPHYbPiEQnJY

### Reference listening

- Nujabes — "Feather"
- J Dilla — "So Far to Go"
- Jinsang — "Affection"
- Ta-ku — "Love Again"

---

## Creative Mission #7: Festival Sunset Moment
### Genre: Progressive House

**Micro-story:** The stage is to your left and the sky has gone that particular shade of orange that makes strangers feel like old friends. You are standing in the middle of a field with ten thousand other people and nobody is talking anymore; everyone stopped at the same moment when the DJ brought the bass back under the pads, and now it's just the melody, the crowd, and that light. This track needs to earn that moment. Build toward something. Make it feel like it was always going to land here.

**Story behind the story:** Progressive house emerged in the early 1990s in the UK, blending house music's four-on-the-floor foundation with longer builds, emotional melodies, and layered synths. Producers like Sasha and John Digweed popularized the genre through extended sets. The "progressive" label refers to how the music evolves over time, not to complexity.

### STYLE prompt

> Progressive house, 124 BPM, classic journey-style progressive groove. Four-on-the-floor kick with heavy sidechain compression on analog pad chords, portamento synth bass with subtle groove swing, layered warm Juno-style pads, acoustic piano hook with light reverb tail, 909 hi-hats building in density across 32 bars. Communal and euphoric mood. Wordless female vocal, breathy upper-register texture, buried mid-mix, not a lead line. Sparse open intro, gradual layering through two extended builds, stripped breakdown with pads-only, full re-entry with kick and bass returning together, no hard drop. Wide festival mix, controlled sub-bass, sidechain pump audible, progressive house groove throughout, clean transients, wet reverb on pads, dry kick.

### NEGATIVE prompt

> big room EDM, supersaw leads, dubstep drop, hard drop, trance anthem, pop ballad, lead vocals, lyrical vocals, breakdown with silence

### Version 2 — Oberheim arpeggio

Swap `acoustic piano hook with light reverb tail` → `arpeggiated Oberheim-style synth hook, staccato, mid-range` *(same structure, different emotional register for when the melody surfaces)*

### Version 3 — Purely instrumental

Swap `Wordless female vocal, breathy upper-register texture, buried mid-mix, not a lead line` → `no vocal elements, purely instrumental, no voice` *(tests whether the emotional lift is carried by the arrangement or by that subliminal human presence)*

### Results

- https://suno.com/s/lkZtfKCEr09wcLrJ
- https://suno.com/s/NYgJjyrByxEVKnYN
- https://suno.com/s/KDUiofjOf3HCUawi

### Reference listening

- Eric Prydz — "Opus"
- deadmau5 — "Strobe"
- Above & Beyond — "Sun & Moon"
- Lane 8 — "Fingerprint"

---

*Fuente original: Reddit r/SunoAI | Compilado y ordenado para uso como repositorio de referencia.*
