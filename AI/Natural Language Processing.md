<p align='right'><a align="right" href="https://github.com/iamkirankumaryadav/Library/blob/main/Interview.md">Back to Questions</a></p>

<h1 align="center"> Natural Language Processing</h1>

<table align="center">
  <tr>
    <td>1. <a href="#nlp">NLP</a> </td>
    <td>2. <a href="#nlu">NLU</a></td>
    <td>3. <a href="#nlq">NLQ</a></td>
    <td>4. <a href="#nlg">NLG</a></td>
  </tr>
  <tr>
    <td>5. <a href="#nltk">NLTK</a> </td>
    <td>6. <a href="#stem">Stemming</a></td>
    <td>7. <a href="#bag">Bag of Words</a></td>
    <td>8. <a href="#ner">Name Entity Recognition</a></td>
  </tr>
  <tr>
    <td>9. <a href="#mine">Text Analysis | Text Mining</a> </td>
    <td>10. <a href="#lemma">Lemmatization</a></td>
    <td>11. <a href="#vector">Vectorization</a></td>
    <td>12. <a href="#cloud">Word Cloud</a></td>
  </tr>
  <tr>
    <td>13. <a href="#app">Real World Application</a> </td>
    <td>14. <a href="#norm">Text Normalization</a></td>
    <td>15. <a href="#tfidf">TF-IDF</a></td>
    <td>16. <a href="#word2vec"> Word2vec </a></td>
  </tr>
  <tr>
    <td>17. <a href="#pipe">NLP Pipeline</a> </td>
    <td>18. <a href="#stop">Stop Word</a></td>
    <td>19. <a href="#ngram">N Grams</a></td>
    <td>20. <a href="#doc2vec"> Doc2vec </a></td>
  </tr>
  <tr>
    <td>21. <a href="#token">Tokenization</a> </td>
    <td>22. <a href="#pos">Part of Speech</a></td>
    <td>23. <a href="#vector">Vectorization</a></td>
    <td>24. <a href="#corpus">Corpus</a></td>
  </tr>
</table>

<h2 name="nlp"> Natural Language Processing (NLP) </h2>

- A field of `AI` that deals with the interaction between computers and human language.
- Ability of computer to `read`, `understand`, `learn`, `analyze`, `translate`, `generate` and `communicate` using **human language**.
- Interaction between `computers` and `humans` using the natural language.
- **Natural Language Understanding (NLU)** and **Natural Language Generation (NLG)** are both subfields of **NLP**
- **Core Idea:**  Equipping computers with the ability to understand, interpret, and manipulate human language.
- NLP holds the potential to revolutionize the way we interact with machines and unlock a new era of human-computer collaboration.  

**Why is NLP Important?**

* **Human-like Interaction:** NLP allows users to interact with computers more naturally and intuitively, using everyday language instead of complex codes.
* **Unlocks Information:** NLP helps computers process and make sense of the massive amount of textual data available in the world, opening doors to new discoveries and insights. 
* **Automates Tasks:** NLP can automate many tasks that previously required human intervention, such as document classification,  sentiment analysis, and  machine translation.

**What Does NLP Do?**

* **Understanding Text:** Analyzing the meaning and intent behind written words, considering factors like grammar, context, and sentiment.
* **Generating Text:** Creating human-readable text formats like news articles, chatbot responses, or even creative content using Natural Language Generation (NLG).
* **Machine Translation:** Converting text from one language to another while preserving the original meaning.
* **Speech Recognition:** Converting spoken language into text, enabling voice-activated applications.
* **Text Summarization:** Extracting the key points from a lengthy piece of text and condensing it into a shorter, more manageable format.

**How Does NLP Work?**

* **Machine Learning:** Training algorithms on vast amounts of text data to identify patterns and relationships within language.
* **Linguistics:** Leveraging the knowledge of language structure and grammar to understand how words and sentences function.
* **Statistical Methods:** Analyzing the statistical properties of language to identify patterns and extract meaning.

**Applications of NLP**

* **Search Engines:** Helping users find the information they need by understanding natural language search queries.
* **Virtual Assistants:** Powering assistants like Siri and Alexa to understand user requests and respond helpfully. 
* **Social Media Analysis:** Extracting insights from social media conversations to understand public opinion and trends.
* **Machine Translation:** Breaking down language barriers by enabling seamless communication across cultures. 
* **Customer Service Chatbots:** Providing 24/7 customer support through chatbots that can answer questions and resolve issues.

