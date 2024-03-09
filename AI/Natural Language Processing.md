<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

<h1 align="center"> Natural Language Processing</h1>

<table align="center">
  <tr>
    <td>1. <a href="#nltk">NLTK</a> </td>
    <td>6. <a href="#stem">Stemming</a></td>
    <td>11. <a href="#bag">Bag of Words</a></td>
    <td>16. <a href="#ner">Name Entity Recognition</a></td>
  </tr>
  <tr>
    <td>2. <a href="#mine">Text Analysis | Text Mining</a> </td>
    <td>7. <a href="#lemma">Lemmatization</a></td>
    <td>12. <a href="#vector">Vectorization</a></td>
    <td>17. <a href="#cloud">Word Cloud</a></td>
  </tr>
  <tr>
    <td>3. <a href="#app">Real World Application</a> </td>
    <td>8. <a href="#norm">Text Normalization</a></td>
    <td>13. <a href="#tfidf">TF-IDF</a></td>
    <td>18. <a href="#word2vec"> Word2vec </a></td>
  </tr>
  <tr>
    <td>4. <a href="#pipe">NLP Pipeline</a> </td>
    <td>9. <a href="#stop">Stop Word</a></td>
    <td>14. <a href="#ngram">N Grams</a></td>
    <td>19. <a href="#doc2vec"> Doc2vec </a></td>
  </tr>
  <tr>
    <td>5. <a href="#token">Tokenization</a> </td>
    <td>10. <a href="#pos">Part of Speech</a></td>
    <td>15. <a href="#vector">Vectorization</a></td>
  </tr>
  
</table>

### `NLP`

- A field of `AI` that deals with the interaction between computers and human language.
- Ability of computer to `read`, `understand`, `learn`, `analyze`, `translate`, `generate` and `communicate` using **human language**.
- Interaction between `computers` and `humans` using the natural language.

#### Applications:
- Chatbots
- Virtual Assistants
- Sentiment Analysis
- Translation

### **Corpus:**
- Corpus: A large collection of text data.
- Corpora are essential for training NLP models, as they provide the models with the raw language data they need to learn from.
- Corpora are used to train ML models for a variety of NLP tasks, such as sentiment analysis, machine translation, and part-of-speech tagging.

Types of corpora:
1. **Newsgroups corpora:** Collections of newsgroup posts.
2. **Web corpora:** Collections of text from the web. 
3. **Social media corpora:** Collections of text from social media platforms such as Instagram, Twitter and Facebook. 
4. **Speech corpora:** Collections of spoken language data. 

<h3 name="nltk"> NLTK ( Natural Language Toolkit ) </h3>

- Open source `toolkit` or `library` created to make `NLP` process in `Python`

<h3 name="mine"> Text Mining | Text Analysis </h3>

- `Analyze` and `understand` text data.  
- Derive **meaningful information** from natural language `text` and `speech`

### Types of text data 
- Web, blogs, articles, feeds, comments, reviews, emails and notes.
- Social media : Messages, hashtags, reference, comments, etc.
- Operations : Logs and trails.
- Emails ( Spam or Ham )
- Voice transcriptions and subtitles.

### Process :

1. Human talk to machine.
2. Machine capture human audio.
3. Convert audio to text.
4. Process text data. 
5. Convert processed text to audio.
6. Machine reply to human.

<h3 name="app"> Applications : NLP in real life </h3>

1. Google translate. ( Speech to text )
2. Email `spam` filter ( Search for texts related to spam email )
3. Google search and Gmail auto complete ( Prediction of **next words** and **suggestions** ) 
4. Word processor | Grammer check | Auto correct in Microsoft and Google productivity Apps.
5. Grammerly | Grammer correction and spelling correction in Gmail and Outlook.
6. IVR | Interactive voice response in call centers.
7. Voice assistant : `Google` Google home, `Apple` siri, `Microsoft` cortana and `Amazon` alexa.
8. Chatbots.
9. Customer feedback sentiment analysis ( 😊🙂😔😡 )
10. Document summarization : Read article and newspaper ( Blind people )
11. Text classification.
12. Part of speech `tagging` ( **Part of speech** of corresponding word )

<h3 name="pipe"> NLP Pipeline </h3>

1. Read **raw** text.
2. Remove `Punctuations`
3. Create `Tokens` (Create a list by splitting each and every `word`)
4. Remove `Stopwords`
5. Apply Stemming | Lemmatization (Reduce derived words to `stem` words)
6. `Vectorize` data to prepare for model built (Convert text to `number`)
7. **Feature Engineering** (**Creating** new feature or **transforming** existing features to get most out of data)

