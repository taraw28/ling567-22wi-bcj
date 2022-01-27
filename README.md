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
 ```
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

Source: a:623
Vetted: t
Judgement: g
Phenomena: wh 
Janambooroongan arr mindin? 
Janambooroo-ngan arr mi-n-di-n 
where-ALL go 2-TR-do/say-CONT 
`Where are you going?’
```


- Interrogative pronouns such as anggaba can modify nouns. That is, they can appear as pronominal modifiers within Noun Phrases.
    - Ex:


```
Source: a:623
Vetted: t
Judgement: g
Phenomena: wh
Anggabanim laanybiid inanggalagaljan ooldoobal?
[Anggaba-nim laanybiid] i-na-ng-gala-gal=jan ooldoobal
‘Which thief [lit. ‘who thief’] went off with my stuff?’
```


 - ‘Why’ questions: 
 	- _Angan_ ‘why’ asks about the **reason** for an action or event. 
	- _anggi_ ‘what’ is used to ask about the **purpos**e of an action. 
	- both are stance-neutral markers
	- Ex(s):


```
Source: a:624
Vetted: t
Judgement: g	
Phenomena: wh
Angan minyjarralagal joornk?
Angan mi-ny-jarrala-gal joornk
why 2-PST-run-REC.PST fast 
`Why did you run so fast?'
```

	- _goonban(kij)_ signals the speaker’s disapproval of an action and is usually translated as ‘why on earth’. 
	- This interrogative adverb may be qualified with =_gija_ ‘very’
	- Ex(s):
	
	
```
Source: a:625
Vetted: t
Judgement: g	
Phenomena: wh
Goonban barda minagal jan aarli?
Goonban barda mi-n-a-gal jan aarli
why.on.earth away 2-TR-give-REC.PST 1M.POSS fish
`Why on earth did you give my fish away?’

Source: a:625
Vetted: t
Judgement: g	
Phenomena: wh
Goonbankij minjoolnggaljin?
Goonban=kij mi-n-joolng-gal=jin
why.on.earth=VERY 2-TR-tell-REC.PST=3M.IO
`Why on earth did you tell him?’

Source: a:625
Vetted: t
Judgement: g	
Phenomena: wh
Goonbankij jarrmin injoongmoord?
Goonban=kij jarrmin i-n-joo-ng=moord 
why.on.earth follow 3-TR-do/say-APPL=1A.DO
`Why on earth does she have to follow us?’
```

- double interrogatives
  - More than one interrogative pronoun can appear in a clause. Multiple interrogatives are allowed, and there are few restrictions on the order, at least of argument interrogatives. The difference in meaning appears to depend on which interrogative has greater focus.
  - Ex(s):

```
Source: a:625
Vetted: t
Judgement: g	
Phenomena: wh
Anggabanim anggi inarligal?
Anggaba-nim anggi i-na-rli-gal
who-ERG what 3-TR-eat-REC.PST
`Who ate what?’
```


  - When it comes to multiple interrogatives with both arguments and adjuncts, however, the judgments are different. This is one of the few places in the grammar where there are differences between free adjunct and argument phrases. For example, multiple interrogatives involving _janaboor_ ‘where’ are fine when the adjunct is fronted before _anggaba_ ‘who’, but only if the verb is final:


```
Source: a:627
Vetted: t
Judgement: g	
Phenomena: wh
Anggaba minjalagal janaboor?
Anggaba mi-n-jala-gal janaboor
who 2-TR-see-REC.PST where
`Who did you see where?’


