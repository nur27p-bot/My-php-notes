# 9. PHP `substr()` — Slice a String

`substr()` is used to extract a part of a string (slice a string). You specify the start index and the number of characters to return.

```php
$x = "Hello World!";
echo substr($x, 6, 5); // "World"
```

> Note: the first character in a string has index `0`.

## Slice to the End

Leaving out the length parameter means the slice goes all the way to the end:

```php
$x = "Hello World!";
echo substr($x, 6); // "World!"
```

## Slice From the End

Using a **negative start index** slices from the end of the string:

```php
$x = "Hello World!";
echo substr($x, -5, 3); // "Wor" — starts at index -5 ("W"), takes 3 characters
```

> Note: the last character in a string has index `-1`.

## Negative Length

Using a **negative length** specifies how many characters to omit from the end of the string:

```php
$x = "Hi, how are you?";
echo substr($x, 5, -3); // "ow are y" — starts at index 5, stops 3 characters before the end
```
