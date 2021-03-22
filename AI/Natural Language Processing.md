# Natural Language Processing

1. <h4><a href="#nltk">NLTK</a></h4>
2. <h4><a href="#mine">Text Analysis | Text Mining</a></h4>
3. <h4><a href="#app">Real World Application</a></h4>
4. <h4><a href="#pipe">NLP Pipeline</a></h4>
5. <h4><a href="#token">Tokenization</a></h4>
6. <h4><a href="#stem">Stemming</a></h4>
7. <h4><a href="#lemma">Lemmatization</a></h4>
8. <h4><a href="#norm">Text Normalization</a></h4>
9. <h4><a href="#stop">Stop Word</a></h4>
10. <h4><a href="#bag">Bag of Words</a></h4>
11. <h4><a href="#vector">Vectorization</a></h4>
12. <h4><a href="#tfidf">TF-IDF</a></h4>
13. <h4><a href="#ngram">N Grams</a></h4>
14. <h4><a href="#vector">Vectorization</a></h4>
15. <h4><a href="#ner">Name Entity Recognition</a></h4>
16. <h4><a href="#cloud">Word Cloud</a></h4>
17. <h4><a href="#word2vec">Word2vec</a></h4>



- Ability of a Computer to `Understand`, `Analyze`, `Manipulate` and `Generate` **Human Language**.
- Computer `Learn` and `Communicate` with Humans using Human Languages.
- NLP makes it possible for Computers to `Read`, `Write`, `Hear`, `Interpret` and `Measure` Sentiments. 
- Interaction between Computers and Humans using the Natural Language.

<h3 name="nltk"> NLTK ( Natural Language Toolkit ) </h3>
- Open Source Tool Library created to make `NLP` Process in `Python`.

<h3 name="mine"> Text Mining | Text Analysis </h3>
- **Analyze** and **Understand** Text Data 
- Deriving **Meaningful Information** from Natural Language **Text** and **Speech**.

### Types of Text Data 
- Web, Blogs, Comments, Reviews and Notes
- Social Media : Messages, Hashtags, Reference
- Operations : Logs and Trails
- Emails ( Spam or Ham )
- Voice **Transcriptions** ( Videos )

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
3. Remove `Stopwords`
4. Stemming | Lemmatizing
5. `Vectorize` Data to Prepare for Model Built
6. **Feature Engineering** ( **Creating** New Feature or **Transforming** Existing Features to get most out of Data )

<h3 name="token"> Tokenization </h3>

- `Break` | `Split` a **Sentence** | **Phrase** | **Paragraph** into `List` of **Individual Words**.

<h3 name="stem"> Stemming </h3>

- Reducing **Derived** Words to there `Stem` Words.
- `Cut` end of the Words into its `Stem` Form.
- Remove `Suffix` and `Prefix` from the Word.
- Stem may not be an **Actual** Word.
- Easy for `Read` and `Compare`.
- e.g. Studies > Studi | Studying > Study

> Stemming is applied on **Tokens** ( `stem ( token )` ) 

### Why Stemming ?
- Reduce `Corpus` of Words
- Correlates Words with `Similar` Meanings.

### Types of Stemmers
1. **Porter** Stemmer ( **Oldest** but very **low Accuracy** : fairly > `fairli` )
2. **Snowball** Stemmer ( Better than **Porter** and **Lancaster** : fairly > `fair` )
3. **Lancaster** Stemmer ( **Fastest** with **Least Accuracy** )
4. Regex Based Stemmer

<h3 name="lemma"> Lemmatization </h3>
  
- Grouping together the **Derived forms** of Word so that they can be Analyzed as a `Single` ( Base ) form
- Actually `Transforms` words to the **Actual Root**.
- `Reduce` Words into its `Base` Form.
- Used in Search Engines to Search by `Keywords`.
- `Lemma` is Actual Word.
- Better > Good.

### WordNet Lemmatizer
- **Database** for `English`
- `Nouns`, `Verbs`, `Adjectives` and `Adverbs` are **Grouped** into Sets of **Cognitive Synonyms**. 
- Most Popular **Lemmatizer**
- e.g. { 'consult', 'consultation', 'consulting', 'consultant' } > consult

Stemming | Lemmatization
:--- | :---
**Speed** | **Accuracy**
Simply `Chops` End of the Word to `Stem` | **Converts** the Word to its **Meaningful** `Base` Form

### Text Preprocessing
- Map the Words wiith different Case to the same `Lowercase` form.

### Noise Removal
- Removing Characters, Digits and Pieces of Text that can `Interfere` with Text Analysis.
- `Punctuation` removal, `Special Character` removal, `Number` removal, `HTML` formatting removal, `Source Code` removal, `Header` removal.

