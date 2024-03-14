
---
title: Flow Control
date: 
---


> [!example] PHP 

```php
<?php
$temperature = 75; // Temperature in degrees Fahrenheit

// If-else statement
if ($temperature > 80) {
    echo "It's too hot!\n";
} elseif ($temperature < 60) {
    echo "It's too cold!\n";
} else {
    echo "The weather is perfect!\n";
}
?>

```

<br />

> [!faq] Python

```python
temperature = 75  # Temperature in degrees Fahrenheit

# If-elif-else statement
if temperature > 80:
    print("It's too hot!")
elif temperature < 60:
    print("It's too cold!")
else:
    print("The weather is perfect!")
```


<br /><br />

## Looping Mechanisms
> [!example] PHP


```php
<?php
// For loop
for ($i = 1; $i <= 5; $i++) {
    echo "PHP Loop iteration: $i\n";
}


//  Foreach (Notice the usage of index )
$colors = ["Red", "Green", "Blue"];

foreach ($colors as $index => $color) {
    echo "Color $index: $color\n";
}


// While loop
$counter = 5;
while ($counter > 0) {
    echo "PHP Counting down: $counter\n";
    $counter--; // Decrement counter
}
?>

```
<br />

> [!faq] Python

```python
# For loop (Python uses 'range' for numeric loops)
for i in range(1, 6):  # Range goes from 1 to 5
    print(f"Python Loop iteration: {i}")

# While loop
counter = 5
while counter > 0:
    print(f"Python Counting down: {counter}")
    counter -= 1  # Decrement counter

```


## Looping  None-Primitives
> [!example] PHP

```php
//Assoc Array (like a dict in python)
$user = [
    "name" => "John Doe",
    "age" => 30,
    "email" => "john.doe@example.com"
];

//Notice how we get the index (key) and value
foreach ($user as $key => $value) {
    echo "$key: $value\n";
}

```


> [!faq] Python

```python

colors = ["Red", "Green", "Blue"]

# List
for index, color in enumerate(colors):
    print(f"Color {index}: {color}")


# Dictionary
user = {
    "name": "John Doe",
    "age": 30,
    "email": "john.doe@example.com"
}

for key, value in user.items():
    print(f"{key}: {value}")

```