<h3 name="token"> Tokenization </h3>

- The process of breaking down text into smaller units, such as words or sentences.
- This is the first step in many NLP tasks, as it allows the model to process the text in a more manageable way.

```python
Word = "Hi, my name is Kirankumar"
["Hi", ",", "my", "name", "is", "Kirankumar"]
```

<h3 name="stem"> Stemming </h3>

- Reducing **derived** words to there `stem` | `root` | `base` form.
- Remove `suffix` and `prefix` from the word.
- The process of reducing a word to its base form. For example, the words "running," "runs," and "ran" would all be stemmed to "run."
- Stemming can be helpful for tasks like information retrieval, as it allows the model to match words with different suffixes.

`Stemming` is applied on `tokens` 

```python
stem(token) 
```

### Why Stemming ?
- Reduce `corpus` of words and `correlate` words with `similar` meanings.

### Types of Stemmers
1. **Porter** Stemmer ( **Oldest** with very **low accuracy** : fairly > `fairli` )
2. **Snowball** Stemmer ( **Better** than **Porter** and **Lancaster** : fairly > `fair` )
3. **Lancaster** Stemmer ( **Fastest** with **least accuracy** )

<h3 name="lemma"> Lemmatization </h3>

- A more sophisticated form of stemming that takes into account the context of a word to determine its base form.
- Grouping together the **derived forms** of words so that they can be analyzed as a `single` base form.
- Actually `transforms` words to the **actual root**. **Reduce** words to its `base` form.
- Used in **search engines** to search by `keywords`. `Lemma` is actual word ( Better > Good )

### WordNet Lemmatizer

- **Database** for `english` ( Most popular **Lemmatizer** )
- `Nouns`, `Verbs`, `Adjectives` and `Adverbs` are **grouped** into sets of **Cognitive Synonyms**.  
- e.g. { 'consult', 'consultation', 'consulting', 'consultant' } - consult

Stemming | Lemmatization
:--- | :---
**Speed** | **Accuracy**
Simply `strips` end of the word to `stem` | **Converts** the word to its **meaningful** `base` form.

### Text Preprocessing

- `Map` the words with any other case to the `lowercase`

### Noise Removal

- Removing `special characters`, `digits` and pieces of text that can `interfere` with text analysis.
- Remove `punctuation`, `special character`, `number`, `HTML` formatting, `source code`, `header`

<h3 name="norm"> Text Normalization </h3>

- Transforming text into its `standard` form.
- e.g. 'gooood' and 'gud' transformed to 'good'
- Mapping of near **identical** words such as 'stopwords', 'stop-words' and 'stop words' to just 'stopwords'
- Important when **noisy**, **misspelled**, **slang** and **out of vocabulory** ( `OOV` ) words are used. 
- **Out of vocabulory** ( `OOV` ) : **Social media** comments, **blog** comments and **text messages**.

<h3 name="stop"> Stop Word </h3>

- Common words that are filtered out before processing text.
- Stop words are `filler` words like `a`, `an`, `in`, `on`, `and`, `the`, `or`, etc.
- Stopwords are ignored and `removed`, so that we can `focus` on **important words** instead.
- Search engine only search on the basis of `keywords`
- Search engines are programmed to `ignore` **stop words**.
- These words don't provide much meaning on their own, so filtering them out can improve the efficiency of NLP tasks.

How to `remove` stopwords using NLTK

1. `Tokenize` and compare with list of predefined `stopwords` and `drop` that words. 

```python
Token for Token in text if not in `Stopwords.words()` 
```

<h3 name="pos"> POS : Parts-of-Speech Tagging</h3>

- The process of assigning a grammatical tag (such as noun, verb, adjective) to each word in a sentence.
- POS tagging can be helpful for tasks like sentiment analysis and machine translation.

<h3 name="bag"> Bag of Words </h3>

- A method for representing text documents as a collection of words.
- Number of `occurence` of words in a paragraph or sentence.
- e.g. well well well, said john. {'well':3, 'said':1, 'john':1}
- Bag of words is represented in form of **dictionary**. 
- Expressed sentiments of words are defined by `polarity`
- `Polarity` : Positive `+1`, Negative `-1` or Neutral `0`
- In a BOW model, the order of the words is not taken into account, only the frequency of each word.
- BOW models are a simple and effective way to represent text data, but they can lose some important information about the structure of the text.

<h3 name="vector"> Vectorization </h3>

- **Converting** text to form `Numbers` that an **algorithm** and a **ML model** can `understand` and `learn`.
- **Process** of `encoding` text as `integers` to create `feature matrix`

