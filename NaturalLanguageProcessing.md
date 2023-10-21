# NLP
giving computers the ability to understand text and spoken words in much the same way human beings can.

## Sentiment analysis
To understand the emotional intent of the text.<br>
**Positive, Negative, Neutral**<br>
A sentiment classification model will output the probability of each quality<br>
 entiment analysis is used to classify customer reviews


Grammatical error correction
Autocomplete 


## How it works
Stemming and lemmatization: Stemming is an informal process of converting words to their base forms using **heuristic rules**. For example, “university,” “universities,” and “university’s” might all be mapped to the base univers. (One limitation in this approach is that “universe” may also be mapped to univers, even though universe and university don’t have a close semantic relationship.) Lemmatization is a more formal way to find roots by analyzing a word’s morphology using vocabulary from a dictionary. Stemming and lemmatization are provided by libraries like spaCy and NLTK. <br><br>

Sentence segmentation breaks a large piece of text into linguistically meaningful sentence units. This is obvious in languages like English, where the end of a sentence is marked by a period, but it is still not trivial. A period can be used to mark an abbreviation as well as to terminate a sentence, and in this case, the period should be part of the abbreviation token itself. The process becomes even more complex in languages, such as ancient Chinese, that don’t have a delimiter that marks the end of a sentence. <br><br>

Stop word removal aims to remove the most commonly occurring words that don’t add much information to the text. For example, “the,” “a,” “an,” and so on.<br><br>



## Tokenization
splits text into **individual words and word fragments.** The result generally consists of a word index and tokenized text in which words may be represented as numerical tokens for use in various deep learning methods. A method that instructs language models to ignore unimportant tokens can improve efficiency. 





 **First principle:**
- words can be encoded using ASCII of its individual letters, but two words can have the same values. It is hard to understand the **sentiment** of a word
- So we **"tokenize"** each seperate word in the phrase instead. Encoding each word. For example I = 1, love = 2, ...

  I love my dog<br>
  1 2 3 4<br>
  I love my cat<br>
  1 2 3 5<br>

  similarity of action, different noun

We use an application programming interface API to do this in python

```py
import tensorflow as tf 
from tensorflow import keras
from keras.preprocessing.text import Tokenizer

sentences = [
    "I love my dog"
    "I love my cat"
]

tokenizer = Tokenizer(num_words = 100)
tokenizer.fit_on_texts(sentences)
word_index = tokenizer.word_index
print(word_index)
```
output: {'love': 1, 'my': 2, 'i': 3, 'dogi': 4, 'cat': 5}

we use keras which is an inbuilt module in tensorflow<br>
**Part-of-Speech Tagging**: Identifying the grammatical parts of a sentence (e.g., nouns, verbs, adjectives).

**sequences of token values** make up the sentences
```py 
sequences = tokenizer.texts_to_sequences(sentences)
```
this code creates a **sequence of tokens** that make each sentence

with words that are not within the word index, eg **unrecognised**, it will just show the sequence of the words it has an index for
OOV is when testing the model. If a word was not in the training data, it is not recognised, henced labelled OOV
we can handle unrecognised words by passing a property called the **oov_token = "<OOV>"**<br><br>
In the word keys, it will **assign a number to an OOV**, and then all unrecognised words will have number 1 for its key
This will maintain the sequence length without removing unknown words

**Ragged Tensor**
### Padding
0 is for padding. It is used in order for the **sentence lengths to be the same when processing**, shorter sentences have 0s filled in so all sentences are the same size as the longest sentence<br>
**0 = padding**
**1 = OOV**
Why padding is used?

Your data comes in many shapes; your tensors should too. Ragged tensors are the TensorFlow equivalent of nested variable-length lists. They make it easy to store and process data with non-uniform shapes, including:

Variable-length features, such as the set of actors in a movie.
Batches of variable-length sequential inputs, such as sentences or video clips.
Hierarchical inputs, such as text documents that are subdivided into sections, paragraphs, sentences, and words.
Individual fields in structured inputs, such as protocol buffers.

**preprocessing is all done**
- tokenizing each word, forming sequences for sentences
- OOV for unknown words not in training data
- padding in sequences

## Estimating sarcasm of headlines

A sentiment of a word, is actually represented as a **coordinate vector**
the uses of axis for good and bad. Each different one is plotted at a certain coordinate on a plane.
![image](https://github.com/Swiftal13/Machine-Learning/assets/76588047/b553a2d1-ebfc-44c1-bab7-76f5489ffb3d)

