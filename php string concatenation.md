# 8. PHP String Concatenation

To concatenate, or combine, two strings, use the `.` operator:

```php
$x = "Hello";
$y = "World";
$z = $x . $y;
echo $z; // HelloWorld
```

Notice there's no space between the two words. You can add one manually:

```php
$x = "Hello";
$y = "World";
$z = $x . " " . $y;
echo $z; // Hello World
```

An easier and cleaner way is using double quotes — by placing the variables inside a double-quoted string with a space between them, the space is included automatically:

```php
$x = "Hello";
$y = "World";
$z = "$x $y";
echo $z; // Hello World
```
