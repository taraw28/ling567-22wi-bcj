# Lab 5
## Things to Do
- Weekend Fixing Fun!!!
  - lexicon
    - add words
    - remove unnecessary words
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
  - TAM
    - add in morphology
  - coordination
    - figure out coord strategies
  - agreement
    - add in morphology?
  - questions
    - wait for feedback from lab4
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