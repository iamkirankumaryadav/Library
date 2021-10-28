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

- **Analyze** and **understand** text data + Derive **meaningful information** from natural language (`Text` and `Speech`)

### Types of text data 
- Web, Blogs, Articles, Comments, Reviews and Notes.
- Social Media : Messages, Hashtags, Reference.
- Operations : Logs and Trails.
- Emails ( Spam or Ham )
- Voice **Transcriptions** 
- Videos Subtitles 

### Process :

1. Human Talk to Machine.
2. Machine Capture Audio.
3. Convert Audio to Text.
4. Process Text Data ( Interpret > Convert )
5. Convert Text to Audio.
6. Machine Talk | Reply to Human.

<h3 name="app"> Applications : NLP in Real Life </h3>

1. Google Translate. ( Speech to Text )
2. Email `Spam` Filter ( Search for Texts related to Spam Email )
3. Google Search and Gmail Auto Complete ( Prediction of **Next Words** ) 
4. Word Processor | Grammer Check | Auto Correct in Microsoft Word, Google Sheet, etc. 
5. Grammerly | Grammer Correction and Spelling Correction in Gmail.
6. IVR | Interactive Voice Response in Call Centers.
7. Voice Assistant : `Google` Google Home, `Apple` Siri, `Microsoft` Cortana and `Amazon` Alexa.
8. Chatbots
9. Customer Feedback Sentiment Analysis ( 😊🙂😔😡 )
10. Document Summarization : Read Article and Newspaper ( Blind People )
11. Text Classification
12. Part of Speech **Tagging** ( **Part of Speech** of Corresponding Word )

<h3 name="pipe"> NLP Pipeline </h3>

1. Read **Raw** Text
2. Remove `Punctuation`
3. Create `Tokens` 
4. Remove `Stopwords`
5. Stemming | Lemmatizing
6. `Vectorize` Data to Prepare for Model Built ( Feature Vector )
7. **Feature Engineering** ( **Creating** New Feature or **Transforming** Existing Features to get most out of Data )

<h3 name="token"> Tokenization </h3>

- `Break` | `Split` a **Sentence** | **Phrase** | **Paragraph** into `List` of **Individual Words**.

<h3 name="stem"> Stemming </h3>

- Reducing **Derived** Words to there `Stem` | `Root` | `Base` Form.
- Remove `Suffix` and `Prefix` from the Word.
- Stem may not be an **Actual** Word, Easy for `Read` and `Compare`.
- e.g. Studies > Studi | Studying > Study

> **Stemming** is applied on **Tokens** (`stem(token)`) 

### Why Stemming ?
- Reduce `Corpus` of Words and Correlate Words with `Similar` Meanings.

### Types of Stemmers
1. **Porter** Stemmer ( **Oldest** but very **low Accuracy** : fairly > `fairli` )
2. **Snowball** Stemmer ( **Better** than **Porter** and **Lancaster** : fairly > `fair` )
3. **Lancaster** Stemmer ( **Fastest** with **Least Accuracy** )

<h3 name="lemma"> Lemmatization </h3>
  
- Grouping together the **Derived forms** of Word so that they can be Analyzed as a `Single` ( Base ) form.
- Actually `Transforms` words to the **Actual Root**.
- **Reduce** Words to its `Base` Form.
- Used in **Search Engines** to Search by `Keywords`.
- `Lemma` is Actual Word ( Better > Good )

### WordNet Lemmatizer

- **Database** for `English` ( Most Popular **Lemmatizer** )
- `Nouns`, `Verbs`, `Adjectives` and `Adverbs` are **Grouped** into Sets of **Cognitive Synonyms**.  
- e.g. { 'consult', 'consultation', 'consulting', 'consultant' } - consult

Stemming | Lemmatization
:--- | :---
**Speed** | **Accuracy**
Simply `Chops` End of the Word to `Stem` | **Converts** the Word to its **Meaningful** `Base` Form

### Text Preprocessing

- Map the Words wiith different Case to the same `Lowercase` form.

### Noise Removal

- Removing **Special Characters**, Digits and Pieces of Text that can `Interfere` with Text Analysis.
- Remove `Punctuation`, `Special Character`, `Number`, `HTML` formatting, `Source Code`, `Header`.

<h3 name="norm"> Text Normalization </h3>

- Transforming Text into a **Standard** form.
- e.g. 'gooood' and 'gud' transformed to 'good'
- Mapping of near **Identical** words such as 'stopwords', 'stop-words' and 'stop words' to just 'stopwords'
- Important when **Noisy**, **Misspelled**, **Slang** and **Out of Vocabulory** ( `OOV` ) Words are used. 
- **Out of Vocabulory** ( `OOV` ) : **Social Media** Comments, **Blog** Comments and **Text Messages**.

<h3 name="stop"> Stop Word </h3>

- Filter out **Useless** low information Words in a Sentence.
- Stop words are the **Filler** words.
- we can `Focus` on the **Important Words** instead.
- Search Engine only Search on the Basis of `Keywords`.
- Search Engines are programmed to `ignore` **Stop Words**.

How to `Remove` Stopwords Using NLTK

1. **Tokenize** and Compare with List of Stopwords and Drop that Words 
2. **Code** : Token for Token in Text if not in `Stopwords.words()` 

<h3 name="pos"> POS : Parts of Speech </h3>

- Classify the **Part of Speech** `tag` of each `Token`.
- Identify `Noun`, `Verb`, `Adjective` in Sentence.

<h3 name="bag"> Bag of Words </h3>

- Number of `occurence` of words in a paragraph or sentence.
- e.g. well well well, said john. {'well':3, 'said':1, 'john':1}
- Bag of words is represented in form of **dictionary**. 
- Expressed sentiments of words are defined by `polarity`
- `Polarity` : Positive `+1`, Negative `-1` or Neutral `0` 

<h3 name="vector"> Vectorization </h3>

- **Converting** Text to form `Numbers` that an **Algorithm** and a **Machine Learning Model** can `Understand` and `Learn`.
- **Process** of `Encoding` Text as `Integers` to Create `Feature Vectors`.

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
- Large `Collection` of Documents ( Accurate Grammer Phrases ) | Knowledge Base that can be used to infer and Validate Language Rules.

### Sparse Matrix
- A `Matrix` in which most entries are `0` helps in **Efficient Storage**.
- Stores only `Location` of **non zero elements**.

### Chunking
- Grouping `Individual` Pieces of Information into Bigger Piece.

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
Multi Dimensional Vector | Sparse Matrix
Capture Words Relationship with other Words | Captures the Importance of Word in a given Documment
Applied on each Word Individully | Applied to each Training Document
More Memory Intensive | Less Memory Intensive
Ideal for Single Word Problems | Ideal for Problems with Multiple Words or Document Files.

### One Hot Vector

![One Hot Vector](Image/OHV.png)

### BERT 
- Google's Pre trained **Bidirectional Encoder Representation for Transformers** used for **Transfer Learning**.

[Text Classification](https://towardsdatascience.com/text-classification-with-nlp-tf-idf-vs-word2vec-vs-bert-41ff868d1794)

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
