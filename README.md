# 📊 Experiment 16: NLP Techniques on Text Data in Python

---

## 🎯 Aim

To perform fundamental Natural Language Processing (NLP) operations such as tokenization, stop word removal, stemming, lemmatization, part-of-speech tagging, and word frequency analysis using Python.

---

## 📚 Theory

Natural Language Processing (NLP) deals with processing and analyzing textual data. Since raw text is unstructured, it must be converted into a structured format before analysis. This experiment demonstrates essential preprocessing steps using the **NLTK (Natural Language Toolkit)** library.

---

### 🔹 1. Data Preparation using NLTK

Before performing NLP operations, required datasets are downloaded using:

* `nltk.download('punkt')` → Required for tokenization
* `nltk.download('stopwords')` → Provides list of stop words
* `nltk.download('wordnet')` → Required for lemmatization
* `nltk.download('averaged_perceptron_tagger')` → Used for POS tagging

These resources enable various NLP functions to work correctly.

---

### 🔹 2. Tokenization

Tokenization is the process of splitting text into smaller units.

* `word_tokenize(text)` → Converts a sentence into individual words
* `sent_tokenize(text)` → Splits a paragraph into sentences

Example:

* Sentence is split into tokens like *Natural, language, processing*
* Paragraph is split into multiple sentences

This step forms the base for all further text processing.

---

### 🔹 3. Stop Word Removal

Stop words are commonly used words that do not add significant meaning.

* `stopwords.words('english')` → Retrieves list of stop words
* `set()` → Converts list into set for faster lookup
* List comprehension → Filters words not present in stop word list

Example:

* Words like *is, in* are removed
* Remaining words carry meaningful information

---

### 🔹 4. Stemming

Stemming reduces words to their root form.

* `PorterStemmer()` → Initializes stemming object
* `stemmer.stem(word)` → Returns root form of a word

Example:

* playing → play
* running → run

This method is fast but may produce non-dictionary words like *studi*.

---

### 🔹 5. Lemmatization

Lemmatization converts words into their correct dictionary form.

* `WordNetLemmatizer()` → Initializes lemmatizer
* `lemmatizer.lemmatize(word)` → Returns meaningful base word

Example:

* studies → study
* writing → writing

It is more accurate than stemming as it considers word meaning.

---

### 🔹 6. Part-of-Speech (POS) Tagging

POS tagging identifies the grammatical role of each word.

* `word_tokenize()` → Tokenizes input sentence
* `pos_tag(tokens)` → Assigns grammatical tags

Example:

* Python → Proper Noun (NNP)
* is → Verb (VBZ)
* powerful → Adjective (JJ)

This helps in understanding sentence structure and context.

---

### 🔹 7. Word Frequency Analysis

Word frequency analysis determines how often each word appears.

* `FreqDist(words)` → Creates frequency distribution
* `fd.most_common()` → Returns words with their frequency

Example:

* Frequently occurring words like *is* appear multiple times
* Less frequent words appear once

This is useful for identifying important terms in text.

---

## 📊 Output Summary

* Text was successfully tokenized into words and sentences
* Stop words were removed to retain meaningful data
* Words were reduced using stemming and lemmatization
* POS tagging identified grammatical roles of words
* Word frequency analysis highlighted commonly used terms

---

## ✅ Conclusion

The experiment demonstrates how unstructured text can be processed using fundamental NLP techniques. Each step, from tokenization to frequency analysis, contributes to converting raw text into meaningful and structured data. These preprocessing techniques are essential for advanced applications such as text classification, sentiment analysis, and language modeling.

