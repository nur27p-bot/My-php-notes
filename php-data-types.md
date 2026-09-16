# 5. PHP Data Types

Variables can store data of different types, and different data types can do different things. PHP supports the following data types:

- **string** — text values
- **int** — whole numbers
- **float** — decimal numbers
- **bool** — true or false
- **array** — multiple values
- **object** — stores data as objects
- **null** — empty variable
- **resource** — reference to an external resource

## Checking a Variable's Type with `var_dump()`

`var_dump()` returns both the data type and the value of a variable:

```php
$x = 5;
var_dump($x); // int(5)
```

## String

A string is a sequence of characters, like `"Hello world!"`.

```php
$x = 'Hello world!';
var_dump($x);
```

## Int

An integer is a non-decimal number between -2,147,483,648 and 2,147,483,647.

Rules for integers:

- Must have at least one digit.
- Must not have a decimal point.
- Can be either positive or negative.
- Can be written in decimal (base 10), hexadecimal (base 16), octal (base 8), or binary (base 2) notation.

```php
$x = 5985;
var_dump($x);
```

## Float

A float (floating point number) is a number with a decimal point, or a number in exponential form.

```php
$x = 10.365;
var_dump($x);
```

## Bool

A boolean represents one of two states: `TRUE` or `FALSE`. Booleans are commonly used in conditional testing (`if`/`else`, loops, etc.).

```php
$x = true;
var_dump($x);
```

## Array

An array stores multiple values in a single variable:

```php
$cars = array("Volvo", "BMW", "Toyota");
var_dump($cars);
```

## Object

An object holds an instance of a programmer-defined class:

```php
class Car {
  public $color;
  public $model;
  public function __construct($color, $model) {
    $this->color = $color;
    $this->model = $model;
  }
  public function message() {
    return "My car is a " . $this->color . " " . $this->model . "!";
  }
}

$myCar = new Car("red", "Volvo");
var_dump($myCar);
```

## Null

`NULL` is a special data type with only one possible value: `NULL`. A variable of type `NULL` has no value assigned to it.

> Tip: A variable created without a value is automatically assigned `NULL`. You can also empty an existing variable by setting it to `null`.

```php
$x = "Hello world!";
$x = null;
var_dump($x); // NULL
```

## Changing Data Type

Assigning a new value to a variable automatically changes its data type:

```php
$x = 5;
var_dump($x); // int

$x = "Hello";
var_dump($x); // string
```

To change a variable's data type without changing its value, use **casting**:

```php
$x = 5;
$x = (string) $x;
var_dump($x); // string(1) "5"
```

## Resource

The `resource` type isn't a real data type in the traditional sense — it holds a reference to an external resource, such as a database connection or a file handle. This is an advanced topic covered elsewhere.
