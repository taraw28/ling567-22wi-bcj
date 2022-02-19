[Back to README](/README.md)
# Lab 7
## MMT Sentences
```
#15
Manyjalnim alig iila irroojij.
manyjal-nim alig iila i-rr-oo-j-ij
hunger-ERG feel.bad dog 3-AUG-TR-do.say-PFV
`The dogs are hungry.'

#16 (park = cave)
Iilanim gardinon irrni.
iila-nim gardin-on i-rr-ni
dog-ERG park-LOC 3-AUG-be
`The dogs are in the park.'

#17 NP
Irr iila irr aarli.
irr iila irr aarli
3AUG dog 3AUG cat
`The dogs are the cats.'
```

## Removed from bardi.tdl
```
;;; Adjectives

adj-lex := basic-intersective-adjective-lex.

adj1-adj-lex := attr-adj-lex & stative-pred-adj-lex &
  [ SYNSEM.LOCAL.CAT.HEAD.PRD - ].

; Basic attributive adjective definition

attr-adj-lex := adj-lex & intersective-mod-lex &
  [ SYNSEM.LOCAL.CAT.HEAD.MOD < [ LOCAL.CAT [ HEAD noun,
                                              VAL.SPR cons ] ] > ].

; Stative predicate adjective definition

stative-pred-adj-lex := adj-lex &
  [ SYNSEM.LOCAL [ CAT.VAL.SUBJ < [ LOCAL [ CAT.HEAD.CASE real-case,
                                            CONT.HOOK.INDEX #xarg,
                                            CAT [ VAL [ SPR < >,
                                                        COMPS < > ],
                                                  HEAD noun ] ] ] >,
                   CONT.HOOK.XARG #xarg ] ].
```