<h3 name="tfidf">TF - IDF</h3>

![TFIDF](Image/TFIDF.png)

- **Term Frequency** - **Inverse Document Frequency**.
- `TF` : Number of `times` term `appears` in document / Number of `terms` in document.
- `IDF` : `log(N/n)` 
- `N` : Number of `documents`
- `n` : Number of `documents` a `term` appeared in.
- Shows how `important` a given `word` is to the `document`
- `IDF` value of a `rare` word is `high` and `low` for `frequent` word.

### Feature Vector
- An `n dimensional vector` of **numerical features** that represents some `object`.

### Different Types
1. **Count** vectorization ( Create a **document term matrix**   that represents `count` of `occurence` )
2. **N Grams** ( Combination of `adjacent` words )
3. **Term Frequence** - **Inverse Document Frequency** ( `TD - IDF` ) 

<h3 name="ngram"> N Grams </h3>

- **Combinations** of `adjacent` words of length `N` in the text.
- A sequence of n words. N-grams are commonly used in NLP tasks such as language modeling and machine translation.
- Bigrams (2-grams) and trigrams (3-grams) are the most common types of n-grams used in NLP.

### Bigrams

- Form **pair** of `adjacent` words from sentence.

### Trigrams

- Form set of **three** `adjacent` words.

`Google Search` **suggests** `bigrams`, `trigrams` in there `keyword` **suggestions**.  

<h3 name="ner"> Name Entity Recognition </h3>

1. **Recognize** elements in text by `category`  
2. `Movie`, `Person`, `Location`, `Organization`, `Quantity Unit`, `Monetory Value` | `Financial` terms.
3. Automatically identify `entity` name in a text and classify it in **predefined categories**.

![NER](Image/NER.png)

### Syntax | Syntactic Analysis
- Syntactic structure of `sentence` or `strings`
- Analyze string by `symbol`

### Sentiment Analysis
- `Feeling`, `emotion`, `reaction`, `satisfaction` of user, customer or consumer expressing there `feedback`

### Information Retrieval
- Process of `accessing` and `retrieval` of appropriate information  from text.
- **Extracting** `title`, `text` and `media` from a `book`, `artice` or simply `HTML tags` from `web page`
- e.g. `Google Search`

<h3 name="cloud"> Word Cloud </h3>

- A graphical display of words in a `corpus`.
- `Size` of word is based on number of `occurences`
- **Visual** view of the most popular terms.

### Corpus | Corpora
- Large `collection` of documents ( Accurate grammer phrases ) 
- `Knowledge base` that can be used to infer and validate language rules.

### Sparse Matrix
- A `matrix` in which most entries are `0` helps in **efficient storage**.
- Stores only `location` of **non zero elements**.

### Chunking
- `Grouping` individual pieces of information into big chunks.

### Transformation
- **Power** Transformation ( `Square`, `Square Root` )
- Standardization or Normalization of Data. 

<table align='center'>
  <tr>
    <th>
      <h4>word2vec ( Word 2 Vector )</h4>      
    </th>
    <th>
      <h4>doc2vec ( Document 2 Vector )</h4>
    </th>
  </tr> 
  <tr>
    <th colspan='2'>Accept large corpus of text as input</th>
  </tr>
  <tr>
    <th colspan='2'>Vector : Numeric representation of word and document ( One Hot Vector )</th>
  </tr>
  <tr>
    <td>Returns a set of vectors for each <b>word</b></t>
    <td>Returns a set of vectors for entire <b>sentence</b></t>
  </tr>
  <tr>
    <td>Vectors are converted to <b>Array</b></t>
    <td>Vectors are converted to <b>List</b></t>
  </tr>
  <tr>
    <th colspan='2'>Use neural network to learn word association from a large corpus of text</th>
  </tr>
  <tr>
    <th colspan='2'>Detect synonymous words or suggest next words for a partial sentence ( Autocomplete | Search bar suggestion )</th>
  </tr>
 </table>

Word2Vec Matrix | TF-IDF Matrix
:--- | :--- 
Multi dimensional vector | Sparse matrix
Capture words relationship with other words | Captures the importance of word in a given documment.
Applied on each word individully | Applied to each training document.
More memory intensive | Less memory intensive.
Ideal for single word problems | Ideal for problems with multiple words or document files.

### One Hot Vector

![One Hot Vector](Image/OHV.png)

### BERT 
- Google's pre trained **bidirectional encoder representation for transformers** used for **transfer learning**.

[Text Classification](https://towardsdatascience.com/text-classification-with-nlp-tf-idf-vs-word2vec-vs-bert-41ff868d1794)

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
