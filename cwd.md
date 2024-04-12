# Woods Cree language model documentation

All doc-comment documentation in one large file.

---

# src-cg3-functions.cg3.md 


S Y N T A C T I C   F U N C T I O N S   F O R  (LANGUAGE NAME HERE)

Sámi language technology project 2003-2014, University of Tromsø # 

This file adds syntactic functions. It was copied from sme.

Syntactic sets

* <cs> : 
* @+FAUXV : finite auxiliary verb 
* @+FMAINV : finite main verb
* @-F<OBJ : Subject of infinite verb outside the verbal.
* @-F<PRED : Predicative complement of infinite verb outside the verbal.
* @-FADVL : Adverbial complement of infinite verb outside the verbal.
* @-FAUXV : infinite auxiliary verb
* @-FMAINV : infinite main verb
* @-FOBJ> : Object of infinite verb outside the verbal.
* @-FSUBJ> : Subject of infinite verb outside the verbal.
* @<ADVL : Adverbial after the main verb.
* @<OBJ : Object, the verb is to the left.
* @<OPRED : Object predicative, the verb is to the left.
* @<SPRED : Subject predicative, the verb is to the left.
* @<SUBJ : Subject, the finite verb is to the left.
* @>A : Modifier of an adjective to the right.
* @>ADVL : Modifier of an adverbial to the right.
* @>N : Modifier of a noun to the right.
* @>Num : Attribute of numeral to the right.
* @>Pron : Modifyer of pronoun to the right.
* @ADVL< : Komplement for adverbial.
* @ADVL> : Adverbial to the left of the main verb
* @ADVL>CS : Adverbial modifying subjunction.
* @APP : Apposition
* @APP-ADVL< : Apposition to adverbial to the left.
* @APP-N< : Apposition to noun to the left.
* @APP-Num< : Apposition to numeral to the left.
* @APP-Pron< : Apposition to pronoun to the left.
* @APP>Pron : Apposition to noun to the right.
* @CMPND
* @CNP : Local conjunction or subjunction.
* @COMP-CS< : Complement of subjunction.
* @CVP : Conjunction or subjunction that conjoins finite verb phrases.
* @HNOUN : Stray noun in sentence fragment.
* @INTERJ : Interjection.
* @N< : Complement of noun to the left.
* @Num< : Complement of numeral to the left.
* @OBJ : Object, the verb is not in the sentence (ellipse)
* @OBJ> : Object, the verb is to the right.
* @OPRED : Object predicative, the verb is not in the sentence (ellipse).
* @OPRED> : Object predicative, the verb is to the right.
* @P< : Complement of preposition.
* @PCLE : Particle.
* @PPRED : Predicative for predicative.
* @Pron< : Complement of pronoun to the left.
* @SPRED : Subject predicative, the verb is not in the sentence (ellipse).
* @SPRED<OBJ : Object of an subsject predicative. (some adjectives are transitive)
* @SPRED> : Subject predicative, the verb is to the left.
* @SUBJ : Subject, the finite verb is not in the sentence (ellipse).
* @SUBJ> : Subject, the finite verb is to the right.
* @VOC : Vocative
* @X : The function is unknown, e.g. because of that the word is unknown

* NP sets defined according to their morphosyntactic features

* The PRE-NP-HEAD family of sets

These sets model noun phrases (NPs). The idea is to first define whatever can
occur in front of the head of the NP, and thereafter negate that with the
expression **WORD - premodifiers**.

The set **NOT-NPMOD** is used to find barriers between NPs.
Typical usage: ... (*1 N BARRIER NPT-NPMOD) ...
meaning: Scan to the first noun, ignoring anything that can be
part of the noun phrase of that noun (i.e., "scan to the next NP head")

## HNOUN MAPPING

The leftovers are tagged @X

###  **missingX** adds @X to all missings

###  **therestX** adds @X to all what is left, often errouneus disambiguated forms

* * *

