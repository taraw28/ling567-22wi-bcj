[Back to README](/README.md)
# Lab 3
- removed troubled words from lexicon

## Phenomena
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

### Agreement
- entirety of chapter 10 is about agreement
- should definitely tackle this

## Morphotactics
### Nouns
- add noun2-case
- add noun2-loc-all
- remove pc5,pc6 (pc5 adds erg with no affix for some reason and pc6 takes output of pc5 and adds it to the end of noun suffixes which is stupid)
- remove pc8,pc9 (pc9 adds all with no affix for some reason and pc9 either takes output of pc8 and adds it to the end of noun suffixes or it takes nouns and adds them to the end of noun suffixes; also stupid)
- remove pc12,pc13 (same reason as pc5,pc6)

## Coverage
- corpus: 1.1%
  - ambiguity: 88 readings for 2 sentences
- lab2 testsuite: 7.1%
  - ambiguity: 25 readings for 4 sentences (12 for 1, 6 for 2, 1 for 1)