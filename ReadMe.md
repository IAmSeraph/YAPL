# YAPL (Yet Another Programming Language)

[![Status](https://img.shields.io/badge/Status-Design%20Phase-yellow.svg)](./Status.md)
[![Status](https://img.shields.io/badge/Notice-Xavier%20Leroy-red.svg)](./Notice.md)

YAPL is a statically-typed, general-purpose programming language designed for ease of use, maintainability, and performance.  
It supports multiple paradigms and offers features like type inference, pattern matching, and a powerful type system.  
YAPL aims to address common issues in other languages by focusing on simplicity, clarity, and readability.  

## Specifications

  * [Syntax Specification](./Syntax.md)
  * [Token Specification](./Tokens.md)

## Comparison with Similar Languages

YAPL combines the best features of languages like TypeScript, Rust, and Swift, offering a unique blend of type safety, performance, and usability.  
Its powerful type system and type inference capabilities enable developers to write robust and maintainable code with ease.  

## Supported Paradigms

YAPL supports object-oriented, functional, and procedural paradigms.  
It allows multi-paradigm programming, enabling developers to choose the most suitable paradigm for their projects.  

## Powerful Type System

YAPL's type system includes features like type unions, generics, and type inference.  
It supports both static and dynamic typing, offering flexibility and safety.  

Example:
```csharp
func add(a: int | float, b: int | float): int | float {
  return a + b;
}
```

## Standard Library

YAPL's standard library includes data structures like `std::vector` and `std::map`.  
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


## Future Directions

YAPL is under active development, with planned features including:

- Improved error handling
- Enhanced support for concurrency and parallelism
- Additional standard library components
- Expanded documentation and learning resources

## Acknowledgements

We appreciate the feedback and suggestions provided by the community.  
Your contributions are invaluable in shaping the future of YAPL.  
