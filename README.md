Translated TACRED (The TAC Relation Extraction Dataset)
============================
Version 1.0 (September 04, 2021)
----------------------------------

This bundle contains 533 parallel examples sampled from [TACRED](https://nlp.stanford.edu/projects/tacred/), translated into Russian and Korean (and 3 additional examples in Russian), accompanied with tranlsation of a list of trigger words collected for the different relations. 

Translation of TACRED:
-----------------------

We sampled the TACRED training set so that approximately 25\% of the examples are labeled as *no_relation* (in TACRED, 79.5\% are labeled as such) and the other 75\% are proportionally distributed between various relation types. The examples were translated using the [Yandex](https://translate.yandex.com) and [Papago](https://papago.naver.com) Translate APIs for Russian and Korean, respectively and were manually filtered and corrected by [Dmitry Nikolaev](https://github.com/macleginn) (in Russian) and [Taelin Karidi](https://github.com/tai314159) (in Korean). They then manually annotated the entity spans of the relation participants corresponding to those identified annotated in English source sentences. The resulting Russian and Korean RE datasets consist of 533 parallel examples in both languages (and 3 additional examples in Russian), thus providing us with parallel, automatically translated, and manually curated and annotated RE datasets.

Annotation:
-----------

TACRED is annotated with [Stanford Dependencies](https://nlp.stanford.edu/software/stanford-dependencies.html), which are not designed to be cross-lingual, thus, we use the [Trankit](https://github.com/nlp-uoregon/trankit) supervised parser for parsing the datasets in [Universal Dependencies](https://universaldependencies.org/) using the default provided pre-trained models. The resulting parses were checked and manually corrected by the annotators.

Trigger Words:
-----------

Several Relation Extraction works consults a list of trigger words collected for the different relations [Yu et al., 2015](https://aclanthology.org/N15-1126/). We translate these trigger words to Korean and Russian in two ways. First, we automatically translate the entire word list using an automated machine translating system (Google Translate). This is not always sufficient, as in many cases there are multiple ways to translate a given trigger word. To remedy this, when annotating the translated TACRED subsample, we also record the spans of the trigger words in the translated sentences that correspond to those in the original English sentences.

Format and Source Code:
----------------------

The files are in [CoNNL-U](https://universaldependencies.org/format.html) format, with metadata fields for the entities spans, types and trigger words. The _docid_ and _id_ fields of each example are the same as the original English TACREd example.


Citation:
---------
```
@inproceedings{arviv2021relation,
    title = "On the Relation between Syntactic Divergence and Zero-Shot Performance",
    author = "Ofir Arviv and Dmitry Nikolaev and Taelin Karidi and Omri Abend",
    booktitle = "Proceedings of the 2021 Conference on Empirical Methods in Natural Language Processing (EMNLP)",
    month = nov,
    year = "2021",
    publisher = "Association for Computational Linguistics",
    url = "https://arxiv.org/abs/2110.04644",
}
```



Licensing:
----------

The translated TACRED is distributed under the 
"Attribution-ShareAlike 3.0 Unported" license (http://creativecommons.org/licenses/by-sa/3.0/).
Please follow the link for exact details.
