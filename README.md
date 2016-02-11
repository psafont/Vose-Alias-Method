#Vose-Alias-Method
Python implementation of Vose's alias method, an efficient algorithm for sampling from a discrete probability distribution (a good explanation of which can be found at http://www.keithschwarz.com/darts-dice-coins/).

This code can be used to create (and efficiently sample from) a probability distribution when rolling a weighted die, or for creating a simple [unigram language model](https://en.wikipedia.org/wiki/Language_model#Unigram_models) (see [example usage below](#example-usage))

##<a name="depends-on">Depends on:</a>
- The Python Standard Library, https://docs.python.org/2/library/
- Python versions 2.7 (tested on Python 2.7.11)

##<a name="example-usage">Example Usage</a>
To create a [unigram language model](https://en.wikipedia.org/wiki/Language_model#Unigram_models) for [Alice in Wonderland](http://www.gutenberg.org/cache/epub/11/pg11.txt) and sample 10 words from this, run the main script with options:
```python vose_sampler.py -p data/Alice.txt -n 10```

(Note, this is intended to illustrate how Vose's alias method could be used. Thus I have not included any preprocessing steps that would make the language model more realistic; for example, we could add handling of upper vs. lower case words (so that e.g. "The" and "the" are not considered distinct), handling of punctuation (e.g. so "the" and "the." are considered the same) and so.)

Unit tests can be run via:
```python unit_tests.py```