<small>This (part of) documentation was generated from [src/cg3/functions.cg3](https://github.com/giellalt/lang-cwd/blob/main/src/cg3/functions.cg3)</small>

---

# src-fst-morphology-affixes-noun_affixes.lexc.md 



Here we continue to lexical prenouns (in prenouns.lexc)

Starting with the general morphosyntactic features in a standardized order

Suffixation for animate nouns

Potentially obsolete code

Suffixation for inanimate nouns

Likely obsolete code

Irregular nouns

NOUN_ENDLEXs for wrapping up various things

End of noun affixes LEXC code

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/affixes/noun_affixes.lexc](https://github.com/giellalt/lang-cwd/blob/main/src/fst/morphology/affixes/noun_affixes.lexc)</small>

---

# src-fst-morphology-affixes-prenouns.lexc.md 


Woods Cree verb morphology                  

Prenouns

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/affixes/prenouns.lexc](https://github.com/giellalt/lang-cwd/blob/main/src/fst/morphology/affixes/prenouns.lexc)</small>

---

# src-fst-morphology-affixes-preverbs.lexc.md 


Woods Cree verb morphology                  

Preverbs

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/affixes/preverbs.lexc](https://github.com/giellalt/lang-cwd/blob/main/src/fst/morphology/affixes/preverbs.lexc)</small>

---

# src-fst-morphology-affixes-verb_affixes.lexc.md 


Plains Cree verb morphology                  

The Plains Cree verbs are divided in four groups:

1. AI: Animate intransitive 
1. II: Inanimate intransitive
1. TA: Transitive animate
1. TI: Transitive inanimate

# Prefixes

LEXICON VerbPrefixes   divides the lexicon into four modes: independent, conjunctive, imperative and future conditional

* @U.order.indep@ INDEPENDENT ;         
* @U.order.cnj@   CONJUNCT ;             
*                 IMPERATIVE ;          
*                 FUTURE_CONDITIONAL ;  

LEXICON INDEPENDENT  gives flags and prefixes for personprefix
Hypotheticals

LEXICON IND_TENSE  gives flags and prefixes for tense 

LEXICON FUTURE_CONDITIONAL  gives flags for future conditional (no prefix)

LEXICON CONJUNCT  gives flag for conjunct and combined tense preverbs

LEXICON CNJ_TENSE    gives prefixes and flags for tense in conjunct

LEXICON IMPERATIVE    gives flag for imperative (no prefixes)

Preverbs

LEXICON VERBPREFIXES   just adds the prefix boundary

Here we will take care of lexical preverbs (in preverbs.lexc)

Now, LEXC directs us to the ../stems/verbs_stems.lexc file,
where we find all the verbal stems. The suffixes are then
found in the section "Suffixes" right underneath.

# Suffixes

Intransitive inanimate (II)

LEXICON VIIn   

LEXICON VIIn_SG   

LEXICON VIIw_PL   

= LEXICON VIIw_PL   NO LONGER NEEDED FROM AROK
+V+II: VIIw_PL_WICI ;	   NO LONGER NEEDED FROM AROK

LEXICON VIIw   

LEXICON VIIw_SG   

LEXICON VIIn_PL   NO LONGER NEEDED FROM AROK
NO LONGER NEEDED FROM AROK

	 NO LONGER NEEDED FROM AROK
@U.wici.NULL@ VIIw_PL_ORDER ; NO LONGER NEEDED FROM AROK

@U.wici.NULL@ VIIw_PL_ORDER ;

LEXICON VIIw_SGPL_ORDER  

LEXICON VIIw_SG_ORDER  singular only

LEXICON VIIw_PL_ORDER  singular only

= LEXICON VIIw_PL_ORDER  plural only 
@U.order.indep@+Ind:@U.order.indep@ VIIw_PL_IND_PERSON ; !
@U.order.cnj@+Cnj:@U.order.cnj@ VIIw_PL_CNJ_PERSON ; !
@U.order.FutCon@+Fut+Cond:@U.order.FutCon@ VIIw_PL_FUT_CON_PERSON ;!

LEXICON VIIn_SGPL_ORDER  

LEXICON VIIn_SG_ORDER  singular only

LEXICON VIIn_PL_ORDER  plural only

LEXICON VIIw_SG_IND_TENSE  plural only

LEXICON VIIw_SG_CNJ_TENSE  plural only

LEXICON VIIw_PL_IND_TENSE  plural only

LEXICON VIIw_PL_CNJ_TENSE  plural only

= LEXICON VIIw_PL_CNJ_TENSE  plural only
@U.tense.Prs@+Prs:@U.tense.Prs@ VIIw_PL_IND_PERSON ; !
@U.tense.Prt@+Prt:@U.tense.Prt@ VIIw_PL_IND_PERSON ; !
@U.tense.FutDef@+Fut+Def:@U.tense.FutDef@ VIIw_PL_IND_PERSON ; !
@U.tense.FutInt@+Fut+Int:@U.tense.FutInt@ VIIw_PL_IND_PERSON ; !

= LEXICON VIIw_PL_CNJ_TENSE  plural only
@U.tense.Prs@+Prs:@U.tense.Prs@ VIIw_PL_CNJ_PERSON ; !
@U.tense.Prt@+Prt:@U.tense.Prt@ VIIw_PL_CNJ_PERSON ; !
@U.tense.FutInt@+Fut+Int:@U.tense.FutInt@ VIIw_PL_CNJ_PERSON ; !

LEXICON VIIn_SG_IND_TENSE  plural only

LEXICON VIIn_SG_CNJ_TENSE  plural only

LEXICON VIIn_PL_IND_TENSE  plural only

LEXICON VIIn_PL_CNJ_TENSE  plural only

LEXICON VIIw_SGPL_IND_PERSON  

LEXICON VIIw_SGPL_CNJ_PERSON  

LEXICON VIIw_SGPL_FUT_CON_PERSON  

LEXICON VIIw_SG_IND_PERSON  

LEXICON VIIw_SG_CNJ_PERSON  

LEXICON VIIw_SG_FUT_CON_PERSON  

LEXICON VIIw_PL_IND_PERSON  

LEXICON VIIw_PL_CNJ_PERSON  

LEXICON VIIw_PL_FUT_CON_PERSON  

= LEXICON VIIw_PL_FUT_CON_PERSON  plural only
@U.person.NULL@ VIIw_IND_PL_SUFFIX ;

= LEXICON VIIw_PL_FUT_CON_PERSON  plural only
@U.person.NULL@ VIIw_CNJ_PL_SUFFIX ;

= LEXICON VIIw_PL_FUT_CON_PERSON  plural only
@U.person.NULL@ VIIw_FUT_CON_PL_SUFFIX ;

LEXICON VIIn_SGPL_IND_PERSON  

LEXICON VIIn_SGPL_CNJ_PERSON  

LEXICON VIIn_SGPL_FUT_CON_PERSON  

LEXICON VIIn_SG_IND_PERSON  

LEXICON VIIn_SG_CNJ_PERSON  

LEXICON VIIn_SG_FUT_CON_PERSON  

LEXICON VIIn_PL_IND_PERSON  plural only

LEXICON VIIn_PL_CNJ_PERSON  plural only

LEXICON VIIn_PL_FUT_CON_PERSON  plural only

LEXICON VIIn_SGPL_IND_NULL 

LEXICON VIIn_SG_IND_SUFFIX    singular

LEXICON VIIn_PL_IND_SUFFIX   plural

LEXICON VIIw_SGPL_IND_NULL 

LEXICON VIIw_SG_IND_SUFFIX    w final singular

LEXICON VIIw_PL_IND_SUFFIX   w final plural

LEXICON VIIn_SGPL_CNJ_NULL 

LEXICON VIIn_SG_CNJ_SUFFIX    singular

LEXICON VIIn_PL_CNJ_SUFFIX   plural

LEXICON VIIw_SGPL_CNJ_NULL 

LEXICON VIIw_SG_CNJ_SUFFIX    w final singular

LEXICON VIIw_PL_CNJ_SUFFIX    w final plural

LEXICON VIIn_SGPL_FUT_CON_NULL 

LEXICON VIIn_SG_FUT_CON_SUFFIX    singular

LEXICON VIIn_PL_FUT_CON_SUFFIX   plural

LEXICON VIIw_SGPL_FUT_CON_NULL 

LEXICON VIIw_SG_FUT_CON_SUFFIX    w final singular

LEXICON VIIw_PL_FUT_CON_SUFFIX    w final plural

Intransitive animate (AI)

LEXICON VAIw_PL  stems that end in â or ê

LEXICON VAIae  stems that end in â or ê

LEXICON VAIio  stems that end in i, î, o, ô

LEXICON VAIn  

LEXICON VAIn_PL  

LEXICON VAIm  These are VTI3 in Arok's database

LEXICON VAIn_ORDER 

LEXICON VAIn_PL_ORDER  plural only  

LEXICON VAIae_ORDER 

LEXICON VAIw_PL_ORDER  plural only 

LEXICON VAIio_ORDER 

LEXICON VAIn_PL_IND_TENSE  plural only

LEXICON VAIn_PL_CNJ_TENSE  plural only

LEXICON VAIw_PL_IND_TENSE  plural only

LEXICON VAIw_PL_CNJ_TENSE  plural only

LEXICON VAIn_IND_PERSON  

LEXICON VAIn_CNJ_PERSON  

LEXICON VAIn_FUT_CON_PERSON  

LEXICON VAIn_IMP_PERSON  

LEXICON VAIn_PL_IND_PERSON  plural only

LEXICON VAIn_PL_CNJ_PERSON  plural only

LEXICON VAIn_PL_FUT_CON_PERSON  plural only

LEXICON VAIn_PL_IMP_PERSON  plural only

LEXICON VAIw_PL_IND_PERSON  plural only

LEXICON VAIw_PL_CNJ_PERSON  plural only

LEXICON VAIw_PL_FUT_CON_PERSON  plural only

LEXICON VAIw_PL_IMP_PERSON  plural only

LEXICON VAIae_IND_PERSON  

LEXICON VAIae_CNJ_PERSON  

LEXICON VAIw_FUT_CON_PERSON  

LEXICON VAIw_IMP_PERSON  

LEXICON VAIio_IND_PERSON  

LEXICON VAIio_CNJ_PERSON  

LEXICON VAIw_IND_NI     

LEXICON VAIw_IND_NI_SG_SUFFIX    

LEXICON VAIw_IND_NI_PL_SUFFIX   

LEXICON VAIw_IND_KI     

LEXICON VAIw_IND_KI_SG_SUFFIX    

LEXICON VAIw_IND_KI_PL_SUFFIX    

LEXICON VAIae_IND_NULL     

LEXICON VAIio_IND_NULL     

LEXICON VAIw_IND_NULL_PL_SUFFIX   

LEXICON VAIn_IND_NI    

LEXICON VAIn_IND_NI_SG_SUFFIX    

LEXICON VAIn_IND_NI_PL_SUFFIX    

LEXICON VAIn_IND_KI     

LEXICON VAIn_IND_KI_SG_SUFFIX    

LEXICON VAIn_IND_KI_PL_SUFFIX    

LEXICON VAIn_IND_NULL     

LEXICON VAIn_IND_NULL_SG_SUFFIX    

LEXICON VAIn_IND_NULL_PL_SUFFIX    

LEXICON VAIae_CNJ_NULL    

LEXICON VAIio_CNJ_NULL    

LEXICON VAIae_CNJ_NULL_SG_SUFFIX    

LEXICON VAIio_CNJ_NULL_SG_SUFFIX    

LEXICON VAIw_CNJ_NULL_PL_SUFFIX    

LEXICON VAIn_CNJ_NULL    

LEXICON VAIn_CNJ_NULL_SG_SUFFIX    

LEXICON VAIn_CNJ_NULL_PL_SUFFIX    

LEXICON VAIae_FUT_CON_NULL    

LEXICON VAIw_FUT_CON_NULL_SG_SUFFIX    

+X+4Sg:%>yiki # ;

LEXICON VAIw_FUT_CON_NULL_PL_SUFFIX    

+X+4Pl:%>yikwâwi # ;

LEXICON VAIn_FUT_CON_NULL    

LEXICON VAIn_FUT_CON_NULL_SG_SUFFIX    

+X+4Sg:%>iyiki # ;

LEXICON VAIn_FUT_CON_NULL_PL_SUFFIX    

+X+4Pl:%>iyikwâwi # ;

Transitive inanimate (TI)

* LEXICON VTIm   

* LEXICON VTIm_PL    Plural

* LEXICON VTIae   NOTE: These inflect just as VAI -w final stems, so they are redirected to those paradigms

* LEXICON VTIio   NOTE: These inflect just as VAI -w final stems, so they are redirected to those paradigms

LEXICON VTIm_ORDER  . 

LEXICON VTIm_PL_ORDER  plural only NOTE: imperative and fut con go straight to person lexica

LEXICON VTIm_PL_IND_TENSE  plural only

LEXICON VTIm_PL_CNJ_TENSE  plural only

LEXICON VTIm_IND_PERSON  

LEXICON VTIm_CNJ_PERSON  

LEXICON VTIm_FUT_CON_PERSON  

LEXICON VTIm_IMP_PERSON  

LEXICON VTIm_PL_IND_PERSON  plural only

LEXICON VTIm_PL_CNJ_PERSON  plural only

LEXICON VTIm_PL_FUT_CON_PERSON  plural only

LEXICON VTIm_PL_IMP_PERSON  plural only

LEXICON VTIm_IND_NI     

LEXICON VTIm_IND_NI_SG_SUFFIX    

LEXICON VTIm_IND_NI_PL_SUFFIX    

LEXICON VTIm_IND_KI     

LEXICON VTIm_IND_KI_SG_SUFFIX    

LEXICON VTIm_IND_KI_PL_SUFFIX    

LEXICON VTIm_IND_NULL     

LEXICON VTIm_IND_NULL_SG_SUFFIX    NOTE: X actor will eventually derive to VII, so it is not yet included as per Arok's paradigm

Derives to VIIn

LEXICON VTIm_IND_NULL_PL_SUFFIX    

Derives to VIIn

LEXICON VTIm_CNJ_NULL    

LEXICON VTIm_CNJ_NULL_SG_SUFFIX    

+X+4Sg:%>mihiyik # ;

LEXICON VTIm_CNJ_NULL_PL_SUFFIX    

+X+4Pl:%>mihiyiki # ;

LEXICON VTIm_FUT_CON_NULL    

LEXICON VTIm_FUT_CON_NULL_SG_SUFFIX    

+X+4Sg:%>mihiyiki # ;

LEXICON VTIm_FUT_CON_NULL_PL_SUFFIX    

+X+3Sg:%>mihkwâwi # ;
+X+4Sg:%>mihiyikwâwi # ;

* LEXICON VTA   Multi-Syllabic stems 

* LEXICON VTA_PL   Multi-Syllabic stems plural only forms

* LEXICON VTAt   Multi-Syllabic t/s-final alternating stems

* LEXICON VTAi   Mono-Syllabic stems

* LEXICON VTA_WICI   -Vw stem-ending verbs; where + i suf deletes w and i

* LEXICON VTA_PL_WICI   -Vw stem-ending verbs; when deletes w and i plural only forms 

* LEXICON VTAt_WICI   -t ending stems

* LEXICON VTAi_WICI   single mora stems

LEXICON VTA_ORDER  Note: Imp and Fut Con don't take tense

LEXICON VTA_PL_ORDER  Note: Imp and Fut Con don't take tense 

LEXICON VTAi_ORDER  Note: Imp and Fut Con don't take tense ; Conjugates as TA regular except in 2sg IMM IMP

LEXICON VTAt_ORDER  Note: Imp and Fut Con don't take tense ; Conjugates as TA regular except in 2sg IMM IMP

LEXICON VTA_IND_TENSE  plural only

LEXICON VTA_CNJ_TENSE  plural only

LEXICON VTA_PL_IND_TENSE  plural only

LEXICON VTA_PL_CNJ_TENSE  plural only

LEXICON VTA_IND_PERSON  

LEXICON VTA_CNJ_PERSON  

LEXICON VTA_FUT_CON_PERSON  

LEXICON VTA_IMP_PERSON  

LEXICON VTA_PL_IND_PERSON  

LEXICON VTA_PL_CNJ_PERSON  

LEXICON VTA_PL_FUT_CON_PERSON  

LEXICON VTA_PL_IMP_PERSON  

LEXICON VTAt_IMP_PERSON  no -i in 2sg+3SgO

LEXICON VTAi_IMP_PERSON  

LEXICON VTA_IND_NI     NOTE: No local, as local forms are always with ki-

LEXICON VTA_IND_NI_SG_SUFFIX   

LEXICON VTA_IND_NI_PL_SUFFIX    

LEXICON VTA_IND_KI     

LEXICON VTA_IND_KI_SG_SUFFIX    

LEXICON VTA_IND_KI_PL_SUFFIX    

LEXICON VTA_IND_NULL     NOTE: never local

LEXICON VTA_IND_NULL_SG_SUFFIX    

LEXICON VTA_IND_NULL_PL_SUFFIX    

~~~~~~~~~~~~~~~~~~~~~~

End of verb affixes LEXC code

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/affixes/verb_affixes.lexc](https://github.com/giellalt/lang-cwd/blob/main/src/fst/morphology/affixes/verb_affixes.lexc)</small>

---

# src-fst-morphology-phonology.xfscript.md 


Definitions

Rules

VG>i2 -> VV

* *mîskanaw>i2^DIMs*
* *mîskanâ000s*

* *mîskanaw>i2hk*
* *mîskanâ000hk*

* *sôniyâw>i2^DIMs*
* *sôniyâ000s0*

* *miskotâkay>i2^DIMs*
* *miskocâkâ000s0*

* *nâpîw>i2^DIMsis*
* *nâpî0000sis*

* *iskwîw>i2^DIMsis*
* *iskwî0000sis*

* *maskosiy>i2^DIMs*
* *maskosî0000s*

* *pikiw>i2^DIMs*
* *pikî0000s*

* *maskosiy>i2hk*
* *maskosî000hk*

* *sîwâpoy>i2^DIMs*
* *sîwâpô0000s*

* *tohtôsâpoy>i2hk*
* *tohtôsâpô000hk*

* *wâwi>i2^DIMs*
* *wâwi000s*

* *ôsi>i2hk*
* *ôsi00hk*

* *atimw>i2^DIMs*
* *acimo000s*

* *mistikw>i2hk*
* *mistiko00hk*
* *sâkahikan>i2^DIMs*
* *sâkahikan0i0s*

* *maskisin>i2hk*
* *maskisin0ihk*

* *atimw*
* *atim0*

* *askihkw*
* *askihk0*

* *nit2<nînihikw*
* *ni00nînihik*

* *a>tân*
* *î0tân*

* *nit2<astotin>i2^DIMs*
* *nic0ascocin0i0s*

* *î^EGLOT<acimo>t*
* *îh0acimo0t*

* *î^EGLOT<d1ay2<acimo>t*
* *îh00ay0acimo0t*

* *î^EGLOT<d2ay3d1âh<acimo>t*
* *îh00ay0âh0acimo0t*

* *nit2<nîhithawî>n2*
* *ni00nîhithawâ0n*
* *kit2<kâsîhkwî>n2*
* *ki00kâsîhkwâ0n*

* *nit2<tipiska>n2*
* *ni00tipiskî0n*
* *kit2<kiskîthihta>n2*
* *ki00kiskîthihtî0n*

* *î-<nîpin3>k*
* *î-0nîpih0k*

* *î-<mispon>k*
* *î-0mispo00k*

* *wapâht4>ikâtî>w*
* *wapâhc0ikâtî0w*

* *î-<mow2>i2ht*
* *î-0mow0iht*
* *î-<ayaw2>i2koyâhk*
* *î-0ayaw0ikoyâhk*
* *kit2<kîskisw>in*
* *ki00kîskiso00n*
* *nit2<kîskisw>i2mâwa*
* *ni00kîskiso00mâwa*
* *î-<kîskisw>i2tân*
* *î-0kîskiso00tân*
* *î-<kîskisw>it*
* *î-0kîskiso00t*
* *î-<kîskisw>i2sk*
* *î-0kîskiso00sk*
* *î-<kîskisw>i2koyâhk*
* *î-0kîskiso00koyâhk*
* *nit2<kîskisw>i2kawin*
* *ni00kîskiso00kawin*
* *kîskisw>in*
* *kîskiso00n*
* *kîskisw>ii2hkan*
* *kîskisô00hkan*

* *kit2<nitonaw>in*
* *ki00nitonaw0in*
* *nit2<nitonaw>i2mâwa*
* *ni00nitonâ000mâwa*
* *î-<nitonaw>i2tân*
* *î-0nitonâ000tân*
* *î-<nitonaw>it*
* *î-0nitonaw0it*
* *î-<nitonaw>i2sk*
* *î-0nitonâ000sk*
* *î-<nitonaw>i2koyâhk*
* *î-0nitonâ000koyâhk*
* *nit2<nitonaw>i2kawin*
* *ni00nitonâ000kawin*
* *nitonaw>in*
* *nitonaw0in*
* *nitonaw>îhkan*
* *nitonaw0îhkan*

* *it3>i*
* *is0i*
* *kit2<nakat3>in*
* *ki00nakas0in*
* *nit2<nakat3>i2mâwa*
* *ni00nakat0imâwa*
* *î-<nakat3>i2tân*
* *î-0nakat0itân*
* *î-<nakat3>it*
* *î-0nakas0it*
* *î-<nakat3>i2sk*
* *î-0nakat0isk*
* *î-<nakat3>i2koyâhk*
* *î-0nakat0ikoyâhk*
* *nit2<nakat3>i2kawin*
* *ni00nakat0ikawin*
* *nakat3>in*
* *nakas0in*
* *nakat3>ii2hkan*
* *nakas0îhkan*

* *kit2<kost3>in*
* *ki00ko0s0in*
* *nit2<kost3>i2mâwa*
* *ni00kost0imâwa*
* *î-<kost3>i2tân*
* *î-0kost0itân*
* *î-<kost3>it*
* *î-0ko0s0it*
* *î-<kost3>i2sk*
* *î-0kost0isk*
* *î-<kost3>i2koyâhk*
* *î-0kost0ikoyâhk*
* *nit2<kost3>i2kawin*
* *ni00kost0ikawin*
* *kost3>in*
* *ko0s0in*
* *kost3>ii2hkan*
* *ko0s0îhkan*

* *mi4<îwat3>i2^DIMs*
* *m00îwac0i0s*

__`OUTSIDE RULES`__

* *d1ay2-<nipâw*
* *na0-0nipâw*

* *d1âh-<nipâw*
* *nâh-0nipâw*

* *d2ay3-d1âh-<nipâw*
* *na0-nâh-0nipâw*

* *d2ay3-d1âh-<ayâw*
* *0ay-0âh-0ayâw*

* *d1âh-<ayâw*
* *0âh-0ayâw*

* *d1ay2-<ayâw*
* *0ay-0ayâw*

INITIAL CHANGE

* *nipât^IC*
* *nêpât0*

* *miyo-nipât^IC*
* *mêyo-nipât0*

* *itwêt^IC*
* *êtwêt0*

* *apit^IC*
* *êpit0*

* *wayawit^IC*
* *wêyawit0*

* *îkatêhtêt^IC*
* *âkatêhtêt0*

* *nîmit^IC*
* *nâmit0*

* *0ohcît^IC*
* *wêhcît0*

* *m0ostohtêt^IC*
* *mwêstohtêt0*

* *0oyôyot^IC*
* *wêyôyot0*

* *k0ocît^IC*
* *kwêcît0*

* *îkatêhât^IC*
* *âkatêhât0*

* *00îkatêhât^IC*
* *iyîkatêhât0*

* *00êskêt^IC*
* *iyêskêt0*

* *00âcimot^IC*
* *iyâcimot0*

* *00ôhkomit^IC*
* *iyôhkomit0*

* *w3<spiton*
* *o0spiton*

* *ni<spiton*
* *ni0spiton*

* *ki<spiton*
* *ki0spiton*

* *w3<îpit*
* *w0îpit*

* *w3<ahkwan*
* *w0ahkwan*

* *ni4<ohkom*
* *n00ôhkom*

* *ni4<ohkom>i2nân>ak*
* *n00ôhkom0inân0ak*

* *ki4<ohkom*
* *k00ôhkom*

* *w3<ohkom>a*
* *00ohkom0a*

* *nit2<ospwâkan*
* *nit0ôspwâkan*

* *kit2<ospwâkan*
* *kit0ôspwâkan*

* *ot2<ospwâkan*
* *ot0ôspwâkan*

Composing the rules together

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/phonology.xfscript](https://github.com/giellalt/lang-cwd/blob/main/src/fst/morphology/phonology.xfscript)</small>

---

# src-fst-morphology-root.lexc.md 


# Woods Cree morphological analyser
INTRODUCTION TO MORPHOLOGICAL ANALYSER OF Plains Cree LANGUAGE.

# Definitions for Multichar_Symbols

## Analysis symbols

The morphological analyses of wordforms of Plains Cree are presented
in this system in terms of the following symbols.
(It is highly suggested to follow existing standards when adding new tags).

POS

* +N	         = Noun
* +V	         = Verb
* +Ipc		 = Indeclinable Particle
* +Prop       
* +Adv        
* +CC         
* +CS         
* +Interj     
* +Phr        
* +Pron       
* +Num        
* +Arab       
* +Rom        
* +PUNCT       = punctuation symbols
* +LEFT        = the left part of a paired punctuation symbol
* +RIGHT       = the right part of a paired punctuation symbol
* +CLB         = clause boundary symbols
* +Symbol = independent symbols in the text stream, like £, €, ©
* +ABBR 

Nominal morphology

* +Loc         Locative
* +Obv         Obviative
* +Voc         Vocative

* +Dim         Diminutive

Particles

* +Def	     This is the intransitive demonstrative, i.e. the definite.
* +Indef       Indefinite

* +Dem         Demonstrative
* +Prox	     Demonstrative Proximate
* +Med	     Demonstrative Medial
* +Dist	     Demonstrative Distal
* +Pers = personal pronouns? At least it seems so based on the code
* +Interr      Interrogative (who/whose/what/what kind)
* +Foc	     Focus particle

ordinals

Verbal MSP
* +Prs  
* +Fut  
* +Prt  
* +Cnj  
* +Int   Future Intentional
* +Def   Future Definite (TODO: okay to overlap with particle tag of the same name?)

* +Ind   Indicative, aka Independent
* +Imp   Imperative, consider deleting +Imp tag
* +Del   Delayed imperative
* +Imm   Immediate imperative, consider deleting +Imp tag
* +Cond  TODO: Should Future Conditional be tagget Fut only? Conor: we will split the Future tags

* +1Sg     first singular
* +2Sg     etc
* +3Sg    

* +1Pl     1Pl is exclusive plural (I, them, not you)
* +2Pl    
* +3Pl    
* +12Pl    12Pl is inclusive plural (I, you, ...)
* +4Sg     Fourth Person inanimate singlar (used only in the VII paradigms)
* +4Pl     Fourth Person inanimate plural (used only in the VII paradigms)
* +4Sg/Pl    
* +5Sg/Pl    
* +0Sg/Pl    

* +1SgO    objective conjugation
* +2SgO   
* +2Sg/PlO    Used in the syncretic 2sg/pl -> 1pl in the VTA paradigms
* +3SgO   
* +SgO    
* +1PlO   
* +2PlO   
* +12PlO	
* +3PlO   
* +PlO    
* +4Sg/PlO  ambiguous 4th person (both Singular and Plural)
* +5Sg/PlO  ambiguous 5th person (both Singular and Plural)
* +X  Unspecified actor forms Okimāsis p. 118

Person prefix fragment features

Nominal morphosyntactic features
* +Sg		  singular
* +Pl		  plural

* +Px1Sg	  person prefixes for nouns
* +Px2Sg	 
* +Px3Sg	 
* +Px4Sg	 
* +Px1Pl	  obviative
* +Px12Pl	  inclusive
* +Px2Pl	 
* +Px3Pl	 
* +Px4Pl	 
* +Der/Dim  diminutive derivation

* RdplW+  Reduplication Type 1 (Weak)
* RdplS+  Reduplication Type 2 (Strong)

* +Der/Com  Comitative circumfix (wîci-...-m)
* +Der/X  VTI x-actor to VII-1

Verb conjugation (transitivity + animacy classes)
* +AI       intransitive with animate subject,
* +II       intransitive with inanimate subject,
* +TA       transitive with animate object, and
* +TI       transitive with inanimate object.

Noun animacy and dependency classes
* +A		  animate noun
* +I		  inanimate noun
* +D		  dependent noun

* +Qst      yes-no question particle; cî
* +Neg      negation; [na]môy[a].

Preverbs

## Auxiliary symbols

These symbols either shape or govern the
morphophonological structure

* %> 		  suffix border
* %< 		  prefix border

## Symbols that need to be escaped on the lower side (towards twolc):
* **»7**:  Literal »
* **«7**:  Literal «
```
 %[%>%]  - Literal >
 %[%<%]  - Literal <
```

Special characters for morphophonology
* w2       mowêw:mow2
* t2 		 Epenthetic -t- between person prefixes and vowel-initial stems
* t3       t to s in VTA-4
* t4       t:c in VTI-1 with unspecified actor
* y2       epenthetic joiner in reduplication of vowel-initial stems
* y3       epenthetic joiner in reduplication of vowel-initial stems
* i2       vta-5i epenthesis.

* h2 		  Prefix in possessives

Triggers for various morphophonological phenomena
Mostly, these are not realized themselves as any grapheme/phoneme

* %^EGLOT    glottal stop after e, for eh- in conjunctive order

## Usage tags

These tags distinguish different special-purpose analysers
and generators from each other. Thus, for examples, we have
normative and descriptive analysers, and generators for different purposes.

* +Err/Orth  tag for substandard forms
* +Err/Frag  tag for word-form fragments
* +Err/Morph  tag for nonstandard morphology
* +Err/Thm  tag for nonstandard possessive theme (0 vs. -im) morphology
* +Err/Dim  tag for nonstandard diminutive morphology (-is vs. -isis)
* +Err/Dummy  tag for dummy lexemes used for testing purposes
* +Dial  tag for dialectical forms that can't be called errors
* +Dial/East  tag for dialectical forms that can't be called errors
* +Dial/West  tag for dialectical forms that can't be called errors
* +Var  tag for dialectical forms that can't be called errors
* +Var/East  tag for dialectical forms that can't be called errors
* +Var/West  tag for dialectical forms that can't be called errors
* +Use/NG   not-generate, for ped generation isme-ped.fst
* +Eng indicates that this is an English form

Flagdiacritics

These are documented in Chapter 8 of Beesley/Karttunen, p. 456 zB.

For indicative, there are prefixes, so here we need one
flag for each person-number combination. Note that
for the inverse objective conjugation, the flag refers to
the **prefix**, not to the subject. So *indsg1* refers to either
subject = 1Sg or object = 1Sg. The 3-3 forms are prefixless.

The conjunct form always has
the ê- prefix, and future conditional never has a prefix.

* @U.verb.FutCon@  Future Conditional

Prefixes with a certain phonological content:

* @U.person.NULL@ 
* @U.person.NI@ 
* @U.person.KI@ 

Order

* @U.order.indep@  Independent
* @U.order.cnj@    Conjunct
* @U.order.imp@    Imperative

Tense

New multichar symbols for nouns

End of new and all Multichar_Symbols

 LEXICON Root          is where it all starts
* NOUN_PREFIXES   ;    
* NOUN_IRREGULARS ;    
* Vocative_Nouns  ;    
* VerbPrefixes    ;    
* Pronoun         ;    
* Propernouns     ;    
* Particles       ;    
* Numerals        ;    
* Abbreviation    ;    
* Punctuation     ;    
* Symbols         ;    
* NON_STANDARD     ;    

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/root.lexc](https://github.com/giellalt/lang-cwd/blob/main/src/fst/morphology/root.lexc)</small>

---

# src-fst-morphology-stems-noun_stems.lexc.md 



Test lemma/stem set for nouns according the new crk FST

Test case wug stems
(marked with +Err/Dummy so that they may be eventually removed)

Animate Noun stems
Regular/Irregular ôsi- both a regularly inflecting stem, and a number of irregular forms enumerated separately

Complete extraction of lemma:stem info from LLR dictionary 2022, according to
LEXC structure in the new crk FST.

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/stems/noun_stems.lexc](https://github.com/giellalt/lang-cwd/blob/main/src/fst/morphology/stems/noun_stems.lexc)</small>

---

# src-fst-morphology-stems-numerals.lexc.md 


# Plains Cree numerals                           

## The file for numerals

* LEXICON Numerals 

## Here start the 999 numbers

* LEXICON UNDERTHOUSAND 

* LEXICON HUNDREDS 

* LEXICON CUODI 

* LEXICON HUNDRED 

* LEXICON TENS 

* LEXICON TEN 

* LEXICON ONESTONEXT 

* LEXICON TEENS 

* LEXICON ONES 

* LEXICON CARDINAL 

* LEXICON NUM  adds +Num+Ipc

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/stems/numerals.lexc](https://github.com/giellalt/lang-cwd/blob/main/src/fst/morphology/stems/numerals.lexc)</small>

---

# src-fst-morphology-stems-particles.lexc.md 


# Plains Cree particles                           

The file contains the following lexicons, with content as described:

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/stems/particles.lexc](https://github.com/giellalt/lang-cwd/blob/main/src/fst/morphology/stems/particles.lexc)</small>

---

# src-fst-morphology-stems-pronouns.lexc.md 


## Plains Cree pronouns

There are more pronoums to be added here.

LEXICON Pronoun 

LEXICON Personal  \\
nîtha+Pron+Pers+1Sg:nîtha # ; 
kîtha+Pron+Pers+2Sg:kîtha # ; 

LEXICON Interrogative   \\
awîna+Pron+Interr+A+Sg:awîna # "who,whose" ; 
awînak+Pron+Interr+A+Sg:awînak # "who,whose" ; 
awîna+Pron+Interr+A+Pl:awîna # "who,whose" ; 
awînak+Pron+Interr+A+Pl:awînak # "who,whose" ; 
awîniki+Pron+Interr+A+Pl+Var/East:awîniki # "who" ; 
awînikik+Pron+Interr+A+Pl+Var/East:awînikik # "who" ; 
awîna+Pron+Interr+A+Obv:awîna # "who,whose" ; 
awînithiwa+Pron+Interr+A+Obv+Var/East:awînithiwa # "who" ; 
awînaka+Pron+Interr+A+Obv+Var/East:awînaka # "who" ; 

LEXICON Indefinite 
awiyak+Pron+Indef+A+Sg:awiyak # "someone" ; 
awiyak+Pron+Indef+A+Pl:awiyakak # "some people" ;

LEXICON Definite  \\

LEXICON Demonstrative    \\
ANIMATE \\
awa+Pron+Dem+Prox+A+Sg:awa # "this" ; 
ôko+Pron+Dem+Prox+A+Pl:ôko # "these" ; 
ôho+Pron+Dem+Prox+A+Obv:ôho # "this/these" ; 

INANIMATE \\

ôma+Pron+Dem+Prox+I+Sg:ôma # "this" ; 
ôho+Pron+Dem+Prox+I+Pl:ôho # "these" ; 
ômîthiw+Pron+Dem+Prox+I+Obv:ômîthiw # "this/these" ; 

ôma+Pron+Def+Prox+I+Sg:ôma # "this one" ; 
ôho+Pron+Def+Prox+I+Pl:ôho # "these one" ; 
ômîthiw+Pron+Def+Prox+I+Obv:ômîthiw # "this/these one(s)" ; 

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/stems/pronouns.lexc](https://github.com/giellalt/lang-cwd/blob/main/src/fst/morphology/stems/pronouns.lexc)</small>

---

# src-fst-morphology-stems-verb_stems.lexc.md 



Model verb lemmas and stems for new crk FST

Full incorporation of AEW 2020 verbs into new crk FST

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/stems/verb_stems.lexc](https://github.com/giellalt/lang-cwd/blob/main/src/fst/morphology/stems/verb_stems.lexc)</small>

---

# src-fst-phonetics-txt2ipa.xfscript.md 



retroflex plosive, voiceless			t`  ʈ	    0288, 648 (` = ASCII 096)
retroflex plosive, voiced			d`	ɖ		0256, 598
labiodental nasal					F 	ɱ		0271, 625
retroflex nasal						n` 	ɳ		0273, 627
palatal nasal						J 	ɲ		0272, 626
velar nasal							N 	ŋ		014B, 331
uvular nasal							N\	ɴ		0274, 628
	