<h2 name="nlu"> Natural Language Understanding (NLU) </h2>

- `NLU` focuses on getting computers to actually understand the meaning behind human language.
- It goes beyond just the literal words and considers factors like grammar, context, and sentiment.
- NLU is crucial for tasks like question-answering systems or chatbots that need to grasp the intent behind a user's query.
* **Goal:** Enable machines to understand the meaning and intent behind human language, similar to how humans comprehend each other.
* **Challenges:** Human language is full of complexities, ambiguity, sarcasm, slang, and cultural references, that make it difficult for computers to grasp the true meaning.

**How Does NLU Work?**

1. **Parsing:**
- Breaking down sentences into their grammatical components like phrases and clauses.
- This helps understand the relationships between words.

2. **Semantic Analysis:**
- Unveiling the meaning of words and phrases. This goes beyond just the dictionary definition and considers context. 

3. **Discourse Analysis:**
- Understanding how sentences flow together and relate to each other within a conversation or text.
- This helps grasp the overall theme and intent.

5. **Machine Learning:**
- NLU systems are often powered by machine learning models trained on vast amounts of text data.
- These models learn to identify patterns and relationships within language, allowing them to make better sense of new inputs.

**Applications of NLU**

* **Chatbots and Virtual Assistants:** NLU empowers chatbots and virtual assistants to understand user queries and requests more accurately, enabling them to provide helpful and informative responses.
* **Machine Translation:** NLU is essential for accurate machine translation, as it allows the system to understand the nuances of the source language and translate it naturally into the target language.
* **Sentiment Analysis:** NLU is used to analyze the sentiment or emotion behind the text, which is valuable for tasks like gauging customer satisfaction or understanding public opinion on social media.
* **Question Answering Systems:** NLU allows machines to comprehend complex questions and answer them accurately by finding relevant information from a vast knowledge base.
* **Text Summarization:** NLU can be used to automatically generate summaries of lengthy pieces of text, helping people quickly grasp the key points.

<h2 name="nlq"> Natural Language Query (NLQ) </h2>

- `NLQ` isn't as widely used as `NLP`, `NLU`, and `NLG`, but it's related.
- `NLQ` refers to formulating a question or request in natural language.
- For instance, instead of using a specific search bar format, you might ask a search engine a question in plain English like "What is the capital of France?".
- NLQ highlights the goal – of allowing users to interact with computers using natural human language.
* **Focus:** Expressing questions or requests in a way that is natural and intuitive for humans.
* **Examples:** Instead of writing a complex SQL query to filter a database, you could ask an NLQ system a question like "What are the top-selling products this month?".
* Similarly, instead of using specific search operators on a search engine, you could ask "What is the capital of France?"

### **Benefits of NLQ:**

* **Accessibility:** NLQ makes information systems more accessible to a wider range of users, even those without any formal training in query languages.
* **Ease of Use:** NLQ allows users to interact with systems in a way that is more natural and intuitive, reducing the need to learn complex syntax.
* **Efficiency:** For simple queries, NLQ can sometimes be faster and more efficient than using traditional query languages.

**Challenges of NLQ:**

* **Ambiguity:** Natural language can be ambiguous, and NLQ systems can sometimes misinterpret the user's intent.
* **Complexity:** For complex queries, NLQ systems may not be able to fully capture all of the nuances of the user's needs.
* **Limited Capabilities:** NLQ systems are still under development, and their capabilities may be limited compared to traditional query languages.

**Where is NLQ Used?**

* **Search Engines:** Many search engines now allow users to submit queries in natural language.
* **Business Intelligence Tools:**  NLQ is being integrated into business intelligence tools like Power BI, Google Sheets (Duet AI) and Microsoft Excel (Copilot) to allow users to ask questions about their data using natural language.
* **Virtual Assistants:** Virtual assistants like Siri and Alexa rely on NLQ to understand user requests.
* **Customer Service Chatbots:** Chatbots can use NLQ to answer customer questions and resolve issues.

<h2 name="nlg"> Natural Language Generation (NLG) </h2>

- NLG flips the script/query and focuses on machines generating human-like text.
- NLG takes data and translates it into natural language that a human can understand.
- Examples include machine translation tools or chatbots that can provide summaries of factual topics.

**How Does NLG Work?**

1. **Data Preparation:**
- The first step involves getting the data in a format that the NLG system can understand.
- This might involve cleaning the data, organizing it, and potentially converting it into a structured format.

