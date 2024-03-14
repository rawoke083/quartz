---
title: 1-Overview
date: 
---

> [!tip] IMPORTANT
> *BOTH* are OOP based
>
> ### PHP: ALL variables declarations needs a ``$`` in front example `$myName`
>
> ### PHP: Never put ``WordPress`` On Your CV
>


### Hello World (PHP)


```php
<?php

// Define a function named 'helloWorld' that expects two string parameters
// and returns a string. The ': string' part specifies the return type of the function.
function helloWorld(string $greeting, string $target): string {
    // Concatenate the strings using the '.' operator and return the result.
    // Unlike Python, PHP uses '.' for string concatenation.
    return $greeting . ", " . $target . "!";
}

// Initialize two variables with string values.
$greeting = "Hello";
$target = "World";

// Call the 'helloWorld' function with the variables as arguments and echo the result.
// 'echo' is used in PHP to output strings to the webpage or console.
echo helloWorld($greeting, $target);
?>
```

### Hello World (Python)
```python
# Define a function named 'hello_world' that takes two strings as input
# and returns a string. The type hints (e.g., 'greeting: str') are used for indicating 
# the expected type of the function parameters and return type.
def hello_world(greeting: str, target: str) -> str:
    # Use an f-string (formatted string literal) for string concatenation.
    # F-strings allow you to embed expressions inside string literals using curly braces.
    return f"{greeting}, {target}!"

# Initialize two variables with string values.
greeting = "Hello"
target = "World"

# Call the 'hello_world' function with the variables as arguments and print the result.
# 'print' is used in Python to output strings to the console.
print(hello_world(greeting, target))
```




### Summary
> [!info] IMPORTANT
> | Feature | PHP | Python |
> |---------|-----|--------|
> | **Paradigm** | OOP | OOP |
> | **Variable Declaration** | Prefixed with ``$``, loosely typed | Implicit declaration, strong typing with optional hints |
> | **Arrays & Dictionaries** | Uses associative arrays for both | Differentiates between lists and dictionaries |
> | **Standard Library** | Extensive, global namespace access | Organized into modules, requires imports |
> | **Error Handling** | Uses both exceptions and special error values | Primarily uses exceptions |

