## Table of Contents

  1. [Basic Types](#basic-types)  
  2. [Variables](#variables)  
  3. [Control Structures](#control-structures)  
  3.1. [Conditionals](#conditionals)  
  3.2. [Loops](#loops)  
  4. [Functions](#functions)  
  5. [Classes](#classes)  
  6. [User-defined Data Types](#user-defined-data-types)  
  7. [The `using` Keyword](#the-using-keyword)  
  8. [Preprocessor Directives](#preprocessor-directives)  

## Syntax Specification

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

```csharp
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

```csharp
for (initialization; condition; increment) {
  // code block
}
```

- Foreach loops:

```csharp
foreach (variable_name : array_variable) {
  // code block
}
```

- While loops:

```csharp
while (condition) {
  // code block
}
```

- Do-while loops:

```csharp
do {
  // code block
} while (condition);
```

### Functions

- Function declaration:

```csharp
func function_name(parameter1: type, parameter2: type, ...): return_type {
  // code block
}
```

- Function parameters: pass by value (default), pass by reference (`ref`)

### Classes

- Class declaration:

```csharp
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
```csharp
type Point = (x: int, y: int);
```

### The `using` Keyword

- Type aliasing

Example:
```csharp
using short_name = long_type_name;
```

- Namespace aliasing

Example:
```csharp
using namespace std;
```

## Preprocessor Directives

Here's an example of how these preprocessor directives could be used in YAPL:

```csharp
#include <std::io>

#define MAX_SIZE 100

#ifdef DEBUG
  #define LOG(message) std::out.write("${message}\n")
#else
  #define LOG(message)
#endif

main() {
  let array = new int[MAX_SIZE];
  let i;

  for (i = 0; i < MAX_SIZE; i++) {
    array[i] = i;
  }

  LOG("Array initialized.");

  return 0;
}
```

In this example, the `#include` directive is used to include the `std::io` standard library.  
The `#define` directive is used to define a constant value `MAX_SIZE` and a macro `LOG`.  
The `#ifdef` and `#ifndef` directives are used to conditionally define the `LOG` macro based on the `DEBUG` preprocessor symbol.  
The `#else` and `#elif` directives can be used for more complex conditional compilation.
