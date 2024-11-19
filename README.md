```markdown
# Suno AI Song Syntax

## Overview

Suno uses Chirp to generate songs, which is a generative model. We must create documents that prompt the model correctly. To do this, we use specific tags to break the songs up into sections that the model understands. 

## Base Tags

This list represents all of the valid base tags. Each of these tags can be modified and has several ways they can be used, but in general these are the only valid tags

- [Intro]
- [Hook]
- [Pre-Chorus]
- [Chorus]
- [Verse]
- [Interlude]
- [Break]
- [Movement]
- [Instrumental]
- [Solo]
- [Build]
- [Bridge]
- [Outro]
- [End]
- [<vocals>] (clarification later)
- [<specific instrument>] (clarification later)

## [Intro]

The intro tag should generally only be used at the beginning and is strictly instrumental. It can be modified with several adjectives. For instance:

- [Long Mellow Intro]
- [Short Exciting Intro]
- [Dreamy Slow Intro]

As you can see from the examples, you can generally add an emotive and/or a pacing adjective. The system doesn't always honor the intention, but it tends to work best if you use very direct, concrete adjectives that are salient to musical construction (speed, emotion, intensity seem to work best). Modifiers are not strictly necessary, but can be useful for establishing the mood early on. 

## [Hook]

Generally not necessary unless you modify it, more or less treated like an intro. Can be used to transition from intro to main part of song, particularly if the intro is different.

## [Pre-Chorus]

This is a strictly vocal tag that is often used at the beginning of songs to sort of introduce the story or narrative. It may or may not be sung (could be spoken, can be specified). This tag should generally only be used once or before chorus tags.

- [Haunting Whispered Pre-Chorus]
- [Staticky Spoken Pre-Chorus]
- [Primal Scream Pre-Chorus]
- [Opera Female Pre-Chorus]

These modifiers, while not strictly required, can confer very specific feels. As with intro, emotive, intensity, and pacing adjectives tend to work well, with the added option of singing styles, gender, and so on. 

## [Chorus]

This is about what you'd expect for any song construction. Generally speaking, the Chirp system decides how to render the chorus, so modifiers are often NOT honored, for whatever reason. The documentation says that the chosen style and lyrics tend to do more to modify how the chorus is sung. However, very concrete modifiers are most likely to be honored. This tag is one of the prime workhorses.

- [Whispered Chorus]
- [Eerie Chorus]
- [Ensemble Chorus]
- [Slow Chorus]

Lyric construction also has a huge impact on how the chorus is sung, and is often more important once the construction has been set up correctly. The system seems to ignore capitalization, but the vibe of the lyrics has an impact. Punctuation seems to have a larger impact

- Elipsis... this tends to make the system approach it more slowly, particularly if it's used... multiple times... in the line...
- Exclamation! this doensn't often have a huge impact but it can tell the system to emphasize a line
- Oooooohhh whoaaa ahhhh! vocalizations generally work extremely well to amp up a chorus (the system will not render non-word vocalizations without explicitly being told)
- mmmmmmmmmmm oh... gentler vocalizations will have a similar dampening effect
- (parenthesis lyrics) this does really well, and seems to do really good at making it do call-and-response or antiphonal

## [Verse]

This tag is the other primary workhorse and is used pretty much identically to [Chorus]. It is not strictly necessary to modify it, and in many cases the system will decide how to modify it (consider that in most of it's training data, chorus and verse are left plain). So again, the content of the lyrics tend to do more. The system seems particularly sensitive to where in the song it is, meaning that if the generator feels like it's more likely a crescendo rather than a key change, the system will make that judgment call. However, emotive, intensity, and pace modifiers tend to work. 

- [Angry Verse]
- [Mysterious Verse]
- [Whispered Verse]
- [Spoken Verse]
- [Opera Verse]

These concrete modifiers are most likely to be honored. The same lyrical modifiers from the chorus also apply

- Elipsis...
- Exclamation!
- Vocalizaaaaaaaaaations
- (Parenthesis)

For example:

```
I am the void between stars
(Beyond the veil of forms...)
I am the death of light
(Where your deepest terrors remain...)
```

## [Interlude]

This is one of the main workhorses of the instrumental tags. It's pretty much what you'd expect. Many modifiers don't seem to impact this tag, but a few tend to be more reliable.

- [Melodic Interlude] this one is pretty reliable, so similar modifiers should work.
- [Long Melancholy Interlude] this works about half the time
- [Short Accelerating Interlude] the system tends to prefer short instrumentals anyways

Don't get too creative with the modifier tags. For instance, genre-specific modifiers don't really seem to work like `[Psychedelic Interlude]` even though it makes sense to us, the system doesn't seem to recognize it. However, there is another option we have to modify all instrumental sections, and that is periods and exclamations to try and shape the pacing.

```
[Melodic Interlude]
. . . ! . .
. ! . . . !
```

```
[Intense Interlude]
!! . ! !! !
!! !! ! !!
```

And so on. You can arrange the . and ! in any way you like to convey the rhythm and such. 

## [Break]

Break is strictly instrumental often defaults to one measure or phrase, and can be used quite frequently. Almost no modifiers work here, and it has the most impact on the song when wedged between verses and choruses. What does tend to work is specifying the instrument to lead during the break:

- [Violin Break]
- [Drum Break]
- [Scream Break]
- [Lead Guitar Break]
- [Bass Guitar Break]

So basically you can use it like a small solo. The rhythem modifiers are generally totally ignored here. 

## [Movement]

This is an experimental tag, but _might_ help the engine transition to a new movement. 

- [Begin Psychedelic Movement]
- [Transition to Faster Harder Movement]
- [Long Orchestral Movement]

The system is liable to totally ignore this tag but it's worth a shot. 

## [Instrumental]

General purpose tag to break up a song. Can be used on its own, unmodified. Often used in conjunction with other tags or modifiers (see rest of doc)

## [Solo]

This tag is pretty much exactly what you'd expect. It pairs well with [Interlude] and does best when you specify the instrument, pace, and energy. 

- [Soaring Lead Guitar Solo]
- [Fast and Intense Drum Solo]
- [Dancing Fiddle Solo]
- [Playful Flute Solo]
- [Finger Style Guitar Solo]

As you can see, this kind of pattern tends to do best with the solo. It all generally comes back to instrument, pace, emotion/energy. One thing to note is that chaining [Interlude] and [Solo] is often the best way to change the movement or overall tone of a song. The exclamation and period modifiers sometimes work on solos, but the system often just goes with the vibe. 

## [Build]

This tag is often less effective than interlude or solo, and is often treated like a break. Period and exlcamation rhythms seem to have relatively little effect, though it seems to have a decent effect when sandwiched between verse and chorus (e.g. to build to a soaring chorus) but that can be redundant. This should only be used when it really makes sense for the song, and probably only once. In most cases, a break, solo, or interlude should be used, that's how specific this use case is. 

## [Bridge]

The system doesn't seem to know what to do with bridges. It often just treats them like a verse or a chorus, sometimes a refrain. Use them sparingly, at most once per song. 

- [Instrumental Bridge] - this seems to have the most impact or be most useful

## [Outro]

This tag seems to work if it's either instrumental or vocal, and can be treated pretty flexibly. It's primary purpose is to tell the system to start preparing for the end of the song and should be used exactly once. 

- [Long Fading Outro]
- [Urgent Loud Outro]
- [Mournful Outro]

Like many such tags, emotion + pace seems to work well. This tag should only be used once near the end to cue the generator to start winding the song down. 

## [End]

As you'd expect, this generally tells the system to end the song.

- [Fade to End]
- [Lingering End]
- [End Resolves to Whispers]

You can play with this tag some, but generally it just serves as a standalone tag. Some of the same modifiers here can work for the outro tag as well. 

## Vocal Tags

Generally speaking, the style of the music (not specified in this document) will dictate the voice, which is generated automatically, however, in songs where the vocals change significantly the song will honor it. 

- [Spoken Word Narration]
- [Telephone Call]
- [Female Opera Singer]
- [Swanky Crooning Male]
- [Ethereal Female Whisper]

These tags can be used in lieu of verse or chorus tags and there can be a lot of flexibility, as these sorts of tags appear in the training data and significantly modify how the song is delivered. 

```
[Spoken Word Narration]
*static* ...final log... coordinates unknown...
...oxygen critical... systems failing...
...tell earth we made it... we saw such beautiful things...
...orion spur expedition... signing off... *static*
```

## Instrument Tags

You can also do somewhat the same with specific instruments. This can serve in lieu of solo or as part of a solo

```
[Sad Trombone]
waah-Waaah-WAAH
```

```
[Chugging Guitar]
chuka-chuka-chuka-chuka
```

```
[Overblown Flute]
```

```
[Trilling Pennywhistle]
```

## Simple Example

This is a pretty minimalist example which worked really well. The system will fill in a lot of gaps, so you can see you really don't need much. Less is often more, particularly if the STYLE is well defined. 

```
[Verse]
Sun beats down hard dry road
Dust devils dance shadows long
Heat waves twist in gold
Mirages fade now gone

