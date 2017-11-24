LÂMPADA 2.0: Second HAREM Resource Package
--------------------------------------


1. Introduction
2. Package structure
3. Second HAREM organization
4. Collections
5. Evaluation programs
6. System runs
7. Differences relative to version 1.0
8. Acknowledgments
 

1. Introduction

This package can be downloaded from http://www.linguateca.pt/HAREM/PacoteRecursosSegundoHAREM.zip, and includes the main resources created in the scope of Second HAREM, a joint evaluation on named entity recognition in Portuguese organized by Linguateca and documented in Mota & Santos (2008).

It is distributed under the Creative Commons Licence 3.0, see https://creativecommons.org/licenses/by/3.0/ie/

2. Package structure

This package has three directories, corresponding to 4., 5. and 6. respectively.
coleccoes/ 
programas/
corridas/


3. Second HAREM organization
----------------------------

3.1 Organizers
HAREM is organized by Linguateca (http://www.linguateca.pt). 
People involved in the Second HAREM: Diana Santos, Cláudia Freitas, Hugo Gonçalo Oliveira, Paula Carvalho and Cristina Mota.

3.2 Second HAREM main dates
First call of participation: October, 2007
Submission period: April, 2008 
Official results: September, 2008

3.3 Documentation
The complete documentation of the Second HAREM, including the guidelines to all tracks, is available from: 
Cristina Mota & Diana Santos (eds.). Desafios na avaliação conjunta do reconhecimento de entidades mencionadas: O Segundo HAREM. Linguateca, 2008. http://www.linguateca.pt/LivroSegundoHAREM/

3.4 How to cite the present package
This package is available from http://www.linguateca.pt/HAREM/PacoteRecursosSegundoHAREM.zip 
and should be cited as "LÂMPADA - Second HAREM Resource Package" 


4. HAREM collection and golden collections
----------------------------------------------

4.1 HAREM collection
This collection, colSegundoHAREM.xml, contains a set of 1,040 documents in Portuguese (from Brazil and from Portugal) that the systems had to annotate in the Second HAREM. 

In colSegundoHAREM-meta.xml, we provide meta-data related to the source and kind of each text, uniquely identified by its DOC (document identification) value. Follows the explanation of the values used:

VARIANTE (language variety): PT (Portugal) or BR (Brazil)

TIPO_TEXTO (text type): the classification in text types is a rough indication of the text genre. In Second HAREM we used:
	- Notícia (news): facts and recent events. Most news have also associated the newspaper section they appeared in, in the attribute SECJORNAL under FONTE (source)
	- Didáctico (didactic): instructional texts, such as encyclopedia articles, course book snippets, state health instructions, etc.
	- Opinião (opinion): newspaper articles and (academic) essays. 
	- Blogue (blog): these texts also express opinions, but usually in a less formal style. Blogs are also subcategorized in "blogue pessoal" (personal blog), when the text is written in a personal register, "blogue jornalístico" (journalistic blog), when the text is close to a newspaper article, and "blogue humorístico" ("humoristic blogs"). 
	- Perguntas (questions): non-articulated texts; only (artificial) questions, specifically used for evaluation of question answering systems (QA@CLEF). 
	- Perguntas faq (FAQ): questions and answers found in Frequently Asked Questions webpages.
	- Entrevista (interview): consisting of dialogues
	- Legislativo (legal): legal text
	- Literário (literary): from literary works
	- Promocional (promotional): advertisements
	- Texto privado manuscrito (private manuscript)

FONTE (source): information about text origin/source.
	NOME encloses the publication channel: newspaper name, book title, site title, previous collections, etc.
	AUTOR the author when known
	DATA-CRIACAO indicates the publication date
	DATA-OBTENCAO indicates when the text was accessed
	REFERENCIA includes the URL
	TITULO encloses the name of the particular piece of text
	SECJORNAL contains the newspaper section to which the particular news belong: Cien_Tecn_Educ, COTIDIANO, Cultura, Desporto, Diversos, Economia, ESPORTE, FOLHATEEN, FOLHINHA, ILUSTRADA, Local, Mundo, Nacional/Brasil, Nacional/Portugal, OPINIÃO, REVISTA_DA_FOLHA, Sociedade, TURISMO, TV_FOLHA


4.2 Golden collections (GC)
Last revision: April 19th, 2010.

Second HAREM GC (CDSegundoHAREMReRelEM.xml): 129 documents from the HAREM collection whose named entities were manually annotated according to HAREM guidelines, and whose semantic relations between entities were also manually annotated according to the ReRelEM guidelines. Differently from the ReRelEM GC, included in the first package LAMPADA, the relations in this CD were annotated by only one annotator. Due to the larger volume of documents annotated, there were minor modifications to the types of relations, documented in http://www.linguateca.pt/aval_conjunta/HAREM/ListaMudancasDirectivasReRelEM.html.

TEMPO GC (CDSegundoHAREM_TEMPO.xml): 30 documents where the EM were also manually annotated according to the TEMPO guidelines for finer analysis and temporal normalization. This GC does not contain relations between EM.




These two collections may in addition contain comments signaled by the COMENT attribute, provided for further study. Follows a short description of the possible values of the COMENT attribute:

a) 2/3 -> the NE classification (category, type or subtype) was not assigned by consensus. Rather it was the result of a majority vote.
b) DUVIDA_DIRECTIVASTEMPO -> cases of TEMPO on which the annotators had doubts, generally because of different interpretations of the TEMPO guidelines (whose proposers, as Second HAREM participants, could not be invoked to clarify).
c) INDEP: concerning the ReRelEM track, it indicates that the relation marked by the annotators could not be inferred by the information given by the text.
d) futuro: also concerning the ReRelEM track, it indicates that the relation marked by the annotators will only become actualized in the future.