2. **Template Selection:**
- NLG systems often rely on pre-defined templates that act as a blueprint for generating text.
- These templates include placeholders for specific information that gets filled in later.

3. **Content Generation:**
- Once the template is chosen, the NLG system uses its knowledge and understanding of language to fill in the placeholders with relevant information and ensure grammatical correctness and coherence.

4. **Review and Refinement:**
- The generated text might undergo review and refinement to ensure it sounds natural and matches the desired style or tone.

**Applications of NLG**

1. **Customer Service:**
- NLG can be used to generate automated responses to frequently asked questions or create personalized reports for customers.

2. **Finance:**
- NLG can be used to create financial reports, summaries of investment performance, or even generate automated news articles about financial markets.

3. **Marketing:**
- NLG can be used to personalize marketing content or generate targeted product descriptions.

4. **Media and News:**
- NLG can be used to automate sports reports, weather forecasts, or even create summaries of news articles.

5. **Healthcare:**
- NLG can be used to generate patient reports, summarize medical findings, or create personalized treatment plans.

As NLG technology continues to develop, we can expect to see even more innovative applications emerge in the future.

<h2 name="corpus">Corpus</h2>

- Corpus: A large collection of real-world text data showing how those words are used in sentences, paragraphs, and entire documents.
- Corpora are essential for training NLP models, as they provide the models with the raw language data they need to learn from.
- Corpus linguistics, collections of spoken and written texts are compiled and analyzed.
- Corpora are used to train ML models for a variety of NLP tasks, such as sentiment analysis, machine translation, and part-of-speech tagging.

It helps us to find:
- How does the meaning of a word change depending on the context?
- How has the way we use language changed over time?
- How do different people (e.g., Doctors, Teenagers | Formal, Informal, Casual, Slang) use language differently?
- Corpora can be specific (subject/domain oriented) or generic (common/public) depending on the research goal.

Types of corpora:
1. **Newsgroups corpora:** Collections of words from newsgroup posts, newspapers, novels, tweets, poetry, etc.
2. **Web corpora:** Collections of text scraped from the web (Biggest corpus)
3. **Social media corpora:** Collections of comments from social media platforms such as Instagram, Twitter and Facebook. 
4. **Speech corpora:** Collections of written text, transcriptions of spoken languages, multilingual

<h2 name="nltk"> NLTK ( Natural Language Toolkit ) </h2>

- Open source toolkit or library created to make NLP process in Python.

<h2 name="mine">Text Mining | Text Analysis</h2>

- Analyze and understand text data (Expression, context, action, grammar)  
- Derive meaningful information from natural language text and speech.

### Text mining process:
1. Collecting text data
2. Cleaning and preprocessing (Remove irrelevant, punctuation, formatting, and stop words)
3. Analysis techniques
4. Result Interpretation

### Types of text data 
- Web, blogs, articles, feeds, comments, reviews, emails, and notes.
- Social media: Messages, hashtags, references, comments, etc.
- Operations: Logs and trails.
- Emails: Formal, informal, business, casual, request, application (Spam or Ham)
- Voice transcriptions and subtitles.

### Process :

1. Humans talk to machines.
2. Machine capture human audio.
3. Convert audio to text.
4. Process text data. 
5. Convert processed text to audio.
6. Machine reply to human.

<h2 name="app"> Applications : NLP in real life </h2>

1. Google Translate. (Speech to text)
2. Email `spam` filter (Search for texts related to spam email)
3. Google search and Gmail auto-complete (Prediction of **next words** and **suggestions**) 
4. Word processor | Grammer check | Autocorrect in Microsoft and Google productivity Apps.
5. Grammerly | Grammer correction and spelling correction in Gmail and Outlook.
6. IVR | Interactive voice response in call centres.
7. Voice assistant: `Google Assistant`, `Apple Siri`, `Microsoft Cortana` and `Amazon Alexa`.
8. Chatbots.
9. Customer feedback sentiment analysis (😊🙂😔😡)
10. Document summarization: Read articles and newspapers (Blind people)
11. Text classification.
12. Part of speech `tagging` (**Part of speech** of the corresponding word)

<h2 name="pipe">NLP Pipeline</h2>

1. Read **raw** text.
2. Remove `Punctuations`
3. Create `Tokens` (Create a list by splitting every `word`)
4. Remove `Stopwords`
5. Apply Stemming | Lemmatization (Reduce derived words to `stem` words)
6. `Vectorize` data to prepare for model built (Convert text to `number`)
7. **Feature Engineering** (**Creating** new feature or **transforming** existing features to get most out of data)

