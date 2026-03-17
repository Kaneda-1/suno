# Suno AI Song Syntax & Prompting Guide

A comprehensive guide for creating professional-quality songs with Suno AI using correct syntax, advanced tags, and optimization techniques.

## 📋 Table of Contents
1. [Overview](#overview)
2. [Base Tags](#base-tags)
3. [Detailed Tag Guide](#detailed-tag-guide)
4. [Vocal and Instrument Tags](#vocal-and-instrument-tags)
5. [Controlling Dynamics & Chorus](#controlling-dynamics--chorus)
6. [Suno Pro Optimization (1000 Chars)](#suno-pro-optimization-1000-chars)
7. [Advanced Notation (Rhythm & Timing)](#advanced-notation-rhythm--timing)
8. [Album Art & Sora Prompts](#album-art--sora-prompts)
9. [Music Style Guide](#music-style-guide)
10. [Examples](#examples)
11. [Supplementary Guides](#supplementary-guides)

---

## 📖 Overview
Suno uses the Chirp model to generate songs. To get the best results, you must use specific metatags to structure your song into sections the model understands. This guide covers how to use these tags effectively, providing a technical blueprint for the AI to follow.

## 🏷️ Base Tags
The following are the standard tags recognized by Suno. Each can be modified with adjectives:
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

---

## 🎯 Detailed Tag Guide

### [Intro]
Used at the beginning, usually strictly instrumental.
*   **Modifiers:** `[Long Mellow Intro]`, `[Short Exciting Intro]`, `[Dreamy Slow Intro]`
*   **Tip:** Use concrete adjectives related to speed, emotion, or intensity.

### [Pre-Chorus]
Strictly vocal, used to introduce the narrative before the chorus.
*   **Modifiers:** `[Haunting Whispered Pre-Chorus]`, `[Primal Scream Pre-Chorus]`

### [Chorus]
The main hook of the song. Lyric construction (punctuation, vocalizations) often has a bigger impact than the tag itself.
*   **Modifiers:** `[Whispered Chorus]`, `[Ensemble Chorus]`, `[Slow Chorus]`
*   **Techniques:** Use `(parentheses)` for call-and-response or `Oooooohhh` for explicit vocalizations.

### [Verse]
The narrative workhorse.
*   **Modifiers:** `[Angry Verse]`, `[Mysterious Verse]`, `[Spoken Verse]`

### [Interlude] & [Solo]
Instrumental sections. Specifying the lead instrument is highly effective.
*   **Examples:** `[Soaring Lead Guitar Solo]`, `[Melodic Interlude]`, `[Fast Drum Solo]`

### [Outro] & [End]
Signals the song's conclusion.
*   **Modifiers:** `[Long Fading Outro]`, `[Fade to End]`, `[End Resolves to Whispers]`

---

## 🎤 Vocal and Instrument Tags
You can specify vocal styles or instrumental cues directly:
- `[Spoken Word Narration]`
- `[Female Opera Singer]`
- `[Ethereal Female Whisper]`
- `[Chugging Guitar]`
- `[Sad Trombone]`

---

## 📈 Controlling Dynamics & Chorus
Suno naturally increases intensity during choruses. To maintain a uniform dynamic (e.g., for intimate ballads), use:
- `restrained chorus dynamics`
- `same arrangement and volume as verses`
- `avoid dramatic build`

Include these in the **Suno Pro** Style Prompt to prevent unwanted crescendos.

---

## 🚀 Suno Pro Optimization (1000 Chars)
Suno Pro/Premier allows up to 1000 characters for the Style Prompt. Use this space for a detailed technical specification.

**Optimization Formula:**
`[Primary Genre] featuring [Vocal Characteristics], [Detailed Instrumentation], [Technical Production Elements (Analog warmth, Dolby Atmos, EQ balance)]. [Musical Structure] at [BPM] in [Time Signature]. [Theme and Mood].`

*   **Characters:** Aim for 950-1000 characters for maximum precision.

---

## 📝 Advanced Notation (Rhythm & Timing)

### Instrumental Rhythms
Use dots and exclamation marks to guide the AI's rhythmic intensity:
- `!! . ! !! !` (Aggressive/Intense)
- `. . . ! . .` (Gentle/Melodic)

### Vocal Timing
- `...` (Ellipses): Slows down delivery or creates pauses.
- `!` (Exclamation): Adds emphasis.
- `(parentheses)`: Indicates backing vocals or echoes.

---

## 🎨 Album Art & Sora Prompts

### Artwork Prompts
Structure: `album art: [main subject], [background/context], [visual style (psychedelic, 8K ultrarealistic)], [colors/mood], text reads "[TITLE]"`

### Sora Prompt (for Album Covers)
`8K ultrarealistic intimate chamber music setting, elegant acoustic grand piano, warm golden lighting, shallow focus with cinematic bokeh, no text, museum-quality photography.`

---

## 🎸 Music Style Guide
A quick reference for style modifiers:
- **Classic Rock:** Distorted guitars, raw noise texture, vintage amp distortion.
- **Ambient:** Spatial depth, analog synth warmth, ethereal vocals, reverb-rich.
- **Acoustic:** Fingerpicked texture, close mic intimacy, raw performance.
- **Electronic:** Modern stereo imaging, sidechain compression, digital clarity.

---

## 🎼 Examples

### Intermediate Structure Example
```markdown
[Long Instrumental Intro]

[Verse 1]
Sun beats down hard dry road
Dust devils dance shadows long...

[Chorus]
Lost in the wasteland void
Seeking the promised land

[Lead Guitar Solo]
!! . ! !! !

[Outro]
[Fade to End]
```

### Complex "Suno Pro" Optimized Example
**Style Prompt:** `Passionate Spanish pop ballad featuring male vocals with Andalusian accent, fingerpicked nylon string Spanish guitar, grand piano, lush string orchestra, traditional cajón percussion. Intimate verses building to soaring choruses. Tempo 80 BPM in 4/4. Warm analog recording, subtle cathedral reverb, 1000 characters of technical detail.`

---

## 📚 Supplementary Guides
*   [Claude Optimization Guide](./README_CLAUDE_EN.md): Learn how to use Claude to generate and optimize Suno songs.
*   [Classical & Fusion Master Prompt](./CLASSICAL_EN.md): Specialized prompt structure for classical and fusion genres.

---
*Created for the Suno AI community. Master the syntax to master the sound.*
