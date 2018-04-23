.. _i_spec_conversions:

Value Conversions
=================

Any conversions not listed here simply *do not exist*, so attempting those will fail.

- Double
    - To Int32
        - Rounds double to Int32.
    - To String
        - Converts value to text form via the engine's/language's standard conversion. While there is no direct standard, it's recommended that this be something like C#'s Double :code:`ToString` method.
    - To Boolean
        - Any non-zero value is true.
- Int32
    - To Double
        - Simply casts the int as a double.
    - To String
        - Converts value to text form via the engine's/language's standard conversion. While there is no direct standard, it's recommended that this be something like C#'s Int32 :code:`ToString` method.
    - To Boolean
        - Any non-zero value is true.
- String
    - To Double
        - Parses the pre-string as a double, using the engine's/language's standard conversion. While there is no direct standard, it's recommended that this be something like C#'s :code:`double.Parse` method.
    - To Int32
        - Parses the pre-string as a 32-bit integer, using the engine's/language's standard conversion. While there is no direct standard, it's recommended that this be something like C#'s :code:`int.Parse` method.
    - Boolean
        - Any non-empty string is true.
- Boolean
    - To Double
        - 1 if true, 0 if false
    - To Int32
        - 1 if true, 0 if false
    - To String
        - "true" if true, "false" if false
- Undefined
    - To String
        - "undefined"