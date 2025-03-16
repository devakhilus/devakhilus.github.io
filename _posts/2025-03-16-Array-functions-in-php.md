---
title: "Array Functions in PHP"
date: 2025-03-16 13:55:00
layout: post
categories: [php]
tags: ["php", "tutorial"]
permalink: /php/array-functions/
---

# Array Functions in PHP

PHP provides a wide range of built-in functions to manipulate arrays efficiently. This tutorial covers some of the most commonly used array functions.

## 1. Counting Elements in an Array (`count()`)
```php
<?php
$ids = [20, 17, 30, 25, 40, 15, 29];
echo "Total Elements: " . count($ids);
?>
```
**Output:**
```
Total Elements: 7
```

## 2. Sorting an Array (`sort()`)
```php
<?php
sort($ids);
print_r($ids);
?>
```
**Output:**
```
Array ( [0] => 15 [1] => 17 [2] => 20 [3] => 25 [4] => 29 [5] => 30 [6] => 40 )
```

## 3. Adding Elements (`array_push()`)
```php
<?php
array_push($ids, 200);
print_r($ids);
?>
```
**Output:**
```
Array ( [0] => 20 [1] => 17 [2] => 30 [3] => 25 [4] => 40 [5] => 15 [6] => 29 [7] => 200 )
```

## 4. Removing the Last Element (`array_pop()`)
```php
<?php
array_pop($ids);
print_r($ids);
?>
```

## 5. Removing the First Element (`array_shift()`)
```php
<?php
array_shift($ids);
print_r($ids);
?>
```

## 6. Adding an Element at the Beginning (`array_unshift()`)
```php
<?php
array_unshift($ids, 205);
print_r($ids);
?>
```

## 7. Extracting a Portion (`array_slice()`)
```php
<?php
$id2 = array_slice($ids, 2, 4);
print_r($id2);
?>
```

## 8. Replacing Elements (`array_splice()`)
```php
<?php
array_splice($ids, 0, 1, 77);
array_splice($ids, 1, 1, 65);
print_r($ids);
?>
```

## 9. Summing Array Values (`array_sum()`)
```php
<?php
echo "Sum of ID array: " . array_sum($ids);
?>
```

## 10. Searching for an Element (`array_search()`)
```php
<?php
$users = ['akhil', 'amal', 'akshaya', 'appu', 'anamika'];
echo "Index of 'amal': " . array_search('amal', $users);
?>
```

## 11. Checking if an Element Exists (`in_array()`)
```php
<?php
if (in_array('manu', $users)) {
    echo "Element is there";
} else {
    echo "Element is not there";
}
?>
```

## 12. Converting a String to an Array (`explode()`)
```php
<?php
$str = 'man,cap,dog';
$arraystr = explode(',', $str);
print_r($arraystr);
?>
```

## 13. Converting an Array to a String (`implode()`)
```php
<?php
echo implode(', ', $users);
?>
```

## Conclusion
Understanding and utilizing array functions in PHP enhances code efficiency and makes data manipulation more straightforward.

