# 10. PHP Escape Characters

To insert characters that are illegal in a string, use an **escape character**. In PHP, this is a backslash `\` followed by the character you want to insert.

An example of an illegal character is a double quote inside a string that's already surrounded by double quotes:

```php
$x = "We are the so-called "Vikings" from the north."; // ❌ error
echo $x;
```

To fix this, escape the inner double quotes with `\"`:

```php
$x = "We are the so-called \"Vikings\" from the north."; // ✅ works
echo $x;
```

## Common Escape Characters

| Code | Result |
|---|---|
| `\'` | Single quote |
| `\"` | Double quote |
| `\$` | PHP variable (dollar sign) |
| `\n` | New line |
| `\r` | Carriage return |
| `\t` | Tab |
| `\f` | Form feed |
| `\ooo` | Octal value |
| `\xhh` | Hex value |
