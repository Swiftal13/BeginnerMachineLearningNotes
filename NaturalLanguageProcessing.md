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
Stemming and lemmatization: Stemming is an informal process of converting words to their base forms using heuristic rules. For example, “university,” “universities,” and “university’s” might all be mapped to the base univers. (One limitation in this approach is that “universe” may also be mapped to univers, even though universe and university don’t have a close semantic relationship.) Lemmatization is a more formal way to find roots by analyzing a word’s morphology using vocabulary from a dictionary. Stemming and lemmatization are provided by libraries like spaCy and NLTK. <br><br>

Sentence segmentation breaks a large piece of text into linguistically meaningful sentence units. This is obvious in languages like English, where the end of a sentence is marked by a period, but it is still not trivial. A period can be used to mark an abbreviation as well as to terminate a sentence, and in this case, the period should be part of the abbreviation token itself. The process becomes even more complex in languages, such as ancient Chinese, that don’t have a delimiter that marks the end of a sentence. <br><br>

Stop word removal aims to remove the most commonly occurring words that don’t add much information to the text. For example, “the,” “a,” “an,” and so on.<br><br>

Tokenization splits text into individual words and word fragments. The result generally consists of a word index and tokenized text in which words may be represented as numerical tokens for use in various deep learning methods. A method that instructs language models to ignore unimportant tokens can improve efficiency. 

tesnorflow
