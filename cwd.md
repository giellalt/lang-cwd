
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


Verb inflection
The Woods Cree language verbs inflect in persons.



Proper noun inflection
The Woods Cree language proper nouns inflect in the same cases as regular
nouns, but with a colon (':') as separator.



Adjective inflection
The Woods Cree language adjectives compare.



Noun inflection
The Woods Cree language nouns inflect in cases.




# Symbol affixes





=================================== !
The Woods Cree morphophonological/twolc rules file !
=================================== !








* *primus%>s*
* *primus00*


* examples:*

* examples:*


* examples:*

* examples:*
Verbs
Verbs in the Woods Cree language are actions.


Pronouns
Pronouns in the Woods Cree language are references to things.


Numerals
Numerals in the Woods Cree language are numbers.


Adjectives
Adjectives in the Woods Cree language describe things.


Prefixes
Prefixes in the Woods Cree language are bound to beginning of other words.



Nouns
Nouns in the Woods Cree language are things.



INTRODUCTION TO MORPHOLOGICAL ANALYSER OF Woods Cree LANGUAGE.


 # Definitions for Multichar_Symbols

## Analysis symbols
The morphological analyses of wordforms for the Woods Cree
language are presented in this system in terms of the following symbols.
(It is highly suggested to follow existing standards when adding new tags).

The parts-of-speech are:

The parts of speech are further split up into:

The Usage extents are marked using following tags:

The nominals are inflected in the following Case and Number

The possession is marked as such:
The comparative forms are:
Numerals are classified under:
Verb moods are:
Verb personal forms are:
Other verb forms are

 * +Symbol = independent symbols in the text stream, like £, €, ©
Special symbols are classified with:
The verbs are syntactically split according to transitivity:
Special multiword units are analysed with:
Non-dictionary words can be recognised with:

Question and Focus particles:


Semantics are classified with


Derivations are classified under the morphophonetic form of the suffix, the
source and target part-of-speech.


Morphophonology
To represent phonologic variations in word forms we use the following
symbols in the lexicon files:

And following triggers to control variation

## Flag diacritics
We have manually optimised the structure of our lexicon using following
flag diacritics to restrict morhpological combinatorics - only allow compounds
with verbs if the verb is further derived into a noun again:
 |  @P.NeedNoun.ON@ | (Dis)allow compounds with verbs unless nominalised
 |  @D.NeedNoun.ON@ | (Dis)allow compounds with verbs unless nominalised
 |  @C.NeedNoun@ | (Dis)allow compounds with verbs unless nominalised

For languages that allow compounding, the following flag diacritics are needed
to control position-based compounding restrictions for nominals. Their use is
handled automatically if combined with +CmpN/xxx tags. If not used, they will
do no harm.
 |  @P.CmpFrst.FALSE@ | Require that words tagged as such only appear first
 |  @D.CmpPref.TRUE@ | Block such words from entering ENDLEX
 |  @P.CmpPref.FALSE@ | Block these words from making further compounds
 |  @D.CmpLast.TRUE@ | Block such words from entering R
 |  @D.CmpNone.TRUE@ | Combines with the next tag to prohibit compounding
 |  @U.CmpNone.FALSE@ | Combines with the prev tag to prohibit compounding
 |  @P.CmpOnly.TRUE@ | Sets a flag to indicate that the word has passed R
 |  @D.CmpOnly.FALSE@ | Disallow words coming directly from root.

Use the following flag diacritics to control downcasing of derived proper
nouns (e.g. Finnish Pariisi -> pariisilainen). See e.g. North Sámi for how to use
these flags. There exists a ready-made regex that will do the actual down-casing
given the proper use of these flags.
 |  @U.Cap.Obl@ | Allowing downcasing of derived names: deatnulasj.
 |  @U.Cap.Opt@ | Allowing downcasing of derived names: deatnulasj.

The word forms in Woods Cree language start from the lexeme roots of basic
word classes, or optionally from prefixes:

















































% komma% :,      Root ;
% tjuohkkis% :%. Root ;
% kolon% :%:     Root ;
% sárggis% :%-   Root ; 
% násti% :%*     Root ; 




We describe here how abbreviations are in Woods Cree are read out, e.g.
for text-to-speech systems.

For example:

 * s.:syntynyt # ;  
 * os.:omaa% sukua # ;  
 * v.:vuosi # ;  
 * v.:vuonna # ;  
 * esim.:esimerkki # ; 
 * esim.:esimerkiksi # ; 



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
QMARK
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

HAB-ACTOR
HAB-ACTOR-NOT-HUMAN


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
REAL-WORD
REAL-WORD-NOT-ABBR
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








