# Types of **Distribution**.

# Density Curve

> **Density Curve** helps us to **Visualize** the overall shape of a distribution. 

- We use **Histogram** to represent **Frequency Distribution** of Data ( Number of Data Points in given **Intervals** )

![Regular to Relative](Image/RegularRelative.png)

- **Regular Frequency Distribution** can be converted into **Relative Frequency Distribution** ( **Proportion** | **Percentage** )

![How](Image/How.png)

- Relative Frequency Distribution : **Divide** Each Interval **Data Points** with **Total** Number of Data Points in a Dataset.

![Density](Image/Total.png)

- **Total Area** of any type of **Distribution** is always **1** or **100%**

> Density Curve gives a better Picture about how the Dataset is distributed. 

## Discrete Events.

- **Finite** number of outcomes : Die | Picking a Card : 

### 1. Uniform Distribution

![Uniform Distribution](Image/Uniform.png)

- **X ~ U ( 3 , 7 )**
- Variable **X** follows an **Uniform Distribution** ranging from 3 to 7.
- Events with **Finite** outcomes. 
- All the outcomes have Equal | **Same** Probability. 
- Flip a Coin ( H | T )
- Roll a Dice ( 1 | 2 | 3 | 4 | 5 | 6 )

### 2. Bernoulli Distribution

- **X ~ Bern ( p )**
- Variable **X** follows a **Bernoulli Distribution** with **p** ( probability | likelihood ) of success. 
- Event with only 1 Trial and 2 Possible Outcomes ( True or False | Yes or No | 1 or 0 ) 
- We know the **Probability** of Outcome.
- If probability of one outcome is **p**(1) the probability of an other outcome is **1 - p**(0).
- E ( X ) = p or ( 1 - p ) | p > 1 - p
- **Expected Outcome** Probability of X : **p** | **Alternative Outcome** : **1 - p**
- Variance : p * ( 1 - p )
- A Coin flip | A Single True or False Question | Vote between 2 Parties.

### 3. Binomial Distribution

- **X ~ B ( n , p )**
- Variable **X** follows a **Binomial Distribution** with **n** trials and **p** ( probability | likelihood ) of success in each **Individual Trial**.
- **Sequence** | **Trials** of **Identical Bernoulli Events**.
- Flipping a Coin **Twice** | Rolling two Dies | Quiz of 10 True or False Questions.

### 4. Poisson Distribution

- **X ~ Po ( lambda )** 
- Number of **Occurences**.
- lambda : **Frequency** with which an **Event** happens or not within a specific interval of **Time**. 
- Number of **Goals** in Football | Number of **Baskets** in Basketball.
- e.g. a Fire Fly lights up 3 times in 10 Seconds.


## Continuous Events.

- **Infiinite** number of outcomes : Time | Distance : 

### 1. Normal Distribution | Gaussian Distribution | Bell Shaped Curve

![Normal Distribution](Image/ND.png)

- **X ~ N ( mean, variance )** 
- Variable **X** follows a **Normal Distribution** with **Mean** and **Variance**. 
- Normal Events in Nature. 
- Average Height of Person (**Exceptions** are considered as **Outliers**).
- Majority of Data is centered around **Mean**.
- Graph is **Symmetric** around **Mean**.

### 68, 95, 99.7 Law

![68 95 99.7 Law](Image/68_95_99.png)

![68 Law](Image/68.png)

- **68 %** of Outcomes fall withins **1** Standard Deviation

![95 Law](Image/95.png)

- **95 %** of Outcomes fall withins **2** Standard Deviation

![99.7 Law](Image/997.png)

- **99.7 %** of Outcomes fall withins **3** Standard Deviation
- **Outliers** are **Extremely Rare** in Normal Distribution.

### 2. Standard Normal Distribution 

- **X ~ N ( mean = 0 , variance = 1 )** 
- Variable **X** follows a **Normal Distribution** with **Mean** = 0 and **Variance** = 1. 
- Standardizing
- Moving Graph to the Left or Right until Mean = 0.
- **Transformation** : **Alter** every elements of a **Distribution** to get **New Distribution**.
- Z = X - Mean / Standard Deviation.

![AS](Image/AS.png)

- **Addition** and **Subtraction** will move the Distribution on **X Axis** to **Left** or **Right**.

![MD](Image/MD.png)

- **Multiplication** and **Division** will **Contract** or **Expand** on **Y Axis**.

### 3. T Distribution

- **X ~ t ( k )** 
- Variable **X** follows a **t Distribution** with k **Degree of Freedom**.
- **Small Sample Size** approximation of a Normal Distrbution.
- Used for **Hypothesis Testing** with **Limited Data**.
- Tails are Fat at the both ends.

### 4. Chi Squared Distribution  

- **X ~ chi<sup>2</sup> ( k )** 
- Variable **X** follows a **chi<sup>2</sup> Distribution** with k **Degree of Freedom**.
- E( X ) = k
- Var ( X ) = 2k
- Few Events in Real Life.
- Used in **Statistical Analysis** ( **Hypothesis Testing** and Computing **Confidence Intervals** ).
- Determine the **Goodness of Fitness**.
- Distribution ( **X Axis** ) Starts from **Zero** and **Asymmetric** in Nature.
- It is Squared therefore only **Positive**.
- Rapid changing Event follows **Exponential Distribution**.
- Forecast and Prediction Events follows **Logistic Distribution**. (Which Team will Win, Weather Forecast)

