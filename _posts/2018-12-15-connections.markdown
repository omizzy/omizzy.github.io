---
layout: post
title: Connections
date: 2018-12-15 18:00
comments: false
external-url:
categories: Wicked PHP
---

> They moved together, blue diamonds on a green field.

Excerpt from **Wicked: The Life and Times of the Wicked Witch of the West** by Gregory Maguire

Connect to Mysql DB
```php
$servername = "serverDomain";
$username = "dbUser";
$password = "dbP455w0rd";
try {
    $conn = new PDO(
        "mysql:host=$servername;dbname=myDB",
        $username,
        $password
    );
    $conn->setAttribute(
        PDO::ATTR_ERRMODE,
        PDO::ERRMODE_EXCEPTION
    );
    echo "G2G"; 
} catch(\Exception $e) {
    echo "!G2G: " . $e->getMessage();
}
```