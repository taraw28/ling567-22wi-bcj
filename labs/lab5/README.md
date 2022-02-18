[Back to README](/README.md)
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
- added personal pronouns
  - 1 more sentence in our testsuite parses!!!
- added possessive pronouns
  - 1 more sentence in our testsuite parses (but it shouldn't)
  - we don't have subjects/objects that are affixed to the verb implemented so it shouldn't parse
  - originally, this was generating sentences with the present tense affix (which is null) but it shouldn't have because this sentence has the rec-pst suffix
    - added forbid constraints to rem-pst and rec-pst on present tense and we no longer generate those sentences

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

## MMT
### First Translation
2. First sentence parsed with 1 reading; it generated 1 sentence and the transfer did 4 successful unifies and 2 failed ones
3. Some of them didn't generate a sentence, some of them did. Some showed transfer or parser output. The last one was really interesting. It translated from eng to sje and then back to eng and actually got the sentence it started with.
4. Had to remove ex-det := extracted-det-phrase. line from rules.tdl to get it to compile.
6. Compiled with no issue
8. First translation attempts:
  Attempt 1: Did not work because, since we use aarli "fish" instead of "car", we needed to change the pred from _fish_n_rel to _car_n_rel.
  Attempt 2: Getting "this does not appear to be a grammar image." error. Posted to Canvas

## TSDB
### Initial Run
  - corpus (tsdb/home/bardi/lab4/lab4grammar/corpus)
    1. 2 items parsed (#410, #1480)
    2. 9 parses per item (14 parses for one sentence, 4 for the other)
    3. Our most ambiguous item got 14 readings.
    4. Most of the ambiguity is coming from the top and bottom coordination rules. For the second sentence, one of our nouns was duplicated so the only other source is using the BASIC-HEAD-OPT-COMP rule versus the HEAD-SUBJ/SUBJ-HEAD rule to form the sentence.

  - testsuite (tsdb/home/bardi/lab5/lab4grammar/lab5)
    1. 4 items parsed (#3, #4, #66, #68)
    2. We averaged 4 parses per parsed item. (4 for each sentence)
    3. Our most ambiguous item got 4 readings.
    4. There isn't much ambiguity. One source is that our initial grammar had a duplicate entry in the lexicon. Another is that one sentence is formed using HEAD-COMP and the other uses BASIC-HEAD-OPT-COMP. There is also some ambiguity from coordination rules that combined the possessive pronoun with it's possessor (a noun).

### Final Run
  - corpus (tsdb/home/bardi/lab5/lab5grammar/corpus)
      1. 0 items parsed
      2. We averaged 0 parses per parsed item.
      3. Our most ambiguous item got 0 readings.
      4. The reason we lost both of the sentences we previously parsed was because, in our lab 5 grammar, we re-did the verb morphology. Previously, verb roots were added as prefixes, which meant that there were no semantics attached. We switched to having the verb roots exist in the lexicon instead. However, we focused on adding the verbs that exist in our testsuite and not on adding verbs that exist in the corpus.

  - testsuite (tsdb/home/bardi/lab5/lab5grammar/lab5)
      1. 11 items parsed
      2. We average ~2 parses per parsed item. (One sentence got 5, the rest got either 1 or 2)
      3. Our most ambiguous item(s) got 6 readings.
      4. One source of ambiguity is that the remote past and continuative tense/aspects share suffixes. This type of ambiguity can't really be fixed (at least not at this stage) as figuring out which one should be applied is based on context. The other source of ambiguity is coming from the sentence "nga-marla-ng nga-na-boo-gal". (Note, this sentence is parsing but most likely for the wrong reasons. We never added subjects like "I" that are affixed to the verb to the grammar.)
        Ngamarlang nganangajimgal.
        nga-marla-ng nga-na-ngajim-gal
        1MIN.POSS-hand-INS 1-TR.PST-hit-REC.PST
        `I hit him with my hand.'
      I posted about this issue on canvas and ran out of time to get it resolved. The first issue that we found was that since this sentence combines the transitive and past markers, it added the null present marker as it thought the "-na-" marker was for transitivity. We fixed this by adding forbid constraints to the rem-pst and rec-pst lexical rules that prevents the present tense null marker with the rem-pst or rec-pst markers. However, there is also an issue with agreement. The possessive marker has pernum 1MIN which must agree with the first person marker on the verb. However, we are getting 2MIN markers on the verb when currently parsing. We tried to inspect different parts of the tree but were unable to figure out why this is happening. I will be following up on canvas about this but wanted to explain a bit about the issue since it is our greatest source of ambiguity at the moment.
### Coverage
  - Initial Run
    - corpus: 1.1% coverage
    - testsuite: 3% coverage
  - Final Run
    - corpus: 0% coverage
    - testsuite: 14.1% coverage
  - Comparison
    - corpus: decreased (explained above)
    - testsuite: increased :D and our ambiguity decreased a lot with most sentences only having 1 or 2 parses