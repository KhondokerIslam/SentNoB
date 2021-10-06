# SentNoB: A Dataset for Analysing Sentiment on Noisy Bangla Texts

This is the implementation of our paper "SentNoB: A Dataset for Analysing Sentiment on Noisy Bangla Texts". You can find the paper [here](http://sudiptakar.info/assets/files/sentnob_emnlp_2021.pdf)


If you use any source codes or datasets included in this toolkit in your work, please cite the paper. The bibtex will be provided later.

## Abstract
In this paper, we propose an annotated sentiment
analysis dataset made of informally written
Bangla texts. This dataset comprises public
comments on news and videos collected
from social media covering 13 different domains,
including politics, education, and agriculture.
These comments are labeled with one
of the polarity labels, namely positive, negative,
and neutral. One significant characteristic
of the dataset is that each of the comments is
noisy in terms of the mix of dialects and grammatical
incorrectness. Our experiments to develop
a benchmark classification system show
that hand-crafted lexical features provide superior
performance than neural network and pretrained
language models.

## Authors

* Khondoker Ittehadul Islam <sup>1</sup>
* Md Saiful Islam <sup>1, 2</sup>
* Sudipta Kar <sup>3</sup>
* Mohammad Ruhul Amin <sup>4</sup>

<sup>1</sup> Shahjalal University of Science and Technology, Bangladesh
<br>
<br>
<sup>2</sup> University of Alberta, Canada
<br>
<br>
<sup>3</sup> Amazon Alexa AI, USA
<br>
<br>
<sup>4</sup> Fordham University, USA

## SentNoB Dataset is available [here](https://www.kaggle.com/cryptexcode/sentnob-sentiment-analysis-in-noisy-bangla-texts) 

#### List of files

* Train.csv
* Val.csv
* Test.csv

#### Files Format
Column Title | Description
------------ | -------------
Data | Social media comment
Label | 0, 1 or 2 . '0' for neutral, '1' for positive and '2' for negative

## INSTALLATION

Requires the following packages:
* Python 3.9.7 or higher

It is recommended to use virtual environment packages such as virtualenv. Follow the steps below to setup the project:
* Clone this repository via `git clone https://github.com/KhondokerIslam/SentNoB.git`
* Use this command to install required packages `pip install -r requirements.txt`
* Type `setup.sh` to download bangla fastText embeddings

## Usage

1. Download the SentNoB dataset from [here](https://www.kaggle.com/cryptexcode/sentnob-sentiment-analysis-in-noisy-bangla-texts)
2. Unzip the folder
3. Ensure the folder name is "SentNoB Dataset"
4. Go to data_processing folder and run `python preprocess.py` to obtain the preprocessed data.

#### Feature-Based Experiments
* Go to Models folder
* Use `python feature_based.py`
* Type in the model name when you will be asked to specify the model name in the console
* Model Names (Please follow the paper to read the details about experiments):
  * Unigram
  * Bigram
  * Trigram
  * U+B
  * B+T
  * U+B+T
  * Char 2-gram
  * Char 3-gram
  * Char 4-gram
  * Char 5-gram
  * C2+C3
  * C3+C4
  * C4+C5
  * C2+C3+C4
  * C3+C4+C5
  * C2+C3+C4+C5
  * U+B+C3+C4+C5
  * U+B+C2+C3+C4+C5
  * U+B+T+C2+C3+C4+C5
  * Embeddings
  * U+B+C2+C3+C4+C5+E
  * U+B+T+C2+C3+C4+C5+E
 
#### Neural Network Experiments
 
##### Random Initialize

* Go to Models folder
* Use "python neural_network_(random).py" to run an experiment.

##### FastText

* Go to Models folder
* Use "python neural_network_(fasttext).py" to run an experiment.

#### mBert

* Go to Models folder
* Use "python mbert.py" to run an experiment.

   