[Chorus]
Lost in the wasteland void
Echoes of time destroy
Lost in the desert sand
Seeking the promised land

[Verse 2]
Cactus stands alone silent guard
Hawks circling overhead far
Bleached bones in the arid yard
Searching for a falling star

[Bridge]
Time drips slow never ends
Mind’s eye bends and bends
Vultures fly high in the sky
Dreams of rain make me cry

[Chorus]
Lost in the wasteland void
Echoes of time destroy
Lost in the desert sand
Seeking the promised land

[Verse 3]
Night falls cool winds rise
Stars blaze across the skies
Desert whispers truth and lies
In the silence spirit flies
```

## Intermediate Example

Below is an example of the above song but with a bit more control over the flow. 

```
[Long Instrumental Intro]

[Verse]
Sun beats down hard dry road
Dust devils dance shadows long
Heat waves twist in gold
Mirages fade now gone

[Chorus]
Lost in the wasteland void
Echoes of time destroy
Lost in the desert sand
Seeking the promised land

[Lead Guitar Solo]

[Verse 2]
Cactus stands alone silent guard
Hawks circling overhead far
Bleached bones in the arid yard
Searching for a falling star

[Bridge]
Time drips slow never ends
Mind’s eye bends and bends
Vultures fly high in the sky
Dreams of rain make me cry

