# **Schame Validation with Joi**

First run:

```
npm install
npm start
```

##another funcation of joi:

- `alow()`:
Whitelists value or set of values that will always be valid before applying other rules. It can take values as its arguments or an array of values.

- `valid()`:
Whitelists value or set of values as the only valid **value(s)** before applying other rules. It can take values as its arguments or an array of values.

- `invalid()`: 
Blacklists value or set of values that will never be valid. It does the direct opposite of **allow()**. It can take values as its arguments or an array of values.

- `required()`:
Prevents the schema from allowing **undefined** as value.

- `optional()`:
The schema can allow **undefined** as value. The schema however, will not allow a value of **null**. This is the default behaviour.

- `raw()`:
This outputs the original untouched value instead of the casted value.

- `strict()`:
This enables strict mode - which prevents type casting for the current key and any child keys. In non-strict mode, the values are casted to match the specified validation schema where possible. This is the default behaviour.

- `default()`:
This sets a default value if the original value is **undefined**. In its simplest form, it takes as its first argument the value to use as default. See the API Reference for a detailed documentation of the **default()** constraint.

## Validating Strings:

- `min()`, `max()`, `length()`
These are used to control the minimum length, maximum length or fixed length of the string. They each take as first argument, an integer that specifies the length limit.

- `email()`, `ip()`, `guid()`, `uri()`, `creditCard()`
These are used to validate email addresses, IP addresses, GUIDs, URIs or credit card numbers (using the Luhn Algorithm) respectively. They each take an optional options object as first argument. See the API Docs for detailed information about the supported options.

- `alphanum()`, `hex()`, `base64()`
These are used to restrict the valid strings to alphanumeric, hexadecimal or base64-encoded strings respectively.

- `regex()`, `replace()`
These allow you to specify a custom regular expression that the string must match for it to be considered valid. They each take a RegExp literal as first argument. regex() can also take an optional options object as second argument. replace() is useful if you want to replace some parts of the matched string with another string. It takes the replacement string as second argument.

lowercase(), uppercase(), insensitive()
These are used to force a case or ignore the case (for insensitive()) on the string during validation. Note that case conversion may happen on the original value except when strict mode is enabled.

## Validating Numbers
- `min()`, `max()`, `greater()`, `less()`
These are used to put a limit on the range of numbers that are considered valid. They each take as first argument, an integer that specifies the limit.

- `precision()`
This specifies the maximum number of decimal places for numbers that are considered valid. It takes an integer as first argument that specifies the maximum decimal places.

- `positive()`, `negative()`
These are used to restrict the valid numbers to only positive or negative numbers respectively.

- `integer()`
This allows only integers (no floating point) to be considered as valid values. In non-strict mode, some type conversion may occur on the value if possible.

Created by [JFalcon](https://jfalcon.net)