<h3 name="norm"> Text Normalization </h3>

- Transforming Text into a **Standard** form.
- e.g. 'gooood' and 'gud' transformed to 'good'
- Mapping of near **Identical** words such as 'stopwords', 'stop-words' and 'stop words' to just 'stopwords'
- Important for **Noisy**, **Misspelled**, **Slang** and **Out of Vocabulory** ( `OOV` ) Words are used. 
- **Out of Vocabulory** ( `OOV` ) : **Social Media** Comments, **Blog** Comments and **Text Messages**.

<h3 name="stop"> Stop Word </h3>

- Filter out **Useless** low information Words in a Sentence
- Stop words are the Filler words.
- we can `Focus` on the **Important Words** instead.
- Search Engine only Search on the Basis of `Keywords`.
- Search Engines are programmed to `ignore` **Stop Words**.

How to `Remove` Stopwords Using NLTK

1. Tokenize 
2. Compare with List of Stopwords and Drop that Words ( Token for Token in Text if not in Stopwords.words( ) ) 

<h3 name="pos"> POS : Parts of Speech </h3>
- Classify the part of Speech `tag` of each `Token`.
- Identify Noun, Verb, Adjective in Sentence.

<h3 name="bag"> Bag of Words </h3>

- Number of `Occurence` of Words in a Paragraph or Sentence.
- e.g. Well well well, Said John
- Bag of Words is represented in form of **Dictionary** 
- **Polarity** : Positive ( +1 ), Negative ( -1 ) or Neutral ( 0 )

<h3 name="vector"> Vectorization </h3>

- **Converting** Text to form `Numbers` that an **Algorithm** and a **Machine Learning Model** can `Understand` and `Learn`.
- **Process** of `Encoding` Text as `Integers` to Create `Feature Vectors`.

<h3 name="tfidf"> TF - IDF </h3>

![TFIDF](Image/TFIDF.png)

- Term Frequency - Inverse Document Frequency
- Create a Document Term **Matrix** 
- One **Row** per **Document** ( Number of Time the Term appears in Document )
- One **Column** per **Word** in the **Corpus** ( Number of Documents containing the Word )
- Shows how Important a given **Word** is to the **Document** 

### Feature Vector
- An `N Dimensional Vector` of **Numerical Features** that Represents some `Object`.

### Different Types
1. Count Vectorization ( Create a **Document Term Matrix**   that represents **Count** of `Occurence` )
2. N Grams
3. Term Frequence - Inverse Document Frequency ( TD - IDF ) 

<h3 name="ngram"> N Grams </h3>

- **Combinations** of `Adjacent` Words of length **N** in the Text

### Bigrams
- Form **Pair** of `Adjacent` Words from Sentence

### Trigrams
- Form Set of **Three** `Adjacent` Words

> Google Search **Suggests** Bigrams, Trigrams in there `Keyword` **Suggestions**.  

<h3 name="ner"> Name Entity Recognition </h3>

1. Recognize Elements in Text by `Category` ( Movie, Person, Location, Organization, Quantity Unit, Monetory Value | Financial Term )
2. `Identification` | `Extraction` technique that automatically identifies named `Entities` in a Text and Classifies in Predefined Categories.

![NER](Image/NER.png)

### Syntax | Syntactic Analysis
- Syntactic Structure of Sentence or Strings.
- Analyze String by `Symbol`. 

### Sentiment Analysis
- Feeling, Emotion, Reaction, Satisfaction of User | Customer | Consumer expressing there Feedback and Reaction.

### Information Retrieval
- Process of **Accessing** and **Retrieval** of appropriate Information  from Text.
- **Extracting** Title, Text and Media from a Book, Artice or Simply Web Page.
- e.g. `Google Search`

<h3 name="cloud"> Word Cloud </h3>

- A **Graphical** Display of Words in a Corpus
- **Size** of Word based on number of **Occurences**
- Visual View of the Most Popular Terms

### Corpus | Corpora
- Large Collection of Documents ( Accurate Grammer Phrases ) | Knowledge Base that can be used to infer and Validate Language Rules.

### Sparse Matrix
- A **Matrix** in which most entries are `0`
- Efficient Storage
- Stores only `Location` of **non zero elements**.

### Chunking
- Grouping `Individual` Pieces of Information into Bigger Piece.

### Transformation
- Power Transformation ( Square, Square Root )
- Standardizing Data 

<h3 name="word2vec"> Word2vec </h3>
- **word2vec** Algorithm uses a Neural Network Model to Learn **Word Associations** from a Large Corpus of Text
- Once trained, can Detect Synonymous Words or Suggest Additional Words for a Partial Sentence ( Autocomplete | Predict Next Words )
