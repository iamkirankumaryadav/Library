<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# AI 🤖

Term | Definition
:--- | :---
**Data** | **Collection** of `Facts`
**Data Design** | How you **Organize** Information and Data.
**Data Strategy** | Management of `People`, `Prices` and `Tools` used in **Data Analysis**.
**Data Analytics** | Future Prediction or Forecasting.
**Data Visualization** | Graphical Representation of **Information**.
**Data Modeling** | Creating a Model for **Reporting** and **Forecasting** Business Decisions.
**Data Analysis** | **Collect**, **Transform** and **Organize** Data in order to Draw **Conclusion** from the past Data.
**Data Science** | **Science** of Extracting **Knowledge** and **Meaningful Insights** from **Structured** and **Unstructured Data**.
**Forecasting** | Making **Predictions** based on **Past** and **Present** Data.
**Training Data Set** | Data used to **Train** the Model ( Allow **Algorithm** to **Learn** from Data )
**Validation Data Set** | Data used to **Select the Best Model** ( **Optimize** Algorithm and **Hyperparameter** Settings )
**Test Data Set** | Data used to provide an **Evaluation**
**Predictive Modeling** | A Process that uses **Data** and **Statistics** to **Predict** outcomes with **Data Models**
<a href='#ml'>Machine Learning</a> \| <a href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">ML</a> | Field of **Science** that gives Computer the Ability to **Learn** from **Data** without being **Explicitly** Programmed
<a href='#ai'>Artificial Intelligence</a> | **Simulation** of **Human Intelligence** in **Machines** to **Think** like **Humans** and **Mimic** their **Actions**
<a href='#dl'>Deep Learning</a> | **ML** inspired by **Human Brains** like **Detect Object**, **Recognize Speech**, **Translate Speech** and **Make Decisions**
<a href='#nn'>Neural Network</a> | **Simulation** of **Human Brain** in **Computers** to **Think** like Humans to make **Decisions** and **Mimic** the **Actions** 
<a href='https://github.com/KIRANKUMAR7296/Library/blob/main/AI/Natural%20Language%20Processing.md'>NLP</a> | Science that gives **Machine** the **Ability** to **Read**, **Understand** and **Communicate** through **Human Language** 
<a href='#cv'>Computer Vision</a> \| <a href="https://github.com/KIRANKUMAR7296/Library/blob/main/AI/Computer%20Vision.md">CV</a> | Field of AI that **Trains Computers** to **Understand** the **Visual World** like a **Human Eye** 
<a href='#iot'>Internet of Things</a> | **Network** of **Physical Objects** embedded with **Sensors**, **Connecting** and **Exchanging Data** with each others 
**Data Mining** | Turn Raw Data into Useful **Information**, Discovering **Patterns** in Large Dataset
**Cloud** | A Place to Keep Data **Online**, rather than Computer Hard Drive
**Ecosystem** | Various Elements that Interact with One another in Order to **Produce**, **Manage**, **Store**, **Organize**, **Analyze** and **Share** Data
Data Driven Decision Making | Using Facts to Guide Business Strategy
Analytical Skills | Qualities and Characteristics associated with **Solving** Problems using **Facts**

---

