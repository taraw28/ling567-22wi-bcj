# Lab 5
## Things to Do
- Weekend Fixing Fun!!!
  - lexicon
    - add words
      - added the lexicon from the nouns.to.add.txt file

    - remove unnecessary words
      - duplicates and unnecessary (e.g. sand.soakage)
      - _anggi_ as a noun stem as well as its pred _what_n_rel to move to question-pronouns and to change to _thing_n_rel

    - organize categories
  - morphology
    - remove ill-formed pcs
    - add back morphology from ill-formed in bettery way
  - testsuite
    - make sure everything is correct/accurate
    - all words here need to be in lexicon
  - other
    - maybe remove masculine gender
- phenomena we've worked on
  - case
    - should be good
  - **TAM**
    - add in morphology
  - coordination
    - figure out coord strategies
  - agreement
    - **add in morphology**
  - questions
    - made changes
     - to lexicon as per feedback from lab 4 to replace what and who w/ thing and person, respectively.  (got snippet)
     - added y/n questions to matrix q/n (got snippet)
    - try making nganyji optional
  - argument optionality
    - wait for feedback from lab4
  - possessives
    - wait for feedback from lab4
- collect MMT sentences
- try first translation

## Morphology
### Verbs
- sentence to parse : i-ny-jarrmi-n gool-nim
- Attempt 1
  - intrans (abs) verb25: jarrmi
  - rem pc78 (non-oblig): -n
  - pst pc79 (non-oblig): ny-
  - third-person pc80 (non-oblig): i-
  - couldn't parse
- Attempt 2
  - intrans (unspcf) verb25: jarrmi
  - rem pc78 (non-oblig): -n
  - pst pc79 (non-oblig): ny-
  - third-person pc80 (non-oblig): i-
  - couldn't parse
- Attempt 3
  - intrans (abs) verb25: jarrmi
  - rem pc78 (oblig): -n
  - pst pc79 (oblig): ny-
  - third-person pc80 (oblig): i-
  - couldn't parse
    - no parse chart for full sentence but parse chart if remove i-
- Attempt 4
  - intrans (abs) verb25: jarrmi
  - rem pc78 (oblig): -n
  - pst pc79 (oblig): ny-
  - third-person pc80 (oblig): i- (removed pernum feature)
  - couldn't parse
    - parse chart for full sentence
    - unified vp and np and realized it wasn't parsing due to
      mismatched cases which is CORRECT BECAUSE IT'S AN
      UNGRAMMATICAL SENTENCE
    - could parse i-ny-jarrmi-n gool
- new sentence to parse: i-ny-jarrmi-n gool
- Attempt 5
  - intrans (abs) verb25: jarrmi
  - rem pc78 (oblig): -n
  - pst pc79 (oblig): ny-
  - third-person pc80 (oblig): i- (added pernum feature back)
  - couldn't parse
    - I think it has issues with pernum: 3rd
- Attempt 6
  - intrans (abs) verb25: jarrmi
  - rem pc78 (oblig): -n
  - pst pc79 (oblig): ny-
  - third-person pc80 (oblig): i- (changed to pernum 3min,3aug)
  - couldn't parse
    - still think the issue has to do with adding the pernum feature
    - doesn't even show part of the parse chart for the verb
- Attempt 7
  - intrans (abs) verb25: jarrmi
  - rem pc78 (oblig): -n
  - pst pc79 (oblig): ny-
  - third-person pc80 (oblig): i- (pernum 3min,3aug; changed to
    specified on subject)
  - it parsed!!!!
    - correctly parses i-ny-jarrmi-n gool
    - correctly fails to parse i-ny-jarrmi-n gool-nim
- replaced pst pc with more general tense pc
  - added more past tense affixes
  - added future tense
    - added sentence to testsuite (will test after adding tv verbs)
      ```
      Anggarramarra.
      a-ngg-arr-a-marra
      1-FUT-AUG-TR-cook
      `We will cook it.'
      ```
  - added present tense (null marked)
- replaced third-person pc with more general pernum pc
  - added 1min, 2min, 3min, 1+2min prefixes
    - still parses i-ny-jarrmi-n gool
    - still correctly doesn't parse i-ny-jarrmi-n gool-nim
  - added 1aug, 2aug, 3aug
    - added aug pc
    - added aug feature to aug pc
    - added constraint to aug pernums that aug pc is required
    - added sentence to testsuite
      ```
      Inyarrjarrmin gool.
      i-ny-arr-jarrmi-n gool
      3-PST-AUG-get.up-REM.PST father.ABS
      `The fathers got up.'
      ```
    - still parses old sentences
- added 2 transitive (tr) pc (tr-min and tr-aug)
  - added min feature to tr-min and aug feature to tr-aug to make sure that pernum prefixes are not in conflict with the different tr markers
  - test sentence
    ```
    Aambanim aarli inamanyana.
    Aamba-nim aarli i-na-ma-nya-na
    man-ERG fish.ABS 3-TR-PST-catch-REM.PST
    `The man caught the fish.'
    ```
  - still parses old sentences
  - parses new sentence too!
- replaced rem pc with more general aspect pc
  - added cont, rem-pst, rec-pst, pfv, and fut aspects (note, fut is
    not an aspect but sometimes takes the same slot as the aspects
    which is why it is included here)
  - still parses old sentences
- removed bad verb types and verb pc
- added new verb types
  - it: abs subj
  - it: erg subj
  - tr: erg subj abs obj
  - tr: erg subj all obj
  - it-preverb
  - tr-preverb
  - light verb
- removed gender
  - bardi doesn't have gender; MIN is often glosses as M
- got rid of auxiliaries


## How Verbs Work
- all verbal predicates: verb inflect for prefixes, suffixes, and clitics
- complex predicates: uninflecting preverb that precedes the root
  ```
  (Preverb) Prefixes-ROOT-Suffixes=Clitics
  ```
- inflecting verbs
  - required
    - person prefix
    - marked for tense
  - optional
    - transitivity
      - min: tr morphene before tense
      - aug: tr morpheme after aug marker
    - tense
    - aspect
    - applicatives
    - reflexive/reciprocal derivation
  - order
    - person-tense-augment
- preverb
  - controls transitivity (pp 514)
- case
  - tr erg subj abs obj (most common)
  - tr erg subj all obj
  - it abs subj (most common)
  - it erg subj

## verbs added to lexicon
