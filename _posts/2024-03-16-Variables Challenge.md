---

title: "PHP Variables Challenge"
date: 2025-03-16 12:00:00
layout: post
categories: php
tags: [php, tutorial]
permalink: /php/variables-challenge/
---

# PHP Variables Challenge

In this challenge, we will work with variables and string concatenation to dynamically generate a web page.

## Challenge Code

```php
<?php
$title = 'Introduction to PHP';
$author = 'John Doe';
$body = 'PHP (Hypertext Preprocessor) is a widely used server-side scripting language that has revolutionized web development. With its simplicity, flexibility, and vast community support, PHP has become the backbone of countless dynamic websites and web applications.';
$pageTitle = 'Brad\'s PHP Blog | ' . $title;
?>

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title><?= $pageTitle ?></title>
</head>

<body>
    <main>
        <h1><?= $title ?></h1>
        <p>
            By:
            <?= $author ?>
        </p>
        <p>
            <?= $body ?>
        </p>
    </main>
</body>

</html>
```

## Explanation
- `$title`, `$author`, and `$body` store details about the post.
- `$pageTitle` uses string concatenation to create a full title.
- The variables are embedded inside HTML to dynamically generate content.

## Expected Output
A simple webpage displaying:

**Title:** "Introduction to PHP"

**Author:** "John Doe"

**Content:** "PHP (Hypertext Preprocessor) is a widely used server-side scripting language..."

## Conclusion

This challenge demonstrates how PHP variables can be used to dynamically generate HTML content. Understanding variable assignment and string concatenation is essential for developing dynamic web applications.

