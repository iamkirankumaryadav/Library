# Function

### User Defined Function

### Parameter vs Argument
- **Parameter** : **Defined** with Function
- **Argument** : Passed to Parameter at the Time of **Function Call**

``` Python
def function(parameter 1, parameter 2):
    """
    This is a Doctstring
    """
    print("The Message")

greet(argument 1, argument 2)
```

### Arbitrary Arguments
- When we don't know about How many Arguments we will Pass 

``` Python
def greet(*names):
    """
    Docstring
    
    parameters (data type) : about parameter
    """

    # names is an iterator with arguments (list, tuple, set, string)
    for name in names:
        print("Hello", name)

greet("Kirankumar", "Paramveer", "Gaurav", "Pranit")
```

### Gloabal Keyword
- Variable created **inside** a Function is a **Local** variable by default.
- Variable created **outside** a Function is a **Global** variable by default.
- To Declare **Global** variable inside a Function use **global** Keyword
