---

title: "Introduction to Arrays in PHP"
date: 2025-03-16 12:50:00
layout: post
categories: php
tags: [php, tutorial]
permalink: /php/arrays-introduction/
---
# Introduction to Arrays in PHP

Arrays in PHP allow you to store multiple values in a single variable. They can hold elements of different data types and are useful for organizing and manipulating data efficiently.

## Creating an Array
You can create an array using the `array()` function or square brackets `[]`.
```php
<?php
$names = ['amal', 'akhil'];
echo "Second element: " . $names[1];
?>
```
**Output:**
```
Second element: akhil
```

## Numeric Indexed Arrays
These arrays store elements with numeric keys starting from 0.
```php
<?php
$numbers = [2, 4, 6, 8, 10];
echo "Third element: " . $numbers[2];
?>
```
**Output:**
```
Third element: 6
```

## Displaying an Array using `var_dump()`
`var_dump()` provides detailed information about the data type and structure of an array.
```php
<?php
echo '<pre>';
var_dump($names);
echo '</pre>';
?>
```
**Output:**
```
array(2) {
  [0]=> string(4) "amal"
  [1]=> string(5) "akhil"
}
```

## Using a Function to Display an Array
Encapsulating array display logic in a function can improve code organization.
```php
<?php
function display($values) {
    echo '<pre>';
    var_dump($values);
    echo '</pre>';
}
display($names);
display($numbers);
?>
```
**Output:** (for `$names` array)
```
array(2) {
  [0]=> string(4) "amal"
  [1]=> string(5) "akhil"
}
```

**Output:** (for `$numbers` array)
```
array(5) {
  [0]=> int(2)
  [1]=> int(4)
  [2]=> int(6)
  [3]=> int(8)
  [4]=> int(10)
}
```

## Printing Arrays using `print_r()`
`print_r()` provides a simpler, more human-readable output.
```php
<?php
print_r($names);
?>
```
**Output:**
```
Array ( [0] => amal [1] => akhil )
```

## Conclusion
Arrays in PHP are powerful and flexible data structures used for storing and manipulating data. Understanding their usage is fundamental for effective programming in PHP.

