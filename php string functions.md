# 7. PHP String Functions

## `strlen()`

Returns the length of a string.

```php
echo strlen("Hello world!");
```

## `str_word_count()`

Counts the number of words in a string.

```php
echo str_word_count("Hello world!");
```

## `str_contains()`

Checks if a string contains a specific substring. Returns `true` if a match is found, `false` otherwise.

> Available only in PHP 8.0+. For older versions, use `strpos()` instead.
> Performs a **case-sensitive** search.

```php
$txt = "I really love PHP!";
var_dump(str_contains($txt, "love")); // true
var_dump(str_contains($txt, "Love")); // false — case-sensitive
```

## `strpos()`

Searches for a specific substring within a string. Returns the character position of the first match, or `false` if no match is found.

> Performs a **case-sensitive** search.
> The first character position in a string is `0`, not `1`.

```php
echo strpos("Hello world!", "world"); // 6
```

## `str_starts_with()`

Checks if a string starts with a specific substring. Returns `true`/`false`.

> Available only in PHP 8.0+.
> Performs a **case-sensitive** search.

```php
$txt = "I really love PHP!";
var_dump(str_starts_with($txt, "I really")); // true
var_dump(str_starts_with($txt, "i really")); // false — case-sensitive
```

## `str_ends_with()`

Checks if a string ends with a specific substring. Returns `true`/`false`.

> Available only in PHP 8.0+.
> Performs a **case-sensitive** search.

```php
$txt = "I really love PHP!";
var_dump(str_ends_with($txt, "PHP!")); // true
var_dump(str_ends_with($txt, "php!")); // false — case-sensitive
```

## `strtoupper()`

Returns a string in upper case.

```php
$x = "Hello World!";
echo strtoupper($x); // HELLO WORLD!
```

## `strtolower()`

Returns a string in lower case.

```php
$x = "Hello World!";
echo strtolower($x); // hello world!
```

## `str_replace()`

Replaces occurrences of some characters with other characters in a string.

```php
$x = "Hello World!";
echo str_replace("World", "Dolly", $x); // Hello Dolly!
```

## `strrev()`

Reverses a string.

```php
$x = "Hello World!";
echo strrev($x); // !dlroW olleH
```

## `trim()`

Removes whitespace (or other specified characters) from the beginning and end of a string. "Whitespace" here means spaces, tabs, newlines, etc., that surround the actual text.

```php
$x = "    Hello World! ";
echo trim($x); // "Hello World!"
```

## `explode()`

Splits a string into an array, based on a given "separator" — the point at which the string is split.

> The separator parameter is required.

```php
$x = "Hello lovely World!";
$y = explode(" ", $x);

// Use print_r() to display the result
print_r($y);
// Array ( [0] => Hello [1] => lovely [2] => World! )
```
