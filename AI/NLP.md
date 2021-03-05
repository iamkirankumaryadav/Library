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
- `Normalize` | `Reduce` | `Cut` end of the Words into its `Stem` Form.
- Remove `Suffix` from the Word.
- Stem may not be an **Actual** Word.
- Easy for `Read` and `Compare`.
- e.g. Studies > Studi | Studying > Study

### Lemmatization
- `Normalize` | `Reduce` Words into its `Base` Form.
- Used in Search Engines to Search by `Keywords`.
- `Lemma` is Actual Word.
- Better > Good.
- ( Consult, Consultant, Consultants, Consultation, Consulting ) > Consult

### Stop Word
- Meaningless Words in a Sentence
- Search Engine only Search on the Basis of `Keywords` and not by whole Sentence.

How to `Remove` Stopwords
Using NLTK
1. Tokenize 
2. Compare with List of Stopwords and Drop that Words ( Token for Token in Text if not in Stopwords.words( ) ) 

Using spaCy

### Part of Speech

### Name Entity Recognition
1. Recognize by Name ( Movie, Person, Location, Organization, Quantity Unit, Monetory Value | Financial Term )


### Syntax
- Syntactic Structure of Sentence or Strings.

### Chunking
- Grouping `Individual` Pieces of Information into Bigger Piece.
