[Back to README](/README.md)
# Lab 6

## Morphology or Semantically Empty Word Clean Up
- #2 Dogs chase cars
  - initial: 19419 results
  - fixed semi for tense: 3072 results
  - fixed semi for aspect: 768 results
  - fixed semi for pernum: 192 results
  - removed iil and just used iila for dog_n_rel: 96 results
  - combine rules
    - combine aug-prefix: 48 results
    - combine 3aug-prefix: 24 results
    - combine tr-aug-prefix: 12 results
    - combined rest of prefixes: 12 results
  - at this point test #4
    - initial: 52 results
    - removed all variations of eat_v_rel: 10 results
      - arli => arli, arl, rl, rli, irli
  - add require/forbid constrains to it/tr verb classes
    - #2: 6 results
    - #4: 6 results
  - at this point test #19: 4 results
  - work on 's possession
    - added possession strategies and it does parse but also parses with wh-ques for some reason
    - does not translate (maybe because of the dog vs dog)
  - work on direct object agreement

## Possessives
- The dog s car sleeps:
  ```
  Iila jina yandilybar irrjarrmi.
  iila jina yandilybar i-rr-jarrmi
  dog 3MIN.POSS car 3-AUG-sleep
  `The dog's car sleeps. (lit. dog his car sleeps)'
  ```
- My dogs sleep:
  ```
  Ngajana iila irrjarrmi.
  ngajana iila i-rr-jarrmi
  1MIN.POSS dog 3-AUG-sleep
  `My dogs sleep.'
  ```

## Argument Optionality
- pp. 402 direct object clitic forms
- pp. 468 "generic third person objects are not overtly marked in the verb."
- pp. 469 "An example showing overt object agreement is given below. The form of
the first person singular object marker is =jarrngay."
- test sentence:
  ```
  Iilanim irroongoorribiirr.
  iila-nim i-rr-oo-ngoorribi-irr
  dog-ERG 3-AUG-TR-chase-3AUG.DO
  `Dogs chase them.'
  ```

## Negation
- negatiion marker arra
  ```
  Arra iilanim irroongoorribi yandilybar.
  arra iila-nim i-la-rr-oo-ngoorribi yandilybar
  NEG dog-ERG 3-IRR-AUG-TR-chase boat
  `The dogs don't chase boats.'
  ```