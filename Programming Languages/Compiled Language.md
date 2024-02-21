A compiled language is **a programming language that is converted into machine code so that the processor can execute it**. The compiled languages are usually compiled, not interpreted.

A **compiled language** is a [[Programming Languages|language]] whose [[Implementation|implementation]] are typically [[Compiler|compilers]] (translators that generate [[Machine Code|machine code]] from [[Source Code|source code]]), and not [[Interpreter|interpreters]] (step-by-step executors of [[Source Code|source code]], where no pre-runtime translation takes place).

The term is somewhat vague. In principle, any language can be implemented with a compiler or with an interpreter. A combination of both solutions is also common: a compiler can translate the source code into some intermediate form (often called [[Bytecode|p-code]] or [[Bytecode|bytecode]]), which is then passed to an interpreter which executes it.

## Advantages and disadvantages

Programs compiled into native code at compile time tend to be faster than those translated at runtime due to the translation process's overhead. Newer technologies such as [[Just-In-Time Compilation|just-in-time compilation]], and general improvements in the translation process are starting to narrow this gap, though. Mixed solutions using bytecode tend toward intermediate efficiency.

[[Low-level programming languages]] are typically compiled, especially when efficiency is the main concern, rather than [[Cross-Platform|cross-platform]] support. For such languages, there are more one-to-one correspondences between the programmed code and the hardware operations performed by [[Machine Code|machine code]], making it easier for programmers to control the use of [[Central Processing Unit (CPU)|central processing unit]] (CPU) and [[Memory|memory]] in fine detail.

With some effort, it is always possible to write compilers even for traditionally [[Interpreted Languages|interpreted languages]]. For example, [[Common Lisp]] can be compiled to [[Java]] bytecode (then interpreted by the [[Java Virtual Machine|Java virtual machine]], [[C]] code (then compiled to native machine code), or directly to native code. Programming languages that support multiple compiling targets give developers more control to choose either execution speed or cross-platform compatibility or usage.