# A-Z App

Alphabet learning for **ages 3–6**, in **Czech and English**. Hear an animal,
tap the letter it starts with, bring it home to the zoo. It opens in Czech.

Everything is spoken aloud, because the audience cannot read yet, and
**there are no lives and no game over** — a wrong tap wobbles the tile, says
"try another one", and leaves the question up. The only thing at stake is how
full the zoo is.

## Download

| File | Size | For |
|---|---|---|
| `AZApp-0.1.0.html` | 118 KB | Everything. One file — double-click and it opens in any browser. No install, works offline, same on Windows, Mac, Chromebook and tablets. |

## What it teaches

Four kinds of question, all answered by tapping:

| | |
|---|---|
| **Sound** | a picture, spoken aloud → tap the letter it starts with |
| **Picture** | a letter, spoken aloud → tap the animal that starts with it |
| **Big & small** | **B** → tap **b** |
| **What is missing** | `A B _ D` → tap the one that is gone |

Czech is its own alphabet, not a translation: **42 letters**, with **CH as one
letter** between H and I. Most Czech letters cannot begin a word at all, so a
letter is only ever asked in a kind it can honestly carry, and the ones with no
animal — Ď, Ň, Ť, the long vowels — are still collected and shown as
themselves.

**MY LETTERS / MOJE PÍSMENKA** shows which letters the child knows and which
keep coming back. Letters that get missed are asked more often.

## Known limitation: the Czech voice

The app uses the browser's own speech synthesis, and **Czech pronunciation is
still not right on many machines.** Where no Czech voice is installed the words
are respelled so a foreign voice gets closer (*Beruška* → `Berooshka`), and the
title screen has a **KTERÝ HLAS** picker so you can choose and preview a voice
yourself. It helps, but it is not finished. Installing a real Czech system
voice is still much better than anything the app can do on its own.

## About this folder

Unlike the other projects here, **the A-Z App's build is committed to this
repo** (`build/`) rather than only existing as a release asset. Its source
repository was lost, and this file — recovered from a published copy — is the
only surviving version of the app. Keeping it in version control as well as in
the release is deliberate.
