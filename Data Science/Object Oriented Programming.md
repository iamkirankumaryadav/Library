# Object Oriented Programming

Structuring a Program by Bundling related **Properties** | **Attributes** and **Behaviors** into Individual **Objects**.

### Procedural Programming
- Structures a Program like a Recipe in that it provides a Set of Steps, in the form of **Functions** and **Code Blocks**, that flow Sequentially in order to complete task.
- 
### Class
- A **Blueprint** for **Creating** an **Object**
- For **Instance**, an object could represent a person with **Properties** like a Name, Age and Address and **Behaviours** such as **Walking**, **Talking** and **Running**.
- An Object could represent an email with **Properties** like **Recipient**, **Subject** and **Body** and **Behaviours** like **Adding Attachments** and **Sending Data**.
- Create **User Defined** Data Structures
- Defines **Functions** called as **Methods** (Identifies the Behaviors and Actions than an **Object** created from  the Class can perform with its Data.

**Define** a **Class** 
``` Python
class Student:
    pass
```

Python Class Names are written in **Capitalized Words**

**__init_()***
- A Constructor Method
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
