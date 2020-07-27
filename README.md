# Project RBZ: Resourcing RBZ for NLP

This is the Github page for my PhD research "Sentiment Analysis for Arabizi on Social Media" where we publicise the outcome resources of the project. Visit the [webpage](https://tahatobaili.github.io/project-rbz/) for more details and content about the project.


## Introduction

Arabizi is the name given to a new social transcription of the spoken Arabic in Latin script. The term comes from the portmanteau of <em>Araby</em> (Arabic) and <em>Englizi</em> (English).
It is an informal written language where Arabs transcribe their dialectal mother tongue in text using Latin alphanumeral instead of Arabic script. For example حبيبي Ḥabībī <em>my-love</em> could be transcribed as
<em>7abibi</em> in Arabizi. 

Arabizi is extremely low resourced for Natural Language Processing (NLP), in this research we focus on resourcing Lebanese dialect Arabizi for sentiment analysis, an NLP classification task of
text into classes of positive, negative, or neutral automatically. However the nature of the Arabizi scripture poses many challenges for sentiment classification, such that it is highly sparse and codeswitched,
meaning words could have a large number of forms, whether orthographic or morphologic, or mixed with words of other languages such as French or English.

Arabic is also a phonetically-rich language containing short and long vowels, soft and emphasised consonants, and guttural phonemes such that transcribing it in Latin script, a relatively phonetically-poor language,
generates severe word ambiguities that it becomes difficult to transliterate to Arabic. For that, one Arabizi word could easily map to several Arabic words of different meanings. We appreciated the fact that Arabizi
is a social language and resourced it independently without attempting to transliterate it to Arabic.

Read more in-depth about the challenges of Arabizi for sentiment classification and transliteration [here](https://towardsdatascience.com/sentiment-analysis-for-low-resourced-languages-on-social-media-128bf01f2547).  

## Resources

Find the following files in the resources directory.

### [Arabizi Identification in Twitter Data (2016)](https://www.aclweb.org/anthology/P16-3008.pdf)

In this paper we present a pilot study about the percentage of Arabizi usage on Twitter across Lebanon and Egypt.
We also describe our approach of training a classifier that identifies Arabizi from other Latin script languages.

This file contains two 5k tweets annotated datasets (Arabizi/Not Arabizi) from Lebanon and Egypt.

### [SenZi: A Sentiment Analysis Lexicon for the Latinised Arabic (2019)](https://www.aclweb.org/anthology/R19-1138.pdf)

In this paper we present the outcomes of the work: SenZi, the new Lebanese dialect Arabizi sentiment lexicon, sentiment annotated datasets, and a Facebook corpus.
We then detail our approach in expanding every sentiment word in SenZi to match with its inflectional and orthgraphic variants automatically using word embeddings jointly with
a simple rule-based technique. 

This file contains:

* SenZi: The original sentiment lexicon consisting of 2K sentiment words.
* Senzi Expanded: Orthographically and morphologically rich sentiment lexicon cosisting of 25K sentiment words.
* Datasets: Arabizi/Not-Arabizi 4.4K tweets, and sentiment (positive/negative) 1.6K tweets annotated datasets.
* Corpus: 1M Arabizi comments extracted from 47 public facebook pages.
* Embeddings: Word2vec and Fasttext word embeddings spaces trained on a filtered corpus.

## Contact

Have any questions? (Get in touch)[https://tahatobaili.github.io/].
