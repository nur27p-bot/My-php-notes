# 2. PHP echo vs print

Both `echo` and `print` just display text on the screen. They work almost the same way — the differences barely matter in practice.

| | `echo` | `print` |
|---|---|---|
| Returns a value? | No | Yes (returns 1) |
| Multiple items at once? | Yes, comma-separated | No, only one |
| Speed | Slightly faster | Slightly slower |
| Parentheses | Optional | Optional |

## Basic Use

Both work the same way:

```php
echo "Hello";
print "Hello";
```

## Multiple Parameters

`echo` can take multiple pieces, `print` can't:

```php
echo "This ", "is ", "one ", "line."; // ✅ works
print "This ", "is ", "one ", "line."; // ❌ error
```

## Putting Variables Into Text

```php
$name = "Alice";

echo "Hello $name";      // double quotes → variable works directly
echo 'Hello ' . $name;   // single quotes → need a dot (.) to join it
```

## Summary

`echo` and `print` both just print stuff to the page — `echo` is the one almost everyone uses because it's slightly faster and more flexible.

👉 If you had to pick one to actually use in real code: **just use `echo`**. `print` exists mostly for historical/legacy reasons.
