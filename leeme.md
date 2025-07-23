# 🎵 Suno AI Song Syntax Guide

Una guía completa para crear canciones profesionales con Suno AI usando la sintaxis correcta y técnicas avanzadas.

## 📋 Tabla de Contenidos

- [🎵 Suno AI Song Syntax Guide](#-suno-ai-song-syntax-guide)
  - [📋 Tabla de Contenidos](#-tabla-de-contenidos)
  - [🌟 Ejemplo Avanzado](#-ejemplo-avanzado)
  - [📖 Descripción General](#-descripción-general)
  - [🏷️ Tags Base](#️-tags-base)
  - [🎯 Tags Detallados](#-tags-detallados)
    - [[Intro]](#intro)
    - [[Hook]](#hook)
    - [[Pre-Chorus]](#pre-chorus)
    - [[Chorus]](#chorus)
    - [[Verse]](#verse)
    - [[Interlude]](#interlude)
    - [[Break]](#break)
    - [[Movement]](#movement)
    - [[Instrumental]](#instrumental)
    - [[Solo]](#solo)
    - [[Build]](#build)
    - [[Bridge]](#bridge)
    - [[Outro]](#outro)
    - [[End]](#end)
  - [🎤 Tags Vocales](#-tags-vocales)
  - [🎸 Tags de Instrumentos](#-tags-de-instrumentos)
  - [📝 Ejemplos Prácticos](#-ejemplos-prácticos)
    - [Ejemplo Simple](#ejemplo-simple)
    - [Ejemplo Intermedio](#ejemplo-intermedio)
    - [Ejemplo Complejo](#ejemplo-complejo)
  - [🎨 Estilos Musicales](#-estilos-musicales)
  - [🖼️ Arte de Álbum](#️-arte-de-álbum)
  - [🎯 Formato de Salida](#-formato-de-salida)
  - [🖼️ Miniaturas](#️-miniaturas)

## 🌟 Ejemplo Avanzado

```markdown
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
```

## 📖 Descripción General

Suno utiliza Chirp para generar canciones, que es un modelo generativo. Debemos crear documentos que guíen correctamente al modelo. Para esto, utilizamos tags específicos para dividir las canciones en secciones que el modelo comprende.

## 🏷️ Tags Base

Lista de todos los tags válidos. Cada uno puede ser modificado y tiene varias formas de uso:

- `[Intro]`
- `[Hook]`
- `[Pre-Chorus]`
- `[Chorus]`
- `[Verse]`
- `[Interlude]`
- `[Break]`
- `[Movement]`
- `[Instrumental]`
- `[Solo]`
- `[Build]`
- `[Bridge]`
- `[Outro]`
- `[End]`
- `[<vocals>]` *(especificación posterior)*
- `[<specific instrument>]` *(especificación posterior)*

## 🎯 Tags Detallados

### [Intro]

**Uso:** Solo al inicio, generalmente instrumental.

**Modificadores recomendados:**
- `[Long Mellow Intro]`
- `[Short Exciting Intro]`
- `[Dreamy Slow Intro]`

> 💡 **Tip:** Funciona mejor con adjetivos emocionales y de ritmo concretos (velocidad, emoción, intensidad).

### [Hook]

**Uso:** No siempre necesario, útil para transiciones desde la intro.

### [Pre-Chorus]

**Uso:** Tag estrictamente vocal, introduce la narrativa.

**Modificadores efectivos:**
- `[Haunting Whispered Pre-Chorus]`
- `[Staticky Spoken Pre-Chorus]`
- `[Primal Scream Pre-Chorus]`
- `[Opera Female Pre-Chorus]`

### [Chorus]

**Uso:** Elemento principal de la canción.

**Modificadores funcionales:**
- `[Whispered Chorus]`
- `[Eerie Chorus]`
- `[Ensemble Chorus]`
- `[Slow Chorus]`

**Técnicas líricas importantes:**
- `...` → Ralentiza la interpretación
- `!` → Enfatiza la línea
- `Oooooohhh whoaaa ahhhh!` → Vocalizaciones explícitas
- `mmmmmmmmmmm oh...` → Vocalizaciones suaves
- `(parenthesis lyrics)` → Call-and-response o efectos antifonales

### [Verse]

**Uso:** Otro elemento principal, similar al chorus.

**Modificadores efectivos:**
- `[Angry Verse]`
- `[Mysterious Verse]`
- `[Whispered Verse]`
- `[Spoken Verse]`
- `[Opera Verse]`

**Ejemplo de técnicas líricas:**
```markdown
I am the void between stars
(Beyond the veil of forms...)
I am the death of light
(Where your deepest terrors remain...)
```

### [Interlude]

**Uso:** Sección instrumental.

**Modificadores confiables:**
- `[Melodic Interlude]`
- `[Long Melancholy Interlude]`
- `[Short Accelerating Interlude]`

**Modificadores rítmicos:**
```markdown
[Melodic Interlude]
. . . ! . .
. ! . . . !
```

```markdown
[Intense Interlude]
!! . ! !! !
!! !! ! !!
```

### [Break]

**Uso:** Instrumental breve, ideal entre versos y chorus.

**Modificadores que funcionan:**
- `[Violin Break]`
- `[Drum Break]`
- `[Scream Break]`
- `[Lead Guitar Break]`
- `[Bass Guitar Break]`

### [Movement]

**Uso:** Tag experimental para transiciones.

**Ejemplos:**
- `[Begin Psychedelic Movement]`
- `[Transition to Faster Harder Movement]`
- `[Long Orchestral Movement]`

> ⚠️ **Advertencia:** El sistema puede ignorar completamente este tag.

### [Instrumental]

**Uso:** Tag multipropósito para separar secciones.

### [Solo]

**Uso:** Exactamente lo que esperas.

**Mejores prácticas:**
- `[Soaring Lead Guitar Solo]`
- `[Fast and Intense Drum Solo]`
- `[Dancing Fiddle Solo]`
- `[Playful Flute Solo]`
- `[Finger Style Guitar Solo]`

> 💡 **Patrón exitoso:** instrumento + ritmo + emoción/energía

### [Build]

**Uso:** Menos efectivo que interlude o solo, úsalo con moderación.

**Mejor aplicación:** Entre verse y chorus para construir hacia un chorus elevado.

### [Bridge]

**Uso:** El sistema a menudo no reconoce este tag correctamente.

**Recomendación:** `[Instrumental Bridge]` tiende a ser más efectivo.

### [Outro]

**Uso:** Señala al sistema que prepare el final.

**Modificadores útiles:**
- `[Long Fading Outro]`
- `[Urgent Loud Outro]`
- `[Mournful Outro]`

### [End]

**Uso:** Finaliza la canción.

**Modificadores:**
- `[Fade to End]`
- `[Lingering End]`
- `[End Resolves to Whispers]`

## 🎤 Tags Vocales

Para cambios significativos en las voces:

```markdown
[Spoken Word Narration]
*static* ...final log... coordinates unknown...
...oxygen critical... systems failing...
...tell earth we made it... we saw such beautiful things...
...orion spur expedition... signing off... *static*
```

**Ejemplos adicionales:**
- `[Telephone Call]`
- `[Female Opera Singer]`
- `[Swanky Crooning Male]`
- `[Ethereal Female Whisper]`

## 🎸 Tags de Instrumentos

Úsalos en lugar de solos o como parte de ellos:

```markdown
[Sad Trombone]
waah-Waaah-WAAH

[Chugging Guitar]
chuka-chuka-chuka-chuka

[Overblown Flute]

[Trilling Pennywhistle]
```

## 📝 Ejemplos Prácticos

### Ejemplo Simple

```markdown
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

### Ejemplo Intermedio

```markdown
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

### Ejemplo Complejo

```markdown
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

[verse]
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

## 🎨 Estilos Musicales

**Límite:** 120 caracteres total, separado por comas.

**Ejemplo exitoso:**
```
stoner space rock shoegaze slow build epic crescendos psychedelic riffing soaring solos pensive interludes long intro
```

**Con comas (recomendado):**
```
space rock, stoner rock, slow build, epic crescendos, psychedelic riffing, soaring solos, pensive interludes, shoegaze
```

**Solo géneros (muy efectivo):**
```
space rock, psychedelic rock, desert rock, stoner rock, shoegaze
```

**Ejemplos adicionales:**
- `witchpop, electro swing, eerie`
- `witchpop, house, hypnotic, dreamy, eerie`
- `Acoustic, Desert, Nubidian, Acoustic nu-metal`
- `Hurdy-gurdy, dark, scary, otherwordly`

**Elementos que funcionan mejor:**
- **Géneros:** Uno o más en secuencia
- **Emociones:** Vibes para acompañar
- **Instrumentos:** Especialmente si no son obvios del género
- **Estilos vocales:** Opera, growling, etc.

## 🖼️ Arte de Álbum

**Estructura básica:**
1. Empezar con "album art"
2. Estilos o géneros principales
3. Sujeto principal y construcción de escena
4. Detalles, colores, modificadores emocionales y texto

**Ejemplos:**
- `album art: psychedelic desert scene, super trippy, cactus and iguana and hot sun, vivid colors`
- `album art: statuesque feminine figure emerging from cosmic darkness, her classical features barely visible beneath translucent hood, wings of pure void extending gracefully outward consuming light`
- `album art, psychedelic, bronze giant, talos on crete, minoan, text reads "STARGAZER" at the top`

## 🎯 Formato de Salida

**Siempre usar tags de escape de código:**

```markdown
[Verse]
<lyrics>
```

> 📝 **Nota:** Esto facilita copiar y pegar tu salida exactamente.

## 🖼️ Miniaturas

**Formato para miniaturas:**

```
- Album art: <sujeto principal>, <fondo/contexto>, <estilos visuales>, <colores y mood>, text reads "STARGAZER" at the top
- Album art: <sujeto principal>, <fondo/contexto>, <estilos visuales>, <colores y mood>, text reads "STARGAZER" at the top
- Album art: <sujeto principal>, <fondo/contexto>, <estilos visuales>, <colores y mood>, text reads "STARGAZER" at the top
- Album art: <sujeto principal>, <fondo/contexto>, <estilos visuales>, <colores y mood>, text reads "STARGAZER" at the top
```

**Ejemplos de detalle variable:**

**Detallado:**
```
album art, psychedelic, a beautiful feminine figure dances in the silver moonlight, temple archway, night sky, dark mountains in the distance, flowing dress and feathers, dark and light, mystical, blues and silver and black, text reads "STARGAZER" at the top
```

**Simple:**
```
album art, psychedelic, a robot surfing the waves, longboard, "STARGAZER" at the top
```

---

> 🎵 **¡Diviértete creando música increíble con Suno AI!** Esta guía te ayudará a dominar la sintaxis y crear canciones profesionales.
