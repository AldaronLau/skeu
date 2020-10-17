# Skeu Sample Pack 1.0
#### Targets SF2, SFZ, And YFS Formats!

A completely public domain sample pack.  That means you can take samples from
this sample pack and use it in a sample pack you're building - no questions
asked, and no attribution required!  And of course, you can sample the sounds in
your own songs as well.  I will maintain this repository, by both adding new
sounds (minor version release), or improving sounds (major version release).

## Files
Heres a list of folders and file naming conventions.

 - `/per/*_one_VARIANT`: Solo percussive recordings
 - `/per/*_mix_VARIANT`: Multiple percussive samples mixed (same instrument)

 - `/sus/*_one_VARIANT`: Solo sustained recordings (5 seconds)
 - `/sus/*_mix_VARIANT`: Section sustained recordings (5 seconds)

 - `/out/skeu.sf2`: Output SoundFont2
 - `/out/skeu.zip`: Output SFZ SoundFont
 - `/out/skeu.yfs`: Output SynthFall SoundPack

### Audio Generation
Not all sounds in this soundfont are just recordings.  The "one" and "mix" kits
are the only two natural SoundKits.  Everything else can be generated either
alone or from those samples.  Here's a list of kits:

 - `one`: A solo instrument
 - `mix`: Multiple instruments blended together (a section)
 - `gat`: Gated reverb samples (`per/one` + synth-tree)
 - `syn`: Purely synthesized samples (synth-tree)
 - `cho`: Chorus effect (`one` + synth-tree)
 - `bit`: Retro 8-Bit samples

## Format
The audio format used is FLAC in a Matroska container.

### WAV To FLAC MKA
```bash
ffmpeg -i ${FILENAME}.wav ${FILENAME}.flac
ffmpeg -i ${FILENAME}.flac -c:a copy ${FILENAME}.mka
```

### FLAC MKA To WAV
```bash
ffmpeg -i ${FILENAME}.mka ${FILENAME}.wav
```
