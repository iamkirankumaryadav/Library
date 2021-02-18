# Object Oriented Programming

Structuring a Program by Bundling related **Properties** | **Attributes** and **Behaviors** into Individual **Objects**.

### Procedural Programming
- Structures a Program like a Recipe in that it provides a Set of Steps, in the form of **Functions** and **Code Blocks**, that flow Sequentially in order to complete task.

### Class
- A **Blueprint** for **Creating** an **Object**
- An object could represent a person with **Properties** like a Name, Age and Address and **Behaviours** such as **Walking**, **Talking** and **Running**.
- An Object could represent an email with **Properties** like **Recipient**, **Subject** and **Body** and **Behaviours** like **Adding Attachments** and **Sending Data**.
- Create **User Defined** Data Structures
- Defines **Functions** called as **Methods** (Identifies the Behaviors and Actions than an **Object** created from  the Class can perform with its Data.

**Define** a **Class** 
``` Python
class Student:
    pass
```

Python Class Names are written in **Capitalized Words**

**__\init_()***
- Like a Constructor Method (**Initialize** an **Object**)
- Evertime a New Object is Created, __init__() Sets the **Initial State** of the Object.
- Method is called when any new **Instance** of an **Object**  is Created.
- Initialize the **Attributes** of the Class.
- You can give any number of **Parameters**
- First Parameter will always be a variable **Self**

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
- Creating a **New Object Instance** from a Class is called **Instantiating** an Object.
- Every New Object Instance is located at a different Memory Address.

### Important Concepts in Class
1. Define a **Class**.
2. Instantiate an **Object** a **Class**.
3. Use **Attributes** and **Methods** to define the **Properties** and **Behaviors** of an Object.
4. Use **Inheritance** to Create **Child Classes** from a **Parent Class**.
5. Reference a method in a **Parent Class** using **super()**
6. Check if an **Object** inherits from another Class using **isinstance()** 
