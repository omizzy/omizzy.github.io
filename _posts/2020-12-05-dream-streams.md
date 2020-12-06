---
layout: post
title: Dream streams
date: 2018-12-15 18:00
comments: false
external-url:
categories: PHP 
---

> In my dream there were sunken pirate ships and robots, not looking for treasure, but a ship itself. It never happened, but in my dream, it did.

Memory as a stream
```php
$f = open('php://memory', 'w+');
// any stream operation here
fputcsv($f, ['Jolly Roger', 'Adventure Galley', 'Fancy']);
// reset the cursor
rewind($f);
// pull the data from memory
$contents = stream_get_contents($f);
// close the stream
fclose($f);
// reminisce
print $contents;
```

Strings as streams
```php
function str_to_stream(string $string) {
  $stream = fopen('php://memory', 'rw+');
  fwrite($stream, $string),
  rewind($stream);
  return $stream);
}

$raw_string=<<<STREAM
4
10
10 12
11 15
STREAM;

$stream = str_to_string($raw_string);

// read in
$vertices = (int)fgets($stream);
$edges = (int)fgets($stream);
print "$vertices $edges";
```