5. Evaluation programs
--------------------------
Version: April 21st, 2010.

5.1 Pre-requisites
- Any operating system that supports Java 1.6 or a more recent version.
- gawk (to evaluate extended TEMPO attributes).
- R 2.7.1 or a more recent version (to generate individual evaluation reports).

5.2 Installation
- Extract the content of this archive
- Invoke the programs through the directory named Av_HAREM_XML

5.3 Manual
- The manual in HTML (in Portuguese) can be found in the Av_HAREM_XML/docs directory
- Additional utilization examples and minimal compilation instructions can be found in programas/Readme_programas.txt

5.4 Licenses
All programs developed within HAREM are distributed under the BSD license (see programas/LICENSE.txt).
In addition, we distribute as well the following external programs, under the directory programas/externos, which have their own licenses
- Jdom (http://www.jdom.org), Apache-style open source license included in file LICENSE.txt in jdom-1.1.zip
- JGraph (http://www.jdom.org), LGPL license included in file LICENSE in jgraph-latest-lgpl-src.jar


5.5 SAHARA web service 
Note that the whole evaluation setup of Second HAREM is also available through the 
SAHARA Web service. Go to http://www.linguateca.pt/HAREM/, and, in the English interface, choose "Scorer" on the left-hand menu. ["Avaliador" in the Portuguese interface.]


6. Runs submitted to the Second HAREM
--------------------------------------

10 systems participated in the Second HAREM and each system could at most submit 4 runs. 
The runs made available in this package (under corridas/) are, for each system:

Cage2:
partic01_1_corr.xml
partic01_2_corr.xml
partic01_3_corr.xml
partic01_4_corr.xml

DobrEM:
partic03_1_corr.xml

PorTexTO:
partic06_1_corr.xml
partic06_2_corr.xml
partic06_3_corr.xml
partic06_4_corr.xml

Priberam:
partic07_1.xml

R3M:
partic09_1.xml
partic09_2.xml

REMBRANDT:
partic10_1.xml
partic10_2.xml
partic10_3_corr.xml

REMMA:
partic11_1_corr.xml
partic11_2_corr.xml
partic11_3_corr.xml

SEI-Geo:
partic13_1.xml
partic13_2.xml
partic13_3.xml
partic13_4.xml

SeRELeP:
partic15_1.xml

XIP-L2F/XEROX:
partic16_2.xml
partic16_3.xml


The filename identifies the number of the system (assigned by the organization), the number of the run, and the suffix "_corr" indicates that the run suffered minor changes (for example, change of character encoding or renaming of document ID).


7. Differences relative to version 1.0 of LÂMPADA (Second HAREM resource package)

- The root directory of the package is now lampada2.0.

- The Second HAREM GC now includes the annotation of semantic relations between entities (see 4.2) 

- The ReRelEM is not included anymore, since all relations are annotated in the Second HAREM GC.

- Inclusion of the list of relations in the Second HAREM GC with the triple format before (triplos_CDSegundoHAREM.txt) and after (triplos_expandidos_CDSegundoHAREM.txt) the expansion of relations.

- Modification in the program that invokes the complete evaluation sequence, Avaliacao.sh, which now uses the Second HAREM GC (instead of the ReRelEM GC) to do the ReRelEM evaluation.

- Inclusion of a program to remove from the golden collection the information about the normalization of TEMPO category and/or of ReRelEM (cdharem_retirainfo.pl).

- Correction of the following problems in the Second HAREM GC:

	a) Entities H2-dftre765-90, H2-dftre765-92, H2-dftre765-94, H2-dftre765-95 were re-annotated as vague entities, and, additionally received the classification of ORGANIZACAO INSTITUICAO.

	b) Entity hub-47914-2 was re-annotated as vague entity, and, additionally received the classification of PESSOA GRUPOMEMBRO.

	c) Entities hub-15590-201, hub-15590-205, hub-15590-78, hub-15590-87, hub-15590-69, hub-15590-124, hub-55847-344 and hub-55847-345 were re-annotated as vague entities, and additionally received the classification of ORGANIZACAO ADMINISTRACAO.

	d) Entities ric-74122-15 and ric-74122-16 had their type corrected, and are now OBRA REPRODUZIDA.

	e) Entities ric-58766-56 and ric-58766-62 were re annotated as vague entities, and additionally received the classification of ORGANIZACAO EMPRESA.

	f) In entities hub-66526-23, hub-66526-25 and hub-66526-545, it was specified the facet that participates in the relations with entity hub-66526-22 was specified.
	
	g) Entity hub-66526-21 (reis de Portugal) includes now two relations of inclusion with entities hub-66526-25 (D. Afonso Henriques) e hub-66526-545 (D. Sancho I).

	h) The attribute TIPOREL of entity hub-49343-32 was corrected from "local_nascimento" to "local_nascimento_de".

