## Table of Contents

  1. [Comment](#comment)  
  2. [Keyword](#keyword)  
  3. [Boolean](#boolean)  
  4. [Type](#type)  
  5. [Delimiter](#delimiter)  
  6. [Operator](#operator)  
  7. [Integer](#integer)  
  8. [Floating-point](#floating-point)  
  9. [String](#string)  
  10. [Identifier](#identifier)  

## Token Specification

### Comment

A comment is a sequence of characters that is ignored by the compiler. There are two types of comments:

* Single-line comments, which start with `//` and continue to the end of the line.
* Multi-line comments, which start with `/*` and continue until the next occurrence of `*/`.

Regular Expression: `/(\/\/[^\n]*\n)|(\/\*[^*]*\*+([^\/][^*]*\*+)*\/\n)/`

### Keyword

Keywords are reserved words that have a special meaning in the language. The following words are keywords in YAPL:

* `let`
* `const`
* `if`
* `else`
* `for`
* `foreach`
* `while`
* `do`
* `while`
* `func`
* `class`
* `type`
* `using`
* `public`
* `protected`
* `private`

Regular Expression: `/(let|const|if|else|for|foreach|while|do|while|func|class|type|using|public|protected|private)\b/`

### Boolean

Boolean values represent true or false. The two boolean values are `true` and `false`.

Regular Expression: `/(true|false)\b/`

### Type

Types define the data type of a value. The following types are defined in YAPL:

* `int`
* `float`
* `bool`
* `string`
* `array`
* `tuple`

Regular Expression: `/(int|float|bool|string|array|tuple)\b/`

### Delimiter

Delimiters are special characters that are used to separate elements in the language. The following characters are delimiters in YAPL:

* `(`
* `)`
* `[`
* `]`
* `{`
* `}`
* `.`
* `,`
* `;`

Regular Expression: `/(\()|(\))|(\[)|\]|(\{)|(\})|(,)|(;)|(\.)/`

### Operator

Operators are symbols that represent mathematical or logical operations. The following operators are defined in YAPL:

* `+`: Addition
* `-`: Subtraction
* `*`: Multiplication
* `/`: Division
* `%`: Modulus
* `<`: Less than
* `<=`: Less than or equal to
* `>`: Greater than
* `>=`: Greater than or equal to
* `==`: Equal to
* `!=`: Not equal to
* `=`: Assignment
* `!`: Logical negation
* `&&`: Logical AND
* `||`: Logical OR
* `&`: Bitwise AND
* `|`: Bitwise OR
* `^`: Bitwise XOR
* `~`: Bitwise NOT
* `<<`: Bitwise left shift
* `>>`: Bitwise right shift

Regular Expression: `/(\+)|(-)|(\*)|(\/)|(\%)|(<)|(<=)|(>)|(>=)|(==)|(!=)|(=)|(!)|(&&)|(\|\|)|(&)|(\|)|(\^)|(~)|(<<)|(>>)/`

### Integer

An integer is a whole number. It can be represented in decimal, hexadecimal, or binary format.

Regular Expression: `/(0[xX][0-9a-fA-F]+)|(\d+(\.\d*)?|\.\d+)([eE][-+]?\d+)?/`

### Floating-point

A floating-point number is a number with a fractional part. It can be represented in decimal or scientific notation.

Regular Expression: `/(0[xX][0-9a-fA-F]+)|(\d+(\.\d*)?|\.\d+)([eE][-+]?\d+)?/`

### String

A string is a sequence of characters enclosed in double quotes.

Regular Expression: `/"(\\.|[^"])*"/`

### Identifier

An identifier is a name given to a variable, constant, function, or class. It consists of a letter followed by any number of letters, digits, or underscores.

Regular Expression: `/([a-zA-Z_][a-zA-Z_0-9]*)/`
