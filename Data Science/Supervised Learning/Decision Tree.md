<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# Decision Tree

- Used for both **Regression** and **Classification** Referred to as **CART** ( **Classification** and **Regression Tree** )
- **Upside Down** Approach
- Top Node ( **Root** ) | Decisions ( **Nodes** ) | Splits of Trees ( **Edges** | **Branches** ) | Terminal Node ( **Leaf** )
- Growing a **Tree** involves deciding on **Which Features to Choose ?** and **What Conditions to Use ?** for splitting.
- We should also know when to **Stop**
- **Pruning** : Removing **Features** that are not important.

 Continuous can be Converted into **Binary** or **Boolean** by Setting **Threshold**.
- Set the Value to **False** or **0** if it is less than the **Median**.
- Set the Value to **True** or **1** if it is greater than the **Median**.

**Information Gain** is used to Choose Right Node
- Information Gain is a Meausre of how much we know about **Y** after looking at **X**.
- We Select the Feature as Node that Splits the Data very well.
- Attribute with **Highest** Information Gain | **Low** Entropy is Selected as **Best Attribute** to Split upon.

e.g. 
- Now you are taking My Interview you asked few Questions,
- You might have set a Threshold that if i know this Concepts, 
- based on my answers you can decide that iam suitable for this Role or not.

- Growing Tree to more Depth may lead to **Overfitting**.
- Control the Depth of Tree by using Parameter `max_depth`

### Advantages of Decision Tree

1. **Decision trees** can learn **Non Linear** Relationships.
2. **Individual Trees** are prone to Overfitting but Improves when **Ensembled**.

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>
