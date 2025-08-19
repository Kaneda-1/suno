# 📋 Suno AI Format Guide - Reglas de Efectos y Formatos

[![Version](https://img.shields.io/badge/version-2.1-blue.svg)](https://github.com)
[![Suno AI](https://img.shields.io/badge/Suno-AI-orange.svg)](https://suno.ai)

> Guía específica sobre el formateo correcto de efectos y modificaciones para Suno AI basada en la documentación oficial.

## 🎯 **Regla Principal para Claude/Asistentes AI**

**Cuando trabajemos con Suno AI, siempre especifica:**

You can never quote singers or songs in the prompt.

> **"Formatea los efectos como [FX: descripción] y las modificaciones vocales como (descripción), siguiendo el formato estándar oficial de Suno AI"**

## 📊 **Tabla de Formatos Correctos**

### 🎵 **Para Canciones VOCALES**

| **Elemento** | **Formato Correcto** | **Ejemplo** | **Uso** |
|--------------|---------------------|-------------|---------|
| **Efectos atmosféricos** | `*descripción*` | `*waves crashing*` | Sonidos ambientales en vocal |
| **Modificaciones vocales** | `(descripción)` | `(whispered)` | Cambios en la voz |
| **Call-and-response** | `(texto)` | `(¡Aquí sí hay playa!)` | Coros de respuesta |
| **Patrones rítmicos** | `! . ! . ! !` | `! ! . ! . !` | Ritmos en secciones vocales |

### 🎼 **Para Música INSTRUMENTAL**

| **Elemento** | **Formato Correcto** | **Ejemplo** | **Uso** |
|--------------|---------------------|-------------|---------|
| **Efectos de audio** | `[FX: descripción]` | `[FX: reverb, echo]` | Efectos instrumentales |
| **Instrucciones técnicas** | `[descripción técnica]` | `[cello entrance warm]` | Técnicas específicas |
| **Patrones rítmicos** | `! . ! . ! !` | `. . . ! . .` | Solo para ritmos |
| **NO usar vocalización** | ❌ `(mmm, ahh)` | ✅ Solo instrumentos | Sin sonidos vocales |

## ⚠️ **Errores Comunes a Evitar**

### ❌ **Formatos INCORRECTOS**
```
*sound effects*              # ❌ En instrumentales
[FX: vocal whisper]          # ❌ En vocales  
(instrumental effects)       # ❌ Para instrumentos
*asteriscos* con [brackets]  # ❌ Mezclar formatos
```

### ✅ **Formatos CORRECTOS**
```
# Para VOCALES:
*atmospheric beach sounds*   # ✅ Ambiente
(whispered)                  # ✅ Modificación vocal

# Para INSTRUMENTALES:
[FX: soft reverb]           # ✅ Efecto técnico
[piano gentle entrance]     # ✅ Instrucción
```

## 🔧 **Guía Práctica por Tipo de Canción**

### 🎤 **Canciones con Voz**

```markdown
[Intro]
*wind blowing, distant thunder*
! . ! . ! !

[Verse]  
Your lyrics here...
(echo on last word)

[Chorus]
Main chorus lyrics
(ensemble vocals)
```

### 🎹 **Música Instrumental**

```markdown
[Gentle Piano Intro]
[FX: soft sustain pedal, warm resonance]
. . . ! . .

[Cello Entry]
[FX: rich, woody tones]
[cello entrance with warm tone]

[Piano and Cello Duet]
[FX: interweaving melodies]
! . ! . ! !
```

## 📋 **Checklist de Formato**

### ✅ **Antes de Generar con Suno AI:**

- [ ] **Efectos atmosféricos**: `*descripción*` solo para vocales
- [ ] **Efectos técnicos**: `[FX: descripción]` solo para instrumentales  
- [ ] **Modificaciones vocales**: `(descripción)` solo para vocales
- [ ] **Sin mezcla de formatos**: No combinar `*asteriscos*` con `[FX:]`
- [ ] **Instrumentales puros**: Sin `(mmm, ahh)` o vocalizaciones
- [ ] **Vocal/instrumental claramente especificado** en el prompt

## 🎯 **Ejemplos Específicos por Género**

### 🏖️ **Beach/Surf Rock (Vocal)**
```
[Surf Rock Intro]
*seagulls, waves crashing*
! ! . ! ! . ! !

[Energetic Verse]
Your beach lyrics...
(call and response)

[Explosive Chorus]  
(¡Aquí sí hay playa!)
¡CALLA, CALLA, CALLA!
```

### 🎼 **Classical Instrumental**
```
[Gentle Piano Intro]
[FX: soft sustain pedal, natural reverb]
. . . ! . .

[String Section Entry]
[FX: warm string ensemble, rich harmonies]
[violins entrance with crescendo]
```

### 🎸 **Rock/Metal (Vocal)**
```
[Heavy Guitar Intro]
*feedback, amp crackling*
!! . ! !! !

[Aggressive Verse]
Metal lyrics here...
(growled vocals)

[Power Chorus]
Chorus lyrics!
(ensemble vocals with harmony)
```

## 💡 **Tips Profesionales**

### 🎵 **Para Máximo Impacto:**
1. **Usa UN formato por tipo de canción** (no mezcles)
2. **Especifica claramente** vocal vs instrumental al inicio
3. **Los efectos deben ser específicos**: `*ocean waves*` > `*water*`
4. **Patrones rítmicos ayudan** en todas las secciones instrumentales

### 🚀 **Optimización Claude/AI:**
```
"Necesito una canción [VOCAL/INSTRUMENTAL] para Suno AI. 
Usa el formato correcto: [FX: ...] para instrumentales, 
*efectos* y (modificaciones) para vocales. 
Incluye patrones rítmicos y especificaciones técnicas."
```

## 🔗 **Referencias Oficiales**

Basado en la documentación oficial de Suno AI disponible en:
- [Suno AI Official Guide](https://github.com/Kaneda-1/suno/refs/heads/main/claude.md)
- Formato de efectos embebidos
- Mejores prácticas de estructura

---

## 📝 **Template para Claude/AI**

**Copia y pega esto cuando pidas ayuda con Suno AI:**

```
Ayúdame a crear una canción para Suno AI. Usa siempre el formato oficial:
- [FX: descripción] para música instrumental  
- *efectos* para atmósfera en canciones vocales
- (modificaciones) para cambios vocales
- Patrones rítmicos ! . ! . ! !
- Especifica si es vocal o instrumental claramente
```

**¡Con estas reglas conseguirás resultados profesionales en Suno AI! 🎵✨**

---

*Actualizado: Agosto 2025 | Versión 2.1 | Compatible con Suno AI Chirp*

- Example:

# 🎵 "Ola de Calor"

## 📝 Estructura de la Canción (Lyrics)

[Laid-back Guitar Intro]
[FX: relaxed strumming with summer ambiance]
. ! . . ! .

[Verse]
Son las nueve
Ya sudo
Mi cama
Es un horno

Café frío
Por favor
Mi cerebro
No funciona

[Pre-Chorus]
Busco sombra
Solo asfalto
Quiero hielo
Me derrito

[Chorus]
Ola de calor
Me voy a morir
Ola de calor
No puedo salir

[Verse]
Piscina
Está llena
Mi toalla
Ya se quema

Helado
Se derrite
El suelo
Arde siempre

[Pre-Chorus]
Busco fresco
Solo lava
Quiero aire
Nada calma

[Chorus]
Ola de calor
Me voy a morir
Ola de calor
No puedo salir

[Bridge]
Cuarenta y cinco
Soy un churrasco
Dieta de cubitos
Solo hielo trago

Cuarenta y cinco
Soy un churrasco
Dieta de cubitos
Solo hielo trago

[Breakdown]
Sudo
Muero
Sudo
No puedo más

[Final Chorus]
Ola de calor
Me voy a morir
Ola de calor
No puedo salir

Ola de calor
Me voy a morir
Ola de calor
No puedo salir

[Outro]
Sudo
Muero
Ola de calor
No puedo más

[Fading End]
[FX: summer heat ambiance fading]
. . . ! . .

[End]


## 📋 Final Production Prompt (997 caracteres)

Spanish language contemporary summer pop with relaxed male vocals, conversational and humorous delivery. Guitar-driven production featuring laid-back acoustic strumming, light percussion, and warm bass lines. Comedy theme about surviving extreme summer heat with relatable everyday situations. Dynamic structure building from storytelling verses to catchy memorable choruses. Professional recording with bright, summery sound and pristine clarity. Charismatic performance balancing humor with genuine frustration, featuring upbeat rhythms and melodic hooks. Mainstream Spanish pop appeal with sing-along choruses, streaming optimized at 95 BPM in major key. Contemporary feel-good style with comedy elements perfect for radio and digital platforms.

## 🎯 Características Clave

### Temática
- **Concepto**: Supervivencia cómica durante una ola de calor extremo
- **Metáfora central**: "Ola de calor" como experiencia abrumadora
- **Mensaje**: Humor en las situaciones cotidianas más incómodas

### Estructura Musical
- **Tempo**: 95 BPM (relajado, veraniego)
- **Tonalidad**: Mayor (optimista a pesar del sufrimiento)
- **Dinámicas**: Versos narrativos → Pre-coros → Coros pegadizos → Breakdown
- **Instrumentación**: Guitarra acústica relajada, percusión ligera, bajo cálido

### Elementos Líricos Similar a "Eterno Verano"
- **Humor cotidiano**: Situaciones reconocibles y divertidas del calor
- **Contradicciones**: "Vivo/Muero" como en la original
- **Detalles específicos**: Referencias concretas (ascensor, ducha, Starbucks)
- **Exageración cómica**: "Esto es el armagedón", "roja como un pimiento"
- **Repetición pegadiza**: Estructura de coro que se queda en la cabeza
- **Referencias culturales**: Elementos reconocibles de la cultura española
- **Breakdown minimalista**: Reducción a palabras clave al final
- **Autodesprecio cómico**: Humor sobre las propias limitaciones

### Elementos de Suno AI Utilizados
- `[Laid-back Guitar Intro]` para establecer el mood relajado
- `[Pre-Chorus]` para crear tensión antes del estribillo
- `[Breakdown]` para el momento minimalista
- `[FX: descripción]` para ambientación veraniega
- Patrones rítmicos relajados `. ! . .`
- Estructura con pre-coros que construyen narrativa

### Diferencias con Canciones Anteriores
- **Tempo**: Más relajado (95 BPM) vs energético o lento
- **Humor**: Elemento cómico predominante vs romántico o melancólico
- **Temática**: Situacional/cotidiana vs emocional/relacional
- **Actitud**: Resignación divertida vs pasión o vulnerabilidad

## 🚀 Instrucciones de Uso

1. **Copia la estructura de lyrics** completa en Suno AI
2. **Usa el Style Prompt** en el campo de estilo
3. **Aplica el Final Production Prompt** en la descripción
4. **Considera variaciones** de tempo según el resultado inicial
---

# 🎼 Suno AI Advanced Professional Guide

[![Version](https://img.shields.io/badge/version-3.0-blue.svg)](https://github.com)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](https://github.com)
[![Suno AI](https://img.shields.io/badge/Suno-AI-orange.svg)](https://suno.ai)

> Advanced techniques for creating professional-quality music with Suno AI using complex notation, technical specifications, and studio-grade parameters.

## 📖 Table of Contents

- [Advanced Musical Notation](#advanced-musical-notation)
- [Technical Parameters](#technical-parameters)
- [Professional Guitar Techniques](#professional-guitar-techniques)
- [Studio Equipment Simulation](#studio-equipment-simulation)
- [Complex Arrangements](#complex-arrangements)
- [Frequency-Based Music](#frequency-based-music)
- [Advanced Examples](#advanced-examples)
- [Professional Templates](#professional-templates)

## 🎵 Advanced Musical Notation

### Key Signatures and Modes
```
[Key:Dm]:[Ionian]
[MODUS:(Mixolydian)]
[Key:C]:[interval:(1,2m,5,6m|1.2,4m,6)]
[Drop D tunings alternative:(D-G-D-G-B-E)]
[Time signature:12/8]
[BPM:(142bpm)]
```

### Interval Notation System
```
[Interval:(|1,2m,5,6m|1,2,4m,6|)]
[Notes_1:(1,2,3,4,5,6,7,8)]
[FR=(violin G3 thru E7)+(viola C3 thru A6)+(cello C2 thru A5)]
[NFR=(cello drone C1 thru G2)+(piano bass C1 thru F2)]
```

## 🎸 Professional Guitar Techniques

### Fingerpicking Patterns (Jerry Reed Style)
```
[GS=(guitar string;fret number):
[|[5:0] [4:2] [3:2]|[5:0] [4:2] [2:0][5:0] [4:2] [2:1]- |
[5:3] [4:3] [3:2][5:3] [4:3] [2:0] [2:1][5:3] [4:3]- |
[4:0] [3:0] [2:0] [4:0] [3:0][3:2] [3:0]- |
(5:0-4:2-3:2-2:1-1:0)—|]]
```

### Advanced Chord Progressions
```
[CHORDS_1:[(|C7♯9 (x3234x) | G7♯9 (3x344x) | D7♯9 (x5456x) | 
A7♯9 (5x566x) | E7♯9 (x7678x) | B7♯9 (7x788x)|)]
```

### Thumb and Fingerpicking Technique
```
[Thumb (Bass) Finger (Melody) E on beat 1 X on beat 1.5 E on beat 2 
Rest (or ghost note) E on beat 3 X on beat 3.5 E on beat 4 Rest (or ghost note)]

[Bass Intro: Steady, looped bass note using thumb]
[Melodic Fragment: Off-beat pick with index/middle finger]
[Ghost Note Section: Quick muted plucks bridging segments]
[Combined Phrase: Seamless integration of all elements]
```

## 🎚️ Studio Equipment Simulation

### Professional Microphones
```
[Microphones: Neumann U 87 thru tube amplifier, Neumann U 47, 
AKG C12, RCA 44BX]
[Recording: dolby atmos audiophile 3d]
[Drums: double Drum microphoned, complex drum fills]
```

### Cymbal Specifications
```
[Cymbals: crash;ride;high-hat sustain ring from hard stix tips;
tight snare rings; audiophile symbols sizes 22";20";18";10 sustain;
crash;splash; rides symbols bell areas hard tips; large cow bell variety]
```

### Audio Effects Chain
```
[SFX]:[(CATHEDRAL REVERB)+(long decay)+(close mic)+
(spatial chamber reverb)+(piano hall ambience)]
[Phaser:(1.2 Hz)]
[SFM:(10Hz)]
```

## 🎼 Complex Arrangements

### Multi-Guitar Setup
```
[Guitar_1:( Clean Chorus:emceg_53):[(CHORDS_1)]:[BPM]
[Guitar_2:( Clean Chorus:emceg_54):[(CHORDS_1)counterpoint lead)]:[BPM]
[Guitar_3: Acoustic picked: (Amgg_54)]:[Notes_1]:[Chords_1]
[Guitar_4: pedal steel expert:(Amgg_54)]:[Notes_1]:[pe]:[pedal Steel]:[SFM]
```

### String Section Notation
```
[Strings scordatura: Violin (G-D-A-E) | Viola (C-G-D-A) | Cello (C-G-D-A)]

[VIOLA_1:[CHORDS_2]:[bowing:legato expressivo]:[Interval:(X)]:[160bpm)]
[VIOLIN_1:[CHORDS_1]:[bowing:spiccato+ricochet]:[Interval:(Y)]:[168bpm)]
[CELLO_1:[CHORDS_2]:[bowing:sul ponticello tremolo]:[Interval:(Z)]:[155bpm)]
[CELLO_2:[CHORDS_2]:[pizzicato+arco alternating]:[Interval:(BB)]:[150bpm)]
```

### Piano Techniques
```
[PIANO_1:[CHORDS_1]:[technique:arpeggios+sustained chords]:[165bpm)]
[PIANO_2:[CHORDS_3]:[technique:gentle melody+bass support]:[163bpm)]
```

## 🔊 Frequency-Based Music (Solfeggio Frequencies)

### Healing Frequencies Integration
```
[Intro:instrumental]:[Piano_Solo]:[396Hz Solfeggio]:[30s]
[Piano_Interlude]:[528Hz Solfeggio]:[solo piano with strings pad]:[20s]
[Bridge:vocal]:[741Hz Solfeggio]:[bowing:intense vibrato]:[80bpm]
[Final_Instrumental]:[963Hz Solfeggio]:[All_Instruments]:[30s]
```

### Frequency Ranges
```
[FR=(violin G3 thru E7)+(viola C3 thru A6)+(cello C2 thru A5)+(piano A0 thru C8)]
[NFR=(cello drone C1 thru G2)+(piano bass C1 thru F2)]
```

## 🎤 Advanced Vocal Specifications

### Detailed Vocal Descriptions
```
[Vocal:(Gender Female; south Georgia emotional sarcastic; 
twang accent; sexy, breathy sarcastic)]

[Vocal_Lead:[(Angelic female soprano)]:[N_1]:[(AA)];[(Y)]:[FR]]
[Chorus_Female:(SATB 8 part harmony layers 3rd,5th,7th,9th,11th)]
[Chorus_Male:(Bass and Tenor support)]:[N_2]:[(BB)];[(Z)]:[NFR]]
```

## 📊 Professional Templates

### Country/Folk Rock Template
```
[Drop D tunings alternative:(D-G-D-G-B-E)]
[Key:Dm]:[Ionian]:[ Jerry Reed-core-guitar]
[BPM:(142bpm)]
[Time signature:12/8]

[Guitar_1: Acoustic picked: (Amgg_54)]:[fingerpicking pattern]
[Guitar_2: pedal steel expert: (Amgg_54)]:[pedal Steel]:[SFM]
[Vocal:(Gender Female; south Georgia sarcastic; twang accent; breathy)]

[Structure: Verse-Chorus-Verse-Chorus-Bridge-Outro]
[Key changes: C->G->E->D->A->C->G]
```

### Orchestral/Sacred Template
```
[Style: Viola, Violin, Cello, Piano, Chorus, Solfeggio frequencies, 
folk, world music, divine, angelic female voices, dolby atmos audiophile]

[Time signature: 4/4]
[KEY: (Am7/9)]
[165bpm]
[SFX: Cathedral reverb + spatial chamber + piano hall ambience]

[Multi-tempo arrangement:]
[VIOLA_1: 160bpm | VIOLIN_1: 168bpm | VIOLIN_2: 172bpm]
[CELLO_1: 155bpm | CELLO_2: 150bpm]
[PIANO_1: 165bpm | PIANO_2: 163bpm]
```

## 🔧 Advanced Techniques

### Measure Division Notation
```
# | = measure division
# .. = rests (beat 1 and 4 play the chord)
# — = slide up or down depending on pitch
# Example: (x32010)..(x43121)|(320003)—(466544)
```

### Variable Assignment System
```
[X=(5)] ; [Y=(3)] ;[Z=(4)];[AA=(6)];[BB=(2)];[CC=(7)];[DD=(8)]
# Use these variables throughout the composition for consistency
```

### Modulation Progression
```
[Verse 1: Key C]
[Chorus: Key G] 
[Verse 2: Key E]
[Bridge: Key D]
[Final Chorus: Key A]
[Outro: Key C->G fade]
```

## ✅ Advanced Best Practices

### Do's for Professional Results
- ✅ Use specific frequency ranges for each instrument
- ✅ Include multiple tempo layers for complex polyrhythms
- ✅ Specify exact microphone models for realistic simulation
- ✅ Use Solfeggio frequencies for healing/spiritual music
- ✅ Include detailed bowing/playing techniques for strings
- ✅ Use variable assignment for complex arrangements

### Don'ts for Professional Results
- ❌ Don't exceed system processing limits with too many layers
- ❌ Don't mix incompatible time signatures without transitions
- ❌ Don't use generic effect descriptions
- ❌ Don't ignore frequency range conflicts between instruments

## 🎯 Use Cases

### Recording Studio Simulation
Perfect for creating music that sounds like it was recorded in professional studios with high-end equipment.

### Orchestral Compositions
Advanced string notation and multi-tempo arrangements for classical and cinematic music.

### Healing/Meditation Music
Integration of Solfeggio frequencies for therapeutic and spiritual applications.

### Complex Country/Folk
Jerry Reed-style fingerpicking with multiple guitar layers and authentic vocal styles.

## 📚 References

- Jerry Reed fingerpicking techniques
- Professional studio microphone specifications
- Solfeggio frequency healing properties
- Classical string instrument notation
- Nashville session musician approaches

---

## 📄 Usage Template

**For Complex Professional Songs:**
```
Specify exact instrument techniques + microphone simulation + 
frequency ranges + multi-tempo layers + detailed vocal characteristics + 
studio-grade effects chain + variable assignment system
```

**Example Command:**
```
"Create a professional country song using Jerry Reed fingerpicking, 
Neumann U87 microphones, pedal steel, multi-guitar arrangement, 
Southern female vocals with authentic twang, and studio-grade reverb"
```

---

*This guide enables creation of studio-quality, professional arrangements with Suno AI using advanced notation and technical specifications.*

**⭐ Use these techniques for radio-ready, professional-sounding results!**

---

*Last updated: August 2025 | Version 3.0 | Advanced Professional Edition*