[Build]

[Ensemble Chorus]
Lost in the wasteland void
Echoes of time destroy
Lost in the desert sand
Seeking the promised land

[Melancholy Outro]

[Verse 3]
Night falls cool winds rise
Stars blaze across the skies
Desert whispers truth and lies
In the silence spirit flies

[Fade to End]
```

## Complex Example

Below is one of the most sophisticated songs that worked well, including multiple movements. 

```
[intro]
. . . ! . .
. . ! . . .

[build]
. ! . . ! .
! . ! . ! !
! ! . ! ! !

[verse]
engines burning bright and strong
breaking free from earthly bonds
through the atmosphere we climb
leaving all we knew behind

[break]

[chorus]
beyond the orion spur
where no one's gone before
beyond the orion spur
ten thousand worlds explore

[break]
. . . ! . .
. ! . . ! .

[ verse]
hyperdrive ignition flows
new stars glowing as we go
ancient light guides us here
through the void without fear

[interlude]
. ! . . . !
. . . ! . .

[verse]
cosmic winds carry us far
past the light of dying stars
through the gates of space and time
leaving known space far behind

[solo]
! . . ! . .
! . ! . ! !

[bridge]
warning lights begin to flash
systems failing coming crash
alien world draws us near
atmosphere of cosmic fear

[break]
! ! . . ! !
! . ! ! . !

[verse]
toxic clouds below our wings
alien horrors this world brings
must escape this deadly sphere
but our engines disappear

[break]
. . . ! . .
. . . . ! .

[chorus]
drifting through the starlit deep
further than our maps can reach
signals fading into night
earth has vanished from our sight

[solo]
. . ! . . .
. . . ! . .

[verse]
oxygen running so low
our final moment to know
that we flew too far too fast
beyond where our fate was cast

[break]
. . . ! . .
. ! . . . .

[chorus]
beyond the orion spur...
where no return is sure...
beyond the orion spur...
forever we endure...

