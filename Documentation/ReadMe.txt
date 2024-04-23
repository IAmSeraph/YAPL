# YAPL (Yet Another Programming Language)

YAPL is a statically-typed, general-purpose programming language designed for ease of use, maintainability, and performance.  
It supports multiple paradigms and offers features like type inference, pattern matching, and a powerful type system.  
YAPL aims to address common issues in other languages by focusing on simplicity, clarity, and readability.  

## Comparison with Similar Languages

YAPL combines the best features of languages like TypeScript, Rust, and Swift, offering a unique blend of type safety, performance, and usability.  
Its powerful type system and type inference capabilities enable developers to write robust and maintainable code with ease.  

## Syntax

### Basic Types

- Integers: `int<size>` (e.g., `int<8>`, `int<16>`, `int<32>`, `int<64>`)
- Floating-point numbers: `float<size>` (e.g., `float<16>`, `float<32>`, `float<64>`)
- Booleans: `bool`
- Strings: `string`
- Arrays: `type[size]` (e.g., `int<8>[10]`)
- Tuples: `(type1, type2, ..., typen)`

### Variables

- Variables: `let variable_name: type = value;`
- Constants: `const constant_name: type = value;`

### Control Structures

#### Conditionals

```
if (condition) {
  // code block
} else if (condition) {
  // code block
} else {
  // code block
}
```

#### Loops

- For loops:

```
for (initialization; condition; increment) {
  // code block
}
```

- Foreach loops:

```
foreach (variable_name : array_variable) {
  // code block
}
```

- While loops:

```
while (condition) {
  // code block
}
```

- Do-while loops:

```
do {
  // code block
} while (condition);
```

### Functions

- Function declaration:

```
func function_name(parameter1: type, parameter2: type, ...): return_type {
  // code block
}
```

- Function parameters: pass by value (default), pass by reference (`ref`)

### Classes

- Class declaration:

```
class ClassName {
  // code block
}
```

- Members declared within the class block
- Inheritance: `class DerivedClass: access_modifier BaseClass { ... }`
  - Access modifiers: `public`, `protected`, `private`

### User-defined Data Types

- User-defined data types using the `type` keyword

Example:
```
type Point = (x: int, y: int);
```

### The `using` Keyword

- Type aliasing

Example:
```
using short_name = long_type_name;
```

- Namespace aliasing

Example:
```
using namespace std;
```

## Supported Paradigms

YAPL supports object-oriented, functional, and procedural paradigms.  
It allows multi-paradigm programming, enabling developers to choose the most suitable paradigm for their projects.  

## Powerful Type System

YAPL's type system includes features like type unions, generics, and type inference.  
It supports both static and dynamic typing, offering flexibility and safety.  

Example:
```
func add(a: int | float, b: int | float): int | float {
  return a + b;
}
```

## Standard Library

YAPL's standard library includes data structures like `std::vector` and `std::map`.  
These data structures offer improved performance and functionality compared to similar structures in languages like C++ or Java.  

Example:
```
#include <std::vector>

main(): int {
  std::vector<int> numbers;
  numbers.push_back(1);
  numbers.push_back(2);
  numbers.push_back(3);

  for (int i = 0; i < numbers.size(); i++) {
    std::out.write("${numbers[i]} ");
  }

  return 0;
}
```

## User-defined Data Types

YAPL allows users to define custom data types using the `type` keyword.

Example:
```
type Point = (x: int, y: int);
```

## The `using` Keyword

The `using` keyword in YAPL facilitates type and namespace aliasing.

Example:
```
using short_name = long_type_name;
using namespace std;
```

## Future Directions

YAPL is under active development, with planned features including:

- Improved error handling
- Enhanced support for concurrency and parallelism
- Additional standard library components
- Expanded documentation and learning resources

## Acknowledgements

We appreciate the feedback and suggestions provided by the community.  
Your contributions are invaluable in shaping the future of YAPL.  
