---

title: "String Functions in PHP"
date: 2025-03-16 12:40:00
layout: post
categories: php
tags: [php, tutorial]
permalink: /php/string-functions/
---
# String Functions in PHP

PHP provides various built-in string functions to manipulate and process strings efficiently.

## Common String Functions

### 1. `strlen()` - String Length
Returns the number of characters in a string.
```php
<?php
$string = 'hai this is akhil';
echo "String Length: " . strlen($string);
?>
```
**Output:**
```
String Length: 17
```

### 2. `str_word_count()` - Word Count
Counts the number of words in a string.
```php
<?php
echo "Word Count: " . str_word_count($string);
?>
```
**Output:**
```
Word Count: 4
```

### 3. `strpos()` - Find Position of a Substring
Finds the position of the first occurrence of a substring in a string.
```php
<?php
echo "Position of 'is': " . strpos($string, 'is');
?>
```
**Output:**
```
Position of 'is': 7
```

### 4. Accessing Specific Character by Index
```php
<?php
echo "Character at index 4: " . $string[4];
?>
```
**Output:**
```
Character at index 4: t
```

### 5. `substr()` - Extract Substring
Extracts part of a string.
```php
<?php
echo "Substring (6,4): " . substr($string, 6, 4);
?>
```
**Output:**
```
Substring (6,4): this
```

### 6. `str_replace()` - Replace String
Replaces all occurrences of a search string with another string.
```php
<?php
echo str_replace('akhil', 'Amal', $string);
?>
```
**Output:**
```
hai this is Amal
```

### 7. `strtolower()` and `strtoupper()` - Convert Case
```php
<?php
echo "Lowercase: " . strtolower($string) . "<br>";
echo "Uppercase: " . strtoupper($string);
?>
```
**Output:**
```
Lowercase: hai this is akhil
Uppercase: HAI THIS IS AKHIL
```

### 8. `ucwords()` - Capitalize Each Word
```php
<?php
echo ucwords($string);
?>
```
**Output:**
```
Hai This Is Akhil
```

### 9. `trim()` - Remove Whitespace
Removes whitespace from the beginning and end of a string.
```php
<?php
echo "Trimmed String: " . trim('   hai working   ');
?>
```
**Output:**
```
Trimmed String: hai working
```

## Conclusion
String functions in PHP are essential for manipulating and processing text. Understanding them helps in writing efficient and effective PHP code.

