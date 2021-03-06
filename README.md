# Comparable text miner

# Description 
Comparable documents miner: Arabic-English morphological analysis, text processing, n-gram features extraction, POS tagging, dictionary translation, documents alignment, corpus information, text classification, tf-idf computation, text similarity computation, HTML documents cleaning, and others. 

This software is implemented by Motaz SAAD (motaz dot saad at gmail do com) during his PhD work. The PhD thesis is available at: https://sites.google.com/site/motazsite/Home/publications/saad_phd.pdf

Motaz Saad. Mining Documents and Sentiments in Cross-lingual Context. PhD thesis, Université de Lorraine, January 2015.

This software processes Arabic and English text. To use this software, load it as follows:

```python
import imp
tp = imp.load_source('textpro', 'textpro.py')
#Then, you can use functions as follows:
clean_text = tp.process_text(text)
```

# Dependencies
This software depends on the following python packages scipy, numpy, nltk, sklearn, bs4. Please make sure that they are installed before using this software. 

# References
This software uses the following resources:
- Arabic stopwords: http://www.ranks.nl/stopwords/arabic 
- Open Multilingual WordNet (OMW) dictionaries http://compling.hss.ntu.edu.sg/omw/ The references of OMW are listed below:
	- Francis Bond and Kyonghee Paik (2012), A survey of wordnets and their licenses In Proceedings of the 6th Global WordNet Conference (GWC 2012). Matsue. 64–71.
	- Francis Bond and Ryan Foster (2013), Linking and extending an open multilingual wordnet. In 51st Annual Meeting of the Association for Computational Linguistics: ACL-2013. Sofia. 1352–1362. 

- ISRI Arabic Stemmer, which is a rooting algorithm for Arabic text. The reference of ISRI Arabic Stemmer is below:
	- Taghva, K., Elkoury, R., and Coombs, J. 2005. Arabic Stemming without a root dictionary. Information Science Research Institute. University of Nevada, Las Vegas, USA.
 

- This software modifies the ISRI Arabic Stemmer to perform light stemming for Arabic words. 

# Usage examples (demos)
- Dictionary translation demo
```
python dict-demo.py <inputfile> <outputfile> <source language>
# translate from Arabic to English
python dict-demo.py test-text-files/dict-test-ar-input.txt test-text-files/dict-out.txt ar
# translate from English to Arabic
python dict-demo.py test-text-files/dict-test-en-input.txt test-text-files/dict--out.txt en
```
- Arabic morphological analysis demo
```
python arabic-morphological-analysis-demo.py <inputfile> <outputfile>
python arabic-morphological-analysis-demo.py test-text-files/test-in.ar.txt test-text-files/test-out.ar.txt
```
