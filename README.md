```yml
title: [Project RBZ]
description: [Resourcing RBZ for NLP]
```

# Project RBZ
## Resourcing RBZ for NLP

This is the Github page for my PhD research "Sentiment Analysis for Arabizi on Social Media" where we publicise the outcome resources of the project. 
Visit the [project page](https://tahatobaili.github.io/project-rbz/) online for more details and content about the project.


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

Read more in-depth about the challenges of Arabizi for sentiment classification and transliteration [here](https://towardsdatascience.com/sentiment-analysis-for-low-resourced-languages-on-social-media-128bf01f2547){:target="_blank"}.  

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


Additionally, you may choose to set the following optional variables:

```yml
show_downloads: ["true" or "false" to indicate whether to provide a download URL]
google_analytics: [Your Google Analytics tracking ID]
```

### Stylesheet

If you'd like to add your own custom styles:

1. Create a file called `/assets/css/style.scss` in your site
2. Add the following content to the top of the file, exactly as shown:
    ```scss
    ---
    ---

    @import "{{ site.theme }}";
    ```
3. Add any custom CSS (or Sass, including imports) you'd like immediately after the `@import` line

*Note: If you'd like to change the theme's Sass variables, you must set new values before the `@import` line in your stylesheet.*

### Layouts

If you'd like to change the theme's HTML layout:

1. [Copy the original template](https://github.com/pages-themes/architect/blob/master/_layouts/default.html) from the theme's repository<br />(*Pro-tip: click "raw" to make copying easier*)
2. Create a file called `/_layouts/default.html` in your site
3. Paste the default layout content copied in the first step
4. Customize the layout as you'd like

### Overriding GitHub-generated URLs

Templates often rely on URLs supplied by GitHub such as links to your repository or links to download your project. If you'd like to override one or more default URLs:

1. Look at [the template source](https://github.com/pages-themes/architect/blob/master/_layouts/default.html) to determine the name of the variable. It will be in the form of `{{ site.github.zip_url }}`.
2. Specify the URL that you'd like the template to use in your site's `_config.yml`. For example, if the variable was `site.github.url`, you'd add the following:
    ```yml
    github:
      zip_url: http://example.com/download.zip
      another_url: another value
    ```
3. When your site is built, Jekyll will use the URL you specified, rather than the default one provided by GitHub.

*Note: You must remove the `site.` prefix, and each variable name (after the `github.`) should be indent with two space below `github:`.*

For more information, see [the Jekyll variables documentation](https://jekyllrb.com/docs/variables/).

## Roadmap

See the [open issues](https://github.com/pages-themes/architect/issues) for a list of proposed features (and known issues).

## Project philosophy

The Architect theme is intended to make it quick and easy for GitHub Pages users to create their first (or 100th) website. The theme should meet the vast majority of users' needs out of the box, erring on the side of simplicity rather than flexibility, and provide users the opportunity to opt-in to additional complexity if they have specific needs or wish to further customize their experience (such as adding custom CSS or modifying the default layout). It should also look great, but that goes without saying.

## Contributing

Interested in contributing to Architect? We'd love your help. Architect is an open source project, built one contribution at a time by users like you. See [the CONTRIBUTING file](docs/CONTRIBUTING.md) for instructions on how to contribute.

### Previewing the theme locally

If you'd like to preview the theme locally (for example, in the process of proposing a change):

1. Clone down the theme's repository (`git clone https://github.com/pages-themes/architect`)
2. `cd` into the theme's directory
3. Run `script/bootstrap` to install the necessary dependencies
4. Run `bundle exec jekyll serve` to start the preview server
5. Visit [`localhost:4000`](http://localhost:4000) in your browser to preview the theme

### Running tests

The theme contains a minimal test suite, to ensure a site with the theme would build successfully. To run the tests, simply run `script/cibuild`. You'll need to run `script/bootstrap` one before the test script will work.
