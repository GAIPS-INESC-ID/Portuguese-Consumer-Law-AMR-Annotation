# Portuguese-Consumer-Law-AMR-Annotation
This repository contains a dataset of 350 sentences of the Portuguese Consumer Law annotated in AMR (Abstract Meaning Representation) by Linguistic Experts

This readme presents the categories (tags) used in annotating abstract semantic representations of legal texts, and was developed within the NLP-LAW project. This tagset is an adaptation of AMR (Banarescu et al. 2013, 2019) to the specific settings of this project as well as to some specificities of the Portuguese language. A detailed set of guidelines (to appear) complements this short document and should be consulted for further information.

**1, Spans**

**Named entities**

TREF: anaphoric textual references;

LREF: absolute legal references;

URL: idem;

NE ADM: named administrative body, irrespective of its hierarchical level in public administration and nature; 

NE ORG: named organization, irrespective of its nature (political, religious, economical, etc.), and excluding any administrative body;

NE OFFICE: person named by the respective office; 

**Time expressions**

TIME DATE ABS[olute]: an absolute date, irrespective of its granularity, that constitute an adequate answer to the interrogative quando? ‘when?’;

TIME DATE REL[ative] ENUNC[iation]: an anaphoric relative date, requiring temporal anaphora resolution, defined from the moment of enunciation (in legal texts, this is usually the date of publication of the legal act);

TIME DATE REL[ative] TEXT: an anaphoric relative date, requiring temporal anaphora resolution, defined from some moment previously mentioned in the text;

TIME DURATION: duration time expressions, which constitute an adequate answer to the interrogative (durante) quanto tempo? ‘for how long/much time?’;

TIME FREQUENCY: frequency time expressions, which constitute adequate answer to the interrogative com que frequˆencia? ‘how frequently?’;


**Multiword expressions (MWE)**

MWE-NUM: spans of tokens with the general value of numerals; includes (compound) cardinal, ordinal fractional and multiplicative numerals;

UNIT: Units of measurement of measurable quantities; includes percentage (%).

MWE-V-IDIOM: indicates a string element (usually involving a verb) forming an idiomatic expression; this span can include more than one graphic word; 

MWE-CONT: marks the second part of the elements of a discontinuous multiword idiom.


**2. Syntactic-semantic relations**

MAIN: connects the root node to the top predicative element of the sentence;

**Auxiliaries**

VAUX : links an auxiliary verb (Vaux) to the main verb on which it directly operates; chains of auxiliaries are recursively annotated; the prepositions of the Vaux construction are linked by the MWE-CONT relation;

VSUP: Support verbs (Vsup) are auxiliary elements of predicate nouns. The VSUP relation links the Vsup to the predicate noun it constructs;

VOP (along with subtypes VOPC and VOPL):  links an operator-verb (Vop) to the predicate noun of a base support-verb construction (SVC); causal (VOPC) and linking (VOPL) Vop further specify whether the Vop conveys either a causal meaning between the Vop’s subject and the predicate noun or no specific meaning and just reordering of the base support-verb and predicate noun elements.


**Parataxis/Hipotaxis**

APPOS: Covers several types of appositive relations, here interpreted as a type of parataxis. Simply put, the APPOS relation connects a nominal apposite to its antecedent;

COORD1, COORD2, . . . COORDn: links the coordinative conjunction to the main operator of each coordinated element;

OP1, OP2, . . . OPN: an auxiliary relation to help represent the underspecified relations between an operator and its arguments, namely for prepositions and conjunctions;

ING: links the verb of a gerundive subordinate clause (in the gerund) to the main predicative element of the sentence or clause on which it depends;

**Argumental relations**

ARG0: Links a predicative element to its subject-argument in the base-construction; typically, an agent of an action or the the experiencer of a state (the so-called agentive complement in a passive sentence is linked by ARG0-OF).

ARG1: Links a predicative element to its argument-first complement in the base-construction; typically, the object or the patient of an action (in passive constructions, where the subject is the ARG1);

ARG2: links a predicative element to its argument-second complement in the base-construction; typically, in a transfer predicate, the recipient or, in a communication predicate the interlocutor;

ARG3, ARG4, ARG5, ARGN: l inks a predicative element to its remaining arguments

ARGi-OF: in a restrictive relative subordinate sentence, links the antecedent of a relative pronoun to the predicative element on which that pronoun directly depends (the index i represents the same concept of semantic roles as in the previous cases);

POSS: Links the noun to the possessive pronoun that determines it; only possession (including inalienable possession, involving part-of-body nouns) relations are considered, relating concrete nouns;

CORREF: links an explicit anaphoric element (for example, a personal pronoun, a demonstrative or a deictic adverbial) to its antecedent;