<h2 name="token">Tokenization</h2>

- The process of breaking down text into smaller units, such as words, punctuations, special characters, characters, etc.
- This is the first step in many NLP tasks, as it allows the model to process the text in the most manageable way.
- Computer works better with smaller chunks, easier to understand, identify important words.

```python
Word = "Hi, my name is Kirankumar"
["Hi", ",", "my", "name", "is", "Kirankumar"]
```

<h2 name="stem">Stemming</h2>

- Stemming is a process of reducing a word to its `stem` | `root` | `base` form.
- Stemming removes common suffixes and prefixes from the word (ing, es, s, ed)
- For example, the words "playing", "played", "plays", and "players" would all be stemmed down to "play"
- Stemming can be helpful for tasks like information retrieval, as it allows the model to match words with different suffixes.
- Reduces data size (saves storage space, improves processing speed)

`Stemming` is applied on `tokens` 

```python
stem(token) 
```

### Types of Stemmers
1. **Porter** Stemmer (**Oldest** with very **low accuracy** : fairly > `fairli`)
2. **Snowball** Stemmer (**Better** than **Porter** and **Lancaster** : fairly > `fair`)
3. **Lancaster** Stemmer (**Fastest** with **least accuracy**)

<h2 name="lemma">Lemmatization</h2>

- A more sophisticated form of stemming that takes into account the context of a word to determine its base form.
- Grouping the **derived forms** of words so that they can be analyzed as a `single` base form.
- Actually `transforms` words to the **actual root**.
- Used in **search engines** to search by `keywords`. `Lemma` is an actual word (Better > Good)

### WordNet Lemmatizer

- **Database** for `English` (Most popular **Lemmatizer**)
- `Nouns`, `Verbs`, `Adjectives` and `Adverbs` are **grouped** into sets of **Cognitive Synonyms**.  
- e.g. {'consult', 'consultation', 'consulting', 'consultant'} - consult

Stemming | Lemmatization
:--- | :---
**Speed** | **Accuracy**
Simply `strips` end of the word to `stem` | **Converts** the word to its **meaningful** `base` form.

### Text Preprocessing

- Transforming raw text data into a format that computers can understand and analyze.
- Cleaning and preparing the text: Removing irrelevant information, fixing errors, fixing spelling mistakes, converting to lowercase.
- Breaking down the text: Tokenization 
- Understand the meaning: Stemming, lemmatization, Part-of-Speech tagging
- Extracting information: Sentiment analysis, information retrieval

### Noise Removal

- Removing characters or pieces of text that can interfere with text analysis.
- Remove punctuation, special characters, numbers, formatting, source code, header, etc.

<h2 name="norm">Text Normalization</h2>

- Transforming text into its standard consistent format to make it easier for computers to understand.
- e.g. 'gooood' and 'gud' transformed into 'good'.
- Case conversion: Putting all in the same case (Either uppercase or lowercase) depending on the situation.
- Punctuation Removal: Unnecessary punctuations are not relevant for analysis.
- Abbreviations and Acronym Expansion: Clarifies the meaning of the text for computer processing (OMG, ASAP, OOO)
- Spelling Correction: Fixing typos and grammatical errors to ensure consistency and error-free.
- Stop Words Removal: Remove common words that don't carry any meaning on their own (a, an, the, is, of)
- Mapping of near identical words such as 'stopwords', 'stop-words' and 'stop words' to just 'stopwords'
- Important when **noisy**, **misspelled**, **slang** and **out of vocabulory** ( `OOV` ) words are used. 
- **Out of vocabulory** ( `OOV` ) : **Social media** comments, **blog** comments and **text messages**.

<h2 name="stop">Stop Word</h2>

- Common words that don't carry any meaning on their own are filtered out before processing text.
- Stop words are filler words like `a`, `an`, `in`, `on`, `and`, `the`, `or`, etc.
- Stopwords are ignored and removed so that we can focus on important words instead.
- Search engines only search based on `keywords`
- Search engines are programmed to `ignore` **stop words**.
- These words don't provide much meaning on their own, so filtering them out can improve the efficiency of NLP tasks.

How to `remove` stopwords using NLTK

1. `Tokenize` and compare with the list of predefined `stopwords` and `drop` those words. 

```python
Token for Token in the text if not in `Stopwords.words()` 
```

<h2 name="pos">POS : Parts-of-Speech Tagging</h2>

- The process of assigning a grammatical tag (such as noun, verb, adjective) to each word in a sentence.
- POS tagging can be helpful for tasks like sentiment analysis and machine translation.

