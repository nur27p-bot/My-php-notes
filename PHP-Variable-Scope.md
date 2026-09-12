# 4. PHP Variable Scope

PHP variables can be declared anywhere in the code. The **scope** of a variable is the part of the script where it can be referenced/used.

PHP has three variable scopes:

- **Global**
- **Local**
- **Static**

## Global Scope

A variable declared outside a function has **global scope** and can only be accessed outside that function — not from inside it:

```php
$x = 5; // global scope

function myTest() {
  // using $x inside this function will not work
  echo "Variable x inside function is: $x";
}
myTest();

echo "Variable x outside function is: $x";
```

## Local Scope

A variable declared inside a function has **local scope** and can only be accessed within that function. Local variables are created when the function is called and destroyed when it finishes executing:

```php
function myTest() {
  $x = 5; // local scope
  echo "Variable x inside function is: $x";
}
myTest();

// using $x outside the function will not work
echo "Variable x outside function is: $x";
```

## Static Scope

Normally, a function's local variables are deleted once it finishes executing. To keep a local variable's value between calls, use the `static` keyword when declaring it. Each time the function runs again, that variable retains the value from its last call.

> Note: the variable is still local to the function — `static` just prevents it from resetting.

```php
function myTest() {
  static $x = 0; // static scope
  echo $x;
  $x++;
}

myTest(); // 0
myTest(); // 1
myTest(); // 2
```

## The `global` Keyword

The `global` keyword lets you access a global variable from inside a function, by declaring it with `global` before use:

```php
$x = 5;
$y = 10;

function myTest() {
  global $x, $y;
  $y = $x + $y;
}

myTest();
echo $y; // outputs 15
```

## The `$GLOBALS` Superglobal

PHP also stores all global variables in an array called `$GLOBALS[index]`, where `index` is the variable name. This array is accessible from within any function and can be used to read or update global variables directly.

The `global` example above can be rewritten using `$GLOBALS`:

```php
$x = 5;
$y = 10;

function myTest() {
  $GLOBALS['y'] = $GLOBALS['x'] + $GLOBALS['y'];
}

myTest();
echo $y; // outputs 15
```
