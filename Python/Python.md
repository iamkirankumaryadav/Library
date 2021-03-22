# Python

1. Easy to **Read**, **Learn** and **Write**
2. **High Level** Programming Language ( Similar to English Language )
3. **Dynamically** Typed ( **Data Type** of Object is based on its **Value** | Object can Change its Data Type Dynamically )
4. Abundance of **Libraries** ( Pandas, NumPy, SciPy, etc. ) and **Frameworks** ( Django, Flask, etc. )
5. Useful for Data Science, Machine Learning, Artificial Intelligence and Web Development
6. **Portable** and **Flexible** ( Jupyter Language, Command Prompt, IDE, Text Editor, Google Colab )
7. Open Source with **Vibrant Community**
8. Rich **Documentation** ( Python as well as Documentation of Libraries )
9. **Interpreted** Language ( Executes **Line by Line**)
10. **Modularity** : Working in Seperate **Modules** | Helps to **Focus** | Make **Development Easy** and Less Error Prone.
11. **Reusability** : **Modules** can be easily reused by other part of the Program

<table align="center">
        <tr>
                <th>Interpreter</th>
                <th>Compiler</th>
        </tr>
        <tr>
                <td>Translate One Statement at a Time into Machine Code</td>
                <td>Translate Entire Program into Machine Code</td>
        </tr>      
         <tr>
                <td>No Intermediate Object Code is generated</td>
                <td>Intermediate Code is generated</td>
        </tr>    
        <tr>
                <td>Error Detection is Easy</td>
                <td>Error Detection is not Easy</td>
        </tr>
</table>      

### PEP- 8
- Python Enhancement Proposal
- Style Guidelines for **Clean Code**.

### Memory Management 
- Python **Memory Manager** | Private **Heap Space**
- All **Objects** are stored in Heap ( **Inaccessible** to the Programmers )
- In built **Garbage Collection** to **Recycle** the unused memory for the **Private Heap Space**.

### Decorator
- A **Decorator** takes in a **Function**, Adds some **Functionality** to that existing **Function** and Returns it without changing **Structure**.

<table align="center">
        <tr>
                <th>Protected</th>
                <th>Private</th>
        </tr>
        <tr>
                <td>Attributes defined with Underscore ( _name )</td>
                <td>Attributes defined with Double Underscore ( __name )</td>
        </tr>      
         <tr>
                <td>Can be Accessed and Modified from outside the Class</td>
                <td>Cannot be Accessed and Modified from outside directly</td>
        </tr>               
</table>      

### Self
- Define an **Instance** or an Object of a class.
- It helps to distinguish between the **Methods** and **Attributes** of a class.

### \_\_init\_\_
- A **Constructor Method**
- Automatically called to **Allocate** Memory when any new **Object | Instance** is created.
- It helps to distinguish between the **Methods** and **Attributes** of a class.

### break
- **Terminates** the loop and control flow to the Statement after the body of loop.

### continue
- **Terminates** the **Current Iteration** of the Statement
- **Skip** the rest of the Code in Current Iteration
- Control Flows to the Next Iteration of the Loop.

### pass
- Empty Statement 

<table align="center">
        <tr>
                <th>Pickling</th>
                <th>Unpickling</th>
        </tr>
        <tr>
                <td>Serialization</td>
                <td>Deserialization</td>
        </tr>      
         <tr>
                <td>Serialize into Format that can be Stored</td>
                <td>Deserialize Stored Byte Stream into File and Load the Object into Memory</td>
        </tr>    
         <tr>
                <td>pickle.dump( )</td>
                <td>pickle.load( )</td>
        </tr>   
</table>      

### Generators
- Functions that returns an **Iterable Collection** of items.

### help()
- Display **Documentation** of Modules, Classes, Functions, Keywords.

### dir()
- List of Valid **Attributes** and **Methods** of an Object based on its Type and State.

### Define Function

``` Python
def functionname( parameter1, parameter2):
        pass
```        

### Call Function

```Python
functionname(argument1, argument2)
```

### Position of Arguments

```Python
def example(arg_1, arg_2, *args, **kwargs):
```