bilabial trill						B\ 	ʙ		0299, 665
uvular trill							R\ 	ʀ		0280, 640
alveolar tap							4	ɾ		027E, 638
retroflex flap						r` 	ɽ		027D, 637
bilabial fricative, voiceless		p\ 	ɸ		0278, 632
bilabial fricative, voiced			B 	β		03B2, 946
dental fricative, voiceless			T 	θ		03B8, 952
dental fricative, voiced				D 	ð		00F0, 240
postalveolar fricative, voiceless	S	ʃ		0283, 643
postalveolar fricative, voiced		Z 	ʒ		0292, 658
retroflex fricative, voiceless		s` 	ʂ		0282, 642
retroflex fricative, voiced			z` 	ʐ		0290, 656
palatal fricative, voiceless			C 	ç		00E7, 231
palatal fricative, voiced			j\ 	ʝ		029D, 669
velar fricative, voiced	        	G 	ɣ		0263, 611
uvular fricative, voiceless			X	χ		03C7, 967
uvular fricative, voiced				R 	ʁ		0281, 641
pharyngeal fricative, voiceless		X\ 	ħ		0127, 295
pharyngeal fricative, voiced			?\ 	ʕ		0295, 661
glottal fricative, voiced			h\	ɦ		0266, 614

alveolar lateral fricative, vl.		K 
alveolar lateral fricative, vd.		K\

labiodental approximant				P (or v\) 
alveolar approximant					r\ 
retroflex approximant				r\` 
velar approximant					M\

retroflex lateral approximant		l` 
palatal lateral approximant			L 
velar lateral approximant			L\
Clicks

