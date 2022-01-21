# LING 567 - Bardi (bcj)
Hanieh Nezakati + Tara Wueger

## Git Commands
```
git add .
git commit -m "commit message"
git push

git pull
```

## 1/20 Notes
- question about ø since it's included in a lot of glosses but make_item has an issue with is

## Original Changes to choices file (later changes will be tracked by git)
- Gen Info
  - changed name of language to bardi
  - used "only split space and tab characters"
- TAM
  - added past, present, future, irrealis tenses
  - added cont, rem, rec, pfv, sim aspects
- Neg
  - unchecked neg auxiliary verb
- Lexicon
  - removed neg from auxiliaries

## Lab 2 Phenomena
### Case
- currently have core cases plus a couple of local cases
- maybe add rest of local cases and nominal cases?

### Tense/aspect
- waiting on responses from canvas on "rl" type
- would need to update auxiliaries

### Coverage
- corpus: 0.6%
  - ambiguity: 3 readings for 1 sentence
- lab2 testsuite: 18.2%
  - ambiguity: 7 readings for 2 sentences (6 for 1, 1 for 1)


## Lab 3 Phenomena
### Determiners/rest of NP
- no official distinction between NP and DP (pp. 327) but...
  - 3rd person pronouns are quite extensively used as determiners + modifiers of nouns (pp. 286)
  - no documentation of this so would be difficult to implement
- choices files lists 2 dets: jarri and barni and says order is det-noun
  - jarri = this
  - barni = around/when/tell/this
    - this case on pp. 717/772
- could do this and there's only two of them so wouldn't be too difficult
- nvm found a section on demonstratives (pp. 323)

### Argument optionality
- subject and object can be inflected on the verb; don't think that counts as this though
- maybe look at 2.1.1 zero marking section?
- we definitely have this

### Coordination
- could do this
- has word for and "agal" which is used monosyndetically
  - can be used under scope of negation
  - can conjoin elements in verbless clauses (not much about them)
  - used in giving choices
- has word for also "biila" which is used for "both...and" constructions
- can chain agal for phrases but not clauses
  - for clauses, use parataxis
- conjoined nouns
  - both NPs have case from pp. 651
    Boonyja may darr inarn bardagayoon agal gaarayoon.
    Boonya may darr i-n-ar-n bardaga-yoon agal gaara-yoon
    all food come 3-TR-pierce-CONT tree-SOURCE and ground-SOURCE
    "All food comes from the trees and from the ground."
  - first NP has case based on pp. 352
    Boorrgoorndanim agal Barlarramay ingirriloongan jinala nimanajina.
    Boorrgoornda-nim agal Barlarramay i-ng-irrr-i-loonga-n jinala nimana=jina
    Boorrgoornda-ERG and Barlarramay 3-PST-AUG-TR-collect-CONT spear many=3M.POSS
    "Boorrgoornda and Balarrmay gathered together many of their spears."
  - second NP has case from pp. 352
    Irralboonjirr nalaarrad birrii agal gooloonim.
    I-rr-alboo-n=jirr nalaarrad birrii agal gooloo-nim
    3-AUG-TR-dig-CONT=3A.IO turtle.eggs mother and father-ERG
    "Their mother and father dug up turtle eggs."
- preverb conjunction
  - from pp. 517
    Bilirl agal girringg nganarij bardi.
    Bilirl agal girringg nga-n-ar-ij bardi
    yawn and cough 1-TR-spear-MID-PFV yesterday
    "I yawned and coughed all day yesterday."
  - from pp. 518
    Bilirl nganarij bardi agal girringgirring nganarij.
    Bilirl nga-n-ar-ij bardi agal girringgirring nga-n-ar-ij
    yawn 1-TR-spear-MID.PFV yesterday and cough 1-TR-spear-MID.PFV
    "I yawned and coughed all day yesterday."
- multiple clause chaining
  - from pp. 658
    Molon goolarrarli agal garaginyarra agal goolarrji agal gambarla.
    Molon goo-la-rr-arli agal garaginyarra agal goolarrji agal gambarla.
    giant.trevally 2-IRR-AUG-eat and garaginya and Spanssh.mackerel and surgeon.fish
    "You must eat molon (giant trevally), garaginya (unidentified fish species), goolarrji (Spanish mackeral) or gambarl (surgeon fish)."

### Agreement
- entirety of chapter 10 is about agreement
- should definitely tackle this

## Lab 3
removed troubled words from lexicon
4 things to do:
  - phenomena 1 - coordination
  - phenomena 2 - agreement
  - phenomena 3 - case
  - morphotactics

### Morphotactics
#### Nouns
add noun2-case
add noun2-loc-all
remove pc5,pc6 (pc5 adds erg with no affix for some reason and pc6 takes output of pc5 and adds it to the end of noun suffixes which is stupid)
remove pc8,pc9 (pc9 adds all with no affix for some reason and pc9 either takes output of pc8 and adds it to the end of noun suffixes or it takes nouns and adds them to the end of noun suffixes; also stupid)
remove pc12,pc13 (same reason as pc5,pc6)

### Coverage
- corpus: 0.6%
  - ambiguity: 26 readings for 1 sentence
- lab2 testsuite: 18.2% (seems off)
  - ambiguity: 25 readings for 4 sentences (12 for 1, 6 for 2, 1 for 1)