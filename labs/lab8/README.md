[Back to README](/README.md)
# Lab 8
## Pronouns
### Goal Sentence
  ```
  Nganangoorribirri.
  nga-na-ngoorribi-rri
  1-TR-chase-2MIN.DO
  `I chase you.'
  ```
### Subject Pronoun
- target sentence:
  ```
  Nganangoorribi iila.
  nga-na-ngoorribi iila
  1-TR-chase dog
  `I chase the dog.'
  ```
- updated arg-opt in customization system:
  ```
  section=arg-opt
  subj-drop=subj-drop-all
  subj-mark-drop=subj-mark-drop-req
  subj-mark-no-drop=subj-mark-no-drop-req
  subj-con=subj-con-some
  ```
- instance of subject dropping rule didn't exist so we added
  ```
  basic-head-opt-subj := basic-head-opt-subj-phrase.
  ```
- was able to parse target sentence but was generating 2 trees
  - "incorrect" tree had 2min prefix instead of 1min prefix
  - this is because nga- is both a 1min and 2min prefix
  - after doing further research, found a way to constrain this a bit more:
  - pp 365: pernum prefixes/tense combos / pp. 396 for forms
    - 2min, 3min, 3aug vary for tense
      - 3 in fut/irr = oo-
      - 3 in pres/past = i-
      - 2min in fut/imp(erative) = a- (tr v.) or nga- (itr v.)
        - (example pp 395)
      - 2min elsewhere = mi-
  - updated morphology for pernum to account for pernum/tense combo
  ```
  verb-pc3_name=pernum
    verb-pc3_obligatory=on
    verb-pc3_order=prefix
    verb-pc3_inputs=verb-pc2, verb-pc5
      verb-pc3_lrt1_name=1min
        verb-pc3_lrt1_feat1_name=pernum
        verb-pc3_lrt1_feat1_value=1min_excl
        verb-pc3_lrt1_feat1_head=subj
        verb-pc3_lrt1_lri1_inflecting=yes
        verb-pc3_lrt1_lri1_orth=nga-
        verb-pc3_lrt1_lri2_inflecting=yes
        verb-pc3_lrt1_lri2_orth=ng-
      verb-pc3_lrt2_name=2min-nfut
        verb-pc3_lrt2_feat1_name=pernum
        verb-pc3_lrt2_feat1_value=2min
        verb-pc3_lrt2_feat1_head=subj
        verb-pc3_lrt2_feat2_name=tense
        verb-pc3_lrt2_feat2_value=pst, prs
        verb-pc3_lrt2_feat2_head=verb
        verb-pc3_lrt2_lri1_inflecting=yes
        verb-pc3_lrt2_lri1_orth=mi-
      verb-pc3_lrt3_name=3-fut
        verb-pc3_lrt3_feat1_name=pernum
        verb-pc3_lrt3_feat1_value=3min, 3aug
        verb-pc3_lrt3_feat1_head=subj
        verb-pc3_lrt3_feat2_name=tense
        verb-pc3_lrt3_feat2_value=fut
        verb-pc3_lrt3_feat2_head=verb
        verb-pc3_lrt3_lri2_inflecting=yes
        verb-pc3_lrt3_lri2_orth=oo-
      verb-pc3_lrt4_name=1plus2min
        verb-pc3_lrt4_feat1_name=pernum
        verb-pc3_lrt4_feat1_value=1min_incl
        verb-pc3_lrt4_feat1_head=subj
        verb-pc3_lrt4_lri1_inflecting=yes
        verb-pc3_lrt4_lri1_orth=a-
      verb-pc3_lrt5_name=1aug
        verb-pc3_lrt5_feat1_name=pernum
        verb-pc3_lrt5_feat1_value=1aug
        verb-pc3_lrt5_feat1_head=subj
        verb-pc3_lrt5_require1_others=verb-pc4
        verb-pc3_lrt5_lri1_inflecting=yes
        verb-pc3_lrt5_lri1_orth=a-
      verb-pc3_lrt6_name=2aug-nfut
        verb-pc3_lrt6_feat1_name=pernum
        verb-pc3_lrt6_feat1_value=2aug
        verb-pc3_lrt6_feat1_head=subj
        verb-pc3_lrt6_feat2_name=tense
        verb-pc3_lrt6_feat2_value=pst, prs
        verb-pc3_lrt6_feat2_head=verb
        verb-pc3_lrt6_require1_others=verb-pc4
        verb-pc3_lrt6_lri1_inflecting=yes
        verb-pc3_lrt6_lri1_orth=goo-
      verb-pc3_lrt7_name=3-nfut
        verb-pc3_lrt7_feat1_name=pernum
        verb-pc3_lrt7_feat1_value=3min, 3aug
        verb-pc3_lrt7_feat1_head=subj
        verb-pc3_lrt7_feat2_name=tense
        verb-pc3_lrt7_feat2_value=pst, prs
        verb-pc3_lrt7_feat2_head=verb
        verb-pc3_lrt7_require1_others=verb-pc4
        verb-pc3_lrt7_lri1_inflecting=yes
        verb-pc3_lrt7_lri1_orth=i-
      verb-pc3_lrt8_name=2min-fut-tr
        verb-pc3_lrt8_feat1_name=pernum
        verb-pc3_lrt8_feat1_value=1min_excl
        verb-pc3_lrt8_feat1_head=subj
        verb-pc3_lrt8_feat2_name=tense
        verb-pc3_lrt8_feat2_value=fut
        verb-pc3_lrt8_feat2_head=verb
        verb-pc3_lrt8_require1_others=verb2, verb6, verb8
        verb-pc3_lrt8_lri1_inflecting=yes
        verb-pc3_lrt8_lri1_orth=a-
      verb-pc3_lrt9_name=2min-fut-it
        verb-pc3_lrt9_feat1_name=pernum
        verb-pc3_lrt9_feat1_value=1min_excl
        verb-pc3_lrt9_feat1_head=subj
        verb-pc3_lrt9_feat2_name=tense
        verb-pc3_lrt9_feat2_value=fut
        verb-pc3_lrt9_feat2_head=verb
        verb-pc3_lrt9_require1_others=verb1, verb3
        verb-pc3_lrt9_lri1_inflecting=yes
        verb-pc3_lrt9_lri1_orth=nga-
      verb-pc3_lrt10_name=2aug-fut
        verb-pc3_lrt10_feat1_name=pernum
        verb-pc3_lrt10_feat1_value=2aug
        verb-pc3_lrt10_feat1_head=subj
        verb-pc3_lrt10_feat2_name=tense
        verb-pc3_lrt10_feat2_value=fut
        verb-pc3_lrt10_feat2_head=verb
        verb-pc3_lrt10_lri1_inflecting=yes
        verb-pc3_lrt10_lri1_orth=a-
  ```
  - no longer generating "incorrect" tree


