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

- Ability of computer to `understand`, `learn`, `analyze`, `manipulate` and `communicate` using **human language**.
- Interaction between `computers` and `humans` using the natural language.

<h3 name="nltk"> NLTK ( Natural Language Toolkit ) </h3>

- Open source toolkit or library created to make `NLP` process in `Python`

<h3 name="mine"> Text Mining | Text Analysis </h3>

- **Analyze** and **understand** text data.  
- Derive **meaningful information** from natural language `Text` and `Speech`

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
3. Create `Tokens` 
4. Remove `Stopwords`
5. Apply Stemming | Lemmatization.
6. `Vectorize` data to prepare for model built (Feature vector)
7. **Feature Engineering** (**Creating** new feature or **transforming** existing features to get most out of data)

<h3 name="token"> Tokenization </h3>

- `Break` | `Split` a **sentence** | **Phrase** | **Paragraph** into `list` of **individual words**.

<h3 name="stem"> Stemming </h3>

- Reducing **derived** words to there `stem` | `root` | `base` form.
- Remove `suffix` and `prefix` from the word.
- Stem may not be an **actual** word, easy to `read` and `compare`.
- e.g. Studies > Studi | Studying > Study

> **Stemming** is applied on **Tokens** (`stem(token)`) 

### Why Stemming ?
- Reduce `corpus` of words and `correlate` words with `similar` meanings.

### Types of Stemmers
1. **Porter** Stemmer ( **Oldest** with very **low accuracy** : fairly > `fairli` )
2. **Snowball** Stemmer ( **Better** than **Porter** and **Lancaster** : fairly > `fair` )
3. **Lancaster** Stemmer ( **Fastest** with **least accuracy** )

<h3 name="lemma"> Lemmatization </h3>
  
- Grouping together the **derived forms** of words so that they can be analyzed as a `single` base form.
- Actually `transforms` words to the **actual root**.
- **Reduce** words to its `base` form.
- Used in **search engines** to search by `keywords`.
- `Lemma` is actual word ( Better > Good )

### WordNet Lemmatizer

- **Database** for `english` ( Most popular **Lemmatizer** )
- `Nouns`, `Verbs`, `Adjectives` and `Adverbs` are **grouped** into sets of **Cognitive Synonyms**.  
- e.g. { 'consult', 'consultation', 'consulting', 'consultant' } - consult

Stemming | Lemmatization
:--- | :---
**Speed** | **Accuracy**
Simply `strips` end of the word to `stem` | **Converts** the word to its **meaningful** `Base` Form

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

- Filter out **useless** low information words in a sentence.
- Stop words are just **filler** words.
- We can `focus` on the **important words** instead.
- Search engine only search on the basis of `keywords`.
- Search engines are programmed to `ignore` **stop words**.

How to `remove` stopwords using NLTK

1. `Tokenize` and compare with list of predefined `stopwords` and `drop` that words. 

```python
Token for Token in text if not in `Stopwords.words()` 
```

<h3 name="pos"> POS : Parts of Speech </h3>

- Classify the **part of speech** `tag` of each `token`.
- Identify `noun`, `verb`, `adjective` in sentence.

<h3 name="bag"> Bag of Words </h3>

- Number of `occurence` of words in a paragraph or sentence.
- e.g. well well well, said john. {'well':3, 'said':1, 'john':1}
- Bag of words is represented in form of **dictionary**. 
- Expressed sentiments of words are defined by `polarity`
- `Polarity` : Positive `+1`, Negative `-1` or Neutral `0` 

<h3 name="vector"> Vectorization </h3>

- **Converting** text to form `Numbers` that an **algorithm** and a **ML model** can `understand` and `learn`.
- **Process** of `encoding` text as `integers` to create `feature matrix`

<h3 name="tfidf"> TF - IDF </h3>

![TFIDF](Image/TFIDF.png)

- **Term Frequency** - **Inverse Document Frequency**.
- Create a document term `matrix`
- `TF` : Number of `times` term `appears` in document / Number of `terms` in document.
- `IDF` : `log(N/n) 
- `N` : Number of `documents`
- `n` : Number of `documents` a `term` appeared in.
- One **row** per **document** ( Number of times the `term` appears in `document` )
- One **column** per **word** in the **corpus** ( Number of `documents` containing the `word` )
- Shows how **important** a given **word** is to the **document**. 

### Feature Vector
- An `n dimensional vector` of **numerical features** that represents some `object`.

### Different Types
1. **Count** Vectorization ( Create a **Document Term Matrix**   that represents **Count** of `Occurence` )
2. **N Grams** ( Combination of `Adjacent` Words )
3. **Term Frequence** - **Inverse Document Frequency** ( `TD - IDF` ) 

<h3 name="ngram"> N Grams </h3>

- **Combinations** of `Adjacent` Words of length **N** in the Text

### Bigrams

- Form **Pair** of `Adjacent` Words from Sentence.

### Trigrams

- Form Set of **Three** `Adjacent` Words

> Google Search **Suggests** `Bigrams`, `Trigrams` in there `Keyword` **Suggestions**.  

<h3 name="ner"> Name Entity Recognition </h3>

1. **Recognize** Elements in Text by **Category** ( `Movie`, `Person`, `Location`, `Organization`, `Quantity Unit`, `Monetory Value` | `Financial` Term )
2. `Identification` | `Extraction` technique that automatically identifies named `Entities` in a Text and Classifies in **Predefined Categories**.

![NER](Image/NER.png)

### Syntax | Syntactic Analysis
- Syntactic Structure of Sentence or Strings.
- Analyze String by `Symbol`. 

### Sentiment Analysis
- `Feeling`, `Emotion`, `Reaction`, `Satisfaction` of User | Customer | Consumer expressing there `Feedback`.

### Information Retrieval
- Process of **Accessing** and **Retrieval** of appropriate Information  from Text.
- **Extracting** `Title`, `Text` and `Media` from a `Book`, `Artice` or Simply `HTML Tags` from `Web Page`.
- e.g. `Google Search`

<h3 name="cloud"> Word Cloud </h3>

- A **Graphical** Display of Words in a `Corpus`.
- **Size** of Word based on number of **Occurences**.
- **Visual** View of the Most Popular Terms.

### Corpus | Corpora
- Large `collection` of documents ( Accurate grammer phrases ) | Knowledge base that can be used to infer and validate language rules.

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
    <th colspan='2'>Accept large Corpus of Text as Input</th>
  </tr>
  <tr>
    <th colspan='2'>Vector : Numeric Representation of Word and Document ( One Hot Vector )</th>
  </tr>
  <tr>
    <td>Returns a Set of Vectors for Each <b>Word</b></t>
    <td>Returns a Set of Vectors for Entire <b>Sentence</b></t>
  </tr>
  <tr>
    <td>Vectors are converted to <b>Array</b></t>
    <td>Vectors are converted to <b>List</b></t>
  </tr>
  <tr>
    <th colspan='2'>Use Neural Network to Learn Word Association from a Large Corpus of Text</th>
  </tr>
  <tr>
    <th colspan='2'>Detect Synonymous Words or Suggest Next Words for a Partial Sentence ( Autocomplete | Search Bar Suggestion )</th>
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
- Google's Pre trained **Bidirectional Encoder Representation for Transformers** used for **Transfer Learning**.

[Text Classification](https://towardsdatascience.com/text-classification-with-nlp-tf-idf-vs-word2vec-vs-bert-41ff868d1794)

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
