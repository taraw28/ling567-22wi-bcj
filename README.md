# LING 567 - Bardi (bcj)
Hanieh Nezakati + Tara Wueger

## Git Commands
```
git add .
git commit -m "commit message"
git push

git pull
```

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

## Lab 2
### Phenomena
#### Case
- currently have core cases plus a couple of local cases
- maybe add rest of local cases and nominal cases?

#### Tense/aspect
- waiting on responses from canvas on "rl" type
- would need to update auxiliaries

### Coverage
- corpus: 0.6%
  - ambiguity: 3 readings for 1 sentence
- lab2 testsuite: 18.2%
  - ambiguity: 7 readings for 2 sentences (6 for 1, 1 for 1)


## Lab 3
- removed troubled words from lexicon

### Phenomena
#### Determiners/rest of NP
- no official distinction between NP and DP (pp. 327) but...
  - 3rd person pronouns are quite extensively used as determiners + modifiers of nouns (pp. 286)
  - no documentation of this so would be difficult to implement
- choices files lists 2 dets: jarri and barni and says order is det-noun
  - jarri = this
  - barni = around/when/tell/this
    - this case on pp. 717/772
- could do this and there's only two of them so wouldn't be too difficult
- nvm found a section on demonstratives (pp. 323)

#### Argument optionality
- subject and object can be inflected on the verb; don't think that counts as this though
- maybe look at 2.1.1 zero marking section?
- we definitely have this

#### Coordination
- could do this
- has word for and "agal" which is used monosyndetically
  - can be used under scope of negation
  - can conjoin elements in verbless clauses (not much about them)
  - used in giving choices
- has word for also "biila" which is used for "both...and" constructions
- can chain agal for phrases but not clauses
  - for clauses, use parataxis

#### Agreement
- entirety of chapter 10 is about agreement
- should definitely tackle this

### Morphotactics
#### Nouns
add noun2-case
add noun2-loc-all
remove pc5,pc6 (pc5 adds erg with no affix for some reason and pc6 takes output of pc5 and adds it to the end of noun suffixes which is stupid)
remove pc8,pc9 (pc9 adds all with no affix for some reason and pc9 either takes output of pc8 and adds it to the end of noun suffixes or it takes nouns and adds them to the end of noun suffixes; also stupid)
remove pc12,pc13 (same reason as pc5,pc6)

### Coverage
- corpus: 1.1%
  - ambiguity: 88 readings for 2 sentences
- lab2 testsuite: 7.1%
  - ambiguity: 25 readings for 4 sentences (12 for 1, 6 for 2, 1 for 1)

## Lab 4

### Phenomena
### Questions
- different ways of asking questions: 
  - polar interrogatives     
     - use either a free question word _nganyji_ or a clitic. They may also be marked with intonation alone.
       - Ex(s) for a free question word _nganyji_ :   
     ```
    Source: a:618
    Vetted: t
    Judgement: g
    Phenomena: q
    Nganyji minjalagal jiyirr ooldoobal?
    **Nganyji** mi-n-jala-gal jiy-irr ooldoobal
    NGANYJI 2-TR-see-REC.PST 2M.POSS-3A things
    `Did you see your things?’
    
    
    Source: a:618
    Vetted: t
    Judgement: g
    Phenomena: q
    Nganyji ngay ngankiida Broomengan?
    Nganyji ngay nga-n-k-iid-a Broome-ngan
    `Will I go to Broome?’
    ```
    - The clitic =_(g)arda_ has a clear deontic meaning. It is probably related to the adverb _garda_, which means ‘still’ in the sense of ‘X still did something (even though I told him not to)’  
      - Ex(s) for the clitic _(g)arda_
     ```
    Source: a:619
    Vetted: t
    Judgement: g
    Phenomena: q
    Gooyarrarda aarli minnyagal?
    Gooyarr=arda aarli mi-n-nya-gal
    two=INT fish 2-TR-[PST]-catch-REC.PST
    `Was it two fish you caught?
    
    Source: a:619
    Vetted: t
    Judgement: g
    Phenomena: q
    Ngayarda ngankiida Broomengan, gardi joowarda?
    Ngay=arda nga-n-k-iid-a Broome-ngan, gardi joo=warda
    1MIN=INT go Broome-ALL “or” 2MIN=INT
    `Will I go to Broome today or will it be you?’
    
    ```
  - content questions
     - interrogative placement and intonation
     - ‘Why’ questions: _goonban(kij)_ and _angan_
     
  - double interrogatives
  
