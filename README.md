# N-Gram Language Model with Beam Search Decoder

This repository contains an implementation of N-Gram Language Models (unigram, bigram, and trigram) and a 
Beam Search Decoder for correcting text with random errors. The code is written in Python and utilizes the NLTK library 
for natural language processing tasks.

## Process Flow

- Creation of Reuters vocabulary.
- Creation of unigram, bigram, and trigram models from the Reuters corpus.
- Calculation of probabilities with Laplace smoothing.
- Evaluation of language models using Cross Entropy and Perplexity.
- Generation of noisy text with random errors.
- Correction of noisy text using a Beam Search Decoder.
- Evaluation of the correction using Word Error Rate (WER) and Character Error Rate (CER).


### Detailed Process Flow

### Training N-Gram Models

- Read the training subset of the Reuters corpus.
- Tokenize and lowercase the text.
- Filter stopwords and create a vocabulary with a minimum token count.
- Replace out-of-vocabulary words with "*UNK*".
- Create unigram, bigram, and trigram models.

### Evaluation with Cross Entropy and Perplexity

- Evaluate the bigram and trigram models using Cross Entropy and Perplexity.
- Cross Entropy measures the average number of bits needed to represent the probability distribution.
- Perplexity indicates how well a language model predicts a given sequence of words.

### Spelling Correction with Beam Search Decoder

- Implement a Beam Search Decoder to correct spelling errors.
- Use bigram probabilities and Levenshtein distance for scoring.

### Generating Noisy Text

- Create a function to generate text with random errors.
- The function introduces errors in the original text with a given probability.

### Evaluation with WER and CER

- Word Error Rate (WER) is the percentage of words incorrectly recognized or corrected.
- Character Error Rate (CER) is the percentage of characters incorrectly recognized or corrected.
- Evaluate the spelling corrector using the original test dataset as the ground truth.