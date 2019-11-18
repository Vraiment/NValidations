[![Build Status](https://travis-ci.com/Vraiment/NValidations.svg?branch=master)](https://travis-ci.com/Vraiment/NValidations)

# NValidations
--------------

NValidations is a small library that provides simple validations:

```C#
void Parse(string value)
{
    Validate.ArgumentNotNull(value, nameof(value));
    Validate.Argument(value.Length != 0, "Input value should not be empty.");

    // Actual parse logic...
}
```

## Argument validations

### `Validate.ArgumentNotNull<T>(T argument, string argumentName)`

Validates the given `argument` is not null, if it is it throws `System.ArgumentNullException` with the given `argumentName`.

### `Validate.Argument(bool condition, string message)`

Validates the given `condition` is true, if is not it throws `System.ArgumentException` with the given `message`.
