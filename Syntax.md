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

## Supported Paradigms

**YAPL** supports object-oriented, functional, and procedural paradigms.  
It allows multi-paradigm programming, enabling developers to choose the most suitable paradigm for their projects.  

## Powerful Type System

**YAPL**'s type system includes features like type unions, generics, and type inference.  
It supports both static and dynamic typing, offering flexibility and safety.  

Example:
```csharp
func add(a: int | float, b: int | float): int | float {
  return a + b;
}
```

## Standard Library

**YAPL**'s standard library includes data structures like `std::vector` and `std::map`.  
These data structures offer improved performance and functionality compared to similar structures in languages like C++ or Java.  

Example:
```csharp
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

**YAPL** allows users to define custom data types using the `type` keyword.

Example:
```csharp
type Point = (x: int, y: int);
```

## The `using` Keyword

The `using` keyword in **YAPL** facilitates type and namespace aliasing.

Example:
```csharp
using short_name = long_type_name;
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

In this example, the `#include` directive is used to include the `stdio.h` standard library. The `#define` directive is used to define a constant value `MAX_SIZE` and a macro `LOG`. The `#ifdef` and `#ifndef` directives are used to conditionally define the `LOG` macro based on the `DEBUG` preprocessor symbol. The `#else` and `#elif` directives can be used for more complex conditional compilation.
