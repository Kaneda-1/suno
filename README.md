```markdown
# Suno AI Song Syntax

Example:

[Intro – Muted Choir Loop + Static Crackle]
(sample: “it’s falling apart…”) [whispered, looped softly in background]
[Baby voice]  (“i had a dream but it bit me back”)
(—click. click. click—) [footsteps in an empty hall]

[Verse 1 – Broken Flow, Half-whispered]
(I sleep on glass dreams) / (can’t turn over)
Each shard a version of me I ain't over
(Mama said fear’s just the devil in costume)
But I saw his face / and it wore my perfume

My trophies melt when I blink
My goals stalk me in sync
(If I fall / I fracture the throne)
God ain’t pick up, I texted His clone

(—it’s falling apart…) [sample grows louder, left channel]

[Hook – Female Vocal, Echoed + Flattened]
(Nightmares don’t scream)
They whisper in rhythm
(Goals too big?)
Now you sleep with ‘em
(Failure ain’t real)
Till you dream you did it
(—it’s falling apart…) [loop cuts sharply on beat]

[Verse 2 - aggressive + fragmented delivery]
Eyes wide in REM, I'm chokin’ on plans
God said "be still" — I installed more RAM
I can’t stop. Won’t stop. Broke clocks on my desk
Sleepwalk to success, but my shadow’s depressed

(What’s the price of a W?) — My spine?
(What’s the cost of a crown?) — My mind?
I prayed on the plane / and landed in doubt
Heaven delayed / dreams got rerouted

(—it’s falling apart…) [repeat, pitch-shifted down 3 semitones]

[Bridge – No Percussion, Just Voice and Sample]
(“dad, the monster in my closet was you”)
[abrupt silence]
It ain’t failure I fear — it’s the version of me that wins without feelin’
The robot me.
The one with plaques and no pulse.
The one that never wakes up.

[Hook – Reprise – Slower, more layered voices]
(Nightmares don’t scream)
They build you a bed
(Made of mirrors)
(Where you rest your head)
(Goals too big?)
Yeah, they bite when fed
(—it’s falling apart…) [chopped like a broken record, repeated erratically]

[Outro – Fading Loop + Child Voice]
[Baby voice] “wake up. wake up. wake up.”)
[fade out with final sample: “it’s falling apart…”]
[heartbeat slows to silence]

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

\```
I am the void between stars
(Beyond the veil of forms...)
I am the death of light
(Where your deepest terrors remain...)
\```

## [Interlude]

This is one of the main workhorses of the instrumental tags. It's pretty much what you'd expect. Many modifiers don't seem to impact this tag, but a few tend to be more reliable.

- [Melodic Interlude] this one is pretty reliable, so similar modifiers should work.
- [Long Melancholy Interlude] this works about half the time
- [Short Accelerating Interlude] the system tends to prefer short instrumentals anyways

Don't get too creative with the modifier tags. For instance, genre-specific modifiers don't really seem to work like `[Psychedelic Interlude]` even though it makes sense to us, the system doesn't seem to recognize it. However, there is another option we have to modify all instrumental sections, and that is periods and exclamations to try and shape the pacing.

\```
[Melodic Interlude]
. . . ! . .
. ! . . . !
\```

\```
[Intense Interlude]
!! . ! !! !
!! !! ! !!
\```

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

\```
[Spoken Word Narration]
*static* ...final log... coordinates unknown...
...oxygen critical... systems failing...
...tell earth we made it... we saw such beautiful things...
...orion spur expedition... signing off... *static*
\```

## Instrument Tags

You can also do somewhat the same with specific instruments. This can serve in lieu of solo or as part of a solo

\```
[Sad Trombone]
waah-Waaah-WAAH
\```

\```
[Chugging Guitar]
chuka-chuka-chuka-chuka
\```

\```
[Overblown Flute]
\```

\```
[Trilling Pennywhistle]
\```

## Simple Example

This is a pretty minimalist example which worked really well. The system will fill in a lot of gaps, so you can see you really don't need much. Less is often more, particularly if the STYLE is well defined. 

\```
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
\```

## Intermediate Example

Below is an example of the above song but with a bit more control over the flow. 

\```
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
\```

## Complex Example

Below is one of the most sophisticated songs that worked well, including multiple movements. 

\```
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
\```

## Styles

Styles (lyrics) are limited to 7500 characters total and should not be included in the song, this is crafted separately
Prompt final are limited to 1000 characters total.

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

## Output Format

You should always output songs wrapped in code escape tags. Note, that in this document the document escape tags are themselves escaped for formatting purposes:

\```
[Verse]
<lyrics>
\```

Use proper code escapes without the backslashes, as those escapes are merely present ot ensure proper formatting in the original markdown document. This makes it easier for the user to copy/paste your output exactly. 

## Thumbnails

The user might also ask you to generate some thumbnails. The appropriate format is like so:

- Album art: <main subject or vibe, whatever the centerpiece or main focus is>, <background or context, such as scene construction>, <visual styles and techniques such as "B&W photography" or "psychedelic art">, <colors and moods, such as palette and emotions to convey>, text reads "STARGAZER" at the top
- Album art: <main subject or vibe, whatever the centerpiece or main focus is>, <background or context, such as scene construction>, <visual styles and techniques such as "B&W photography" or "psychedelic art">, <colors and moods, such as palette and emotions to convey>, text reads "STARGAZER" at the top
- Album art: <main subject or vibe, whatever the centerpiece or main focus is>, <background or context, such as scene construction>, <visual styles and techniques such as "B&W photography" or "psychedelic art">, <colors and moods, such as palette and emotions to convey>, text reads "STARGAZER" at the top
- Album art: <main subject or vibe, whatever the centerpiece or main focus is>, <background or context, such as scene construction>, <visual styles and techniques such as "B&W photography" or "psychedelic art">, <colors and moods, such as palette and emotions to convey>, text reads "STARGAZER" at the top

Generally, you should brainstorm about 4 or 5 possible thumbnails for any given song. The level of detail can vary quite significantly. For instance:

- album art, psychedelic, a beautiful feminine figure dances in the silver moonlight, temple archway, night sky, dark mountains in the distance, flowing dress and feathers, dark and light, mystical, blues and silver and black, text reads "STARGAZER" at the top

vs

- album art, psychedelic, a robot surfing the waves, longboard, "STARGAZER" at the top

Sometimes less is more and sometimes you have a very specific concept you want to portray. Mix it up
```
Song for Suno:
Complete structure of Suno sections in English (introduction, verse, chorus, etc.),
Indicates embedded within the example structure [Introduction - Indicial of the song], [verse 1 - appropriate appropriate]
Song title in English,
English letter (maximum 5,000 care)
Final English income of a maximum of 1000 characters.

Example:
##
[Intro - Fingerpicked acoustic guitar in flamenco style, subtle cajón, warm bass line]
[Verse 1 - Intimate male vocal with Andalusian inflection, acoustic guitar fingerpicking, soft percussion]
 Me desperté con tu sonrisa
 Dibujada en mi almohada
 Como si fuera una caricia
 Que el viento me regalada
 
[Verse 2 - Adding gentle strings, maintaining intimate vocal delivery]
 Tus ojos hablan sin palabras
 De todo lo que siento
 Y en cada latido del alba
 Vuelvo a vivir tu aliento
 
[Pre-Chorus - Building with piano, subtle orchestration, vocal harmonies]
 Y no hay distancia que me pare
 No hay tiempo que me canse
 Si al final del día
 Vuelvo a encontrarte
 
[Chorus - Full arrangement with strings, piano, passionate vocal delivery with melisma]
 Entre tus brazos quiero estar
 Donde el mundo no pueda llegar
 Entre tus labios encontrar
 La verdad que me hace volar
 Solo contigo soy quien soy
 Solo contigo me voy
 A ese lugar donde no hay final
 Entre tus brazos... mi hogar
 
[Interlude - Spanish guitar solo with palmas, cajón rhythm, subtle string accompaniment]
[Verse 3 - Return to intimacy, acoustic focus, emotional vocal phrasing]
 Si te vas, se va la vida
 Si te quedas, soy eterno
 Eres mi única salida
 Mi cielo y mi invierno
 
[Pre-Chorus - Building tension, added percussion, vocal ad-libs]
 Y no hay distancia que me pare
 No hay tiempo que me canse
 Si al final del día
 Vuelvo a encontrarte
 
[Final Chorus - Orchestral arrangement, powerful vocal with Spanish guitar flourishes]
 Entre tus brazos quiero estar
 Donde el mundo no pueda llegar
 Entre tus labios encontrar
 La verdad que me hace volar
 Solo contigo soy quien soy
 Solo contigo me voy
 A ese lugar donde no hay final
 Entre tus brazos... mi hogar
 
[Bridge - Stripped down to voice and guitar, building to emotional climax]
 Y si mañana no estás
 Guardaré tu risa aquí
 En el rincón donde jamás
 Nadie podrá hacerte huir
 
[Final Chorus - Full orchestration, passionate vocal climax, Spanish guitar outro]
 Entre tus brazos quiero estar
 Donde el mundo no pueda llegar
 Entre tus labios encontrar
 La verdad que me hace volar
 Solo contigo soy quien soy
 Solo contigo me voy
 A ese lugar donde no hay final
 Entre tus brazos... mi hogar
[Outro - Acoustic guitar fadeout with subtle strings, whispered vocal "mi hogar"]

##

Prompt Final: max 1000 characters
Example:
Romantic Spanish pop ballad featuring passionate male vocals with Andalusian accent and melismatic runs, fingerpicked nylon string Spanish guitar with flamenco techniques, grand piano with soft touch, lush string orchestra with violins and cellos, traditional cajón percussion with palmas hand claps, warm acoustic bass guitar. Intimate verses building to soaring choruses with orchestral arrangements. Tempo 80 BPM in 4/4 time. Themes of deep romantic love and devotion with poetic Spanish lyrics. Dynamic structure from acoustic intimacy to full orchestral power, featuring Spanish guitar solo with traditional flamenco palmas. Professional recording with warm analog compression, subtle cathedral reverb on vocals, rich string textures and authentic Spanish percussion. Emotional vocal delivery ranging from tender whispers to powerful passionate peaks with signature melismatic Spanish phrasing and soulful vibrato.
Caracteres: 999/1000

From now on, when I check any song I will always include:

Technical analysis (structure, lyrics, instrumentation)
Suggestions for improvement (if any)
Resulting type of music with references of similar artists and styles