[AI](https://www.reaktor.com/work/artificial-intelligence/) | [Elements of AI](https://www.elementsofai.com/) | [Building AI](https://buildingai.elementsofai.com/) | [Real World Applications](https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/IBM%20Machine%20Learning.md) | [Data Science Elite](https://github.com/KIRANKUMAR7296/Library/blob/main/Data%20Science/Primer%20Steps.md)

AI > ML > DL

<h1 name='ai'>AI | Artificial Intelligence</h1>

- Computers Perform the Task that Normally requires Human Intelligence.
- Mimic the Intelligence or Behavioural Patterns of Humans.
- Ability to Learn and Reason like Humans.
- Make Smart Computers like Human to Solve Complex Problems
- Deals with Structures | Semi Structured and Unstructured Data

Types :
1. **Weak** AI ( **Narrow** AI ) | Good in `One` Task
2. **General** AI ( Computer as Smart as Human )
3. **Strong** AI ( **Super** AI ) Reduce Human Error | **24 x 7** Availability | Digital Assistance | Fast and Accurate Decisions.

<h1 name='ml'>Machine Learning | <a href="https://github.com/KIRANKUMAR7296/Library/blob/main/Machine%20Learning/Machine%20Learning%20Models.md">ML</a></h1>

- Subset of AI
- Art of Extracting Knowledge from Data
- Computers Learn from Data and Act like Humans.
- Computers Learn from Past Data without being Explicitly Programmed.
- Find Patterns and Relationship between Features and Labels.
- Improve Automatically through Experience.
- A Set of Algorithms that Allows Computers to Learn from Data without being Explicitly Programmed.
- Deals with Structured and Semi Structured Data.

Types :
1. Supervised Learning
2. Unsupervised Learning
3. Semisupervised Learning ( Small amount of Labeled Data + Large Amount of Unlabeled Data )
4. Reinforcement Learning

Applications :
1. Predictions
2. Classifications
3. Segmentation
4. Recommendation System
5. Google Search Algorithm
6. Facebook Auto Friend Tagging Suggestions

<h1 name='dl'>DL | Deep Learning</h1>

- AI Function that mimics the workings of **Human Brain** in Processing Data 
- Use in Detecting Objects, Recognizing Speech, Translating Languages and Making Decisions.
- Perform ML Inspired by Human Brain Networks of Neurons.
- Able to Learn without Human Supervision.
- Artificial Neural Networks Adapt and Learn from Vast Amounts of Data.
- Based on **Artificial Neural Network**

<h1 name='nn'>Neural Network</h1>

- **Pattern Matching** through **Connection** of many **Small Functions** to Create one very **Powerful Function** ( Like **Neurons** in **Brains** ) 
- Also Called as **Deep Neural Network** ( **Deep** Refers to Number of `Hidden Layers` Typically )
- Neural Network Connects Simple Nodes | Neurons | Units
- Collection of Such Neurons form a **Network** ( Recognize Relationships in Data Set )
- Neural Network are **Designed** to Adapt to **Dynamic Input**

### Components of Neural Network

### 1. Neurons
- Nodes Receives Data Input and Combine Inputs with Activation Function + Bias 

### 2. Connections and Weights
- Nodes are Connected through **Edges**
- A **Weight** is Assigned on each Connection | Edges
- Bias is added at Nodes

### 3. Activation Functions
- A Function that takes in the **Weighted Sum** of all the **Inputs** from Previous Layer + **Bias** and Generates Output for Next Layer.

1. **Sigmoid** : form S Shaped Curve ( Range between 0 and 1 )  
2. **tanh** : Hyperbolic Tangent ( Range between -1 and 1 )
3. **ReLu** : Rectified Linear Unit ( **0** for **Negative Input** and **Same Input** for Inputs > 0 ) max(0, x)
4. **Leaky ReLu** : ( Allow **Small Negative** Inputs and Returns Same Input for Inputs > 0 ) max(0.1x, x)
5. **ELU** : Exponential Linear Unit ( Similar to Linear for Inputs > 0 )

### 4. Learnable Parameters
- Parameters that will be Learned by the Model during the Training ( **Weights** and **Biases** )

### Artificial Neural Network | ANN 

- Simulate the Way the **Human Brain** Analyzes and Process Information.
- Foundation of AI | Solve Difficult Problems that are Impossible for Human Brain.
- Finding **Patterns** and **Relationships** between Data like Human Brains.

- Application
1. Foreign Exchange Trading
2. Forcasting Weather Patterns
3. Speech Recognition

### Convolutional Neural Network | <a href="https://github.com/KIRANKUMAR7296/Library/blob/main/AI/CNN.md" target='_blank'>CNN</a>
 
Designed for working with **Two Dimensional Image** Data

1. Decoding Facial Recognition
2. Analyzing Documents
3. Understanding Climate
4. Image Caption Generation
5. Object Classification

### Recurrent Neural Network | RNN

- Feed Forward and **Feedback** Netwrok 
- Better for **Sequential** Data
- Application
1. Language Translation ( Text Data )
2. Speech Recognition
3. Video Tagging
4. Image Description

### CNN ( Faster ) > RNN > ANN

<h1 name='nlp'>NLP | Natural Language Processing</h1>

- Branch of AI
- Computer Learn | Gain | Understand from Human Languages.
- Interaction between Computers and Humans using the Natural Language.
- Objective of NLP is to Read, Interpret, Understand and Make Sense of the Human Languages.
- NLP rely on ML to Derive Meaning from Human Lanuages.

Process :
1. Human Talk to Machine. 
2. Machine Capture Audio.
3. Convert Audio to Text.
4. Process Text Data ( Interpret > Convert )
5. Convert Data to Audio.
6. Machine Talk | Reply to Human.

Applications :
1. Google Translate 
2. Word Processor | Grammer Check in Microsoft Word.
3. IVR | Interactive Voice Response in Call Centers.
4. Voice Assistant : OK Google, Siri, Cortana and Alexa.

<h1 name='cv'>Computer Vision</h1>

- Computers Gain High Level Understanding from Digital Images or Videos.
- Works on Pattern Recognition.
- Understand and Automate the Task of Human Visual System.
- Detecting **Image** | **Object** and Labeling has Surpassed Humans.
- Faster than Human Reaction and 99% Accuracy
- High Amount of Visual Data ( Images and Videos ) with Processing Capabilities.

Applications :
1. Self Driving Cars
2. Facial Recognition
3. Augmented Reality and Virtual Reality
4. Health Care ( X Ray and MRI Scan )
5. Video Motion Analysis 
6. Image Segmentation ( Camera Detects the Multiple Faces in a Group Selfie )
7. Scene Reconstruction ( 3D Model Creation in Architecture )
8. Image Restoration ( Filtering Blur Images and Removing Noise )

Task :
1. Object Classification : Image consist a Cat
2. Object Detection: Classification + Localization : Multiple Objects can be Detected in the Image ( Dog | Cat | Rat )
3. Object Identification : Type of Object in an Image
4. Instant Segmentation : Extract the Images from its Edges | Boundaries.

<h1 name='iot'>IoT | Internet of Things</h1>

- Connecting Everything in the World to the Internet
- Gives Ability to Send and Receive Information.
- Sea of Data
- Extending Power of Internet beyond Computers and Smartphones to a Whole Range of other Things in the Environments.
- A System of **Interconnected** Computing Devices, Mechaniacal Devices and Digital Machines | Gadgets.
- Every Machine, Device, Object, Animal and Person is Provided with Unique Identifier.
- Ability to Transfer Data over a Network without Human to Human or Human to Machine Interaction. 
- Integrate and Control Everything in the House using Device.

Simple Examples :
1. Search : We can Search | Upload | Download  Any Data, Image, Song, Documents, Audio Stored at one Place from Anywhere in this World.
2. Wearables : Fitness Bands | Smart Watches Measures Human Health and Captures Behavioural Patterns and Transfer Data to Database.
3. Health : Wearables consisting of Sensors Monitor Humans Health Patterns and Alert on some Vital Sign | Risk Situation.
4. Traffic Monitoring : Traffics are Visible on Maps, Fastest Route or Alternate Routes.
5. Fleet Management : Connect Fleets of Vehicles with the Drivers and Co Drivers, Fuel, Tyre Pressure, GPS Tracking and Many More.
6. Smart Farming : Quality of Soil, Amount of Water Required, Suitable Crop for Type of Land
7. Hospitality : Electronic Key and Availability of Rooms.
8. Smart Grid and Energy Saving : Grid of Solar Panels, Amount of Energy it Generates, Maintenance

Data Science Process :
1. Obtain Data : Gather Data from Relevant Sources.
2. Scrub : Clean Data to Formats that Machine Understands.
3. Explore : Find Significant Patterns and Trends using Statistical Methods.
4. Model : Construct Models to Predict | Forecast | Estimate. 

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
