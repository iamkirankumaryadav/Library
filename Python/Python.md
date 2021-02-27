# Python

1. Easy to Read, Learn and Write
2. **High Level** Programming Language ( Similar to English Language )
3. **Dynamically** Typed ( Object has no Type | Value has types | Object can Change its Data Type Dynamically )
4. Abundance of Libraries ( Pandas, NumPy, SciPy, etc. ) and Frameworks ( Django, Flask, etc. )
5. Useful for Data Science, Machine Learning, Artificial Intelligence and Web Development
6. Portable and Flexible ( Jupyter Language, Command Prompt, IDE, Text Editor, Google Colab )
7. Open Source with **Vibrant Community**.
8. Rich Docuumentation ( Python as well as Documentation of Libraries )
9. Interpreted Language ( Executes **Line by Line**)
10. Modularity : Working in Seperate **Modules** | Helps to **Focus** | Make **Development Easy** and Less Error prone.
11. Reusability : Modules can be easily reused by other part of the program.

| Interpreter                                                 | Compiler                                           |
| :---                                                        | :---                                               |
| Translate **One Statement** at a Time into **Machine Code** | Translate **Entire Program** into **Machine Code** |
| No Intermediate Object Code is generated                    | Intermediate Code is generated                     |
| Error Detection is Easy                                     | Error Detection is not Easy                        |

### PEP- 8
- Python Enhancement Proposal
- Style Guidelines for **Clean Code**.

### Memory Management 
- Python Memory Manager
- Private Heap Space
- All **Objects** are stored in Heap ( **Inaccessible** to the Programmers )
- In built **Garbage Collection** to **Recycle** the unused memory for the **Private Heap Space**.

### Decorator
- Add **Functionality** to an existing function without changing **Structure**.

### Built in Data types
1. None Type  
- Represents the **null | NULL values**

2. Numeric
- int : Integer, Hex, Octal and Binary Numbers 
- float : Decimal, Exponent and Floating Point Number
- complex : Complex Numbers with real + img
- bool : Boolean ( True | False )

3. Sequence
- list : Mutable
- tuple : Immutable
- range : Immutable Generated Numbers 
- str : Sequence of Characters
- dict : Mapping Key Value pairs
- set : Mutable Unordered Collection of Unique Values
- frozenset : Immutable Collection of Unique Values

### Protected 
- Attributes defined with Underscore (**\_name**)
- Still can be **Accessed** and **Modified** from outside the class.

### Private 
- Attributes defined with Double Underscore (**\_\_name**)
- Cannot be **Accessed** and **Modified** from outside directly

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

### Pickling
- **Serialization** : **Transforming** it into format that can be stored.
- Object can be **Serialized** into a **byte** stream and dumped as a file in the memory.
- **pickle.dump()**

### Unpickling
- **Deserialization**
- Object can be **deserialized** the **byte** stream to **recreate** the Object stored in the file and **load** the Object to Memory.
- **pickle.load()**

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
