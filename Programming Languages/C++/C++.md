- **[[Compiled Language|Compiler-Based]]**: C++ is a compiled language, meaning C++ programs are compiled before execution. This makes it relatively faster than languages like [[Java]] and [[Python]].

- **[[Static-Typed]]**: C++ is a static-typed language, that is, when compiling, it's verified the types of variables, expressions, functions signatures to ensure correctness in the program along with type consistency before generating the executable code.

- **[[Object-Oriented Programming|Object-Oriented Programming (OOP)]]**: C++ is an object-oriented programming language, unlike C, which is a procedural programming language. This is the most significant feature of C++. It allows creating and destroying objects during programming, along with defining “blueprints” (classes) from which objects can be instantiated. Key OOP concepts in C++ include **[[Classes|classes]]**, **[[Objects|objects]]**, **[[Encapsulation|encapsulation]]**, **[[Polymorphism|polymorphism]]**, and **[[Inheritance|inheritance]]**.

- **[[Cross-Platform|Platform Independence]]**: Although a C++ executable is not platform-independent (programs compiled on Linux won’t run on Windows, for example), the source code can be written to be executed on different operating systems, making C++ **machine-independent**.

- **Simplicity**: C++ is relatively straightforward. Programs can be divided into logical units and parts, and the language supports various data types. Additionally, the C++ `auto` keyword simplifies variable declarations by allowing the compiler to automatically deduce the type based on the initialized value.
    
    ```cpp
    #include <iostream>
    using namespace std;
    
    int main() {
        auto an_int = 26;
        auto a_bool = false;
        auto a_float = 26.24;
        auto ptr = &a_float;
    
        cout << typeid(a_bool).name() << "\n"; // Output: b
        cout << typeid(an_int).name() << "\n"; // Output: i
    
        return 0;
    }
    ```

- **[[High-Level Language]]**: C++ is considered a high-level language. Its syntax is closer to human language, making it easier to develop complex programs.

- **Popularity**: C++ is widely used and serves as the foundation for many other programming languages that support object-oriented features. Bjarne Stroustrup, the creator of C++, developed the language as an extension of [[C]] to include object-oriented capabilities.

- **[[Case Sensitivity]]**: C++ is a case-sensitive language. For example, `cin` is used for input, but `Cin` won’t work. Unlike other languages like [[HTML]] and [[MySQL]], C++ distinguishes between uppercase and lowercase letters.

---

In summary, C++ is a powerful and versatile language suitable for a wide range of applications, from embedded systems to game development and high-performance software.