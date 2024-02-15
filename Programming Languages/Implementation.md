In computer programming, a programming language implementation is a system for executing computer programs. There are two general approaches to programming language implementation:
### Interpretation: 
The program is read as input by an interpreter, which performs the actions written in the program.
### Compilation:
The program is read by a compiler, which translates it into some other language, such as bytecode or machine code. The translated code may either be directly executed by hardware, or serve as input to another interpreter or another compiler.

### Just-in-time compiler
Some virtual machines include a just-in-time (JIT) compiler to improve the efficiency of bytecode execution. While the bytecode is being executed by the virtual machine, if the JIT compiler determines that a portion of the bytecode will be used repeatedly, it compiles that particular portion to machine code. The JIT compiler then stores the machine code in memory so that it can be used by the virtual machine. JIT compilers try to strike a balance between longer compilation time and faster execution time.

[[Compiler]]
A compiler translates a program written in one language into another language. Most compilers are organized into three stages: a front end, an optimizer, and a back end. The front end is responsible for understanding the program. It makes sure the program is valid and transforms it into an intermediate representation, a data structure used by the compiler to represent the program. The optimizer improves the intermediate representation to increase the speed or reduce the size of the executable which is ultimately produced by the compiler. The back end converts the optimized intermediate representation into the output language of the compiler.

If a compiler of a given high level language produces another high level language, it is called a transpiler. Transpilers can be used to extend existing languages or to simplify compiler development by exploiting portable and well-optimized implementations of other languages (such as C).

Many combinations of interpretation and compilation are possible, and many modern programming language implementations include elements of both. For example, the Smalltalk programming language is conventionally implemented by compilation into bytecode, which is then either interpreted or compiled by a virtual machine. Since Smalltalk bytecode is run on a virtual machine, it is portable across different hardware platforms.

### Multiple implementations
Programming languages can have multiple implementations. Different implementations can be written in different languages and can use different methods to compile or interpret code. For example, implementations of Python include: 