# Natural Language Processing

- Ability of a Computer to `Understand`, `Analyze`, `Manipulate` and `Generate` **Human Language**.
- Computer `Learn` and `Communicate` with Humans using Human Languages.
- NLP makes it possible for Computers to `Read`, `Write`, `Hear`, `Interpret` and `Measure` Sentiments. 
- Interaction between Computers and Humans using the Natural Language.

### NLTK ( Natural Language Toolkit ) 
- Open Source Tool Library created to make `NLP` Process in `Python`.

### Text Mining | Text Analysis 
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

### Applications : NLP in Real Life

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

### NLP Pipeline
1. Read **Raw** Text
2. Remove `Punctuation`
3. Remove `Stopwords`
4. Stemming | Lemmatizing
5. `Vectorize` Data to Prepare for Model Built
6. **Feature Engineering** ( **Creating** New Feature or **Transforming** Existing Features to get most out of Data )

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
1. **Porter** Stemmer ( **Oldest** but very **low Accuracy** : fairly > `fairli` )
2. **Snowball** Stemmer ( Better than **Porter** and **Lancaster** : fairly > `fair` )
3. **Lancaster** Stemmer ( **Fastest** with **Least Accuracy** )
4. Regex Based Stemmer

### Lemmatization
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

### Text Normalization
- Transforming Text into a **Standard** form.
- e.g. 'gooood' and 'gud' transformed to 'good'
- Mapping of near **Identical** words such as 'stopwords', 'stop-words' and 'stop words' to just 'stopwords'
- Important for **Noisy**, **Misspelled**, **Slang** and **Out of Vocabulory** ( `OOV` ) Words are used. 
- **Out of Vocabulory** ( `OOV` ) : **Social Media** Comments, **Blog** Comments and **Text Messages**.

### Stop Word
- Filter out **Useless** low information Words in a Sentence
- Stop words are the Filler words.
- we can `Focus` on the **Important Words** instead.
- Search Engine only Search on the Basis of `Keywords`.
- Search Engines are programmed to `ignore` **Stop Words**.

How to `Remove` Stopwords Using NLTK

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

### N Grams
- **Combinations** of `Adjacent` Words of length **N** in the Text

### Bigrams
- Form **Pair** of `Adjacent` Words from Sentence

### Trigrams
- Form Set of **Three** `Adjacent` Words

> Google Search **Suggests** Bigrams, Trigrams in there `Keyword` **Suggestions**.  

### Name Entity Recognition
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

### Word Cloud 
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

### Bag of Words
- **Polarity** : Positive ( +1 ), Negative ( -1 ) or Neutral ( 0 )