CONSIST-OF links a noun to its substance/material complement;

DEGREE: links a predicative element to quantification (intensive) adverbial expressions;

QUANT: Links a given noun to any determinative elements, particularly numerical quantifiers determining that noun;

AGE: links a temporal expression indicative of idade ‘age’, to the noun that this expression predicates (in the absence of the predicative noun idade , or another synonym);


**Modality and polarity**

PODER (NLP-LAW-specific); links the modal auxilkiary verb poder ‘may/can’ to the full verb it auxiliates;

DEVER (NLP-LAW-specific); links the modal auxilkiary verb dever should/ought/must’ to the full verb it auxiliates;

NEG: links a negation adverb to the predicative element it modifies;


**Non-argumental/circumstantial semantic roles**

BENEFICIARY:	connects a predicative element to a benefactive complement, that is, the entity that benefits from the action expressed by an operator (NB: and which is not its argument);

CAUSE: connects a predicative element to the connector (preposition or conjunction) of the causative complement; in the case of Vopc, links this element to its subject;

COMMITATIVE: links a predicative element to a complement of a nonargumental nature with companion meaning (comitative); (NB: excludes the arguments of symmetrical predicates); 

COMPARED-TO: links the comparative conjunction (como ‘like, as’, do que ‘than’) to the predicative element of the main clause.

CONCESSION: links the subordinating concessive conjunction/preposition (embora, apesar de, conquanto, ainda que, etc.) to the predicative element in the main clause;

CONDITION: links the conditional subordinating conjunction/preposition (se, no caso de, caso, etc. ’if’ ) to the predicative element of the main clause; 

CONFORMAT	links the conformative subordinating conjunction/preposition (consoante, conforme, à medida que, etc. ’according to, conform to, as,’) to the predicative element of the main clause;

CONSEQUENCE: links the subordinating conjunction/preposition (tanto que, tal que, de forma que, de maneira que, de modo que, de sorte que, que (consecutive), etc. ‘so that, such that, in such a way that’) to the predicative element of the main clause;

DURATION: links a predicate to an adverbial complement of time-duration (not a clause); 

EXCEPTION: links the exceptive subordinating conjunction/preposition (a não ser (que), à/com_a exceção de, aparte, exceto, fora, menos, salvo, salvo se, etc.’unless, except for, apart from, save, except if’) to the predicative element of the main clause;

FOCUS: links a focus adverb to the element it focalizes;

FREQUENCY: links a predicate to an adverbial complement of time-frequency (not a clause); 

INSTRUMENT	Connects a predicative element to an instrumental complement (NB: excludes medium); 

MANNER: Connects a predicative element to the nucleus of a manner complement (NB:not to be confused with INSTRUMENT and MEDIUM); manner adverbs are directly linked to this element; includes point-of-view adverbs;

MEDIUM: connects a predicative element to an instrumental complement hat designates a medium (cp. INSTRUMENT), e.g. by fax; 

MOD: (umbrella-tag) establishes a generic syntactic-semantic relation of modifier between two elements or between two constituents, provided that this relation is not already represented in one of the previous relations. The relation is oriented from the modified (head) element to the modifier element; includes non-predicative (mostly classifying) adjectives, non-quantifying determiners;

MWE-CONT: links the two parts of a discontinuous MWE;

PURPOSE: links the finality subordinating conjunction/preposition (a fim de, para, para que,  com vista a, para fins de, etc.) to the predicative element of the main clause;

TIME; links the temporal subordinating conjunction/preposition (quando, enquanto, depois que, até que, desde que, cada vez que, todas as vezes que, antes que, sempre que, logo que, mal, etc. ‘when, while, after, until, since, every time, before, whenever, as soon as, etc.’) with a time-date  value to the predicative element of the main clause; time adverbs are directly linked to this element;

TOPIC: Connects a predicative element to a topic complement value (usually introduced by prepositions acerca de, sobre, relativamente a, em relação a ‘about’). 


**References**
Banarescu, L., Bonial, C., Cai, S., Georgescu, M., Griffitt, K., Hermjakob, U., Knight, K., Koehn, P., Palmer, M., Schneider, N.: Abstract meaning representation for sembanking. In: Proceedings of the 7th Linguistic Springer Nature 2021 LATEX template 22 AMR for Legal Texts - Guidelines Annotation Workshop and Interoperability with Discourse, pp. 178–186 (2013) 

Banarescu, L., Bonial, C., Cai, S., Georgescu, M., Griffitt, K., Hermjakob, U., Knight, K., Koehn, P., Palmer, M., Schneider, N.: Abstract Meaning Representation (AMR) 1.2.6 Specification”, (2019). https://github.com/amrisi/amr-guidelines
