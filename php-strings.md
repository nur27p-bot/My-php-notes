# 6. PHP Strings

A string is a sequence of characters, like `"Hello world!"`.

In PHP, strings can be surrounded by either double quotes or single quotes.

```php
echo "Hello";
echo 'Hello';
```

> **Note:** There is a real difference between double quotes and single quotes in PHP — it's not just a style choice.

## Double or Single Quotes?

A **double-quoted** string will substitute the value of variables, and supports escaping special characters like `\n`, `\r`, `\t`.

```php
$x = "John";
echo "Hello $x"; // Returns: Hello John
```

A **single-quoted** string does *not* substitute variables — it outputs the string exactly as written:

```php
$x = "John";
echo 'Hello $x'; // Returns: Hello $x
```

## Differences Between Single and Double Quotes

| Feature | Single Quotes | Double Quotes |
|---|---|---|
| Variable interpolation | No — variables like `$x` are output literally | Yes — variables are replaced with their values |
| Escape sequences | Only `\'` and `\\` are supported | Supports many, like `\n`, `\t`, `\r`, `\$`, `\"` |
| Performance | Slightly faster (PHP doesn't need to parse the content) | Slightly slower (PHP must scan for variables and escape sequences) |
| Readability | Cleaner for simple, constant strings | More readable for strings with many variables (no need for the concatenation operator `.`) |

## Example

```php
// Using double quotes
$x = "John";
echo "Hello $x\n";
echo "\tHow are you?\n";

// Using single quotes
$x = 'John';
echo 'Hello $x\n';
echo '\tHow are you?\n';
```