Source: a:627
Vetted: t
Judgement: g	
Phenomena: wh
Janaboor anggaba minjalagal?
Janaboor anggaba mi-n-jala-gal
where who 2-TR-see-REC.PST
`Who did you see where?’

Source: a:628
Vetted: t
Judgement: g	
Phenomena: wh
Nyanyjirrgoordoo aarli minjooloonggalirr baanigarr?
Nyanyjirrgoordoo aarli mi-n-jooloong-gal=irr baanigarr?
how.many fish 2M-TR-collect-REC.PST=3A.DO when
`How many fish did you collect when?/When did you collect
how many fish?’
```


### Argument Optionality

Bardi has free argument omission (‘pro-drop’). It does allow subjects and objects to be dropped with 
Pronouns are not syntactically obligatory in the clause. They are not used for reference tracking. 

Even in cases of potentially ambiguous argument tracking, free NPs or pronouns are seldom used. The ambiguity is tolerated, though there is some assumption of argument continuity (that is, that subjects continue subjects and objects continue objects); however, likelihood and real world knowledge are used to infer who is doing what.

In the following example argument continuity is inferred by the absence of free NPs or pronouns and the subject marking on the verb provides information about which participants. Context identifies the referent of the verb agreement. The following example contains no argument NPs or pronouns at all; the only NPs are place names or locations.

```
Roowil	ingirrinyana Ngalngoorarra 	yoorr 		ingarraman 		 Balalbalalngarr daab  ingirrinyan 		  goona goorriron.
Roowil	i-ng-irr-i-nya-na Ngalngoorarra yoorr 		i-ng-arr-a-ma-n 	 Balalbalalngarr daab  i-ng-irr-i-nya-n 	  goona goorrir-on
walk 	3-PST-AUG-TR-catch-REM.PST Ng. 	come.down	3-PST-AUG-TR-put-REM.PST B.		 climb 3-PST-AUG-TR-catch-REM.PST back 	fig.tree-LOC
`They walked to Ngalngoorarra and came down at Balalbalalngarr, and climbed up at the big fig tree.’


Source: author
Vetted: t
Judgement: g	
Phenomena: pro-d
Roowil	ingirrinyana Ngalngoorarra. 
Roowil	i-ng-irr-i-nya-na Ngalngoorarra
`They walked to Ngalngoorarra.'
```
Heads of relative clauses, for example, can be omitted. Both speech act participants can be omitted. Subjects and objects of gerunds can be omitted, even though they are not cross-referenced on the verb. 


**No omission cases**
However, there are contexts under which free noun phrases appear not to be omissible

Other evidence may come from speaker intuitions about arguments which are omitted and understood from context, versus cases where there are no arguments (that is, distinctions between sentences like ‘he’s eating [cake]’ and ‘*we put the table’).

- Pronouns cannot be omitted if the argument is in focus. But if they are in special focus (Kiss 1998), they may also get reinforcement, such as with the exclamative _arra_:

```
Arra 	ngay bard arr  ngandan.
Arra 	ngay bard arr  nga-n-da-n
INTERJ  1MIN away come 1-TRdo/say-CONT
`Hey look! It’s ME coming.’

Ngayoonim  ngananarri         malarr.
Ngayoo-nim nga-na-na=rri      malarr
1MIN-ERG 1-CONT-REM.PST=2M.DO wife
`I gave you wives.’
```
- The following show that the ergative differentiates subject from oblique; it is not omissible even when the semantic roles are clear from context.

```
p. 465
Inyjargijin ngaarri.
I-ny-jargi=jin ngaarri-ø
3-PST-fear=3MIN.IO devil-ABS
`He was afraid of the devil.’
*`The devil was afraid of him.’

Maanka injoogal    		 gaara  noorroonim.
Maanka i-n-joo-gal 		 gaara  n˙oorroo-nim
black   3-[PST]-TR-do/say-REC.PST sand   fire-ERG
`The ground got black from the fire.’
```

- In some cases the presence or absence of overt nominal material appears to be grammatically constrained. In the following Bardi sentence the noun _oorany_ is not omissible:

```
Jaarla 		nganjalagal 	*(oorany)  wiliwilon 	inkalgal.
Jaarla 		nga-n-jala-gal 	*(oorany)  wiliwil-on 	i-n-kal-gal
beach(ø-loc) 	1M-TR-see-PST	woman	   fishing 	3M-TR-visit-REC.PST
`I saw a woman on the beach, she was fishing.’ / ‘I saw the woman fishing on the beach.’

```

- Pronouns (or free nouns) which are part of a coordinated phrase cannot be omitted:

```
p. 294
Monty, Lionel agal ngayoo angarrjarrarra barda Broomengan.
Monty, Lionel agal ngayoo a-ng-arr-jarrarra barda Broome-ngan
M.     L.     and  1MIN   1-PST-AUG-get.up. away  B.-ALL
`Monty, Lionel and I got up and went off to Broome.’
```


### Adverbial Clauses
 Oola b i-n-ar-n wiinya i-n-d-an jamb   
 rain rel 3m-tr-pierce-cont full 3m-tr-do.say-cont rel // 
 When it rains it becomes full. 
