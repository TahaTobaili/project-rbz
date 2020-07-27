---
title: Project RBZ
layout: default
---

# Sentiment Analysis for Arabizi on Social Media

Author: [Taha Tobaili](https://tahatobaili.github.io/){:target="_blank"}, PhD candidate, [Knowledge Media Institute (KMi)](http://kmi.open.ac.uk/){:target="_blank"}.  
Sytem Developer: [Chris Sanders](http://kmi.open.ac.uk/people/member/chris-sanders){:target="_blank"}, KMi.  
Supervisors: [Miriam Fernandez](http://people.kmi.open.ac.uk/miriam-fernandez/){:target="_blank"} and [Harith Alani](http://people.kmi.open.ac.uk/harith/){:target="_blank"}, KMi.  
Contributors: [Rania Islambuli](https://people.epfl.ch/rania.islambouli?lang=en){:target="_blank"}, [Omar Farhat](https://www.linkedin.com/in/omar-farhat-2aa689102/){:target="_blank"}, and [Omar Osman](https://www.linkedin.com/in/omar-osman/){:target="_blank"}, computer science graduates, Lebanese American University.

## Introduction

Arabizi is the name given to a new social transcription of the spoken Arabic in Latin script. The term comes from the portmanteau of <em>Araby</em> (Arabic) and <em>Englizi</em> (English).
It is an informal written language where Arabs transcribe their dialectal mother tongue in text using Latin alphanumeral instead of Arabic script. For example حبيبي Ḥabībī <em>my-love</em> could be transcribed as
<em>7abibi</em> in Arabizi. 

Arabizi is extremely low resourced for Natural Language Processing (NLP), in this research we focus on resourcing Lebanese dialect Arabizi for sentiment analysis, an NLP classification task of
text into classes of positive, negative, or neutral automatically. However the nature of the Arabizi scripture poses many challenges for sentiment classification, such that it is highly sparse and codeswitched,
meaning words could have a large number of forms, whether orthographic or morphologic, or mixed with words of other languages such as French or English.

Arabic is also a phonetically-rich language containing short and long vowels, soft and emphasised consonants, and guttural phonemes such that transcribing it in Latin script, a relatively phonetically-poor language,
generates severe word ambiguities that it becomes difficult to transliterate to Arabic. For that, one Arabizi word could easily map to several Arabic words of different meanings. We appreciated the fact that Arabizi
is a social language and resourced it independently without attempting to transliterate it to Arabic. Read more in-depth about the challenges of Arabizi for sentiment classification and transliteration in the link below.  

{% include article.html %}

## Timeline

We kicked off the research by a pilot study quantifying Arabizi on Twitter across two different Arab regions, and discovered language identification features that could be used in training a classifier to identify Arabizi
from non-Arabizi text. From this point onwards, our goal was to create a new sentiment lexicon and evaluation datasets, however the main challenge was mapping sentiment words with their inflectional and orthographic variants.
The deeper we ingressed into the study the more we realised how challenging this was. Hence the research was more applied than theoretical, we kept trying different approaches, failing relentlessly, but slowly paving the way
for a sucessful approach at the end:

{% include timeline.html %}

## Presentation

I presented my work to the lab during the early stages of the PhD. In this talk I described some of the challenges for processing Arabizi and the development of the sentiment annotated dataset:

{% include video.html %}
  

# Resources

## [Arabizi Identification in Twitter Data (2016)](https://www.aclweb.org/anthology/P16-3008.pdf){:target="_blank"}

In this paper we present a pilot study about the percentage of Arabizi usage on Twitter across Lebanon and Egypt.
We also describe our approach of training a classifier that identifies Arabizi from other Latin script languages.

This file contains two 5k tweets annotated datasets (Arabizi/Not Arabizi) from Lebanon and Egypt.

{% include download.html filename = "arabizi-identification" %}

## [SenZi: A Sentiment Analysis Lexicon for the Latinised Arabic (2019)](https://www.aclweb.org/anthology/R19-1138.pdf){:target="_blank"}

In this paper we present the outcomes of the work: SenZi, the new Lebanese dialect Arabizi sentiment lexicon, sentiment annotated datasets, and a Facebook corpus.
We then detail our approach in expanding every sentiment word in SenZi to match with its inflectional and orthgraphic variants automatically using word embeddings jointly with
a simple rule-based technique. 

This file contains:

* SenZi: The original sentiment lexicon consisting of 2K sentiment words.
* Senzi Expanded: Orthographically and morphologically rich sentiment lexicon cosisting of 25K sentiment words.
* Datasets: Arabizi/Not-Arabizi 4.4K tweets, and sentiment (positive/negative) 1.6K tweets annotated datasets.
* Corpus: 1M Arabizi comments extracted from 47 public facebook pages.
* Embeddings: Word2vec and Fasttext word embeddings spaces trained on a filtered corpus.

{% include download.html filename = "senzi" %}

## Coming Soon

By far our work scratches the surface in addressing the lexical sparsity of Arabizi, we are currently working on a new approach that extracted 200K variants of the same sentiment words.
Our next direction would be to explore resourcing other low resourced languages with similar or new challenges.

# Appreciation

I would like to thank every individual who contributed to this project from producing datasets to developing and maintaining the data annotation system and especially my supervisors for their
continuous guidance and support.
  
If you find the resources useful and would like to appreciate the work or have any question, please drop [me](https://tahatobaili.github.io/){:target="_blank"} an email.  