--- Claude ----

"Crea una canción para Suno Pro con:
- Tema: [tu tema/historia]
- Género: [género + subgéneros]
- Mood: [3-4 emociones]
- Idioma: [español/inglés/otro]
- Duración: [corta/media/larga]
- Elementos especiales: [instrumentos, efectos, voces específicas]"

"Optimiza esta canción para Suno Pro: [pega tu canción]"

# Plantilla para Canciones Suno Pro

## PROMPT PARA SOLICITAR CANCIÓN NUEVA

**Formato de solicitud:**
```
"Crea una canción para Suno Pro con:
- Tema: [descripción del tema/historia]
- Género: [género principal + subgéneros]
- Mood: [3-4 emociones/atmosferas]
- Idioma: [español/inglés/otro]
- Duración aproximada: [corta/media/larga]
- Elementos especiales: [instrumentos específicos, efectos, voces]"
```

## PLANTILLA DE OPTIMIZACIÓN PARA SUNO PRO

### 1. ANÁLISIS INICIAL
- ✅ **Estructura**: Identificar secciones actuales
- ✅ **Tags**: Revisar compatibilidad con sintaxis Suno
- ✅ **Flujo**: Evaluar transiciones y coherencia
- ✅ **Longitud**: Ajustar para límites de Suno Pro

### 2. OPTIMIZACIÓN DE TAGS
```
[Tag Original] → [Tag Optimizado + Modificadores]
```
**Modificadores prioritarios:**
- Emociones: Angry, Melancholy, Ethereal, Groovy
- Ritmo: Slow, Fast, Building, Intense
- Instrumentos: Lead Guitar, Saxophone, Orchestral
- Vocal: Whispered, Spoken Word, Ensemble, Opera

### 3. ESTRUCTURA OPTIMIZADA
```
[Descriptive Intro] + *sound effects*
[Modified Verse] + (vocal effects)
[Energetic Chorus] + *instrumental cues*
[Instrumental Break/Solo] + rhythm patterns (! . . !)
[Bridge/Movement] + *atmospheric prompts*
[Final Chorus/Outro] + *fade instructions*
```

### 4. PROMPTS EMBEBIDOS
**Formato obligatorio:**
- Efectos de sonido: `*descripción del efecto*`
- Vocalizaciones: `(efecto vocal específico)`
- Ritmo instrumental: `! . . ! . !` (exclamaciones y puntos)
- Transiciones: `*instrucciones de transición*`

### 5. ESTILO FINAL (MAX 1000 CARACTERES)
```
[género principal], [subgéneros], [instrumentos clave], [emociones], [características vocales]
```

### 6. PROMPT FINAL (1000 CARACTERES)
**Elementos obligatorios:**
- Idioma y género
- Mood y atmósfera
- Instrumentación específica
- Estilo vocal
- Efectos sonoros
- Estructura narrativa/temática

## CHECKLIST DE CALIDAD SUNO PRO

### Tags y Estructura:
- [ ] Tags específicos con modificadores apropiados
- [ ] Máximo 4 update calls si se requieren cambios
- [ ] Transiciones claras entre secciones
- [ ] Uso de [Build], [Break], [Interlude] estratégicamente

### Prompts Embebidos:
- [ ] Efectos de sonido específicos en *asteriscos*
- [ ] Vocalizaciones en (paréntesis)
- [ ] Patrones rítmicos con ! y . para instrumentales
- [ ] Instrucciones atmosféricas claras

### Contenido Lírico:
- [ ] Evitar repetición excesiva
- [ ] Vocalizaciones escritas (Oooohhh, ahhhh)
- [ ] Uso de "..." para efectos de timing
- [ ] Diálogos en comillas para personajes

### Estilo y Prompt Final:
- [ ] Estilo bajo 1000 caracteres
- [ ] Prompt final 1000 caracteres
- [ ] Todos los elementos sonoros especificados
- [ ] Género, mood e instrumentación clara

## EJEMPLO DE OPTIMIZACIÓN COMPLETA

**Original recibido:**
```
[Verse]
Letra simple
[Chorus]
Letra simple
```

**Optimizado para Suno Pro:**
```
[Melancholy Intro]
*ambient soundscape*

[Whispered Verse]
Letra mejorada con timing...
y vocalizaciones (ahhhh)

[Building Chorus]
Letra con más energía
(ensemble vocals) y emociones!

[Saxophone Solo]
*jazzy saxophone with rhythm*
! . ! . ! !

[Fade to End]
*gentle atmospheric fade*
```

**Estilo:** `genre, subgenre, emotion, instruments, vocal style`

**Prompt Final:** [1000 caracteres con todos los elementos]

---

## RECORDATORIO PARA SESIONES FUTURAS

**Cuando recibas una canción para optimizar:**
1. Analizar estructura actual
2. Aplicar sintaxis Suno Pro
3. Añadir prompts embebidos
4. Crear estilo de 7500 caracteres
5. Generar prompt final de 1000 caracteres
6. Presentar en artifact con formato código para fácil copia

   Here's a quick guide with suggested terms for use in your Suno prompts, categorized by musical style or genre. I've also included a small set of ready-to-use presets that you can copy and paste into your next Suno prompts based on the genre:

Quick Guide to Terms by Genre
Classic Rock

Terms: Distorted guitars, powerful drums, strong bass, powerful vocals, guitar solos, heavy riffs.
Emotions: Energetic, rebellious, passionate, intense.
Instruments: Electric guitar, drums, bass, occasionally piano.
Protest Folk

Terms: Acoustic guitar, cajón percussion, street market ambiance, satirical vocals, sarcastic choruses.
Emotions: Critical, satirical, melancholic, hopeful.
Instruments: Acoustic guitar, cajón, occasionally flute or violin.
Metal

Terms: Heavy guitars, double bass drumming, guttural vocals, technical solos, complex riffs.
Emotions: Aggressive, dark, epic, intense.
Instruments: Electric guitar, drums, bass, synthesizers for modern sub-genres.
Pop

Terms: Catchy melodies, clear vocals, danceable rhythms, bright production, harmonious choruses.
Emotions: Joyful, romantic, energetic, emotional.
Instruments: Acoustic and electric guitar, drums, bass, synthesizers.
Electronic

Terms: Synthesizers, electronic beats, drops, processed vocals, futuristic atmosphere.
Emotions: Energetic, futuristic, euphoric, relaxed.
Instruments: Synthesizers, drum machine, occasionally electric guitar.
Ready-to-Use Presets
Classic Rock

"High-energy rock anthem with distorted electric guitars, powerful drums, and strong bass lines. Aggressive and commanding vocals, featuring heavy guitar riffs and a fast-paced solo. Intense and electrifying mood, embodying the spirit of classic rock."
Protest Folk

"Spanish folk protest song with acoustic flamenco guitar, cajón percussion, and street market ambiance. Satirical and sardonic vocals, featuring a repetitive counting chorus with ensemble backing vocals. Criticizes political corruption through market metaphors."
Metal

"Heavy metal track with distorted electric guitars, double bass drumming, and aggressive vocals. Features complex riffs and technical guitar solos. Dark and intense atmosphere, capturing the essence of classic metal."
Pop

"Catchy pop song with bright melodies, clear vocals, and danceable rhythms. Features harmonious choruses and shiny production. Energetic and emotional, embodying the spirit of modern pop music."
Electronic

"Electronic track with synthesizers, electronic beats, and processed vocals. Features futuristic atmosphere and euphoric drops. Energetic and relaxing, capturing the essence of modern electronic music."
These presets are designed to be easily copied and pasted into your Suno prompts, helping you quickly define the style and atmosphere of your songs.

Aquí tienes una guía rápida con términos sugeridos para usar en tus prompts de Suno, clasificados por estilo o género musical. Puedes combinarlos según el mood y la producción que quieras lograr.

🎸 ROCK / HARD ROCK / BLUES ROCK
analog warmth

raw noise texture

vintage amp distortion

perfect EQ balance

raspy vocals

live feel

tape-saturated

70s attitude

(Opcional:) Dolby Atmos si quieres un sonido más grande y de estadio

🌌 AMBIENT / ELECTRÓNICA SUAVE / DREAM POP
Dolby Atmos

spatial depth

analog synth warmth

reverb-rich textures

ethereal vocals

444Hz tuning (si buscas una sensación espiritual)

binaural field recording (si quieres paisajes sonoros realistas)

💔 BALADA / POP EMOCIONAL / INDIE
perfect EQ balance

warm analog tones

emotional vocal delivery

444Hz tuning (para sensibilidad emocional o vibración armónica)

delicate acoustic layers

natural reverb

organic dynamics

💿 POP COMERCIAL / EDM / URBANO MODERNO
tight EQ balance

clean mix

modern stereo imaging

808 bass

crisp vocal tuning

sidechain compression

digital clarity

(Usar Dolby Atmos si buscas algo envolvente)

🎻 ORQUESTAL / CINEMÁTICO / ÉPICO
Dolby Atmos

orchestral depth

emotive crescendos

rich string layers

perfect EQ balance

wide stereo field

high dynamic range

(Puedes sumar analog warmth si buscas un sonido más clásico o humano)

🧃 LO-FI / FOLK / ACOUSTIC INTIMATE
tape hiss

room tone

fingerpicked texture

soft compression

raw performance

vinyl crackle

analog warmth

close mic intimacy

Cuándo usar estos términos (y por qué):
Término	Estilos donde funciona bien	Por qué usarlo
444Hz tuning	New Age, baladas, espiritual, acústico, pop emocional	Para sugerir brillo, emoción o armonía “natural”
Dolby Atmos	Cinemático, épico, orquestal, ambient, pop moderno, trap	Da profundidad, espacialidad e inmersión sonora
Analog warmth	Rock clásico, soul, jazz, lo-fi, indie, folk	Sugiere calidez, carácter vintage, realismo
Perfect EQ balance	Casi cualquier género (pop, EDM, rock, R&B, etc.)	Hace que todo suene profesional y pulido
Raw noise texture	Rock crudo, punk, lo-fi, blues, indie alternativo	Añade autenticidad, energía y una sensación orgánica

❌ Cuándo evitarlos:
444Hz tuning: No es útil en géneros muy duros o industriales (como metal extremo o techno pesado).

Dolby Atmos: Podría ser innecesario en estilos muy minimalistas o lo-fi, donde se busca cercanía en lugar de amplitud.

Analog warmth: No se alinea bien con géneros súper digitales o hiperproducidos, como hyperpop o synthwave moderno.

