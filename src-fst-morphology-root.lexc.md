
INTRODUCTION TO MORPHOLOGICAL ANALYSER OF Paumarí LANGUAGE.

# Definitions for Multichar_Symbols

## Analysis symbols
The morphological analyses of wordforms for the Paumarí
language are presented in this system in terms of the following symbols.
(It is highly suggested to follow existing standards when adding new tags).

The parts-of-speech are:

The parts of speech are further split up into:

The Usage extents are marked using following tags:
* **+Use/TTS** – **only** retained in the HFST Text-To-Speech disambiguation tokeniser
* **+Use/-TTS** – **never** retained in the HFST Text-To-Speech disambiguation tokeniser

The nominals are inflected in the following Case and Number

## Possessive tags
* **+PxSg1** Singular First Person
* **+PxSg2** Singular Second Person
* **+PxSg3F** Singular Third Person Feminine
* **+PxSg3M** Singular Third Person Male
* **+PxPl1** Plural First Person
* **+PxPl2** Plural Second Person
* **+PxPl3F** Plural Third Person Feminine
* **+PxPl3M** Plural Third Person Male

The comparative forms are:
Numerals are classified under:

Verb moods are:

Pronoun personal forms are:

## Verb person-number-gender

* **+ScSg1** subject conjugation first person singular
* **+ScSg2** subject conjugation second person singular
* **+ScSg3F** subject conjugation third person singular Feminine
* **+ScSg3M** subject conjugation third person singular Male
* **+ScPl1** subject conjugation first person plural
* **+ScPl2** subject conjugation second person plural
* **+ScPl3** subject conjugation third person plural 
* **+ScPl3F** subject conjugation third person plural Feminine
* **+ScPl3M** subject conjugation third person plural Male

* **+OcSg1** object conjugation first person singular
* **+OcSg2** object conjugation second person singular
* **+OcSg3F** object conjugation third person singular Feminine
* **+OcSg3M** object conjugation third person singular Male
* **+OcPl1** object conjugation first person plural
* **+OcPl2** object conjugation second person plural
* **+OcPl3F** object conjugation third person plural Feminine
* **+OcPl3M** object conjugation third person plural Male

Other verb forms are

* +Symbol = independent symbols in the text stream, like £, €, ©
Special symbols are classified with:
The verbs are syntactically split according to transitivity:
Special multiword units are analysed with:
Non-dictionary words can be recognised with:

Question and Focus particles:

Semantics are classified with

Derivations are classified under the morphophonetic form of the suffix, the
source and target part-of-speech.

Morphophonology
To represent phonologic variations in word forms we use the following
symbols in the lexicon files:

And following triggers to control variation

## Flag diacritics
We have manually optimised the structure of our lexicon using following
flag diacritics to restrict morhpological combinatorics - only allow compounds
with verbs if the verb is further derived into a noun again:
|  @P.NeedNoun.ON@ | (Dis)allow compounds with verbs unless nominalised
|  @D.NeedNoun.ON@ | (Dis)allow compounds with verbs unless nominalised
|  @C.NeedNoun@ | (Dis)allow compounds with verbs unless nominalised

For languages that allow compounding, the following flag diacritics are needed
to control position-based compounding restrictions for nominals. Their use is
handled automatically if combined with +CmpN/xxx tags. If not used, they will
do no harm.
|  @P.CmpFrst.FALSE@ | Require that words tagged as such only appear first
|  @D.CmpPref.TRUE@ | Block such words from entering ENDLEX
|  @P.CmpPref.FALSE@ | Block these words from making further compounds
|  @D.CmpLast.TRUE@ | Block such words from entering R
|  @D.CmpNone.TRUE@ | Combines with the next tag to prohibit compounding
|  @U.CmpNone.FALSE@ | Combines with the prev tag to prohibit compounding
|  @P.CmpOnly.TRUE@ | Sets a flag to indicate that the word has passed R
|  @D.CmpOnly.FALSE@ | Disallow words coming directly from root.

Use the following flag diacritics to control downcasing of derived proper
nouns (e.g. Finnish Pariisi -> pariisilainen). See e.g. North Sámi for how to use
these flags. There exists a ready-made regex that will do the actual down-casing
given the proper use of these flags.
|  @U.Cap.Obl@ | Allowing downcasing of derived names: deatnulasj.
|  @U.Cap.Opt@ | Allowing downcasing of derived names: deatnulasj.

Possessor indices

finite verb negation

Subject person indices

Intransitive Subject person indices

The word forms in Paumarí language start from the lexeme roots of basic
word classes, or optionally from prefixes:

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/root.lexc](https://github.com/giellalt/lang-pad/blob/main/src/fst/morphology/root.lexc)</small>
