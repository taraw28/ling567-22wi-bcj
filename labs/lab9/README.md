[Back to README](/README.md)
# Lab 9

- removed PRON bool from noun since it was already in HEAD

## Coordination
- started w/ 15 trees for `aarli-nim agal iila-nim i-rr-oo-ngoorribi-irr yandilybar`
- had a bunch of trees that had "dog and cats" or "and cats" going through the locative-pp rule
- realized that coordination wasn't preserving case
- tried modifying top-coord rule but that didn't work (syntax error) so posted to canvas
- was told that the top-coord rule was also applying to verbs so switched to modifying np coordination rules
- changed bardi.tdl:
  ```
  np2-top-coord-rule := basic-np-top-coord-rule & monopoly-top-coord-rule &
    [ SYNSEM.LOCAL [ CAT.HEAD.CASE #case,
                    COORD-STRAT "2" ],
      LCOORD-DTR.SYNSEM.LOCAL.CAT.HEAD.CASE #case,
      RCOORD-DTR.SYNSEM.LOCAL.CAT.HEAD.CASE #case ].

  np2-mid-coord-rule := basic-np-mid-coord-rule & monopoly-mid-coord-rule &
    [ SYNSEM.LOCAL [ CAT.HEAD.CASE #case,
                    COORD-STRAT "2" ],
      LCOORD-DTR.SYNSEM.LOCAL.CAT.HEAD.CASE #case,
      RCOORD-DTR.SYNSEM.LOCAL.CAT.HEAD.CASE #case ].

  np2-bottom-coord-rule := conj-first-bottom-coord-rule & np-bottom-coord-phrase &
    [ SYNSEM.LOCAL [ CAT.HEAD.CASE #case,
                    COORD-STRAT "2" ],
      NONCONJ-DTR.SYNSEM.LOCAL.CAT.HEAD.CASE #case ].
  ```
- went from 15 trees down to 1!
- translate from eng w/ 84 results
- some sentences allowing min verb, probably not making "cat and dog" be plural
- asked on canvas

## Locative PP
- does parse but doesn't translate
- have trigger rule for copula
- instantiated transfer rule for _in_p_rel -> _loc_p_rel
- recompiled transfer grammar
- still doesn't translate, posted on canvas
- was missing period at the end
- translated with 336 results
- allowing minimal sentences
- not sure why so posted on canvas

## Possession
- "The dog's car sleeps" parses (with 3 trees) but doesn't translate
  - posted on canvas
  -  HEAD-DTR.SYNSEM.LOCAL.CAT.HEAD.INIT +  in HEAD comp got rid of ambiguity
  - added trigger rule for jina
  - made possessor-adp-lex-1 complement be 3min and have abs case
- "my dogs sleep" doesn't parse
  - posted on canvas

## Translation
1
  - 2 results (in both sje and eng)
  - this is expected due to free word order
2
  - 12 results
  - this is expected due to free word order and because having a direct object suffix is optional
3
  - 0 results even after instantiating pro-insert-arg1 and pro-insert-arg2 transfer rules
4
  - 2 results (in both sje and eng)
  - this is expected due to free word order
5
  - 24 results (in both sje and eng)
  - this is expected due to free word order
6 SKIPPED (not implemented)
7 SKIPPED (not implemented)
8
  - started with 16464 results (in both sje and eng)
  - after modifying the np2 coord rules
    - 84 results in eng
      - some sentences are not augmented
      - made mother of np2 top third person augmented
      - 12 results
        - this is expected due to free word order and because having a direct object suffix is optional
    - 12 results in sje
      - this is expected due to free word order and because having a direct object suffix is optional
9
  - doesn't parse because vp coordination doesn't work
10
  - doesn't parse because vp coordination doesn't work
11
  - 24 results in eng
    - this is expected due to free word order and because having a direct object suffix is optional
  - 12 results in sje
    - results aren't correct because they don't include the interrogative nganyji
12 SKIPPED (not implemented)
13
  - 8 results in eng
    - not completely correct; 4 sentences have the interrogative nganyji for some reason and other 4 sentences are missing ergative case on the subject
  - SKIPPED in sje
14
  - 18 results in eng
    - some sentences have interrogative nganyji, all sentences missing ergative case on the subject, some verbs have irrealis marker for some reason
  - SKIPPED in sje
15 SKIPPED (not implemented)
16
  - 336 results in eng
    - allowing for min prefixes on verb for some
!      - need to fix pernum/aug position classes with customization
    - allowing any case on subject
      - constrained subject of copula to be ergative
  - SKIPPED in sje
17
  - 28 results in eng
    - all cases allowed on the subject but there shouldn't be any case
    - not included the pronoun to make this plural but not really sure how to fix that (maybe trigger rule?)
  - SKIPPED in sje
18
  - parses but doesn't translate
  - did stuff listed under possession above
    - 8 results
19
  - doesn't parse because this kind of possession doesn't work yet
20
  - doesn't parse because we haven't fully implemented wh-questions
21-26 SKIPPED (not implemented)