- Correction of the following problems in the TEMPO GC:

	i) The attribute VAL_DELTA of the following entities has now the value "A0M0S0D0H0M0S0": H2-Ren_2003_6465-178, aa58069-184, aa58069-432, aa56088-483, bob-14949-583, bob-14949-640, hub-16268-5, hub-16268-20, hub-71248-192, hub-41899-399, hub-41899-360, aa33715-460, hub-71248-4, hub-71248-5, hub-21881-182, hub-60382-125 and hub-51467-321.

- Correction of the following problems in the Second HAREM GC and TEMPO GC:

	j) Entities hub-71248-195, hub-71248-206, hub-71248-213 and hub-21881-184 were reclassified as PESSOA GRUPOMEMBRO, since their interviewing facet is being referred.

	k) Entities aa55968-499 and aa55968-500 were re annotated as vague entities, and additionally received the classification of PESSOA GRUPOMEMBRO.

	l) Entity hub-49343-22 was created for one of the segmentation alternatives of entity "rei D. Fernando de Nápolis", specifically for the alternative "rei D. Fernando".

	m) The facet OUTRO in the vague entity hub-94570-120 was re-annotated as ABSTRACCAO DISCIPLINA.
	
- In file colSegundoHAREM-meta.xml, the type of the text documents ric-85133 and ric-46546 was corrected from "opiniao" to "opinião".


8. Acknowledgments
------------------

Linguateca is jointly funded by the Portuguese Government and the European Union (FEDER and FSE) under contract ref. POSC/339/1.3/C/NAC, and by FCCN and by UMIC. 
We are grateful to Jorge Baptista, Caroline Hagège and Nuno Mamede for introducing the TEMPO track, to Nuno Cardoso for deploying SAHARA, and to Luís Miguel Cabral, Luís Costa and David Cruz for their support in several other tasks.
We also thank all Second HAREM participants for granting us permission to further distribute their runs. 


Date of the last update of this file: 10 September 2015