## Object Pronoun
- target sentence:
  ```
  Iilanim oorroongoorribirri.
  iila-nim oo-rr-oo-ngoorribi-rri
  dog-ERG 3-AUG-TR-chase-2MIN.DO
  `Dogs chase you.'
  ```
- we partially worked on this a couple of weeks ago so we already had this in our choices file:
  ```
  section=arg-opt
  ...
  obj-drop=obj-drop-all
  obj-mark-drop=obj-mark-drop-req
  obj-mark-no-drop=obj-mark-no-drop-opt
  ```
- and had this position class for direct object suffixes:
  ```
  verb-pc7_name=dir-obj
  verb-pc7_order=suffix
  verb-pc7_inputs=verb-pc1, verb-pc3
    verb-pc7_require1_others=verb2, verb6, verb8
    verb-pc7_lrt1_name=1min-dir-obj
      verb-pc7_lrt1_feat1_name=pernum
      verb-pc7_lrt1_feat1_value=1min_excl
      verb-pc7_lrt1_feat1_head=obj
      verb-pc7_lrt1_lri1_inflecting=yes
      verb-pc7_lrt1_lri1_orth=-ngay
    verb-pc7_lrt2_name=2min-dir-obj
      verb-pc7_lrt2_feat1_name=pernum
      verb-pc7_lrt2_feat1_value=2min
      verb-pc7_lrt2_feat1_head=obj
      verb-pc7_lrt2_lri1_inflecting=yes
      verb-pc7_lrt2_lri1_orth=-rri
    verb-pc7_lrt3_name=3min-dir-obj
      verb-pc7_lrt3_feat1_name=pernum
      verb-pc7_lrt3_feat1_value=3min
      verb-pc7_lrt3_feat1_head=obj
      verb-pc7_lrt3_feat2_name=overt-arg
      verb-pc7_lrt3_feat2_value=not-permitted
      verb-pc7_lrt3_feat2_head=obj
      verb-pc7_lrt3_lri1_inflecting=no
    verb-pc7_lrt4_name=1plus2min-dir-obj
      verb-pc7_lrt4_feat1_name=pernum
      verb-pc7_lrt4_feat1_value=1min_incl
      verb-pc7_lrt4_feat1_head=obj
      verb-pc7_lrt4_lri1_inflecting=yes
      verb-pc7_lrt4_lri1_orth=-way
    verb-pc7_lrt5_name=1aug-dir-obj
      verb-pc7_lrt5_feat1_name=pernum
      verb-pc7_lrt5_feat1_value=1aug
      verb-pc7_lrt5_feat1_head=obj
      verb-pc7_lrt5_lri1_inflecting=yes
      verb-pc7_lrt5_lri1_orth=-moord
    verb-pc7_lrt6_name=2aug-dir-obj
      verb-pc7_lrt6_feat1_name=pernum
      verb-pc7_lrt6_feat1_value=2aug
      verb-pc7_lrt6_feat1_head=obj
      verb-pc7_lrt6_lri1_inflecting=yes
      verb-pc7_lrt6_lri1_orth=-goorr
    verb-pc7_lrt7_name=3aug-dir-obj
      verb-pc7_lrt7_feat1_name=pernum
      verb-pc7_lrt7_feat1_value=3aug
      verb-pc7_lrt7_feat1_head=obj
      verb-pc7_lrt7_lri1_inflecting=yes
      verb-pc7_lrt7_lri1_orth=-irr
  ```
- we were able to parse the target sentence and it produced 2 trees, one of which was incorrect
  - the root S was being created using basic-head-opt-comp rule
  - we took this problem to canvas and were advised to constrict the basic-head-opt-come rule to require [SUBJ cons ] on the head daughter so we added this to bardi.tdl:
  ```
  basic-head-opt-comp-phrase :+ [ HEAD-DTR.SYNSEM.LOCAL.CAT.VAL.SUBJ cons ].
  ```
  - this worked and only one tree is generated
