# Object Oriented Programming

Structuring a Program by Bundling related **Properties** | **Attributes** and **Behaviors** into Individual **Objects**.

### Procedural Programming
- Structures a Program like a Recipe in that it provides a Set of Steps, in the form of **Functions** and **Code Blocks**, that flow Sequentially in order to complete task.

### Object
- A **Collection** of **Data** (**Variables**) and **Methods** (**Functions**) that act on that **Data**.

An Object has two **Characteristics**
1. Attributes | Properties
2. Behaviour | Action


An object can be a person with **Attributes** like a **Name**, **Age** and **Address** and **Behaviours** such as **Walking**, **Talking** and **Running**.

The Concept of **OOP** in Python focuses on Creating **Reusable** Code | **DRY** (Don't Repeat Yourself)


### Class
- A **Blueprint** for **Creating** an **Object**.
- Contains **Attributes** and **Behaviour** of an Object.
- Create **User Defined** Data Structures.
- **class** is a **Keyword** used to **Define Class**.
- **Class Names** are written in **Capitalized Words**.
- Defines **Functions** called as **Methods** (Identifies the Behaviors and Actions than an **Object** created from  the Class can perform with its Data.

**Define** a **Class** 
``` Python
class Student:
    pass
```

### Object
- An Object (**Instance**) is an Instantiation of a Class.
- When Class is Defined, only the **Description** for an Object is **Defined**.
- No **Memory** or **Storage* is allocated.

### \__init\_()
- Like a Constructor Method (**Initialize** an **Object**)
- Evertime a New Object is Created, __init__() Sets the **Initial State** of the Object.
- Method is called when any new **Instance** of an **Object**  is Created.
- Initialize the **Attributes** of the Class.
- You can give any number of **Parameters**
- First Parameter will always be a variable **Self**

### self
- Instance Methods can **Access** Attributes and other Methods on the Same Objects.

``` Python
class Student:
    def __init__(self, name, age):
        self.name = name
        self.age = age
```

``` Python
class Student:

    # Class Attribute (Common Attribute for all Class Instances)
    school_name = "IES GNV"
    
    def __init__(self, name, age):
        self.name = name
        self.age = age
```

Class Attributes are Defined Directly beneath the First Line of the Class Name.
- Must always Assigned an **Initial Value**

### Instantiate an Object
- Process of **Creating** an **Object** is called **Instantiation**.
- Creating a **New Object Instance** from a Class is called **Instantiating** an Object.
- Every New Object Instance is located at a different Memory Address.

### Methods
- **Functions** defined inside body of a **Class**
- Defines **Behavior** | **Action** of an Object.

### Inheritance
- A Way of Creating a New Class for using Details of an Existing Class without Modifying it.
- The Newly Formed Class is known as a **Derived** Class (**Child Class**)
- The Pre Existing Class is Known as a **Base** Class (**Parent Class**)
- To use the \__init\__() method of the **Parent Class**, use **super()** Function inside \__init\__() method of **Child Class**.

### Encapsulation
- **Restrict Access** to Methods and Variables of Class.
- Prevents Data from **Direct Modification**.
- We Denote **Private Attribute** using single underscore(\_) or double underscore (\__)

### Polymorphism
- Ability to use a common **Interface** for Multiple forms (**Data Type**)
- Create a Common Function | Method that can be used by two different Classes.

### Important Concepts in Class
1. Define a **Class**.
2. Instantiate an **Object** a **Class**.
3. Use **Attributes** and **Methods** to define the **Properties** and **Behaviors** of an Object.
4. Use **Inheritance** to Create **Child Classes** from a **Parent Class**.
5. Reference a method in a **Parent Class** using **super()**
6. Check if an **Object** inherits from another Class using **isinstance()** 

### Benefits of Object Oriented Programming
- Makes Program easy to understand
- **Class** is Sharable, Code can be **Reused**.
- Data is **Safe** and **Secure** with **Data Abstraction**.
