# Brahui Dictionary

A single-file Brahui ⇄ Urdu-script dictionary and speech bridge. Open
[`brahui-dictionary.html`](brahui-dictionary.html) in a browser — there is no build step, no
dependency, no network call. Material 3 interface: an Android app on a phone, a two-pane desktop
app in a window.

Brahui is the Dravidian language of Balochistan, written in a Perso-Arabic alphabet with two letters
of its own — **ڷ** /ɬ/ and **ں** /ɳ/. No text-to-speech voice for it exists anywhere, so this app
generates fully vocalized Urdu orthography (zabar / zer / pesh / sukun) that an Urdu, Hindi or
English voice can be made to read out loud without guessing the short vowels.

## What it does

- **254 sourced entries and 36 phrases.** Every one carries a source tag; nothing is invented.
- **Search** across Brahui Latin, Urdu script and English at once.
- **One tap per entry** gives the Brahui orthography, IPA, the vocalized string to send to a voice,
  a diacritic-stripping fallback, Devanagari, an English respelling, the Azure IPA string, the form
  exactly as printed in the source, and the citation.
- **Speech** through the browser's own voices or Azure Speech (with `<phoneme>` IPA, the only mode
  that dictates the sounds instead of hoping). A per-machine diagnostic says which of Brahui / Urdu /
  Hindi / Punjabi / Persian / Arabic / English voices exist and what to do about the gaps —
  macOS ships no Urdu voice at all, for instance.
- **Sound inventory** with a drill button per phoneme, including the ڷ /ɬ/ check.
- **Both converters**: Latin → Brahui script, and Perso-Arabic → Latin with a marker on every short
  vowel the script could not record.
- **Your own entries** persist locally; export the whole lexicon as JSON, or as a TSV review sheet
  with the unconfirmed rows first, to hand to a Brahui speaker.

The Brolikva Latin is the source of truth. Script, IPA, Devanagari and the respelling are regenerated
from it on every read, so fixing the engine fixes every entry at once.

## Sources

| Tag | Source |
|---|---|
| `LSI` | Grierson, *Linguistic Survey of India*, Vol. IV: *Muṇḍā and Dravidian Languages* (Calcutta, 1906). Brahui occupies pp. 619–681. The 94 entries and 24 sentences come from its Standard List of Words and Phrases, Brahui of Kalat, items 1–241 — read off the page scans, because the archive's own OCR scrambles that table. [archive.org](https://archive.org/details/in.ernet.dli.2015.42222) |
| `BRAY` | Bray, *The Brahui Language, Part I: Introduction and Grammar* (Calcutta, 1909). Settles readings the 1906 scan had damaged: *khākhar* "fire", *tuh* "moon", *kātum* "head", *bīsh* "donkey", *mē* "slave". [archive.org](https://archive.org/details/in.ernet.dli.2015.13132) |
| `UDHR` | Universal Declaration of Human Rights, Article 1, Brahui parallel text (Brahui Language Board / University of Balochistan). The transliteration engine is validated against it: 11 of 11 words render exactly. |
| `TOC` | Ali, Liaquat & Masato Kobayashi, *Brahui Texts* (ILCAA, Tokyo University of Foreign Studies, 2024) — glosses published by the authors. |
| `GRAM` | Published grammatical description: verb paradigms, numerals, pronouns. |
| `CORP` | ILCAA corpus, meaning inferred from unambiguous context. |
| `MINE` | Added by you, in your browser only. |

The two books are long out of copyright. Everything else is cited rather than reproduced.

## What is not confirmed

83 rows are flagged **needs a speaker** — the corpus-inferred glosses, plus glosses I read out of the
LSI sentences (*pin* "name", *zen* "saddle", *illa* "uncle"), plus a few where the 1906 print was hard to
read. Filter for them with the chip in the app, or export the review sheet, which sorts them first.
Two conflicts are recorded rather than papered over:

- LSI items 33 and 38 give *nat* "foot" and *xaf* "ear", against a corpus reading of *nat* as "ear".
- LSI item 46 glosses *zar* as "silver", where Persian *zar* is normally "gold".

## Limits

- **ڷ /ɬ/ is unreachable.** No Urdu, Hindi or English voice has a voiceless lateral fricative; a voice
  will substitute plain *l*. That is a limit of the voice, not of the spelling.
- Hindi is the best free substitute for Urdu — it carries the retroflexes, the aspirates and vowel
  length. English is the weakest: it can express none of the three.
- The dictionary is a research aid built from published sources, not the judgement of a native speaker.

`brahui-dictionary-original-backup.html` is the earlier single-page version, kept for provenance.
