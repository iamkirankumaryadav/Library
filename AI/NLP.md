# Natural Language Processing

### Text Mining | Text Analysis 
- Deriving **Meaningful Information** from Natural Language **Text** and **Speech**.

### NLP
- Computer Learn and Understand from Human Languages.
- NLP makes it possible for Computers to `Read`, `Write`, `Hear`, `Interpret` and `Measure` Sentiments. 
- Interaction between Computers and Humans using the Natural Language.

### Process :

1. Human Talk to Machine.
2. Machine Capture Audio.
3. Convert Audio to Text.
4. Process Text Data (Interpret > Convert)
5. Convert Text to Audio.
6. Machine Talk | Reply to Human.

### Applications :

1. Google Translate.
2. Word Processor | Grammer Check in Microsoft Word.
3. Grammerly Grammer and Spelling Checking in Gmail.
4. IVR | Interactive Voice Response in Call Centers.
5. Voice Assistant : OK Google, Siri, Cortana and Alexa.
6. Chatbots
7. Customer Feedback Sentiment Analysis ( 😊🙂😔😡 )

### Tokenization
- `Break` | `Split` a **Sentence** | **Phrase** | **Paragraph** into `List` of **Individual Words**.

### Stemming 
- `Cut` end of the Words into its `Stem` Form.
- Remove `Suffix` and `Prefix` from the Word.
- Stem may not be an **Actual** Word.
- Easy for `Read` and `Compare`.
- e.g. Studies > Studi | Studying > Study

### Lemmatization
- `Reduce` Words into its `Base` Form.
- Used in Search Engines to Search by `Keywords`.
- `Lemma` is Actual Word.
- Better > Good.
- ( Consult, Consultant, Consultants, Consultation, Consulting ) > Consult

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

### Bigrams
- Form Pair of Words from Sentence

### Trigrams
- Form Set of Triple Words

### Name Entity Recognition
1. Recognize by Name ( Movie, Person, Location, Organization, Quantity Unit, Monetory Value | Financial Term )

### Syntax | Syntactic Analysis
- Syntactic Structure of Sentence or Strings.
- Analyze String by `Symbol`. 

### Sentiment Analysis
- Feeling, Emotion, Reaction, Satisfaction of User | Customer | Consumer expressing there Feedback and Reaction.

### Information Retrieval
- Process of Accessing and Retrieval of appropriate Information  from Text.
- e.g. Google Search

### Chunking
- Grouping `Individual` Pieces of Information into Bigger Piece.
