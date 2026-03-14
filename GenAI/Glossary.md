# Glossary

### Generative AI (GenAI)
AI built on ML that creates new content like text, image, audio, and video, based on patterns learned during training.

### Large Language Models (LLMs)
A GenAI that utilizes natural language processing techniques to generate huam-like text based on patterns from the huge amounts of text it was trained on.

### Model
- A program trained on large amount of data that processes inputs and produces outputs based on learned patterns.
- LLMs is a type of AI model, there are also models for generation of image, audio, video, and many other tasks.

### Training Data
- Data such as text, image, video, or audio that are used to teach AI models.
- The quality, quantity, and diversity of the training data significantly impacts how the system performs.
- If the training data is bad, the output will be bad (Garbage In, Garbage Out)

### AI Agents
- Autonomous or semi autonomous AI entity that can make decisions with some amount of independence.
- Example: Virtual Assistance that can book appointments, book food, book cab, book hotels, etc.

### Prompt
The input a user provides to an AI model to generate an output

### Bias
Skewed training data can lead to false outputs that can reproduce or amplify misinformation present in the training data.

### Hallucination
- When an AI model generates factually incorrect sounding or nonsense information.
- It is important to always fact-check AI outputs, especially for academic or professional use.

### Deepfakes
Highly realistic fake images, audio, and video generated using AI

### Guardrails
- Mechanisms to filter the inputs or outputs of GenAI to ensure the model is used ethically and safely.
- Guardrails are essential to prevent from biased, harmful, or inappropriate web content (inputs or outputs)

### Neural Network
Modeled after the human brain, neural networks are made up of interconnected layers of nodes that work together to process and analyze complex data.

### Deep Learning
A subset of ML that uses multilayered neural networks, including an input layer, often hundreds of hidden layers, and an output layer.

### Supervised Learning
An approach for training AI models where the model learns from a set of labeled examples called a training set.

### Unsupervised Learning
An approach for training AI models where the model learns from unlabeled data by understanding patterns and similarity.

### Reinforcement Learning
An approach for training AI models where the model learns through trial and error in which correct outputs result in reward and incorrect outputs result in penalty.

### Attention
- A mechanism that allows AI models to focus on the most relevant parts of an input when processing information.
- Models capture relationships between words regardless of distance, resulting in the ability to understand context and generate relevant content.

### Transformers
A type of architecture in deep learning that uses attention mechanism to process entire sequences of data simultaneously.

### Foundational Model
- AI models that are pre-trained on large amount of data to perform a wide range of generic tasks and can be fine tuned for specific tasks.
- This accelerates the development of AI as developers can adapt these foundation models rather than starting from scratch.

### Fine Tuning
The process of taking a pre-trained AI model and training it on a specific dataset for new use case or a certain task.

### Reinforcement Learning with Human Feedback (RLHF)
- A technique used to fine tune a pre-trained model through human feedback on the model's outputs.
- The process teaches AI systems to respond in ways that align with human preferences and values.

### Retrieval Augmented Generation (RAG)
- A method where the AI model retrieves information from external sources like documents (PDFs, DOCXs, PPTs, TXTs) and other user-uploaded material to help generate responses.
- Allows to create personal AI assistance on our own research materials or confidential data that was not included in the model's training data.

### Parameters
- The internal variables of an AI model learned from training data.
- Proprietary models like ChatGPT and Claude do not publiclt share their parameter counts.
- Open source models like Llama contains 17B parameters (According to Meta)

### Temperature
A parameter that controls the randomness of a model's responses where the higher temperature values generates more random and unpredictable outputs.

### Embeddings
- Representations of words or phrases as vectors in high-dimensional space where the location and distance between indicates their semantic similarity.
- Allows AI models to recognize synonyms, context, and semantic aspects.

### Token
The smallest unit of text an AI model processes, AI usage limits are often defined in terms of tokens.

### Context Window
- The maximum tokens thar an AI model can process simultaneously when generating a response.
- This is esentially the memory capacity of an AI model during an interaction.
- The larger context window helps the model to remember more information while generating the response.

 ### Application Programming Interface (API)
 API enables the developers to access the functionality of AI models and implement them into their own applications.

