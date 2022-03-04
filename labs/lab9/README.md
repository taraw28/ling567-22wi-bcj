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

## Possession
- "The dog's car sleeps" parses (with 3 trees) but doesn't translate
  - posted on canvas
- "my dogs sleep" doesn't parse
  - posted on canvas

## Translation
1
2
3
4
5
6 SKIPPED (not implemented)
7 SKIPPED (not implemented)
8
  - started with 16464 results (in both sje and eng)
  - after modifying the np2 coord rules
    - 84 results in eng
      - some sentences are not augmented
    - 12 results in sje
9
10 SKIPPED
  <!-- - As far as we can tell, there is no evidence that a sentence like "Cats chase dogs and sleep" can exist with full verbs. The only example we have that involves two full verb phrases is in a construction like "He jumped into the ashes and looked around for the spirit". This type of construction does exist with preverbs (which we didn't implement) but is very rare. -->
  aarli-nim iila i-rr-oo-ngoorribi-irr agal i-rr-jarrmi
  cat-ERG dog 3AUG-AUG-TR-chase-3AUG and 3AUG-AUG-sleep
  `Cats chase dogs and sleep.'
11
12 SKIPPED (not implemented)
13
14
15 SKIPPED (not implemented)
16
17
18
19
20
21-26 SKIPPED (not implemented)