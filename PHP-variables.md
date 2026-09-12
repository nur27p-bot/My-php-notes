# 3. PHP Variables

Variables are "containers" for storing information. A variable can have a short name (like `$x` and `$y`) or a more descriptive name (`$age`, `$carname`, `$total_volume`).

## Rules for PHP Variables

- A variable must start with the `$` sign, followed by the name of the variable.
- A variable name must start with a letter or an underscore character.
- A variable name cannot start with a number.
- A variable name can only contain alpha-numeric characters and underscores (`A-z`, `0-9`, and `_`).
- Variable names are case-sensitive (`$age` and `$AGE` are two different variables).

## Creating Variables

```php
$x = 5;
$y = "John";
```

Here, `$x` holds the value `5`, and `$y` holds the value `"John"`.

> **Note:** When assigning a text value to a variable, wrap it in quotes.
> **Note:** Unlike some other languages, PHP has no separate command for declaring a variable — it's created the moment you assign a value to it.

## Outputting Variables

```php
$txt = "W3Schools.com";
echo "I love $txt!";
```

This produces the same output as:

```php
$txt = "W3Schools.com";
echo 'I love ' . $txt . '!';
```

You can also output the result of an expression:

```php
$x = 5;
$y = 4;
echo $x + $y; // 9
```

## PHP is Loosely Typed

PHP doesn't require you to declare a variable's data type — it automatically assigns one based on the value. 
Since types aren't strict by default, you can do things like adding a string to an integer without an error.

PHP 7 introduced optional **type declarations**, which let you specify the expected data type for function parameters/returns, 
and a **strict mode** that throws a Fatal Error on a type mismatch.

## PHP Variables and Data Types

```php
$x = 5;      // $x is an integer
$y = "John"; // $y is a string
```

PHP supports the following data types:

- **string** — text values
- **int** — whole numbers
- **float** — decimal numbers
- **bool** — true or false
- **array** — multiple values
- **object** — stores data as objects
- **null** — empty variable
- **resource** — reference to an external resource
- **mixed** — any value

## Checking a Variable's Type with `var_dump()`

`var_dump()` returns both the data type and the value of a variable:

```php
var_dump(5);
var_dump("John");
var_dump(3.14);
var_dump(true);
var_dump([2, 3, 56]);
var_dump(NULL);
```

## Assigning Multiple Values at Once

You can assign the same value to multiple variables in a single line:

```php
$x = $y = $z = "Fruit"; // all three variables now hold "Fruit"
```
