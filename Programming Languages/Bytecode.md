**Bytecode** (also called **portable code** or **[[P-Code|p-code]]** is a form of [[Instruction Set|instruction set]] designed for efficient execution by a software [[Interpreter|interpreter]]. Unlike [[Human-Readable|human-readable]] [[Source Code|source code]], bytecodes are compact numeric codes, constants, and references (normally numeric addresses) that encode the result of [[Compiler|compiler]] parsing and performing [[Semantic Analysis|semantic analysis]] of things like type, scope, and nesting depths of program objects.

The name bytecode stems from instruction sets that have one-[[Byte|byte]] [[Opcodes|opcodes]] followed by optional parameters. [[Intermediate representations]] such as bytecode may be output by [[Programming Languages|programming language]] implementations to ease [[Interpretation|interpretation]], or it may be used to reduce hardware and [[Operating System|operating system]] dependence by allowing the same code to run [[Cross-Platform|cross-platform]], on different devices. Bytecode may often be either directly executed on a [[Virtual Machine|virtual machine]] (a [[P-Code Machine|p-code machine]], or it may be further compiled into [[Machine Code|machine code]] for better performance.

Since bytecode instructions are processed by software, they may be arbitrarily complex, but are nonetheless often akin to traditional hardware instructions: virtual [[stack machines]] are the most common, but virtual [[register machines]] have been built also. Different parts may often be stored in separate files, similar to [[object modules]], but dynamically loaded during execution.

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
- [[Common Intermediate Language]] executed by [[Common Language Runtime]], used by [[.NET]] languages such as [[C#]]
- [[Dalvik]] bytecode, designed for the [[Android]] platform, is executed by the [[Dalvik virtual machine]]
- Dis bytecode, designed for the [[Inferno (operating system)]], is executed by the [[Dis virtual machine]]'
- [EiffelStudio](https://en.wikipedia.org/wiki/EiffelStudio "EiffelStudio") for the [Eiffel](https://en.wikipedia.org/wiki/Eiffel_(programming_language) "Eiffel (programming language)") programming language
- EM, the [Amsterdam Compiler Kit](https://en.wikipedia.org/wiki/Amsterdam_Compiler_Kit "Amsterdam Compiler Kit") virtual machine used as an intermediate compiling language and as a modern bytecode language
- [Emacs](https://en.wikipedia.org/wiki/Emacs "Emacs") is a text editor with most of its functions implemented by [Emacs Lisp](https://en.wikipedia.org/wiki/Emacs_Lisp "Emacs Lisp"), its built-in dialect of [Lisp](https://en.wikipedia.org/wiki/Lisp_(programming_language) "Lisp (programming language)"). These features are compiled into bytecode. This architecture allows users to customize the editor with a high level language, which after compiling into bytecode yields reasonable performance.
- [Embeddable Common Lisp](https://en.wikipedia.org/wiki/Embeddable_Common_Lisp "Embeddable Common Lisp") implementation of [Common Lisp](https://en.wikipedia.org/wiki/Common_Lisp "Common Lisp") can compile to bytecode or C code
- [Common Lisp](https://en.wikipedia.org/wiki/Common_Lisp "Common Lisp") provides a `disassemble` function[[10]](https://en.wikipedia.org/wiki/Bytecode#cite_note-11) which prints to the standard output the underlying code of a specified function. The result is implementation-dependent and may or may not resolve to bytecode. Its inspection can be utilized for debugging and optimization purposes.[[11]](https://en.wikipedia.org/wiki/Bytecode#cite_note-12) [Steel Bank Common Lisp](https://en.wikipedia.org/wiki/Steel_Bank_Common_Lisp "Steel Bank Common Lisp"), for instance, produces:

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

- Ericsson implementation of [Erlang](https://en.wikipedia.org/wiki/Erlang_(programming_language) "Erlang (programming language)") uses BEAM bytecodes
- [Ethereum](https://en.wikipedia.org/wiki/Ethereum "Ethereum")'s Virtual Machine (EVM) is the runtime environment, using its own bytecode, for transaction execution in Ethereum (smart contracts).
- [Icon](https://en.wikipedia.org/wiki/Icon_(programming_language) "Icon (programming language)")[[12]](https://en.wikipedia.org/wiki/Bytecode#cite_note-Arizona_Icom-13) and [Unicon](https://en.wikipedia.org/wiki/Unicon_(programming_language) "Unicon (programming language)")[[13]](https://en.wikipedia.org/wiki/Bytecode#cite_note-Icon_Unicon-14) programming languages
- [Infocom](https://en.wikipedia.org/wiki/Infocom "Infocom") used the [Z-machine](https://en.wikipedia.org/wiki/Z-machine "Z-machine") to make its software applications more portable
- [Java bytecode](https://en.wikipedia.org/wiki/Java_bytecode "Java bytecode"), which is executed by the [Java virtual machine](https://en.wikipedia.org/wiki/Java_virtual_machine "Java virtual machine")
    - [ASM](https://en.wikipedia.org/wiki/ObjectWeb_ASM "ObjectWeb ASM")
    - [BCEL](https://en.wikipedia.org/wiki/BCEL "BCEL")
    - [Javassist](https://en.wikipedia.org/wiki/Javassist "Javassist")
- [Keiko bytecode](https://en.wikipedia.org/wiki/Keiko_bytecode "Keiko bytecode") used by the [Oberon-2](https://en.wikipedia.org/wiki/Oberon-2 "Oberon-2") programming language to make it and the [Oberon operating system](https://en.wikipedia.org/wiki/Oberon_operating_system "Oberon operating system") more portable.
- [KEYB](https://en.wikipedia.org/wiki/KEYB_(command) "KEYB (command)"), the [MS-DOS](https://en.wikipedia.org/wiki/MS-DOS "MS-DOS")/[PC DOS](https://en.wikipedia.org/wiki/PC_DOS "PC DOS") keyboard driver with its resource file [KEYBOARD.SYS](https://en.wikipedia.org/wiki/KEYBOARD.SYS "KEYBOARD.SYS") containing layout information and short [p-code](https://en.wikipedia.org/wiki/P-code_machine "P-code machine") sequences executed by an interpreter inside the resident driver.[[14]](https://en.wikipedia.org/wiki/Bytecode#cite_note-Paul_2001_KEYBOARD-15)[[15]](https://en.wikipedia.org/wiki/Bytecode#cite_note-Mendelson_2001_KEYBOARD-16)
- [LLVM IR](https://en.wikipedia.org/wiki/LLVM_IR "LLVM IR")
- LSL, a scripting language used in virtual worlds compiles into bytecode running on a virtual machine. Second Life has the original Mono version, Inworldz developed the Phlox version.
- [Lua](https://en.wikipedia.org/wiki/Lua_(programming_language) "Lua (programming language)") language uses a register-based bytecode virtual machine
- m-code of the [MATLAB](https://en.wikipedia.org/wiki/MATLAB "MATLAB") language[[16]](https://en.wikipedia.org/wiki/Bytecode#cite_note-Patent_6973644-17)
- [Malbolge](https://en.wikipedia.org/wiki/Malbolge "Malbolge") is an [esoteric](https://en.wikipedia.org/wiki/Esoteric_programming_language "Esoteric programming language") [machine language](https://en.wikipedia.org/wiki/Machine_language "Machine language") for a ternary virtual machine.
- [Microsoft P-code](https://en.wikipedia.org/wiki/P-code_machine#Microsoft_P-code "P-code machine") used in [Visual C++](https://en.wikipedia.org/wiki/Visual_C%2B%2B "Visual C++") and [Visual Basic](https://en.wikipedia.org/wiki/Visual_Basic_(classic) "Visual Basic (classic)")
- [Multiplan](https://en.wikipedia.org/wiki/Multiplan "Multiplan")[[17]](https://en.wikipedia.org/wiki/Bytecode#cite_note-Multiplan-18)
- [O-code](https://en.wikipedia.org/wiki/O-code "O-code") of the [BCPL](https://en.wikipedia.org/wiki/BCPL "BCPL") programming language
- [OCaml](https://en.wikipedia.org/wiki/OCaml "OCaml") language optionally compiles to a compact bytecode form
- [p-code](https://en.wikipedia.org/wiki/P-code_machine "P-code machine") of [UCSD Pascal](https://en.wikipedia.org/wiki/UCSD_Pascal "UCSD Pascal") implementation of the [Pascal](https://en.wikipedia.org/wiki/Pascal_(programming_language) "Pascal (programming language)") language
- [Parrot virtual machine](https://en.wikipedia.org/wiki/Parrot_virtual_machine "Parrot virtual machine")
- [Pick BASIC](https://en.wikipedia.org/wiki/Pick_operating_system "Pick operating system") also referred to as Data BASIC or [MultiValue BASIC](https://en.wikipedia.org/wiki/MultiValue#MultiValue_DataBASIC "MultiValue")
- The [R environment for statistical computing](https://en.wikipedia.org/wiki/R_(programming_language) "R (programming language)") offers a bytecode compiler through the compiler package, now standard with R version 2.13.0. It is possible to compile this version of R so that the base and recommended packages exploit this.[[18]](https://en.wikipedia.org/wiki/Bytecode#cite_note-cran_r-19)
- [Pyramid 2000](https://en.wikipedia.org/wiki/Pyramid_2000 "Pyramid 2000") adventure game
- [Python](https://en.wikipedia.org/wiki/Python_(programming_language) "Python (programming language)") scripts are being compiled on execution to Python's bytecode language, and the compiled files (.pyc) are cached inside the script's folder

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