bilabial								O\	(O = capital letter) 
dental								|\
(post)alveolar						!\ 
palatoalveolar						=\ 
alveolar lateral						|\|\
Ejectives, implosives

ejective								_>	e.g. ejective p		p_>
implosive							_<	e.g. implosive b	b_<
Vowels

close back unrounded					M
close central unrounded 				1 
close central rounded				} 
lax i								I 
lax y								Y 
lax u								U

close-mid front rounded				2 
close-mid central unrounded			@\ 
close-mid central rounded			8 
close-mid back unrounded				7

schwa	ə							@

open-mid front unrounded				E 
open-mid front rounded				9
open-mid central unrounded			3 
open-mid central rounded				3\ 
open-mid back unrounded				V 
open-mid back rounded				O

ash (ae digraph)						{ 
open schwa (turned a)				6

open front rounded					& 
open back unrounded	        		A 
open back rounded					Q
Other symbols

voiceless labial-velar fricative		W 
voiced labial-palatal approx.		H 
voiceless epiglottal fricative		H\ 
voiced epiglottal fricative			<\ 
epiglottal plosive					>\

alveolo-palatal fricative, vl. 		s\ 
alveolo-palatal fricative, voiced	z\ 
alveolar lateral flap				l\ 
simultaneous S and x					x\ 
tie bar								_
Suprasegmentals

primary stress						" 
secondary stress						% 
long									: 
half-long							:\ 
extra-short							_X 
linking mark							-\
Tones and word accents

level extra high						_T 
level high							_H
level mid							_M 
level low							_L 
level extra low						_B
downstep								! 
upstep								^	(caret, circumflex)

contour, rising						 
contour, falling						_F 
contour, high rising					_H_T 
contour, low rising					_B_L 

contour, rising-falling				_R_F 
(NB Instead of being written as diacritics with _, all prosodic 
marks can alternatively be placed in a separate tier, set off 
by < >, as recommended for the next two symbols.)
global rise						<R> 
global fall						<F>
Diacritics						
									
voiceless						_0	(0 = figure), e.g. n_0
voiced							_v 
aspirated						_h 
more rounded						_O	(O = letter) 
less rounded						_c 
advanced							_+
retracted						_-
centralized						_" 
syllabic							=	(or _=) e.g. n= (or n_=) 
non-syllabic						_^ 
rhoticity						`
									
breathy voiced					_t 
creaky voiced					_k
linguolabial						_N 
labialized						_w 
palatalized						'	(or _j) e.g. t' (or t_j) 
velarized						_G 
pharyngealized					_?\
									
dental							_d 
apical							_a 
laminal							_m
nasalized						~	(or _~) e.g. A~ (or A_~) 
nasal release					_n
lateral release					_l 
no audible release				_}

velarized or pharyngealized		_e 
velarized l, alternatively		5 
raised							_r 
lowered							_o 
advanced tongue root				_A 
retracted tongue root			_q

* * *

<small>This (part of) documentation was generated from [src/fst/phonetics/txt2ipa.xfscript](https://github.com/giellalt/lang-cwd/blob/main/src/fst/phonetics/txt2ipa.xfscript)</small>

---

# src-fst-transcriptions-transcriptor-abbrevs2text.lexc.md 



We describe here how abbreviations are in Woods Cree are read out, e.g.
for text-to-speech systems.

For example:

* s.:syntynyt # ;  
* os.:omaa% sukua # ;  
* v.:vuosi # ;  
* v.:vuonna # ;  
* esim.:esimerkki # ; 
* esim.:esimerkiksi # ; 

* * *

<small>This (part of) documentation was generated from [src/fst/transcriptions/transcriptor-abbrevs2text.lexc](https://github.com/giellalt/lang-cwd/blob/main/src/fst/transcriptions/transcriptor-abbrevs2text.lexc)</small>

---

# src-fst-transcriptions-transcriptor-numbers-digit2text.lexc.md 



% komma% :,      Root ;
% tjuohkkis% :%. Root ;
% kolon% :%:     Root ;
% sárggis% :%-   Root ; 
% násti% :%*     Root ; 

* * *

<small>This (part of) documentation was generated from [src/fst/transcriptions/transcriptor-numbers-digit2text.lexc](https://github.com/giellalt/lang-cwd/blob/main/src/fst/transcriptions/transcriptor-numbers-digit2text.lexc)</small>

---

# tools-grammarcheckers-grammarchecker.cg3.md 


[ L A N G U A G E ]  G R A M M A R   C H E C K E R

# DELIMITERS

# TAGS AND SETS

## Tags

This section lists all the tags inherited from the fst, and used as tags
in the syntactic analysis. The next section, **Sets**, contains sets defined
on the basis of the tags listed here, those set names are not visible in the output.

### Beginning and end of sentence
BOS
EOS

### Parts of speech tags

N
A
Adv
V
Pron
CS
CC
CC-CS
Po
Pr
Pcle
Num
Interj
ABBR
ACR
CLB
LEFT
RIGHT
WEB
PPUNCT
PUNCT

COMMA
¶

### Tags for POS sub-categories

Pers
Dem
Interr
Indef
Recipr
Refl
Rel
Coll
NomAg
Prop
Allegro
Arab
Romertall

### Tags for morphosyntactic properties

Nom
Acc
Gen
Ill
Loc
Com
Ess
Ess
Sg
Du
Pl
Cmp/SplitR
Cmp/SgNom Cmp/SgGen
Cmp/SgGen
PxSg1
PxSg2
PxSg3
PxDu1
PxDu2
PxDu3
PxPl1
PxPl2
PxPl3
Px

Comp
Superl
Attr
Ord
Qst
IV
TV
Prt
Prs
Ind
Pot
Cond
Imprt
ImprtII
Sg1
Sg2
Sg3
Du1
Du2
Du3
Pl1
Pl2
Pl3
Inf
ConNeg
Neg
PrfPrc
VGen
PrsPrc
Ger
Sup
Actio
VAbess

Err/Orth

### Semantic tags

Sem/Act
Sem/Ani
Sem/Atr
Sem/Body
Sem/Clth
Sem/Domain
Sem/Feat-phys
Sem/Fem
Sem/Group
Sem/Lang
Sem/Mal
Sem/Measr
Sem/Money
Sem/Obj
Sem/Obj-el
Sem/Org
Sem/Perc-emo
Sem/Plc
Sem/Sign
Sem/State-sick
Sem/Sur
Sem/Time
Sem/Txt

HUMAN

PROP-ATTR
PROP-SUR

TIME-N-SET

###  Syntactic tags

@+FAUXV
@+FMAINV
@-FAUXV
@-FMAINV
@-FSUBJ>
@-F<OBJ
@-FOBJ>
@-FSPRED<OBJ
@-F<ADVL
@-FADVL>
@-F<SPRED
@-F<OPRED
@-FSPRED>
@-FOPRED>
@>ADVL
@ADVL<
@<ADVL
@ADVL>
@ADVL
@HAB>
@<HAB
@>N
@Interj
@N<
@>A
@P<
@>P
@HNOUN
@INTERJ
@>Num
@Pron<
@>Pron
@Num<
@OBJ
@<OBJ
@OBJ>
@OPRED
@<OPRED
@OPRED>
@PCLE
@COMP-CS<
@SPRED
@<SPRED
@SPRED>
@SUBJ
@<SUBJ
@SUBJ>
SUBJ
SPRED
OPRED
@PPRED
@APP
@APP-N<
@APP-Pron<
@APP>Pron
@APP-Num<
@APP-ADVL<
@VOC
@CVP
@CNP
OBJ
<OBJ
OBJ>
<OBJ-OTHERS
OBJ>-OTHERS
SYN-V
@X

## Sets containing sets of lists and tags

This part of the file lists a large number of sets based partly upon the tags defined above, and
partly upon lexemes drawn from the lexicon.
See the sourcefile itself to inspect the sets, what follows here is an overview of the set types.

### Sets for Single-word sets

INITIAL

### Sets for word or not

WORD
NOT-COMMA

### Case sets

ADLVCASE

CASE-AGREEMENT
CASE

NOT-NOM
NOT-GEN
NOT-ACC

### Verb sets

NOT-V

### Sets for finiteness and mood

REAL-NEG

MOOD-V

NOT-PRFPRC

### Sets for person

SG1-V
SG2-V
SG3-V
DU1-V
DU2-V
DU3-V
PL1-V
PL2-V
PL3-V

### Pronoun sets

### Adjectival sets and their complements

### Adverbial sets and their complements

### Sets of elements with common syntactic behaviour

### NP sets defined according to their morphosyntactic features

### The PRE-NP-HEAD family of sets

These sets model noun phrases (NPs). The idea is to first define whatever can
occur in front of the head of the NP, and thereafter negate that with the
expression **WORD - premodifiers**.

### Border sets and their complements

### Grammarchecker sets

* * *

<small>This (part of) documentation was generated from [tools/grammarcheckers/grammarchecker.cg3](https://github.com/giellalt/lang-cwd/blob/main/tools/grammarcheckers/grammarchecker.cg3)</small>

---

# tools-tokenisers-tokeniser-disamb-gt-desc.pmscript.md 

# Tokeniser for cwd

Usage:
```
$ make
$ echo "ja, ja" | hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
$ echo "Juos gorreválggain lea (dárbbašlaš) deavdit gáibádusa boasttu olmmoš, man mielde lahtuid." | hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
$ echo "(gáfe) 'ja' ja 3. ja? ц jaja ukjend \"ukjend\"" | hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
$ echo "márffibiillagáffe" | hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
```

Pmatch documentation:
<https://github.com/hfst/hfst/wiki/HfstPmatch>

Characters which have analyses in the lexicon, but can appear without spaces
before/after, that is, with no context conditions, and adjacent to words:
* Punct contains ASCII punctuation marks
* The symbol after m-dash is soft-hyphen `U+00AD`
* The symbol following {•} is byte-order-mark / zero-width no-break space
`U+FEFF`.

Whitespace contains ASCII white space and
the List contains some unicode white space characters
* En Quad U+2000 to Zero-Width Joiner U+200d'
* Narrow No-Break Space U+202F
* Medium Mathematical Space U+205F
* Word joiner U+2060

Apart from what's in our morphology, there are
1. unknown word-like forms, and
2. unmatched strings
We want to give 1) a match, but let 2) be treated specially by
`hfst-tokenise -a`
Unknowns are made of:
* lower-case ASCII
* upper-case ASCII
* select extended latin symbols
ASCII digits
* select symbols
* Combining diacritics as individual symbols,
* various symbols from Private area (probably Microsoft),
so far:
* U+F0B7 for "x in box"

## Unknown handling
Unknowns are tagged ?? and treated specially with `hfst-tokenise`
hfst-tokenise --giella-cg will treat such empty analyses as unknowns, and
remove empty analyses from other readings. Empty readings are also
legal in CG, they get a default baseform equal to the wordform, but
no tag to check, so it's safer to let hfst-tokenise handle them.

Finally we mark as a token any sequence making up a:
* known word in context
* unknown (OOV) token in context
* sequence of word and punctuation
* URL in context

* * *

<small>This (part of) documentation was generated from [tools/tokenisers/tokeniser-disamb-gt-desc.pmscript](https://github.com/giellalt/lang-cwd/blob/main/tools/tokenisers/tokeniser-disamb-gt-desc.pmscript)</small>

---

# tools-tokenisers-tokeniser-gramcheck-gt-desc.pmscript.md 

# Grammar checker tokenisation for cwd

Requires a recent version of HFST (3.10.0 / git revision>=3aecdbc)
Then just:
```
$ make
$ echo "ja, ja" | hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
```

More usage examples:
```
$ echo "Juos gorreválggain lea (dárbbašlaš) deavdit gáibádusa boasttu olmmoš, man mielde lahtuid." | hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
$ echo "(gáfe) 'ja' ja 3. ja? ц jaja ukjend \"ukjend\"" | hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
$ echo "márffibiillagáffe" | hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
```

Pmatch documentation:
<https://github.com/hfst/hfst/wiki/HfstPmatch>

Characters which have analyses in the lexicon, but can appear without spaces
before/after, that is, with no context conditions, and adjacent to words:
* Punct contains ASCII punctuation marks
* The symbol after m-dash is soft-hyphen `U+00AD`
* The symbol following {•} is byte-order-mark / zero-width no-break space
`U+FEFF`.

Whitespace contains ASCII white space and
the List contains some unicode white space characters
* En Quad U+2000 to Zero-Width Joiner U+200d'
* Narrow No-Break Space U+202F
* Medium Mathematical Space U+205F
* Word joiner U+2060

Apart from what's in our morphology, there are
1) unknown word-like forms, and
2) unmatched strings
We want to give 1) a match, but let 2) be treated specially by hfst-tokenise -a
* select extended latin symbols
* select symbols
* various symbols from Private area (probably Microsoft),
so far:
* U+F0B7 for "x in box"

TODO: Could use something like this, but built-in's don't include šžđčŋ:

Simply give an empty reading when something is unknown:
hfst-tokenise --giella-cg will treat such empty analyses as unknowns, and
remove empty analyses from other readings. Empty readings are also
legal in CG, they get a default baseform equal to the wordform, but
no tag to check, so it's safer to let hfst-tokenise handle them.

Finally we mark as a token any sequence making up a:
* known word in context
* unknown (OOV) token in context
* sequence of word and punctuation
* URL in context

* * *

<small>This (part of) documentation was generated from [tools/tokenisers/tokeniser-gramcheck-gt-desc.pmscript](https://github.com/giellalt/lang-cwd/blob/main/tools/tokenisers/tokeniser-gramcheck-gt-desc.pmscript)</small>

---

# tools-tokenisers-tokeniser-tts-cggt-desc.pmscript.md 

# TTS tokenisation for smj

Requires a recent version of HFST (3.10.0 / git revision>=3aecdbc)
Then just:
```sh
make
echo "ja, ja" \
| hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
```

More usage examples:
```sh
echo "Juos gorreválggain lea (dárbbašlaš) deavdit gáibádusa \
boasttu olmmoš, man mielde lahtuid." \
| hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
echo "(gáfe) 'ja' ja 3. ja? ц jaja ukjend \"ukjend\"" \
| hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
echo "márffibiillagáffe" \
| hfst-tokenise --giella-cg tokeniser-disamb-gt-desc.pmhfst
```

Pmatch documentation:
<https://kitwiki.csc.fi/twiki/bin/view/KitWiki/HfstPmatch>

Characters which have analyses in the lexicon, but can appear without spaces
before/after, that is, with no context conditions, and adjacent to words:
* Punct contains ASCII punctuation marks
* The symbol after m-dash is soft-hyphen `U+00AD`
* The symbol following {•} is byte-order-mark / zero-width no-break space
`U+FEFF`.

Whitespace contains ASCII white space and
the List contains some unicode white space characters
* En Quad U+2000 to Zero-Width Joiner U+200d'
* Narrow No-Break Space U+202F
* Medium Mathematical Space U+205F
* Word joiner U+2060

Apart from what's in our morphology, there are
1) unknown word-like forms, and
2) unmatched strings
We want to give 1) a match, but let 2) be treated specially by hfst-tokenise -a
* select extended latin symbols
* select symbols
* various symbols from Private area (probably Microsoft),
so far:
* U+F0B7 for "x in box"

TODO: Could use something like this, but built-in's don't include šžđčŋ:

Simply give an empty reading when something is unknown:
hfst-tokenise --giella-cg will treat such empty analyses as unknowns, and
remove empty analyses from other readings. Empty readings are also
legal in CG, they get a default baseform equal to the wordform, but
no tag to check, so it's safer to let hfst-tokenise handle them.

Needs hfst-tokenise to output things differently depending on the tag they get

* * *

<small>This (part of) documentation was generated from [tools/tokenisers/tokeniser-tts-cggt-desc.pmscript](https://github.com/giellalt/lang-cwd/blob/main/tools/tokenisers/tokeniser-tts-cggt-desc.pmscript)</small>