<h2 name="bag"> Bag of Words </h2>

- A method for representing text documents as a collection of words.
- Number of `occurrence` of words in a paragraph or sentence.
- e.g. well well well, said John. {'well':3, 'said':1, 'john':1}
- Bag of words is represented in the form of **dictionary**. 
- Expressed sentiments of words are defined by `polarity`
- `Polarity`: Positive `+1`, Negative `-1` or Neutral `0`
- In a BOW model, the order of the words is not taken into account, only the frequency of each word.
- BOW models are a simple and effective way to represent text data, but they can lose some important information about the structure of the text.

<h2 name="vector"> Vectorization </h2>

- **Converting** text to form `Numbers` that an **algorithm** and a **ML model** can `understand` and `learn`.
- **Process** of `encoding` text as `integers` to create `feature matrix`

<h2 name="tfidf">TF - IDF</h2>

![TFIDF](Image/TFIDF.png)

- **Term Frequency** - **Inverse Document Frequency**.
- `TF`: Number of `times` term `appears` in document / Number of `terms` in document.
- `IDF`: `log(N/n)` 
- `N`: Number of `documents`
- `n`: Number of `documents` a `term` appeared in.
- Shows how `important` a given `word` is to the `document`
- The `IDF` value of a `rare` word is `high` and `low` for a `frequent` word.

### Feature Vector
- An `n-dimensional vector` of **numerical features** that represents some `object`.

### Different Types
1. **Count** vectorization ( Create a **document term matrix**   that represents `count` of `occurrence` )
2. **N Grams** ( Combination of `adjacent` words )
3. **Term Frequency** - **Inverse Document Frequency** ( `TD - IDF` ) 

<h2 name="ngram"> N Grams </h2>

- **Combinations** of `adjacent` words of length `N` in the text.
- A sequence of n words. N-grams are commonly used in NLP tasks such as language modelling and machine translation.
- Bigrams (2-grams) and trigrams (3-grams) are the most common types of n-grams used in NLP.

### Bigrams

- Form **pair** of `adjacent` words from the sentence.

### Trigrams

- Form set of **three** `adjacent` words.

`Google Search` **suggests** `bigrams`, and `trigrams` in their `keyword` **suggestions**.  

<h2 name="ner"> Name Entity Recognition </h2>

1. **Recognize** elements in the text by `category`  
2. `Movie`, `Person`, `Location`, `Organization`, `Quantity Unit`, `Monetary Value` | `Financial` terms.
3. Automatically identify the `entity` name in a text and classify it in **predefined categories**.

![NER](Image/NER.png)

### Syntax | Syntactic Analysis
- Syntactic structure of `sentence` or `strings`
- Analyze string by `symbol`

### Sentiment Analysis
- `Feeling`, `emotion`, `reaction`, `satisfaction` of the user, customer or consumer expressing their `feedback`

### Information Retrieval
- Process of `accessing` and `retrieval` of appropriate information  from text.
- **Extracting** `title`, `text` and `media` from a `book`, `article` or simply `HTML tags` from `web page`
- e.g. `Google Search`

<h2 name="cloud"> Word Cloud </h2>

- A graphical display of words in a `corpus`.
- The `size` of the word is based on the number of `occurrences`
- **Visual** view of the most popular terms.

### Corpus | Corpora
- Large `collection` of documents ( Accurate grammar phrases ) 
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
    <th colspan='2'>Vector: Numeric representation of word and document ( One Hot Vector )</th>
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
    <th colspan='2'>Use the neural network to learn word association from a large corpus of text</th>
  </tr>
  <tr>
    <th colspan='2'>Detect synonymous words or suggest next words for a partial sentence ( Autocomplete | Search bar suggestion )</th>
  </tr>
 </table>

Word2Vec Matrix | TF-IDF Matrix
:--- | :--- 
Multi-dimensional vector | Sparse matrix
Capture word's relationship with other words | Captures the importance of the word in a given document.
Applied on each word individually | Applied to each training document.
More memory intensive | Less memory intensive.
Ideal for single-word problems | Ideal for problems with multiple words or document files.

### One Hot Vector

![One Hot Vector](Image/OHV.png)

### BERT 
- Google's pre trained **bidirectional encoder representation for transformers** used for **transfer learning**.

[Text Classification](https://towardsdatascience.com/text-classification-with-nlp-tf-idf-vs-word2vec-vs-bert-41ff868d1794)

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
