# Voice Asset Pipeline

This repository documents a CSV-driven workflow for creating reusable voice and dialogue assets, primarily for game development and interactive media.

The core idea is to **plan everything in a CSV, then derive everything else from it.**

Filenames, folder structure, and embedded metadata are not authored manually. They are generated from the CSV in a repeatable, scriptable way. The CSV is the single source of truth for each asset pack.

This repo exists for two reasons:

1. PTo serve as personal documentation for maintaining a consistent audio library over time
2. To share with collaborators or customers

## What Problem This Solves

Lots of sound libraries suffer from a lack of structure. Problems start to show as soon as they grow past a few dozen files. Filenames tend to become either totally overloaded or utterly cryptic, leaving artists with the burden of having to re-name and sort everything to make it usable.

This workflow aims to avoid that from the start by separating concerns:

1. identity lives in stable asset names
2. meaning lives in the CSV and metadata
3. delivery lives in the audio itself

That separation enables things like localization, repackaging, and reuse to be possible painlessly.

## The Project Structure

The workflow revolves around a small number of largely independent concepts:

 - a custom voice category system that is trigger-based rather than descriptive, for ease of use especially in video game development.
 - a fixed CSV schema that encodes intent, structure, and all metadata
 - iXML / ASWG metadata embedding for portability.
 - a script that allows me to do all mastering on a single sound project, and then export into multiple files without having to do anything manually.

The documentation is split accordingly.

## About UCS and iXML standards

This system is inspired by the Universal Category System (UCS), but not UCS-compliant.

UCS is a system for and by sound-designers, who mostly work with abstract noises. It does not formally support spoken dialogue as a category. Rather than forcing voice into ill-fitting classifications, this workflow uses an explicit VOICE category and documents how it maps conceptually to UCS-style thinking.

The same applies to metadata: iXML and the ASWG extension are used, but they are not treated as mandatory.

## Intended audience

This repository is written for:
 - individual creators like myself, building reusable dialogue libraries
 - small teams that want a shared, predictable structure

It assumes basic familiarity with CSV files, WAV audio, and scripting, but does not assume any particular DAW or game engine.

## Status

This system has evolved along with my audio production workflow, driven by my twin desires of a) not having to manually edit hundreds of sound files, and b) producing assets that are actually pleasant to work with. It might still evolve further, but this can be considered a 1.0 release: It is now stable and mature enough to produce results I am not ashamed to charge money for.   - Vorox Audio, 06-Feb-2026