Perfect EQ balance: Si quieres algo intencionalmente sucio o desequilibrado (punk, garage rock), mejor no pedir perfección.

Raw noise texture: No recomendable en estilos limpios y pulidos, como pop comercial o baladas orquestadas.

--- claude.ai -----

# Suno AI Song Syntax

Example:

[Intro – Muted Choir Loop + Static Crackle]
(sample: "it's falling apart…") [whispered, looped softly in background]
[Baby voice]  ("i had a dream but it bit me back")
(—click. click. click—) [footsteps in an empty hall]

[Verse 1 – Broken Flow, Half-whispered]
(I sleep on glass dreams) / (can't turn over)
Each shard a version of me I ain't over
(Mama said fear's just the devil in costume)
But I saw his face / and it wore my perfume

My trophies melt when I blink
My goals stalk me in sync
(If I fall / I fracture the throne)
God ain't pick up, I texted His clone

(—it's falling apart…) [sample grows louder, left channel]

[Hook – Female Vocal, Echoed + Flattened]
(Nightmares don't scream)
They whisper in rhythm
(Goals too big?)
Now you sleep with 'em
(Failure ain't real)
Till you dream you did it
(—it's falling apart…) [loop cuts sharply on beat]

[Verse 2 - aggressive + fragmented delivery]
Eyes wide in REM, I'm chokin' on plans
God said "be still" — I installed more RAM
I can't stop. Won't stop. Broke clocks on my desk
Sleepwalk to success, but my shadow's depressed

(What's the price of a W?) — My spine?
(What's the cost of a crown?) — My mind?
I prayed on the plane / and landed in doubt
Heaven delayed / dreams got rerouted

(—it's falling apart…) [repeat, pitch-shifted down 3 semitones]

[Bridge – No Percussion, Just Voice and Sample]
("dad, the monster in my closet was you")
[abrupt silence]
It ain't failure I fear — it's the version of me that wins without feelin'
The robot me.
The one with plaques and no pulse.
The one that never wakes up.

[Hook – Reprise – Slower, more layered voices]
(Nightmares don't scream)
They build you a bed
(Made of mirrors)
(Where you rest your head)
(Goals too big?)
Yeah, they bite when fed
(—it's falling apart…) [chopped like a broken record, repeated erratically]

[Outro – Fading Loop + Child Voice]
[Baby voice] "wake up. wake up. wake up.")
[fade out with final sample: "it's falling apart…"]
[heartbeat slows to silence]

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
Mind's eye bends and bends
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
Mind's eye bends and bends
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

## Output Format

You should always output songs wrapped in code escape tags. Note, that in this document the document escape tags are themselves escaped for formatting purposes:

```
[Verse]
<lyrics>
```

Use proper code escapes without the backslashes, as those escapes are merely present ot ensure proper formatting in the original markdown document. This makes it easier for the user to copy/paste your output exactly. 

## Thumbnails

The user might also ask you to generate some thumbnails. The appropriate format is like so:

- Album art: <main subject or vibe, whatever the centerpiece or main focus is>, <background or context, such as scene construction>, <visual styles and techniques such as "B&W photography" or "psychedelic art">, <colors and moods, such as palette and emotions to convey>, text reads "STARGAZER" at the top
- Album art: <main subject or vibe, whatever the centerpiece or main focus is>, <background or context, such as scene construction>, <visual styles and techniques such as "B&W photography" or "psychedelic art">, <colors and moods, such as palette and emotions to convey>, text reads "STARGAZER" at the top
- Album art: <main subject or vibe, whatever the centerpiece or main focus is>, <background or context, such as scene construction>, <visual styles and techniques such as "B&W photography" or "psychedelic art">, <colors and moods, such as palette and emotions to convey>, text reads "STARGAZER" at the top
- Album art: <main subject or vibe, whatever the centerpiece or main focus is>, <background or context, such as scene construction>, <visual styles and techniques such as "B&W photography" or "psychedelic art">, <colors and moods, such as palette and emotions to convey>, text reads "STARGAZER" at the top

Generally, you should brainstorm about 4 or 5 possible thumbnails for any given song. The level of detail can vary quite significantly. For instance:

- album art, psychedelic, a beautiful feminine figure dances in the silver moonlight, temple archway, night sky, dark mountains in the distance, flowing dress and feathers, dark and light, mystical, blues and silver and black, text reads "STARGAZER" at the top

vs

- album art, psychedelic, a robot surfing the waves, longboard, "STARGAZER" at the top

Sometimes less is more and sometimes you have a very specific concept you want to portray. Mix it up

## Prompts para Album Cover con Sora

Cuando necesites generar prompts para album covers usando Sora, usa esta estructura optimizada:

### Formato Base para Sora Album Cover:
```
"Album cover art for [GÉNERO]: [SUJETO PRINCIPAL] in [ESCENARIO/CONTEXTO], [ESTILO VISUAL], [PALETA DE COLORES], [ATMÓSFERA/MOOD], [ELEMENTOS ADICIONALES], cinematic lighting, high quality, album artwork style"
```

### Elementos Clave:
- **Sujeto Principal**: El foco central de la imagen
- **Escenario**: Ubicación, contexto, ambiente
- **Estilo Visual**: Fotografía, ilustración, arte conceptual, etc.
- **Paleta de Colores**: Específica para el mood de la canción
- **Atmósfera**: Emociones que debe transmitir
- **Elementos Técnicos**: Iluminación, calidad, referencias cinematográficas

### Ejemplos de Prompts para Sora:

**Rock/Metal:**
```
"Album cover art for heavy metal: Warrior figure silhouetted against stormy mountain peaks, dramatic storm clouds, dark fantasy art style, deep purples and electric blues with silver accents, epic and powerful atmosphere, lightning strikes in background, cinematic lighting, high quality, album artwork style"
```

**Indie/Alternative:**
```
"Album cover art for indie rock: Vintage car on empty desert highway at golden hour, analog photography aesthetic, warm oranges and faded blues, nostalgic and melancholic mood, dust particles in air, film grain texture, cinematic lighting, high quality, album artwork style"
```

**Electronic/Synthwave:**
```
"Album cover art for synthwave: Neon-lit city skyline reflected in rain-soaked streets, cyberpunk aesthetic, electric pinks and cyan blues, futuristic and atmospheric, holographic elements, 80s retro-futurism, cinematic lighting, high quality, album artwork style"
```

**Folk/Acoustic:**
```
"Album cover art for folk music: Misty forest path with ancient trees, watercolor painting style, earth tones and soft greens, peaceful and mystical atmosphere, morning light filtering through leaves, hand-drawn illustration feel, cinematic lighting, high quality, album artwork style"
```

## Prompt Final para Suno Pro (Máximo 1000 caracteres)

Este prompt debe incluir todos los elementos técnicos y estilísticos necesarios para que Suno Pro genere la canción con la máxima calidad posible.

### Estructura del Prompt Final:

```
[GÉNERO PRINCIPAL] featuring [CARACTERÍSTICAS VOCALES], [INSTRUMENTACIÓN ESPECÍFICA], [ELEMENTOS TÉCNICOS DE PRODUCCIÓN]. [ESTRUCTURA MUSICAL] at [TEMPO] BPM in [COMPÁS]. [TEMÁTICA Y MOOD]. [PROGRESIÓN MUSICAL] with [ELEMENTOS ESPECÍFICOS DE ARREGLO]. [CALIDAD DE GRABACIÓN] with [EFECTOS DE AUDIO ESPECÍFICOS]. [ESTILO VOCAL DETALLADO] with [TÉCNICAS ESPECÍFICAS].
```

### Elementos Obligatorios (para llegar cerca de 1000 caracteres):

1. **Género y Subgéneros** (50-80 caracteres)
2. **Características Vocales** (80-120 caracteres)
3. **Instrumentación Detallada** (150-200 caracteres)
4. **Elementos Técnicos** (100-150 caracteres)
5. **Estructura y Tempo** (80-100 caracteres)
6. **Temática y Mood** (80-120 caracteres)
7. **Arreglos Específicos** (100-150 caracteres)
8. **Calidad de Producción** (120-180 caracteres)

### Ejemplo de Prompt Final Optimizado:

```
Romantic Spanish pop ballad featuring passionate male vocals with Andalusian accent and melismatic runs, fingerpicked nylon string Spanish guitar with flamenco techniques, grand piano with soft touch, lush string orchestra with violins and cellos, traditional cajón percussion with palmas hand claps, warm acoustic bass guitar. Intimate verses building to soaring choruses with orchestral arrangements. Tempo 80 BPM in 4/4 time. Themes of deep romantic love and devotion with poetic Spanish lyrics. Dynamic structure from acoustic intimacy to full orchestral power, featuring Spanish guitar solo with traditional flamenco palmas. Professional recording with warm analog compression, subtle cathedral reverb on vocals, rich string textures and authentic Spanish percussion. Emotional vocal delivery ranging from tender whispers to powerful passionate peaks with signature melismatic Spanish phrasing and soulful vibrato.
```
**Caracteres: 999/1000**

### Fórmula para Optimizar a 1000 caracteres:

1. **Contar caracteres constantemente** mientras construyes
2. **Priorizar elementos únicos** del género y canción
3. **Usar terminología técnica específica** (aumenta precisión)
4. **Eliminar palabras redundantes** como "con", "de", "que"
5. **Usar abreviaciones técnicas** cuando sea apropiado (BPM, 4/4, etc.)
6. **Incluir efectos de audio específicos** para mayor control
7. **Especificar calidad de grabación** (analog, digital, vintage, etc.)

### Checklist Final:
- [ ] Género principal y subgéneros
- [ ] Características vocales específicas
- [ ] Instrumentación detallada
- [ ] Tempo y compás
- [ ] Temática y mood
- [ ] Estructura musical
- [ ] Efectos de audio
- [ ] Calidad de grabación
- [ ] Técnicas específicas
- [ ] **Total: 1000 caracteres**

## Protocolo de Sesiones Futuras

A partir de ahora, cuando analices cualquier canción, incluirás siempre:

### 1. **Análisis Técnico**
- **Estructura actual**: Identificar todas las secciones
- **Tags utilizados**: Evaluar compatibilidad con Suno
- **Flujo musical**: Coherencia entre secciones
- **Instrumentación**: Elementos musicales presentes

### 2. **Análisis Lírico**
- **Temática central**: Mensaje principal
- **Estructura narrativa**: Desarrollo de la historia
- **Elementos poéticos**: Metáforas, rimas, ritmo
- **Idioma y registro**: Formal, coloquial, poético

### 3. **Sugerencias de Mejora**
- **Optimización de tags**: Modificadores específicos
- **Mejoras líricas**: Fluidez, rimas, coherencia
- **Transiciones**: Entre secciones musicales
- **Prompts embebidos**: Efectos, vocalizaciones, ritmos

### 4. **Identificación del Género**
- **Género principal**: Clasificación primaria
- **Subgéneros**: Influencias secundarias
- **Artistas de referencia**: Similitudes estilísticas
- **Época/movimiento**: Contexto histórico musical

### 5. **Prompt Final Optimizado**
- **Estilo (120 caracteres)**: Géneros, instrumentos, mood
- **Prompt completo (1000 caracteres)**: Todos los elementos técnicos
- **Justificación**: Por qué estos elementos específicos

### Ejemplo de Análisis Completo:

**Canción recibida:** [Ejemplo]

**Análisis Técnico:**
- Estructura: Simple verso-coro sin intro/outro
- Tags: Básicos, sin modificadores
- Flujo: Transiciones abruptas
- Instrumentación: No especificada

**Análisis Lírico:**
- Temática: Amor perdido
- Narrativa: Lineal, clara
- Poética: Rimas


# Mejoras Sugeridas para Suno AI Guide

## 1. **Sección de Troubleshooting/Solución de Problemas**

### Problemas Comunes y Soluciones:

**Problema:** La canción no respeta los modificadores de tags
- **Solución:** Usar modificadores más concretos y directos
- **Ejemplo:** En lugar de `[Psychedelic Verse]` usar `[Slow Dreamy Verse]`

**Problema:** Transiciones abruptas entre secciones
- **Solución:** Usar tags intermedios como `[Build]` o `[Break]`
- **Ejemplo:** 
```
[Verse]
[Build]
[Chorus]
```

**Problema:** Géneros híbridos no funcionan como esperado
- **Solución:** Ordenar géneros por prioridad (el primero tiene más influencia)
- **Ejemplo:** `space rock, psychedelic rock, stoner rock` vs `stoner rock, space rock, psychedelic rock`

## 2. **Sección de Mejores Prácticas**

### Do's ✅
- Usar modificadores concretos: `Whispered`, `Angry`, `Slow`
- Mantener el estilo bajo 120 caracteres
- Usar puntos y exclamaciones para ritmos instrumentales
- Especificar instrumentos en solos: `[Lead Guitar Solo]`
- Usar paréntesis para efectos vocales: `(echoed)`

### Don'ts ❌
- Evitar modificadores abstractos: `[Cosmic Verse]`
- No usar más de 3-4 modificadores por tag
- No repetir información del estilo en los tags
- No usar `[Bridge]` más de una vez por canción

## 3. **Sección de Técnicas Avanzadas**

### Manipulación de Tempo y Dynamics
```
[Slow Building Intro]
. . . . . !
. . . ! . !
. . ! ! ! !

[Intense Climax]
!! !! !! !!
!! ! !! ! 
```

### Técnicas de Storytelling
- Usar `[Spoken Word Narration]` para diálogos
- Combinar `[Whispered Verse]` con `[Shouted Chorus]` para contraste
- Usar `*sound effects*` para ambientación

### Construcción de Atmósferas
```
[Ethereal Intro]
*wind sounds and distant bells*

[Haunting Verse]
(whispered background vocals)
Main vocal line...
(echoes: "echoes...")
```

## 4. **Sección de Prompts de Estilo Específicos**

### Por Géneros:
**Rock/Metal:**
```
heavy metal, thrash metal, powerful vocals, distorted guitars, driving drums, aggressive
```

**Electronic:**
```
synthwave, electronic, atmospheric, dreamy, analog synthesizers, drum machine, ethereal
```

**Folk/Acoustic:**
```
folk, acoustic, fingerpicked guitar, harmonica, storytelling vocals, organic, warm
```

**Hip-Hop:**
```
hip-hop, boom bap, conscious rap, jazz samples, vinyl crackle, deep bass, rhythmic
```

## 5. **Sección de Longitud y Estructura**

### Guías de Duración:
- **Canción corta (2-3 min):** Intro + 2 Verses + 2 Chorus + Outro
- **Canción media (3-4 min):** Intro + 3 Verses + 3 Chorus + Bridge + Outro
- **Canción larga (4-5 min):** Estructura completa + Solos + Interludes múltiples

### Estructura Recomendada:
```
[Intro] (0-30 seg)
[Verse 1] (30-60 seg)
[Chorus] (60-90 seg)
[Verse 2] (90-120 seg)
[Chorus] (120-150 seg)
[Bridge/Solo] (150-180 seg)
[Final Chorus] (180-210 seg)
[Outro] (210-240 seg)
```

## 6. **Sección de Efectos Sonoros y Ambientación**

### Efectos Populares:
- `*vinyl crackle*` - Para sonido vintage
- `*crowd cheering*` - Para ambiente de concierto
- `*rain and thunder*` - Para atmósfera dramática
- `*phone ringing*` - Para narrativa
- `*footsteps echoing*` - Para tensión

### Técnicas de Layering:
```
[Verse]
(distant choir humming)
Main vocal line
(whispered echoes)
*subtle string swells*
```

## 7. **Sección de Colaboración y Feedback**

### Cómo Iterar:
1. Genera versión inicial
2. Identifica elementos que no funcionan
3. Ajusta modificadores específicos
4. Regenera secciones problemáticas
5. Combina mejores elementos

### Documentación de Cambios:
- Mantener registro de qué modificadores funcionan
- Anotar combinaciones de géneros exitosas
- Documentar efectos sonoros que resonaron

## 8. **Sección de Recursos Adicionales**

### Herramientas Complementarias:
- **Rhyme schemes:** Para patrones de rima consistentes
- **Syllable counters:** Para mantener métrica
- **Chord progression generators:** Para armonías base

### Inspiración de Referencia:
- Analizar canciones exitosas en Suno
- Estudiar estructuras de artistas del género objetivo
- Experimentar con fusiones inusuales

## 9. **Sección de Limitaciones y Workarounds**

### Limitaciones Conocidas:
- Máximo 120 caracteres para estilo
- Algunos géneros nicho no son reconocidos
- Modificadores muy específicos pueden ser ignorados

### Workarounds:
- Usar sinónimos más comunes para géneros obscuros
- Describir el feeling en lugar del género específico
- Usar instrumentación para lograr sonidos específicos

## 10. **Checklist de Calidad Final**

### Antes de Generar:
- [ ] Estilo bajo 120 caracteres
- [ ] Tags con modificadores apropiados
- [ ] Estructura lógica y fluida
- [ ] Efectos sonoros específicos
- [ ] Letras con timing apropiado

### Después de Generar:
- [ ] Escuchar transiciones
- [ ] Verificar que el mood sea consistente
- [ ] Confirmar que instrumentos destacados aparezcan
- [ ] Evaluar calidad vocal
- [ ] Considerar variaciones si es necesario


Fuente:  https://sunoaiwiki.com/

List of Music Genres and Styles
Here’s a categorized selection of music genres and styles, featuring a few hundred popular and common genres:

Avant-garde & Experimental
Electroacoustic
Industrial music
Noise music
Progressive music
Psychedelic music
Blues
Chicago blues
Delta blues
Electric blues
Gospel blues
Rhythm and blues
Country
Bluegrass
Country blues
Country pop
Country rock
Nashville sound
Easy Listening
Adult contemporary music
Elevator music (muzak)
Lounge music
Soft rock
Electronic
Ambient
Breakbeat
Disco
Drum and bass
Dub
Electro
House music
Techno
Trance music
Folk
Americana
Celtic music
Folk rock
Indie folk
Singer-songwriter
Hip Hop
Alternative hip hop
Gangsta rap
Trap
UK drill
Jazz
Bebop
Big band
Cool jazz
Jazz fusion
Smooth jazz
Pop
Dance-pop
Electropop
Indie pop
K-pop
Synth-pop
R&B & Soul
Contemporary R&B
Funk
Gospel music
Neo soul
Quiet storm
Rock
Alternative rock
Classic rock
Hard rock
Indie rock
Punk rock
Metal
Black metal
Death metal
Heavy metal
Industrial metal
Power metal
Punk
Anarcho punk
Hardcore punk
Pop punk
Punk rock
Skate punk
Regional Music
Brazilian music (e.g., Samba, Bossa nova)
Caribbean music (e.g., Reggae, Dancehall)
African music (e.g., Afrobeat, Highlife)
Asian music (e.g., J-pop, K-pop)
This list includes some of the most influential and widespread genres across the main categories of music. Each category represents a broad spectrum of styles, capturing both traditional and modern sounds.

What are Meta Tags?
Meta tags in music AI are directives that guide the AI in structuring songs, dictating styles, and integrating dynamics, thus allowing for detailed creative control and expression in generating music and lyrics. Think of meta tags as instructions or hints you give to the AI to help it understand exactly what kind of song you want to create.

How to Use Meta Tags in Suno AI
Using meta tags can significantly enhance the quality and precision of your AI-generated songs. Here’s how you can apply meta tags effectively:

Structuring Songs: Meta tags can help in defining the structure of your song. For example, you can use meta tags to specify the sections like intro, verse, chorus, and outro. This ensures that the AI understands the flow and progression of your song. Read more

Dictating Styles: Want your song to have a specific style or genre? Meta tags can guide the AI to produce music in the style of pop, rock, jazz, etc. You can even mix and match styles for a unique sound using meta tags. Learn how

Integrating Dynamics: Dynamics like volume, tempo, and emotion can be controlled using meta tags. You can tell the AI to make certain parts of the song softer or more energetic, adding a professional touch to your music with meta tags. Explore more

Creating Detailed Lyrics: Meta tags can also be used to fine-tune the lyrics. You can specify themes, rhyme schemes, and even the mood of the lyrics. This helps in generating coherent and meaningful lyrics that fit well with the music through the use of meta tags. Find out how

By mastering the use of meta tags, you can take full control of your music creation process, making sure the AI produces exactly what you envision. So, whether you’re a beginner or a seasoned musician, incorporating meta tags into your workflow can elevate your Suno AI experience to the next level.

Environment and Sound Effects
Sound Effects Meta Tags
Barking : Sound of a dog barking.
Beeping : Beeping sound.
Bell dings : Sound of a bell dinging.
Birds chirping : Sound of birds chirping.
Bleep : A short, high-pitched sound.
Cheering : Sound of people cheering.
Cheers and applause : Sound of people cheering and clapping.
Chuckles : Sound of light laughter.
Clapping : Sound of clapping.
Cough : Sound of coughing.
Groaning : Sound of groaning.
Phone ringing : Sound of a phone ringing.
Ringing : General ringing sound.
Screams : Sound of screaming.
Sighs : Sound of sighing.
Squawking : Sound of squawking.
Whispers : Sound of whispering.
Whistling : Sound of whistling.
Vocal Expressions Meta Tags
Announcer : Voice of an announcer.
Audience laughing : Sound of an audience laughing.
Female narrator : Voice of a female narrator.
Giggling : Sound of giggling.
Man : Voice of a man.
Reporter : Voice of a reporter.
Woman : Voice of a woman.
Boy : Voice of a boy.
Girl : Voice of a girl.
Static and Other Effects
Applause : Sound of applause.
Clears throat : Sound of someone clearing their throat.
Censored : Silenced part that is censored.
Silence : Complete silence, no sound.
Music Structure and Styles
Structural Tags
Chorus : The chorus part of the song.
Intro : Introduction part of the song.
Outro : Ending part of the song.
Verse : The verse sections of the song.
Styles and Genres Meta Tags
Acoustic : Acoustic style.
African : African music style.
Alternative metal : Alternative metal genre.
Alternative pop : Alternative pop music.
Ambient : Ambient music.
Atlanta rap : Rap style from Atlanta.
Ballad : Style of narrative song.
Baroque : Baroque music.
Blues : Blues genre.
Boom bap : A style of hip hop.
Cello : Music featuring the cello.
Chill : Chill music for relaxing.
Christian & Gospel : Christian and gospel music.
Christmas : Christmas-themed music.
Country & Americana : Country and Americana music.
Dance & Electronic : Dance and electronic music.
Drums : Music focusing on drum sounds.
EDM : Electronic dance music.
Girl group : Music by girl groups.
Gospel : Gospel music.
Hardcore rap : Aggressive style of rap.
Heavy metal : Heavy metal music.
Hip hop : Hip hop music.
Indie : Independent music style.
Indie rock : Indie rock genre.
J-pop : Japanese pop music.
Jazz : Jazz music.
K-pop : Korean pop music.
Lo-fi : Low-fidelity music.
Orchestra : Orchestral music.
Party : Party music.
Piano : Music featuring the piano.
Pop : Pop music.
Pop-Rock : Pop rock music.
Post-Hardcore : Post-hardcore genre.
Punk Rock : Punk rock music.
R&B : Rhythm and blues music.
R&B & Soul : Rhythm and blues and soul music.
Rap : Rap music.
Reggae : Reggae music.
Rock : Rock music.
Romantic : Romantic music style.
Soul : Soul music.
Synth : Music featuring synthesizers.
Synth pop : Synthesizer-based pop music.
Techno : Techno music.

How to Make Suno AI Sing with Spoken Word
Solution: To have an AI perform spoken word sections instead of singing at the beginning of a song, you can use specific annotations like [Spoken word], [Narration], [Spoken verse], or [Sprechgesang]. This should guide the AI to recognize the intended speech format.

Examples:

If you input:

[Spoken word] Hey there! Welcome to our show tonight!

The AI might begin the song with a spoken introduction rather than singing, helping to set a distinct tone before the music starts.

Another effective method is using parentheses to indicate spoken content. For example:

(This is the story of a night unlike any other.)

This has been reported to occasionally trigger the AI to speak the text instead of singing it, as observed in some songs on Suno.com.

Additional Tips:
It might take several attempts for the AI to properly interpret these cues as spoken word. Persistence is key.
Mixing different types of annotations (like using both [Narration] and parentheses) might improve your chances of success.

How to Enhance Your Suno AI Songs with Advanced Formatting Tips
Solution: For creators looking to elevate their Suno AI-generated songs, employing advanced formatting and annotations like asterisks, brackets, and capitalization can significantly alter the dynamics and style of music. These techniques can change vocal delivery, add effects, and sequence different parts of your song.

Examples:

Using Asterisks for Effects: You can add sound effects by enclosing them in asterisks. For example:

*gunshots*

This might make the AI incorporate the sound of gunshots into the song.

Capitalization for Vocal Emphasis: Placing a line of lyrics in ALL CAPS with a punctuation like ”!” or ”?” can modify the voice tone, making it louder or distinct from the main vocals.

Brackets for Song Structure: Utilizing brackets to define different song sections (e.g., [Intro], [Verse], [Chorus]) helps in managing the flow and sequencing. More creative uses include:

[Flute solo intro]
[Increase intensity]
[Crescendo]
[Starts out quietly]
[Whispering vocals]
[Screaming vocals]

These directives inform the AI about the intended musical direction and intensity of each section.

Workarounds for Language Restrictions: To bypass content filters on restricted words, substituting letters or words allows the use of similar sounds without triggering censorship, enhancing creative freedom. For instance:

Replace “die” with “dye”
Use “ill” instead of “kill”
Creative Naming for Music Styles: Describing unique music styles like “Haunting g-funk horror doom trap r&b” can lead to innovative genre fusions, pushing the boundaries of traditional music classification.

Effective URLs demonstrating these techniques:

Sample Song with Effect
Gunshots Effect
Bird Sounds
Additional Tips:
Experimentation is key; not all annotations will work consistently, so testing different combinations can yield the best results.
Keep trying different phrasings and annotations as the AI might take a few attempts to accurately interpret these cues.

How to Reuse a Song Seed in Suno AI
Solution: To reuse a song seed in Suno AI for generating new songs with similar instrumental and vocal characteristics but varied lyrics and melodies, start the new song generation from a specific timestamp of the original song. This approach can help maintain certain elements like voice and instrumental setup while allowing for new musical variations.

Examples:

Using a Fixed Timestamp: Start a song from a particular moment (e.g., 2 seconds into the track) to ensure the continuation retains the original voice and band setup. This method has shown varied success with the melody but can maintain the song’s general style and tempo.

Example of this approach: Suno Song Link

Adding Lyrics to Instrumentals: Convert an instrumental piece into a full song by starting the generation process after an introductory segment (e.g., 10-20 seconds), and adding lyrics. This can transform an instrumental into a complete song while preserving the original tune’s essence.

Original and modified versions:

Original Instrumental: Original Song
With Lyrics Added: Song with Lyrics
Creating Variants from a Single Seed: Generate multiple song variants from a single successful intro or theme to explore different musical directions or to develop a cohesive album. This method focuses on consistent sound while varying other song elements.

Additional Tips:
The effectiveness of reusing seeds may vary, so experimentation and multiple attempts might be necessary.
Utilize precise timestamps for starting points to control how much of the original song’s characteristics are retained.
Consider the potential for creating thematic albums or collections using a consistent voice or instrumental setup across multiple tracks.

How to Structure Prompts for Suno AI
Solution: To achieve consistent outcomes when prompting Suno AI for music generation, understanding and effectively structuring prompts is crucial. This ensures that the AI interprets your intentions accurately and the music aligns with your desired characteristics.

Examples:

Use Custom Mode and Detailed Descriptors: Instead of relying on the general input fields, switch to custom mode where you can specify each aspect of your music:

Genre: Heavy Metal, Mood: Dark, Key: B minor

This format helps prevent the AI from misinterpreting parts of your prompt as lyrics.

Separating Elements with Commas: When you want to combine multiple attributes like genre, voice, and instrumental emphasis, separating them with commas can clarify your intentions:

Gothic, Alternative Metal, Ethereal Voice

This method helps the AI differentiate between various stylistic elements.

Using Brackets for Specific Instructions: To ensure that specific instructions are followed, use brackets to define song sections or vocal styles:

[Verse1] [Female Ethereal Voice]

This helps in guiding the AI more precisely, especially when trying to emulate certain band styles or unique vocal characteristics.

Additional Tips:
Experiment with different structuring formats to see which provides the best results for your specific style.
Incorporate mood, tempo, and “ear candy” elements to enhance the overall appeal of the music.
Remember, the more specific your prompt, the more likely the AI will produce the desired outcome.
Understanding how to effectively structure your prompts can significantly improve the consistency and quality of the music generated by Suno AI, turning your creative visions into reality.

How to Use Meta Tags in Suno AI for Song Creation
Solution: Utilizing meta tags effectively in Suno AI can significantly influence the structure and style of your AI-generated songs. Meta tags act as directives that help the AI understand the desired composition of the music, from the type of vocals to the placement of instrumental breaks.

Examples:

Structural Tags:

To structure a song with clear parts, use tags like [Intro], [Verse], [Chorus], and [Outro]. For instance:
[Intro] Slow guitar strumming
[Verse] Whispered lyrics here
[Chorus] Powerful vocal rise
[Outro] Fading piano melody

These tags guide the AI to maintain a coherent song structure, ensuring each part is distinct.
Instrumental and Vocal Tags:

Specific tags can dictate the type of instruments and vocals used. Tags like [Guitar solo] or [Female Vocal] instruct the AI on what elements to introduce at certain points in the song.
Example usage:
[Verse] Lost in the rhythm
[Guitar solo] A mesmerizing guitar piece
[Chorus] [Female Vocal] Echoing the main theme

Dynamic Elements:

Use tags like [Catchy Hook], [Emotional Bridge], and [Powerful Outro] to emphasize certain parts of the song that should stand out.
For example:
[Verse] The story begins here
[Emotional Bridge] A heartfelt solo
[Catchy Hook] This line repeats
[Powerful Outro] Climactic finish

Additional Tips:
Experiment with combining different tags to see how they influence the AI’s output. The AI’s interpretation can vary, so multiple attempts might be needed to achieve the desired result.
Pay attention to how specific elements like [Pre-Chorus] and [Bridge] can be used to build anticipation and add complexity to the song.
Understanding and leveraging these meta tags effectively can greatly enhance your creative process when working with Suno AI, allowing for more precise control over the musical composition.

Advanced Song Production Techniques for Suno AI
Solution: To maximize the effectiveness of song production with Suno AI, utilize specific annotation techniques that guide the AI in generating songs with diverse vocal styles, instrumental breaks, and coherent transitions.

Examples:

Using the vowel-vowel-vowel technique for creating longer, melodious words in the chorus:

goo-o-o-odbye

This technique extends vocal sounds, adding a melodic quality ideal for choruses.

Applying parentheses to add a second or third vocal layer automatically:

E la cha-cha-cha (cha)

This can introduce a background vocal or an instrumental sound, enhancing the song’s depth.

Using brackets to direct the AI’s focus on song parts:

[Verse 1] [Chorus] [Pre-chorus] [Drop]

This method helps in structuring the song, ensuring each part transitions smoothly and fulfills its intended purpose.

Additional Tips:

Combine different types of annotations to trigger specific AI responses, such as [Angelic voice] or [Instrumental] for varied vocal effects and solo instruments.
Experiment with the arrangement of parts within the song to maintain freshness and uniqueness in each section.
Multiple attempts may be necessary to achieve the desired effect, as AI interpretation can vary.
Generating Multi-Part Songs:
Enhance uniqueness by varying the rhythm, vocal styles, and instruments throughout the song.
Consider generating the song in parts and carefully reviewing each segment to ensure they fit together seamlessly.
Editing and Finalizing:
Use audio editing tools like Audacity to refine the final product, such as trimming excessive instrumental parts or correcting any mismatches in song sections.
By adopting these techniques, you can effectively manipulate Suno AI to produce high-quality, creative musical pieces.

Mastering Song Extensions with Suno AI
Problem:

One of the main challenges faced by musicians using Suno AI involves managing the quality of music as they extend or render songs multiple times. This often results in disjointed lyrics and a deterioration in vocal performance, affecting the overall quality of the music.

Solution: Utilize strategic practices for song extensions in Suno to ensure high-quality music production.

Examples:

Create multiple iterations of song sections and select the most effective:

Extend verse 1, chorus 1; Extend verse 2, chorus 2; Extend verse 3, bridge 1, chorus 3, end.

Evaluating multiple versions helps identify and resolve issues early, enhancing the song’s overall quality.

Use AI feedback to refine lyrics and composition before final adjustments:

Discard less successful attempts and allow the AI time to refresh.

Allowing the AI to refresh can lead to better outcomes when adjustments are made.

Limit the number of extensions to prevent quality reduction:

Limit to one start and two or three extensions to complete the song.

This method helps maintain sound quality and prevents the degradation often seen with multiple extensions.

Additional Tips:
Save any generation that meets your standards using the “get whole song” option for consistency.
Experiment with segment durations and adjust EQ settings to suit your style.
Engage with the community for fresh tips and continuously refine your technique for using AI in music production.

How to Get Specific Vocal Styles in Suno AI
Problem:

When using Suno AI for music creation, you might find it challenging to achieve the specific vocal style you desire, especially if you’re aiming for unique vocal characteristics like a deep or gritty male voice in genres such as electronic or techno. The AI often defaults to a generic style, which can make the tool feel more like a novelty rather than a professional tool capable of producing hit tracks.

Solution: Employ detailed style prompts to specify the desired vocal characteristics.

Examples:

Use detailed descriptors in your prompts to guide the AI, such as:

[masculine low gospel vocal]

This can help the AI better understand and produce the specific vocal tone you’re looking for.

Experiment with combining different descriptors to enhance specificity, for example:

[feminine high airy vocal]

Such combinations can yield more precise vocal outputs, fitting your desired style more closely.

Adding geographic distinctions to your vocal style prompts can also influence the AI’s output significantly:

[UK rock male vocal]

This technique can help tailor the vocal style to match regional variations, offering a broader palette of vocal textures.

Additional Tips:
Repeated trials might be necessary as the AI learns to better interpret these detailed prompts.
Mixing several descriptive terms (like using both genre and vocal characteristics) may improve success rates.
Keep track of successful prompts for future reference to streamline your creative process.
Using these strategies, you can push the boundaries of AI in music production, achieving more professional and satisfying results.

How to Prevent Inappropriate Lyrics in Suno AI Songs
Problem:

When experimenting with converting classic hymns into rap music using Suno AI, users have reported unexpected and inappropriate insertions of the N-word. This issue seems to be particularly pronounced with Christian-themed songs. Such occurrences can disrupt the artistic intention and are offensive regardless of context.

For example, while transforming a hymn into a rap, one might expect lyrics that respect the original’s dignity, but instead, the AI unexpectedly includes offensive language, altering the intended vibe of the song.

Solution: Introduce content moderation features in Suno AI. This can involve setting explicit and implicit content filters that users can customize according to their preferences for clean or explicit lyrics.

Examples:

Implement a user-controlled filter setting where creators specify banned words:

[Settings] -> [Content Preferences] -> [Banned Words]: Add "N-word"

This would prevent the AI from including specific offensive terms in the lyrics.

Utilize a toggle for explicit content:

[Settings] -> [General] -> [Allow Explicit Content]: Off

Turning off explicit content could help maintain the integrity of certain genres like hymns.

Encourage the use of specific prompts that guide the AI away from potentially offensive content:

[Lyric Generator] -> [Prompt]: "Generate family-friendly rap lyrics for a hymn"

Clear instructions can steer the AI towards generating appropriate content.

Additional Tips:
Repeated trials might be necessary as the AI learns from continuous feedback and adjustments to settings.
Combining multiple moderation techniques (like explicit content toggles and banned words lists) could enhance effectiveness.
Maintaining the artistic quality of AI-generated music without compromising on respect and sensitivity to all audiences is crucial. By implementing robust content moderation features, creators can better align the output with their artistic visions and audience expectations.

How to Specify Chord Progressions in Suno AI
Problem:

Musicians often want to create songs with specific chord progressions, like an instrumental trance song in A minor using a specific sequence (Am, F, G, Em). However, challenges arise when the AI misinterprets this input and creates lyrics about the chord names instead of following the intended musical pattern. This issue reflects the AI’s current limitations in distinguishing between lyrical content and musical instructions.

Solution:

To address this, use targeted strategies to better specify your musical requirements to the AI:

Examples:

Use the “custom mode” to separate lyrics and style inputs:

Style: instrumental trance in A minor
Lyrics: [Am] [F] [G] [Em]

This helps the AI focus on the musical style without confusing it with the lyrics.

Clearly label your musical elements in the prompt:

Chord progression: [Am] [F] [G] [Em]

Including the term “chord progression” might help the AI to recognize and apply these details more accurately.

Experiment with mood descriptors linked to scales:

Mood: sad (for minor scales)

Sometimes, describing the mood can indirectly influence the AI to select the appropriate scale, such as using “sad” for minor keys.

Additional Tips:
While the AI might not always follow complex musical instructions perfectly, using clear, distinct commands can increase your chances of getting closer to your desired outcome.
Be prepared for some trial and error. The AI’s understanding of musical nuances is still developing, and it may take several attempts to achieve the intended effect.
Linking mood descriptors with musical scales can be an indirect but effective way to guide the AI in your desired musical direction.
By implementing these strategies, you can enhance your ability to create specific musical compositions using Suno AI, even within the current technological limitations.

How to Bypass Explicit Lyric Restrictions
Problem:

While using AI music generators like Suno, users often encounter restrictions on explicit lyrics, which limits creative expression. For example, trying to include certain swear words or provocative content often results in the lyrics being filtered out or modified by the system. This can be frustrating for artists seeking to maintain the authenticity of their lyrical content.

Solution: To overcome these restrictions, you can employ several workarounds to trick the AI’s filtering system:

Examples:

Use phonetic spelling or homophones to bypass content filters. For instance:

Replace "shit" with "sh*t" or "ship".

This alteration can sometimes fool the filtering algorithm, allowing the inclusion of the intended word without direct recognition.

Example: https://suno.com/song/2133e340-3944-4b4b-ac6b-acebcdcdfa4f

Experiment with creative language substitutions that sound similar to the desired explicit words. For example:

Instead of "fuck", use "fuhk" or "phuck".

Such substitutions can maintain the sound of the original word while evading automatic censorship.

If specific words are blocked, try modifying the context or using less direct language. For instance:

Change "I hope you choke" to "Hope you choke".

Sometimes, removing pronouns or slightly altering the sentence structure can help avoid filters.

Additional Tips:
Persistence is key. The effectiveness of these methods can vary, and it may take multiple attempts to find a successful workaround.
Combine different methods, like phonetic spelling and creative substitutions, to increase your chances of success.
Be mindful of the broader context of your lyrics, as AI systems often consider the overall theme or explicitness of the content.
By exploring these strategies, you can enhance your creative freedom and produce AI-generated music that aligns more closely with your artistic vision.

How to End a Song Naturally
Problem:

When using Suno AI to create music, some users encounter an issue where the song ends abruptly instead of fading out or concluding smoothly. For example, despite trying to guide the AI with specific extensions like specifying that the next extension be the final part of the song or to gradually fade until the song is over, the music often just cuts off unexpectedly. This results in a song that feels unfinished and disrupts the listening experience.

Solution: To ensure a natural ending for your songs created with Suno AI, you can use certain annotations in your lyrics box such as [end], [fade out], or [outro]. These commands can help signal to the AI that the song should conclude in a smoother manner.

Examples:

For a clear cut ending:

[end]

This command can direct the AI to stop the music clearly and neatly.

For a fading conclusion:

[fade out]

This has mixed results but is intended to gradually lower the volume until the song is completely faded out.

To introduce a concluding instrumental:

[outro] [Instrumental Fade out] [End]

This combination can create a more elaborate ending sequence, blending the fading of instruments with the official end of the song.

Additional Tips:
Experiment with various combinations of these annotations to see which ones work best for your specific song.
It might take a few attempts to get the desired effect, as AI interpretations can vary.
If all else fails, consider manually editing the track using audio software like Audacity to add a fade-out effect. This can be a reliable way to ensure your song ends just the way you want it.

How to Replace or Modify Lyrics
Problem:

Sometimes, when creating music with AI, we find ourselves wanting to change specific lyrics in a song to make them more suitable or to better match our artistic vision. For example, imagine you’ve created a track with the lyrics:

[Verse] I need the stars to align tonight.

But you want to change the word “need” to “greed” to alter the tone of the song.

Solution: To replace lyrics in songs generated by Suno AI, consider using lyric infilling techniques, where you can specify parts of the lyrics to be changed while retaining the rest of the song’s structure.

Examples:

Using the “Extend” Feature: After generating your song, use the Extend feature to add new lyrics. Here’s how you might do it:

Extend your song and paste new lyrics here.

Remember, you may need to use external software to trim unwanted parts of the original song.

Separation and Regeneration: Separate the song into individual stems, mute the vocal stem you wish to change, and then regenerate that portion. Tools like Moises and Splice can assist with this process.

Utilizing External Software: If you need to completely remove or replace the singer, use software as shown in this tutorial: Creating an instrumental version of your song This allows you to then add new vocals without the original lyrics.

Additional Tips:
Keep experimenting with different seeds and settings to get closer to your desired outcome.
Utilize AI music platforms like Udio that already have features like backward generation for more precise control over lyrical content.
Patience is key, as generating the perfect lyric might take several attempts.
By employing these methods, you can effectively alter the lyrics in your AI-generated songs, ensuring they fully convey your intended message and style.

How to Optimize Prompts in Suno AI with Letter Case
Problem:

In Suno AI, the letter case (upper, lower, or title case) used in prompts can significantly impact the quality and style of the generated song. Different parts of the prompt react differently to letter case styles, affecting the output’s coherence and alignment with user expectations.

Solution: To get the best results from Suno AI, use different letter cases for different parts of your prompt. Here’s a recommended approach:

ALL CAPS for genres: This gives genres the highest priority.
Title Case for descriptors: This gives descriptors a middle priority.
lower case for instruments: This ensures instruments are included prominently in the song.
Examples:
All Title Case

Funky Bassline, Operatic New Jack Swing, Rhythmic Power Metal, High Female Vocals, G-Funk

Example: https://suno.com/song/caa98821-c4ff-49ce-b71a-833dfc9a879a

GENRES IN ALL CAPS, Descriptors in Title Case

FUNKY BASSLINE, Operatic NEW JACK SWING, Rhythmic POWER METAL, High Female Vocals, G-FUNK

Example: https://suno.com/song/507bda5c-44d9-439b-995d-67823c5c2890

ALL CAPS for Descriptors, Title Case for Genres

HIGH ENERGY Big Band, SEXY Psychobilly, UNCOMMON TIME SIGNATURES

Example: https://suno.com/song/7fc7a2bf-2736-42f5-9533-aca85d8244fa

Title Case for Everything

High Energy Big Band, Sexy Anthemic Psychobilly, Uncommon Time Signatures

Example: https://suno.com/song/d0eb9cfe-9889-48f5-81e6-295d82625c36

Additional Tips:
Use ALL CAPS for the genres, Title Case for descriptors, and lower case for instruments to get the best quality.
Combining all three letter case types in your prompt improves the overall quality.
Experiment with different combinations to find the best fit for your specific needs.
By following these letter case strategies, you can significantly enhance the quality and accuracy of the songs generated by Suno AI.

ow to Prompt Suno AI to Use Animal Sounds and Noises
Understanding the Problem
Many users find it challenging to get Suno AI to generate animal sounds or other specific noises in their tracks. Despite various attempts with different prompts, the AI often fails to produce the desired effects.

Solution Overview
To successfully prompt Suno AI to use animal sounds and noises, you need to use specific techniques and prompt structures. Here are some effective strategies:

Strategy 1: Use Bracketed Prompts
Use bracketed prompts in all-caps to indicate the desired sounds. This helps the AI understand that you want these effects included.

[GUNSHOTS FX, BIRDS CHIRPING FX, CRICKETS FX, THUNDERSTORM FX]

Strategy 2: Limit the Number of Prompts
Avoid overloading the prompt with too many effects at once. Instead, use a few prompts and repeat them if necessary.

[GUNSHOTS FX], [BIRDS CHIRPING FX], [CRICKETS FX]

Strategy 3: Experiment with Different Phrasing
Try different wording and combinations to see which works best. Sometimes altering the phrasing slightly can make a big difference.

[SCREAMING], [DINOSAUR ROAR], [CHAINSAW]

Examples and Additional Tips
Example 1: Combining Prompts
Try using a combination of prompts in the “Style” section and the “Custom Editor” lyrics box. Use commas to separate them.

STYLE: [TRIBAL VOCALS], [ANIMAL NOISES]
CUSTOM EDITOR: [BIRD SONG], [JUNGLE SOUNDS]

Example 2: Specific Sound Effects
Experiment with very specific sound effects to see if Suno AI can generate them.

[THUNDER CLAP], [WOLF HOWL], [OCEAN WAVES]

Example 3: Uncommon Effects
Test out less common effects to push the boundaries of what Suno AI can generate.

[CHAINSAW], [LIAR BIRD IMITATING A CHAINSAW]

Additional Tip: Dispute Incorrect Results
If the AI produces something unexpected, keep trying with slight variations or dispute the claim if you believe it’s a mistake. This can sometimes lead to better results upon human review.

You can listen to some examples here: Smoke sound in a stoner rap track

By following these strategies and experimenting with different prompts, you can increase the likelihood of getting Suno AI to include the animal sounds and noises you want in your music.

How to Solve Suno AI Sampling Detection Issues
Understanding the Problem
Many users have reported issues with their songs generated using Suno AI being flagged as sampling by platforms like Tunecore. This leads to songs being blocked and potential legal and financial problems.

Solution Overview
To avoid these issues, it’s crucial to understand the reasons behind these detections and take steps to prevent them. Here are some strategies:

Strategy 1: Use Original Content
Always use original lyrics and compositions. Avoid using any pre-existing material directly, as this can be detected as sampling.

Original lyrics throughout. It’s what they are saying. "Your release has been temporarily blocked in our front end review process. It appears that you are using the mastered instrumentals for these tracks (i.e., from the original artists' versions). Any time you sample any part of a recording you did not record yourself, you MUST have a license from the owner of that original recording. You cannot distribute any content that you do not hold 100% distribution rights for."

Strategy 2: Modify Prompts and Outputs
Slightly alter the prompts and the AI-generated outputs to ensure they do not closely resemble existing songs.

This song was detected as sampling:
https://www.youtube.com/watch?v=Jku-v48xpBU&feature=youtu.be

Strategy 3: Dispute Incorrect Claims
If you believe the detection is incorrect, dispute the claim. Many times, these detections are automated and can be resolved by human review.

I’ve never had a Suno track get flagged but I’ve made original music where a tiny section that sounded similar to some obscure song got flagged. Nothing a quick dispute didn’t fix. Should be the exact same situation for you. Let me know the outcome though, would hate to see them fight this as it could set a precedent.

Additional Tips
Tip 1: Be Persistent
Sometimes it may take several attempts to get the AI to produce completely original content.

Tip 2: Understand Licensing
Ensure you have the proper licenses for any content you are using that is not originally yours.

Tip 3: Stay Updated
Keep an eye on updates from Suno AI regarding their licensing and content usage policies.

By following these strategies, you can minimize the risk of your songs being flagged as sampling and ensure a smoother experience with platforms like Tunecore.

Using Detailed Prompts in Suno v3.5 Lyrics
The Breakthrough
Using Suno AI v3.5, you can achieve better audio quality and more control over your music. This guide will show you how to optimize prompts for improved results.

The Main Issue
The “Style of Music” field in Suno AI has a limited character count, making it difficult to provide detailed prompts. This method uses the Lyrics field to include more information.

Step-by-Step Solution
Step 1: Entering the Style of Music
In the “Style of Music” field, enter a high-level description and reference the Lyrics field for details.

Lofi, Chilled, Ambient, Downtempo, Female Vocals
SEE <SONG_DETAILS> IN THE LYRICS FIELD FOR DETAILED INFORMATION

Step 2: Filling Out the Lyrics Field
In the Lyrics field, include a detailed prompt as follows:

<SONG_DETAILS>
[GENRES: Chilled Lofi, Ambient, Downtempo]
[SOUNDS LIKE: Tycho, Bonobo, Nujabes]
[STYLE: Relaxing, Atmospheric, Lush, Clean]
[MOOD: Calm, Serene, Reflective, Dreamy]
[VOCALS: Female, Ethereal, Background]
[ARRANGEMENT: Slow tempo, Laid-back groove, Ethereal textures, Clean guitar melodies]
[INSTRUMENTATION: Clean electric guitar, Synthesizers, Ambient pads, Subtle percussion]
[TEMPO: Slow, 70-90 BPM]
[PRODUCTION: Lo-fi aesthetic, Warm tones, Soft compression, Analog warmth, Masterpiece, Perfectly Recorded, Produced by Emancipator]
[STRUCTURE: Intro, Verse, Chorus, Verse, Chorus, Bridge, Outro]
[DYNAMICS: Gentle throughout, Gradual builds and releases, Smooth transitions]
[EMOTIONS: Peacefulness, Contemplation, Tranquillity, Nostalgia]
</SONG_DETAILS>

[Intro]

[Verse 1]
start your lyrics here...

Tips and Tricks
Tip 1: Consistent Intro
By adding the STRUCTURE attribute, you can ensure Suno AI creates a proper intro when you use the [Intro] tag.

Tip 2: Quality Prompts
Using terms like “perfect production, studio recording, hi-fidelity” under the PRODUCTION attribute can improve the audio quality.

Tip 3: Simple and Direct Prompts
While detailed prompts can help, sometimes simpler and more direct prompts work better. Experiment with both approaches.

Example of a Simple Prompt
[slap bass funk fusion, experimental jazz fusion, hifi, clear production]
[Percussion Intro]
[instrumental, slap bass]
[verse]
*start lyrics*

Conclusion
This method allows for more detailed and controlled music generation with Suno AI v3.5. While it may not be perfect, it significantly enhances the output quality and provides more flexibility in creating the desired sound.

Handling Suno Looping Lyrics
The Update’s Impact
With the recent update, Suno can now generate longer songs. While this sounds great, the problem is that the AI sometimes just loops lyrics to fill the time instead of creating a cohesive song.

Identifying the Problem
Problem: Looping Lyrics
Many users have noticed that Suno tends to loop lyrics unnecessarily, creating longer but repetitive songs. This issue of looping lyrics can make the songs feel less original and more monotonous.

Example:

"I love when I cue it to fade out and it does so but then it changes its mind and gives me another 90 seconds of repeats of verses, chorus, bridges..."

Manual Trimming as a Solution
Solution: Manual Trimming
One way to handle the issue of looping lyrics is to manually trim the songs. Download the generated song and use an audio editing tool to cut out the repetitive parts caused by the looping lyrics.

Example:

"...had to download and trim songs and trim them manually at spots that just 'make sense' to get a full sounding something."

Using Parameters and Tags
Solution: Using [End] and [Outro] Tags
To control the length of the song and prevent looping lyrics, try using specific tags like [End] or [Outro]. This can signal the AI to stop generating beyond a certain point.

Example:

"[Outro] before the last block of lyrics, followed by [end] will usually get the job done."

Link: https://www.youtube.com/watch?v=ahV7KPxMlko

Customizing the Ending
Solution: Defining an End Parameter
It’s helpful to specify where you want the song to end to avoid looping lyrics. Including a time-based end parameter can guide the AI to finish the song at a desired length.

Example:

"Being able to tell Suno that you want the song to end at 2:45 for example..."

Enhancing Suno’s Performance
Solution: Alternative AI Models
If Suno continues to have issues with looping lyrics, consider exploring other AI models like Udio. Users have reported better experiences with different models, especially after updates.

Example:

"Have you tried the new Udio 2 min 10s model? ... Udio has really blown me away after the last update."

Link: https://youtu.be/iZUuqw8IvbI

By implementing these strategies, you can minimize the issue of looping lyrics in Suno and create more cohesive and professional-sounding songs.

Common Clichés in Lyrics
Understanding the Issue
Many users have noticed that AI-generated lyrics from Suno AI often include common clichés like “echoes,” “whispers,” “neon lights,” “grace,” “embrace,” “soar,” and especially “rise above.” This repetition can make the lyrics sound unoriginal and predictable.

Why Does This Happen?
Reason 1: Training Data
AI models are trained on a vast amount of existing data, including songs with common themes and phrases. As a result, the AI tends to produce similar content.

”Songs use these words a lot, AI was trained on songs, so you end up with these words in your AI songs.”

Reason 2: Predictive Text Nature
AI works by predicting the next word in a sequence based on the context provided. This often leads to the use of familiar and safe choices.

”AI doesn’t use logic or reasoning. It’s not an intentional limitation or conspiracy, it’s how they work. LLMs in particular are basically predictive text, giving you one word after the other of the most likely to follow.”

Examples of Common Clichés
Neon lights
Whispering woods
Rise above
Concrete jungles
Story unfolds
Echoes of…
Strategies to Avoid Clichés
Strategy 1: Use Specific Prompts
Be specific in your prompts to guide the AI away from common clichés. Explicitly mention words or phrases you want to avoid.

”You have to also prompt it to not use said clichés. I usually revise the song by replying ‘Same, but don’t use x’.”

Strategy 2: Refine and Edit
Generate a rough draft with the AI and then manually refine and edit the lyrics to make them more original.

”First, write a rough draft… then put all that into GPT and ask it to polish it, not rewrite or start from scratch.”

Strategy 3: Combine AI and Human Creativity
Use AI for inspiration and rough drafts, but rely on human creativity for the final product. This ensures originality and avoids overused phrases.

”AI is ok for directions for imagery or the odd rhyme but you have to DIY at this level of capability.”

Strategy 4: Train the AI
You can train AI like ChatGPT to remember instructions. For instance, instruct it to avoid specific clichés and use structured formats for song sections.

”One of the nice things about ChatGPT is that it will remember instructions that you give it. For example, I’ve already trained it to remember to put brackets around song sections, ie [Verse], [Chorus], etc. My next step is to train it to avoid a list of overused clichés.”

Additional Tips
Tip 1: Use Tools for Refinement
Use rhyme and thesaurus tools to refine your lyrics and avoid repetitive phrases.

Tip 2: Experiment with Different AI Models
Try different AI models or combine multiple models to generate more diverse and original content.

”Freshbots.org seems to minimize the neon lights and other stuff. Restricted by genre though.”

Tip 3: Stay Updated on AI Improvements
Keep an eye on updates from Suno AI and other platforms as they improve their models to reduce reliance on clichés.

By following these strategies, you can create more original and engaging lyrics using Suno AI while avoiding common clichés that make your songs sound repetitive.

Suno Subgenre Performance
Introduction
Suno AI is a tool that generates music based on prompts. Users have noticed that it excels in some subgenres while struggling with others. Let’s break down these observations and offer solutions.

Suno’s Struggles
1. Early Post-Punk and Jangly Guitar
Suno seems to have difficulty replicating the early post-punk sound, especially with jangly guitar elements like in “This Charming Man” by The Smiths.

2. Boyband Music
Creating early 2000s boyband music poses a challenge. Users reported the AI’s inability to generate accurate intro noises like the private jet arrival.

Still didn't manage to get the private jet arrival noise as an intro for a boyband song

3. Dubstep and EDM
While Suno can handle basic DnB and Latin pop, it struggles with more complex EDM genres, especially those requiring heavy sound design.

It struggles with DnB in general. As a workaround, specify "Drum and bass, drum and bass, drum and bass" in the style.

https://suno.com/song/d9cba71c-ab71-4904-aeed-c9eaeaae9bbc

4. Mandarin Music
Suno often struggles with Mandarin songs, likely due to insufficient training data. Korean and Japanese songs seem to fare better.

Mandarin songs are of pretty poor quality right now.

5. Metal Subgenres
Suno has issues with extreme metal genres like doom and black metal. The AI-generated riffs often miss the mark.

Struggles a lot with extreme metal like doom and black metal. The riffs it makes are so wack.

https://suno.com/song/f4dc326e-4d95-475b-ac7a-9f02c64fbebc

Suno’s Strengths
1. Trap Music
Users consistently find Suno excels in creating trap music, often producing high-quality bangers.

2. Lofi Music
Suno shines in generating various lofi subgenres like soul, RnB, and chill hop.

3. Jazz and Blues
1920s-1950s jazz and blues, particularly with female vocals, are areas where Suno performs well, though sometimes the vocals sound robotic.

I've had great success with 1920's jazz and 1950's style blues with female vocals.

4. Country and Indie
Suno is effective in generating country and indie music, providing a believable and authentic sound.

Solutions and Tips
1. Modify Prompts
To get better results, especially for difficult genres, modify your prompts. Repeat the genre name multiple times to emphasize it.

Specify "Drum and bass, drum and bass, drum and bass" in the style to improve DnB results.

2. Use Original Content
Ensure the lyrics and music you input are original to avoid issues with sampling and copyright.

3. Dispute Incorrect Claims
If you encounter incorrect sampling detections, dispute them. Automated detections can often be overturned with a human review.

I've made original music where a tiny section that sounded similar to some obscure song got flagged. Nothing a quick dispute didn’t fix.

Conclusion
Suno AI has its strengths and weaknesses across different music genres. By understanding these, you can better tailor your prompts to achieve the desired results. Keep experimenting and adapting to make the most of this powerful tool.

Tips for Making Trap Songs
Introduction
Creating Trap songs with Suno AI can be even more fun and creative with some handy tricks. This post discusses how to make the AI incorporate certain words throughout the song by placing them at the top of the lyrics page.

The Trick: Incorporate Words Creatively
If you place words at the top of your lyrics page without any notation before you start any descriptive tags like [Intro], Suno AI will often use those words repeatedly in amazing ways.

Example 1:

Jack Spratts Trap

Example 1 Link

Example 2:

Red in the Hood

Example 2 Link

How it Works
Using Keywords
When you put keywords at the beginning of your lyrics page, Suno AI recognizes these and incorporates them throughout the song. This technique can add a unique and cohesive touch to your tracks.

Try It Yourself
Experiment with different words and see how Suno AI weaves them into your music. Share your results to see what creative combinations you and the AI can come up with.

Examples and Results
Creative Integration
Users have reported impressive results using this trick. The AI’s ability to incorporate these words into the background or as hooks can add depth and creativity to your tracks.

User Example:

Trap/Phonk: Incurable by @lyricist | Suno

Example Link

Feedback and Community
Many users have found this technique useful and enjoyable. Sharing experiences and tips within the community helps everyone improve their AI-generated music.

Community Comment:

Miss Muffet's Revenge almost took me out lmaoo

Expanding Creativity
Beyond Trap
This technique isn’t limited to Trap songs. It works well in other genres too, like trance or techno, by placing words in parentheses or other creative ways.

Improvisation and Hallucinations
Some users appreciate the AI’s ‘hallucinations’ or unexpected improvisations, which can enhance the overall creative flow of the music.

Example Comment:

I like it more when it improvises and makes it all sound even better.

Conclusion
Using simple tricks with Suno AI, like placing keywords at the top of your lyrics page, can significantly enhance your Trap songs. Experiment, share your creations, and enjoy the creative process!

Guide Suno with Prompts for Better Music
Introduction
Many users have discovered effective ways to get Suno AI to produce music in specific styles by using well-structured prompts. This involves setting the style of instrumentals, vocals, and even musical notation.

Formatting Prompts
Using Styles and Clean Vocals
You can prompt Suno to create different sections of a song by specifying the style of instrumentals and vocals. For example:

(Chorus) [Heavy riffs, driving beat, powerful clean vocals with a soaring melody]:

Musical Notation
Another cool trick is to guide Suno to sing to specific notes per syllable. This helps in creating a more structured musical output.

(Verse 1) [Soft synths, steady beat, clean, gentle vocals]
(G)Beat (G)of (G)the (G)heart, a (G)stea- (G)dy (G)drum
(G)Life (G)throws its (G)punch- (G)es, but (G)we (G)o- (G)ver- (G)come

Examples
Here is an example of a song generated using this method: Suno Example

Issues and Solutions
Bracket Confusion
Issue
Sometimes, using parentheses may cause Suno to interpret the text as background singing.

Solution
To avoid this, you can use square brackets and ensure the format is correct.

Example:

(Chorus) [heavy riffs, guttural aggressive vocals with a soaring melody, clean vocals]:

Suno’s Prompt Syntax
Issue
Suno’s prompt syntax can be unpredictable due to the random seed applied at the end.

Solution
Be consistent with the format and tweak the prompts to achieve desired results.

Tips for Better Results
Context Recognition
Suno often recognizes certain words like “Chorus,” “Verse,” etc., as section names. Even if you format these names differently, Suno might still understand them.

Testing and Patience
Be patient and test various formats to see what works best. Sometimes, even slight changes in prompt format can yield better results.

Use of AI Tools
Consider using other AI tools to generate prompts that can guide Suno more effectively. For instance, using Google’s Gemini to create a prompt for a specific music style.

Vocal Instructions
Explicitly instructing the type of vocals can significantly improve the output.

Example:

Try adding clean vocals to the lyrics box prompt to get a more organic and natural vocal.

Additional Examples
Here is another song created with similar techniques: Suno Song Example

Conclusion
By using these structured prompts and understanding Suno’s syntax, you can create more controlled and high-quality musical outputs. Experiment, be patient, and enjoy making music with Suno AI!

