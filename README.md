# Summary

UD_Middle_French-PROFITEROLE is the Middle French section of the PROFITEROLE corpus, the Old French section is UD_OLD_FRENCH-PROFITEROLE.

# Description

UD_Middle_French-PROFITEROLE includes Middle French texts that were annotated during the PROFITEROLE funded project (Projet ANR- 16-CE38-0010, 2017-2022; supervised by Sophie Prévost; https://www.lattice.cnrs.fr/projets/projets-passes/projets-anr/projet-anr-profiterole)
Texts were automatically annotated with part-of-speech and dependencies (with the SRCMF corpus <srcmf.org> as a training corpus), and are currently running a process of correction. 
Texs will be released in UD as they are corrected.
Old French texts that were annotated in the PROFITEROLE project are to be found in UD_Old_French-PROFITEROLE.

Main development happens on the [GitLab of the Profiterole Project](https://gitlab.huma-num.fr/profiterole/srcmf-ud).

# Introduction

UD_Middle_French-PROFITEROLE is meant to include texts spanning from the early 14th to the late 15th C. 
At the present it includes 3 (extracts of) texts dating from the late 14th and from the late 15th C. 
It includes XXX sentences and XXX tokens.

Sentences are annotated with the following metadata:

- `sent_id` : a unique id for each sentence in the treebank
- `text` : the sentence
- `newdoc_id` : a unique id for each of the texts. This id can be split on underscores to get back :
  - name of the text
  - date
  - form : verse and/or prose


The following table lists the texts used in this treebank [A REMETTRE DANS L'ORDRE CHRONOLOGIQUE]:

| ID                            | Name of the text       |       Author        | Tokens | Trees |
| :---------------------------- | :--------------------- | :-----------------: | -----: | ----: |
| grchronj2c5_1381_prose        | Chroniques des règnes de Jean II et de Charles V|      anonymous      | 2710 | 103 |
| Jehpar_1494_prose             | jehan de Paris         |      anonymous        | 5893 | 291 |
| Commyn_1497_prose             | Mémoires, Livre 1      |  Philippe de Commynes | 3422 | 118 |

| Total                         |                        |                       | 12025 | 512 |

# Structure

Texts with less than about 40,000 words were entirely annotated, while texts
with more than 40,000 words were sampled in three parts (beginning, middle and end of the text) to
reach a total amount of about 40000 words.

At the moment, UD_Middle_French-PROFITEROLE includes 3 extracts of full texts, the remainig parts of which will be released in May 2024.

The treebank is currently not split.
.. as follows (in number of tokens) :
# Deviations from UD

We added some more specific relations (subtypes), either to specify a relation, or in the case of tokens entering a double dependency relation (typically : relative pronouns and  contracted forms) :

- `acl:relcl` : relative clause
- `advmod:obl` : contracted `advmod` + `obl` (e.g. _sin_ = _si_ + _en_)
- `aux:pass` : passive auxiliary
- `case:det` : contracted `case` + `det` (e.g. _del_ = _de_ + _le_)
- `cc:nc` : non coordinating conjunction (e.g. _et_ at the beginning of a sentence)
- `mark:advmod` : `mark` and `advmod` (e.g. _coment_ at the beginning of a subordinate clause)
- `nsubj:advmod` : contracted `nsubj` + `advmod` (e.g. _jon_ = _jo_ + _en_)
- `nsubj:obj` : contracted `nsubj` + `obj` (e.g. _quil_ = _qui_ + _le_)
- `obj:advmod` : contracted `advmod` + `obj` (e.g. _sis_ = _si_ + _les_)
- `obj:advneg` : contracted `negation` + `obj` (e.g. _nes_ = _ne_ + _les_)
- `obj:obl` : contracted `obl` + `obj` (e.g. _oul_ = _ou_ + _le_)
- `obl:advmod` : the double labelling accounts for the difficulty to decide between obl and advmod
  relations (`en` and `i`).

We added some features:

- `Morph=VFin` : finite verb
- `Morph=VInf` : non-finite verb
- `Morph=VPar` : verbal participle

Consult [the language specific documentation](http://universaldependencies.org/fro/dep/index.html)
for further details.

# Acknowledgments

UD_Middle_French-PROFITEROLE results from the automatic annotation (PROFITEROLE project, 2017-2022) of Middle French texts (with the PROFITEROLE/SRCMF Old French corpus being used as a training corpus), which were/are then manually corrected along with the UD guidelines. 
The contributors to the syntactic part of the PROFITEROLE project were: Prévost, Sophie; Villemonte de la Clergerie, Eric; Regnault, Mathilde; Grobol, Loïc; Crabbé, Benoît; Dehouck, Mathieu; Lavrentiev, Alexei.

## References

- Prévost, Sophie, Mathieu Dehouck, Alexei Lavrentiev, Serge Heiden et Loïc Grobol. To appear. ['Profiterole : un corpus morpho-syntaxique et syntaxique de français médiéval'], Corpus


# Changelog

* 2023-11-15 v2.13
  * Initial release in Universal Dependencies.

* 2022-05-15 v2.10
  * Initial repository creation in Universal Dependencies.


<pre>
=== Machine-readable metadata (DO NOT REMOVE!) ================================
Data available since: UD v2.13
License: CC BY-NC-SA 4.0
Includes text: yes
Genre: fiction nonfiction
Lemmas: manual native
UPOS: converted with corrections
XPOS: manual native
Features: automatic
Relations: automatic with corrections
Contributors: Prévost, Sophie; Villemonte de la Clergerie, Eric; Regnault, Mathilde; Grobol, Loïc; Crabbé, Benoît; Dehouck, Mathieu; Lavrentiev, Alexei.
Contributing: elsewhere
Contact: sophie.prevost@ens.psl.eu
===============================================================================
</pre>
