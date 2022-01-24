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
- polar interrogatives 
  - using the interrogative particle _nganyji_. The particle usually appears first in the clause. This particle questions the proposition in the **clause as a whole**.     
       - Ex(s) for a free question word _nganyji_ :   														
     ```																		
    Source: a:618
    Vetted: t
    Judgement: g
    Phenomena: q
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
    
    Nganyji lol inyjiidigal jan mayar?
    Nganyji lol i-ny-jiidi-gal jan mayar
    INTERROG burn 3-PST-go-REC.PST 1MIN.POSS house
    `Did my house burn?’
    
    ```
    - There are some derivatives of nganyji, such as _nganyjal_ and _nganyjirrgoordoo_ ‘how many’ (and in the old texts, nganyjarda)._ Nganyjal_ is marked with the indefinite marker -al. 
      - Ex(s):
      - ```
	Nganyjal darr oonkara ngoorrij.
	Nganyjal darr oo-n-k-ar-a ngoorrij
	hopefully come 3-TR-FUT-pierce-FUT future
	`Hopefully he will come tomorrow.’
	
	
	Nganyjal irrgoordoo aalga ingarralanana namard.
	Nganyjal irrgoordoo aalga i-ng-arr-ala-na-na namard
	NGANYJAL how.much day 3-PST-AUG-live-CONT-REM.PST just
	`We don’t know how long they lived without fire.’
	
	```
	
   - using clitic =_(g)arda_ which has a clear deontic meaning. It is probably related to the adverb _garda_, which means ‘still’ in the sense of ‘X still did something (even though I told him not to).’ This clitic interacts with **focus** and is used to question **particular constituents**. The clitic attaches to the item under interrogation. (It seems to have single word scope, e.g. aarlarda in the following would be ‘two FISH, or something else, like octopus?’) 
      - Ex(s) for the clitic _(g)arda_
     ```
    Source: a:619
    Vetted: t
    Judgement: g
    Phenomena: q
    Gooyarrarda aarli minnyagal?
    Gooyarr=arda aarli mi-n-nya-gal
    two=INT fish 2-TR-[PST]-catch-REC.PST
    `Was it **two** fish you caught?
    
    Source: a:619
    Vetted: t
    Judgement: g
    Phenomena: q
    Ngayarda ngankiida Broomengan, gardi joowarda?
    Ngay=arda nga-n-k-iid-a Broome-ngan, gardi joo=warda
    1MIN=INT go Broome-ALL “or” 2MIN=INT
    `Will I go to Broome today or will it be you?’
    
    ```
    
    - using _=bard(a)_, also a clitic with identical distribution to _=gard_. It appears to have an epistemic function in interrogatives; that is, it questions an **individual constituent** and asks the question ‘was it this or something else?’
```
Source: a:620
Vetted: t
Judgement: g
Phenomena: q 
Ginyinggi ball garndi inin bardagonbard?
Ginyinggi ball garndi i-ni-n bardagon=bard
3MIN ball on.top 3-sit-CONT tree-LOC=INTERROG
`Is the ball at the top of the TREE?’

Ginyinggarda jina jiiwa minjoogoolij?
Ginyingg=arda jina jiiwa mi-n-joogool-ij
3min=interrog 3M.POSS boomerang 2-TR-break-PFV
`Was it HIS boomerang you broke?’


Nyimoonggoon ginyingginim aamba joowarda jiy iila inangajim?
Nyi-moonggoon ginyinggi-nim aamba joo=warda jiy iila i-na-ngajim
2-know 3MIN-ERG man 2MIN=INT 2M.POSS dog 3-TR-hit
`Do you know if it was the man who hit YOUR dog?’


Source: a:622
Vetted: t
Judgement: g
Phenomena: q 
Ngayarda ngankiida Broomengan, gardi joowarda?
Ngay=arda nga-n-k-iid-a Broome-ngan, gardi joo=warda
1sg=INT go Broome-ALL “or” 2MIN=INT
`Will I go to Broome today or will it be you?’

```
- content questions
  - interrogative placement and intonation: 
     - asked with one of a number of interrogative pronounsinterrogative pronoun, usually first in the clause, receives intonational focus, with a H* tone; interrogative clauses have a sharp rise at the end of the clause, which may occur over a single syllable. Although the pronoun is usually first in the clause, it need not be, and examples of both _nganyji_ and _anggi_ are found which are non-initial, and which still have an interrogative reading.
     - Ex(s):
 ```
Source: a:622
Vetted: t
Judgement: g
Phenomena: wh 
Anggaba nyinga joo?
Anggaba nyi-nga joo
who 2MIN-name 2MIN
`What’s your name?’

<img width="691" alt="Screen Shot 2022-01-24 at 11 05 16 AM" src="https://user-images.githubusercontent.com/49420070/150847542-10a3b771-a6e9-4f08-93d5-ce16899f00b9.png">


     - ‘Why’ questions: _goonban(kij)_ and _angan_
    
  - double interrogatives
  
