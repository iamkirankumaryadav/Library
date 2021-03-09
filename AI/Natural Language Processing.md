# Natural Language Processing

- Ability of a Computer to `Understand`, `Analyze`, `Manipulate` and `Generate` **Human Language**.
- Computer `Learn` and `Communicate` with Humans using Human Languages.
- NLP makes it possible for Computers to `Read`, `Write`, `Hear`, `Interpret` and `Measure` Sentiments. 
- Interaction between Computers and Humans using the Natural Language.

### NLTK ( Natural Language Toolkit ) 
- Open Source Tool Library created to make `NLP` Process in `Python`.

### Text Mining | Text Analysis 
- Deriving **Meaningful Information** from Natural Language **Text** and **Speech**.

### Process :

1. Human Talk to Machine.
2. Machine Capture Audio.
3. Convert Audio to Text.
4. Process Text Data ( Interpret > Convert )
5. Convert Text to Audio.
6. Machine Talk | Reply to Human.

### Applications : NLP in Real Life

1. Google Translate. ( Speech to Text )
2. Email `Spam` Filter ( Search for Texts related to Spam Email )
3. Google Search and Gmail Auto Complete ( Prediction of **Next Words** ) 
4. Word Processor | Grammer Check | Auto Correct in Microsoft Word. 
5. Grammerly | Grammer Correction and Spelling Correction in Gmail.
6. IVR | Interactive Voice Response in Call Centers.
7. Voice Assistant : `Google` OK Google, `Apple` Siri, `Microsoft` Cortana and `Amazon` Alexa.
8. Chatbots
9. Customer Feedback Sentiment Analysis ( 😊🙂😔😡 )
10. Document Summarization : Read Article and Newspaper ( Blind People )
11. Text Classification
12. Part of Speech **Tagging** ( **Part of Speech** of Corresponding Word )

### Tokenization
- `Break` | `Split` a **Sentence** | **Phrase** | **Paragraph** into `List` of **Individual Words**.

### Stemming 
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
1. **Porter** Stemmer
2. Snowball Stemmer
3. Lancaster Stemmer
4. Regex Based Stemmer

### Lemmatization
- Grouping together the **Derived forms** of Word so that they can be Analyzed as a `Single` form ( Base )
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
Speed | Accuracy
Simply `Chops` End of the Word | Informed `Analysis` to Create Group of Words with `Similar` Meaning

### Normalization
- Normalize Words : Converting all Text to Same Case, removing Punctuation, Converting Number to Words.

### Stop Word
- Filter out **Useless** Words in a Sentence
- Stop words are the Filler words.
- Search Engine only Search on the Basis of `Keywords`.
- Search Engines are programmed to `ignore` **Stop Words**.

How to `Remove` Stopwords
Using NLTK
1. Tokenize 
2. Compare with List of Stopwords and Drop that Words ( Token for Token in Text if not in Stopwords.words( ) ) 

### POS : Parts of Speech
- Classify the part of Speech `tag` of each `Token`.
- Identify Noun, Verb, Adjective in Sentence.

### Bag of Words
- Number of `Occurence` of Words in a Paragraph or Sentence.
- e.g. Well well well, Said John
- Bag of Words is represented in form of **Dictionary** 

### Vectorization
- **Converting** Text to form `Numbers` that an **Algorithm** and a **Machine Learning Model** can `Understand` and `Learn`.
- **Process** of `Encoding` Text as `Integers` to Create `Feature Vectors`.

### Feature Vector
- An `N Dimensional Vector` of **Numerical Features** that Represents some `Object`.

### Different Types
1. Count Vectorization ( Create a **Document Term Matrix**   that represents **Count** of `Occurence` )
2. N Grams
3. Term Frequence - Inverse Document Frequency ( TD - IDF ) 

### Bigrams
- Form Pair of Words from Sentence

### Trigrams
- Form Set of Triple Words

### Name Entity Recognition
1. Recognize Elements in Text by `Category` ( Movie, Person, Location, Organization, Quantity Unit, Monetory Value | Financial Term )
2. `Identification` | `Extraction` technique that automatically identifies named `Entities` in a Text and Classifies in Predefined Categories.

### Syntax | Syntactic Analysis
- Syntactic Structure of Sentence or Strings.
- Analyze String by `Symbol`. 

### Sentiment Analysis
- Feeling, Emotion, Reaction, Satisfaction of User | Customer | Consumer expressing there Feedback and Reaction.

### Information Retrieval
- Process of **Accessing** and **Retrieval** of appropriate Information  from Text.
- **Extracting** Title, Text and Media from a Book, Artice or Simply Web Page.
- e.g. `Google Search`

### Corpus | Corpora
- Large Collection of Documents ( Accurate Grammer Phrases ) | Knowledge Base that can be used to infer and Validate Language Rules.

### Chunking
- Grouping `Individual` Pieces of Information into Bigger Piece.