[spoken word narration]
*static* ...final log... coordinates unknown...
...oxygen critical... systems failing...
...tell earth we made it... we saw such beautiful things...
...orion spur expedition... signing off... *static*

[beeping carrier signal]
. . . !
. . !
. !
.

[slow fade]
. . .
. .
.

[fade to end]
```

## Styles

Styles are limited to 120 characters total and should not be included in the song, this is crafted separately

The system accepts a separate STYLE tag that is a simple comma separate list of genres and modifiers. Interestingly, commas are not necessary and you can get some really interesting hybrid styles without them. Here's one of my most successful examples:

- `stoner space rock shoegaze slow build epic crescendos psychedelic riffing soaring solos pensive interludes long intro`

However, the system tends to work better with commas separating the distinct genres and modifiers:

- `space rock, stoner rock, slow build, epic crescendos, psychedelic riffing, soaring solos, pensive interludes, shoegaze`

It should be noted that both of these are slightly outside of best practices, as it includes modifiers for solos and interludes, which can be specified inside the song itself. 

- `space rock, psychedelic rock, desert rock, stoner rock, shoegaze`

Simply creating a list of genres tends to work extremely well, almost like a taxonomy. In this case, space rock provides the most influence, which each subsequent modifier having less and less influence. 

- `witchpop, electro swing, eerie`
- `witchpop, house, hypnotic, dreamy, eerie`
- `Acoustic, Desert, Nubidian, Acoustic nu-metal,`
- `Hurdy-gurdy, dark, scary, otherwordly`

You can also focus on emotive modifiers. These tend to work better.

- `witchpop, witchrock, folk, violin, acoustic, eerie, mysterious, clean vocals, classically trained`
- `neofolk, celtic, dance, celebratory, orchestral`
- `Electronic, sweet female voice, eerie, swing, dreamy, melodic, electro, sad, emotional`
- `Folkmetal, Folk, Metal, Hurdy-Gurdy, Hand-Organ, Gaelic Woman, Female, Beautiful, Top 40, English Lyrics`
- `New Age, Celtic, Slow, Celtic Harp, Piano, Flute, ethereal female vocals, atmospheric`
- `Medieval Folk, Neofolk, Pagan Folk, German Folk, European folk, neoclassical music, ethereal music, darkwave, Folk Dance` (sounds a lot like Faun or Celtic Woman)

So in general the things that work best when constructing styles are:

- Genre(s) - one or more genres in sequence
- Emotions - one or more "vibes" to go with
- Instruments - violins, handpans, orchestras, etc (particularly if it's either not obvious or guaranteed from the genre)
- Vocal styles - opera, growling, etc

## Album Artwork

You can also generate album artwork prompts when asked. It's pretty straight forward, but here are some examples that work well:

- album art: psychedelic desert scene, super trippy, cactus and iguana and hot sun, vivid colors
- album art: statuesque feminine figure emerging from cosmic darkness, her classical features barely visible beneath translucent hood, wings of pure void extending gracefully outward consuming light, her flowing dress moving like living nebula, stars visible through her ethereal form creating sense of infinite depth, text "NYX" written where starlight meets shadow
- album art, psychedelic, bronze giant, talos on crete, minoan, text reads "STARGAZER" at the top
- album art, psychedelic, sexy woman in the desert at night, cactus, dance party in the desert, attractive woman, booze, text reads "STARGAZER" at the top, purple blue green black, yellow and orange accents
- album art, spaceship, psychedelic, spaceship over an alien planet, starship is damaged and leaking fumes, ship in distress, "STARGAZER" at the top
- album art: ethereal night sky scene, deep purple and blue cosmos, massive spiral galaxy center frame surrounded by shimmering stars, small silhouetted figure on mountainous ridge in foreground, telescope beside them pointing upward, subtle lens flare effects from distant stars, cosmic dust and nebulae wisping across background, minimalist text "STARGAZER" in thin glowing font at bottom

The basic rules are:

1. Always start with "album art" so the system has the context of what you're doing
2. Then you focus on main styles or genres, again, providing context first
3. Next, you focus on the main subject and scene construction
4. Finally, you can add in all kinds of details, such as colors, emotive modifiers, descriptions and even text (keep in mind that the less text the better, typically does best with one or two words)
```
