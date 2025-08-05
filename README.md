# Ganim Medical | Codebase Conventions

Using Python as our sample language for code:

## Naming conventions

* We use snake_case naming rather than CamelCase as much as possible.  For example:

```
GanimEmployees = [...] # This is incorrect
ganim_employees = [...] # This is correct
```

## Logging conventions

## Function conventions

### Function modularity, outsourcing, and minimalism

### Function documentation

### Function precondition tests and exceptions

* Functions must tests for all possible invalid arguments, unless doing so is computationally expensive.  For example, a square root function which does not handle imaginary numbers must ensure the argument is not a negative real number before proceeding with function logic.  In `Python`, it could look like this:

```
def square_root(x):

    # Preconditions
    assert isinstance(x, (int, float)), "x must be an int or float"
    assert x >= 0, "x must be non-negative"
    
    # Logic
    ... # Take the square root here

```
