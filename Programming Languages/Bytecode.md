**Bytecode** (also called **portable code** or **[[P-Code|p-code]]** is a form of [[Instruction Set|instruction set]] designed for efficient execution by a software [[Interpreter|interpreter]]. Unlike [[Human-Readable|human-readable]] [[Source Code|source code]], bytecodes are compact numeric codes, constants, and references (normally numeric addresses) that encode the result of [[Compiler|compiler]] parsing and performing [[Semantic Analysis|semantic analysis]] of things like type, scope, and nesting depths of program objects.

The name bytecode stems from instruction sets that have one-[[Byte|byte]] [[Opcodes|opcodes]] followed by optional parameters. [[Intermediate Representations|Intermediate representations]] such as bytecode may be output by [[Programming Languages|programming language]] implementations to ease [[Interpretation|interpretation]], or it may be used to reduce hardware and [[Operating System|operating system]] dependence by allowing the same code to run [[Cross-Platform|cross-platform]], on different devices. Bytecode may often be either directly executed on a [[Virtual Machine|virtual machine]] (a [[P-Code Machine|p-code machine]], or it may be further compiled into [[Machine Code|machine code]] for better performance.

Since bytecode instructions are processed by software, they may be arbitrarily complex, but are nonetheless often akin to traditional hardware instructions: virtual [[Stack Machines|stack machines]] are the most common, but virtual [[Register Machines|register machines]] have been built also. Different parts may often be stored in separate files, similar to [[Object Modules|object modules]], but dynamically loaded during execution.

## Execution

A bytecode program may be executed by parsing and _directly_ executing the instructions, one at a time. This kind of _bytecode interpreter_ is very portable. Some systems, called dynamic translators, or _[[just-in-time]]_ (JIT) compilers, translate bytecode into [[Machine Code|machine code]] as necessary at [[runtime]]. This makes the virtual machine hardware-specific but does not lose the portability of the bytecode. For example, [[Java]] and [[Smalltalk]] code is typically stored in bytecode format, which is typically then JIT compiled to translate the bytecode to machine code before execution. This introduces a delay before a program is run, when the bytecode is compiled to native machine code, but improves execution speed considerably compared to interpreting source code directly, normally by around an order of magnitude (10x).

Because of its performance advantage, today many language implementations execute a program in two phases, first compiling the source code into bytecode, and then passing the bytecode to the virtual machine. There are bytecode based virtual machines of this sort for [[Java]], [[Raku]], [[Python]], [[PHP]], [[Tcl]], [[mawk]] and [[Forth]] (however, Forth is seldom compiled via bytecodes in this way, and its virtual machine is more generic instead). The implementation of [[Perl]] and [[Ruby]] 1.8 instead work by walking an [[abstract syntax tree]] representation derived from the source code.

More recently, the authors of [[V8]] and [[Dart]] have challenged the notion that intermediate bytecode is needed for fast and efficient VM implementation. Both of these language implementations currently do direct JIT compiling from source code to machine code with no bytecode intermediary.

## Examples

- [[ActionScript]] executes in the ActionScript Virtual Machine (AVM), which is part of Flash Player and [[AIR]]. ActionScript code is typically transformed into bytecode format by a [[Compiler|compiler]]. Examples of compilers include one built into Adobe Flash Professional and one built into Adobe Flash Builder and available in the [[Adobe Flex SDK]].
- [[Adobe Flash]] objects
- [[BANCStar]], originally bytecode for an interface-building tool but used also as a language
- [[Berkeley Packet Filter]]
- [[Berkeley Pascal]]
- [[Byte Code Engineering Library]]
- C to [[Java virtual machine]] compilers
- [[CLISP]] implementation of [[Common Lisp]] used to compile only to bytecode for many years; however, now it also supports compiling to native code with the help of [[GNU lightning]]
- [[CMUCL]] and Scieneer Common Lisp implementations of [[Common Lisp]] can compile either to native code or to bytecode, which is far more compact
- [[Common Intermediate Language]] executed by [[Common Language Runtime]], used by [[.NET]] languages such as [[C-Sharp|C#]]
- [[Dalvik]] bytecode, designed for the [[Android]] platform, is executed by the [[Dalvik virtual machine]]
- Dis bytecode, designed for the [[Inferno (operating system)]], is executed by the [[Dis virtual machine]]'
- [[EiffelStudio]] for the [[Eiffel]] programming language
- EM, the [[Amsterdam Compiler Kit]] virtual machine used as an intermediate compiling language and as a modern bytecode language
- [[Emacs]] is a text editor with most of its functions implemented by [[Emacs Lisp]], its built-in dialect of [[Lisp]]. These features are compiled into bytecode. This architecture allows users to customize the editor with a high level language, which after compiling into bytecode yields reasonable performance.
- [[Embeddable Common Lisp]] implementation of [[Common Lisp]] can compile to bytecode or C code
- [[Common Lisp]] provides a `disassemble` function which prints to the standard output the underlying code of a specified function. The result is implementation-dependent and may or may not resolve to bytecode. Its inspection can be utilized for debugging and optimization purposes, for instance, produces:

```
(disassemble '(lambda (x) (print x)))
; disassembly for (LAMBDA (X))
; 2436F6DF:       850500000F22     TEST EAX, [#x220F0000]    ; no-arg-parsing entry point
;       E5:       8BD6             MOV EDX, ESI
;       E7:       8B05A8F63624     MOV EAX, [#x2436F6A8]     ; #<FDEFINITION object for PRINT>
;       ED:       B904000000       MOV ECX, 4
;       F2:       FF7504           PUSH DWORD PTR [EBP+4]
;       F5:       FF6005           JMP DWORD PTR [EAX+5]
;       F8:       CC0A             BREAK 10                  ; error trap
;       FA:       02               BYTE #X02
;       FB:       18               BYTE #X18                 ; INVALID-ARG-COUNT-ERROR
;       FC:       4F               BYTE #X4F                 ; ECX 
```

- Ericsson implementation of [[Erlang]] uses BEAM bytecodes
- [[Ethereum]]'s Virtual Machine (EVM) is the runtime environment, using its own bytecode, for transaction execution in Ethereum (smart contracts).
- [[Icon]] and [[Unicon]] programming languages
- [[Infocom]] used the [[Z-machine]] to make its software applications more portable
- [[Java bytecode]], which is executed by the [[Java virtual machine]]
    - [[ASM]]
    - [[BCEL]]
    - [[Javassist]]
- [[Keiko bytecode]] used by the [[Oberon-2]] programming language to make it and the [[Oberon operating system]] more portable.
- [[KEYB]], the [[MS-DOS]]/[[PC DOS]] keyboard driver with its resource file [[KEYBOARD.SYS]] containing layout information and short [[Bytecode|p-code]] sequences executed by an interpreter inside the resident driver.
- [[LLVM IR]]
- LSL, a scripting language used in virtual worlds compiles into bytecode running on a virtual machine. Second Life has the original Mono version, Inworldz developed the Phlox version.
- [[Lua]] language uses a register-based bytecode virtual machine
- m-code of the [[MATLAB]] language
- [[Malbolge]] is an [[Esoteric Programming Language|esoteric]] [[Machine Language|machine language]] for a ternary virtual machine.
- [[Microsoft P-code]] used in [[Visual C++]] and [[Visual Basic]]
- [[Multiplan]]
- [[O-code]] of the [[BCPL]] programming language
- [[OCaml]] language optionally compiles to a compact bytecode form
- [[Bytecode|p-code]] of [[UCSD Pascal]] implementation of the [[Pascal]] language
- [[Parrot virtual machine]]
- [[Pick BASIC]] also referred to as Data BASIC or [[MultiValue BASIC]]
- The [[R environment for statistical computing]] offers a bytecode compiler through the compiler package, now standard with R version 2.13.0. It is possible to compile this version of R so that the base and recommended packages exploit this.
- [[Pyramid 2000]] adventure game
- [[Python]] scripts are being compiled on execution to Python's bytecode language, and the compiled files (.pyc) are cached inside the script's folder

Compiled code can be analysed and investigated using a built-in tool for debugging the low-level bytecode. The tool can be initialized from the shell, for example:

```
>>> import dis # "dis" - Disassembler of Python byte code into mnemonics.
>>> dis.dis('print("Hello, World!")')
  1           0 LOAD_NAME                0 (print)
              2 LOAD_CONST               0 ('Hello, World!')
              4 CALL_FUNCTION            1
              6 RETURN_VALUE
```

- [[Scheme 48]] implementation of Scheme using bytecode interpreter
- Bytecodes of many implementations of the [[Smalltalk]] language
- The [[Spin interpreter]] built into the [[Parallax]] Propeller [[microcontroller]]
- The [[SQLite]] database engine translates SQL statements into a bespoke byte-code format.
- Apple [[SWEET16]]
- [[Tcl]]
- [[TIMI]] is used by compilers on the [[IBM i]] platform.
- [[Tiny BASIC]]
- [[Visual FoxPro]] compiles to bytecode
- [[WebAssembly]]
- [[YARV]]
- [[ZCODE]]
- [[Zend Engine]] opcodes for [[PHP]]