# A Corpus Preprocessing Paradigm with spaCy

![spaCy pipeline](https://d33wubrfki0l68.cloudfront.net/3ad0582d97663a1272ffc4ccf09f1c5b335b17e9/7f49c/pipeline-fde48da9b43661abcdf62ab70a546d71.svg)

This is a paradigm for corpus preprocessing, especially for the raw text directly extreacted from the Internet.

This code implementation is based on the blog [Text Preprocessing for NLP (Natural Language Processing),Beginners to Master](https://medium.com/analytics-vidhya/text-preprocessing-for-nlp-natural-language-processing-beginners-to-master-fd82dfecf95) by [Ujjawal Verma](https://medium.com/@ujjawalv05).

The main difference from the preprocessing in the blog is that:
- This paradigm relies on [spaCy](https://spacy.io/models/en#en_core_web_lg), instead of [nltk](https://www.nltk.org/).
- We removed stopwords twice, once after the pre-tokenization, once after the pipeline processing, in order to reduce the wordload and running-time of while using spaCy large pre-trained model. (Please note using [transformer-based model](https://spacy.io/models/en#en_core_web_trf) for huge corpus could result in a very long running-time.)
- After the pipeline preprocessing, we stripped all the blank space elements in the list of tokens/lemmas.
