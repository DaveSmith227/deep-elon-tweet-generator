# deep-elon-tweet-generator
Elon Musk-like tweets generated with a recurrent neural network (RNN).

This project was built with the fastai library (built on Pytorch) and the language model used to generate the tweets is an AWD-QRNN (ASGD Weight-Dropped Quasi-Recurrent Neural Network).

The task involves predicting the next token (i.e. a word, a character, a punctuation mark, etc.) in a sequence given the n preceding tokens.

It was trained with the WikiText-103 dataset (https://www.sysml.cc/doc/50.pdf) and then fine-tuned with Elon's tweets and speeches using transfer learning.

- The WikiText language modeling dataset is a collection of over 100 million tokesn extracted from Wikipedia.
- Elon's tweets are from 2010 to 2018 and contain over 6,000 tweets
- Elon's speeches are from 2003 to 2017 and contain ~60 speeches with ~1,300 paragraphs of text

All the processing steps are in the jupyter notebook. The other fields are used to build a web app that generates Musk-like tweets on demand. It is hosted using Zeit.

The app can be seen live here: https://deepelon.com/

Inference (generated tweets) can take a couple of minutes and the generated tweets are still prone to errors depending on which root word(s) you use to generate the tweet.
