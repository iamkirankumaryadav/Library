NLP (Deals with interaction between computer and human language)

Corpus: A large collection of real world text data used to train and test NLP models (Generic and Specific) Newspapaer, Web, Social Media, Speech
NLTK: Opensource toolkit created for Python to make NLP process.
Tokenization: Breaking down text into smaller units for analysis
Stemming: Reducing words to its based form | Porter (Old, Low accuracy) | Snowball (Better and accurate) | Lancaster (Fast and least accuracy)
Lemmatization: Reducing words to its dictionary form using vocabulory and morphological analysis (Considering the context and meaning) WordNet 
Text Normalization: Consistent format, case conversion, punctuation removal, abbrevation expansion, spellcheck, stopwords removal, mapping of similar words, slang, OOV
Stop Words: Common words with little meaning are filtered out before processing text.
POS Tagging: Process of identifying and assigning/tagging a part of speech label to each words.
Word Embedding: Understand meaning and relationship between words, represent words as vectors in high dimension space, words with similar meaning are positioned close together in space.
Vectorization: Converting textual data to numerical vectors that an algorithm and ML model can understand and process.
1. Bag of Words: Represent documents based on word frequency 
2. TF-IDF: How many times the term appears in a document. More times the word appears means high TF, frequent words have low IDF, rare words have high IDF (Important words: High weight)
3. Word Embedding: Words with similar meaning are positioned close together in the space, capturing relationship and context.
4. Word2Vec: Continuous BoW (Predict current word based on surrounding words) | Skip Gram (Predict surrounding words based on single word) with a specific context window.
5. GloVe: Analyze the ratio of co-occurence probabilities between words. Each word is assigned with a uique vector in HD space, words with similar occurence pattern will have vector positioned close together
6. Doc2Vec: Represents entire document as numerical vector. Predict the document vector based on words within it. Model considers the words cooccurence patterns within a document.
                     Documents with similar meanings will have vectors closer together in HD space.
7. NGrams: Sequence of N words that appears together in a text. Grouped like chunks. | Unigram (N=1) | Bigram (N=2) | Trigram (N=3)
8. NER: Identifying and classifying named entites in text (words) and assigning labels (categories) | Helps to extract meaning, relationship, pattern, context, information from large amount of data

How to update NER?
- Incremental Training: SpaCy allows to update pre trained models with custom own data | Add new entities 
- Retraining: Retrain entire model with new entities.
- Rule Based Method: Update the existing rules, define pattern and context clues.
- Expand Dictionaries: Add key value pair for entities.

Word Cloud: A graphical way to see which word appears most in the piece of text | Analyze text | Identify words | Calculate frequency of each word | Build cloud.
Token: Basic units/words fed into LLM from a vocabulory
Embeddings: Vector representation that capture the meaning and relationship of words/tokens, allow the LLM to process them numerically.
Transformers: Neural Network Architecture, they use an attention mechanism that allows the transformers to focus on relevant parts of input.
Fine Tuning: Process of further training a pre-trained LLM on specific task dataset to specialize its capabilities.
Pre Training: Initial training phase where LLM ingests a huge text corpus to build broad language understanding.
Generative Models: LLMs that can generate new text continuations from prompts in an open ended way.
Perplexity: An evaluation metric quantifying how uncertain the LLM is about a text sample based on its probability.
Backpropagation: An algorithm used by LLM to adjust the weights based on error during training to improve performance.
