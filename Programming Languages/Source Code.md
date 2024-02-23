In [[computing]], **source code**, or simply **code**, is text (usually [[plain text]] that conforms to a [[human-readable]] [[Programming Languages|programming language]] and specifies the behavior of a computer. A programmer writes code to produce a program that runs on a computer.

Since a computer, at base, only understands [[Machine Code|machine code]], source must be translated in order to be used by the computer and this can be implemented in a variety of ways depending on available technology. Source code can be converted by a [[Compiler|compiler]] or an [[Assembler|assembler]] into machine code that can be directly executed. Alternatively, source code can be processed without conversion to machine code via an [[Interpreter|interpreter]] that performs the actions prescribed by the source code via the interpreter's machine code. Other technology (i.e. [[Bytecode|bytecode]] incorporates both mechanisms by converting the source code to an intermediate form that is often _not_ human-readable but also _not_ machine code and an interpreter executes the intermediate form.

Most languages allow for comments. The programmer can add comments to document the source code for themself and for other programmers reading the code. Comments cannot be represented in machine code, and therefore, are ignored by compilers, interpreters and the like.

Often, the source code of application software is not distributed or publicly available since the producer wants to protect their Intellectual property. But, if the source code is available (open source), it can be useful to a user, programmer or a system administrator, any of whom might wish to study or modify the program.

## Definitions

[Richard Stallman's](https://en.wikipedia.org/wiki/Richard_Stallman "Richard Stallman") definition, formulated in his [1989 seminal license](https://en.wikipedia.org/wiki/GPL "GPL"), proposed source code as whatever form in which software is modified:

> The "source code" for a work means the preferred form of the work for making modifications to it.

Some classical sources define source code as the text form of programming languages, for example:

> Source code (also referred to as source or code) is the version of software as it is originally written (i.e., typed into a computer) by a human in plain text (i.e., human readable alphanumeric characters).

This responds to the fact that, when [[Program Translation|program translation]] first appeared, the contemporary form of software production were textual programming languages, thus source code was text code while [[Machine Code|machine code]] was target code. However, as programming pipelines started to incorporate more intermediate forms, some in languages like JavaScript that could be either source or target, text code stopped being synonymous with source code.

Stallman's definition thus contemplates JavaScript and HTML's source-target ambivalence, as well as contemplating possible future forms of software production, like visual programming languages, or datasets in Machine Learning.

Other broader interpretations, however, consider source code to include the machine code along with all the high level languages that produce it, this definition undoes the original machine/text distinction by considering each step in the program translation to be source code.

> For the purpose of clarity "source code" is taken to mean any fully executable description of a software system. It is therefore so construed as to include machine code, very high level languages and executable graphical representations of systems.
This approach allows for a much more flexible approach to system analysis, dispensing with the requirement for designer to collaborate by publishing a convenient form for understanding and modification. It can also be applied to scenarios where a designer is not needed, like DNA. However, this form of analysis does not contemplate a costlier machine-to-machine code analysis than human-to-machine code analysis.

The earliest programs for stored-program computers were entered in binary through the front panel switches of the computer. This first-generation programming language had no distinction between source code and machine code.

When IBM first offered software to work with its machine, the source code was provided at no additional charge. At that time, the cost of developing and supporting software was included in the price of the hardware. For decades, IBM distributed source code with its software product licenses, until 1983.

Most early computer magazines published source code as type-in programs.

Occasionally the entire source code to a large program is published as a hardback book, such as _Computers and Typesetting_, vol. B: _TeX, The Program_ by Donald Knuth, _PGP Source Code and Internals_ by Philip Zimmermann, _PC SpeedScript_ by Randy Thompson, and _µC/OS, The Real-Time Kernel_ by Jean Labrosse.

## Organization

The source code which constitutes a program is usually in one or more text files stored on a computer file system. A larger codebase may be organized in a directory tree known as a _source tree_. Source code can also be stored in a database, as is common for stored procedures, or elsewhere.

[![](https://upload.wikimedia.org/wikipedia/commons/thumb/7/75/CodeCmmt002.svg/220px-CodeCmmt002.svg.png)](https://en.wikipedia.org/wiki/File:CodeCmmt002.svg)

A more complex [[Java]] source code example. Written in [[Object-Oriented Programming]] style, it demonstrates [boilerplate code](https://en.wikipedia.org/wiki/Boilerplate_code "Boilerplate code"). With prologue comments indicated in red, inline comments indicated in green, and program statements indicated in blue.

A program's source code can be written in multiple programming languages.For example, it is not uncommon for a program written primarily in [[C]] or [[C++]] to have portions written in [[Assembly|assembly language]] for optimization purposes.

Some languages allow multiple languages in the same file. For example, a block of assembly embedded in a C file.

[[Library Linking]] allows for components to be written and compiled separately, sometimes in multiple languages, and later integrated into a program. For example, with [[Java]], classes are compiled into separate files that are linked together by the interpreter at [[Runtime|runtime]]. Microsoft Windows supports programs built from [[DLLs]]; each of which can be written in any language that can be compiled to a DLL. Similarly, [[.NET Core]] supports programs built from [[Assembly (CLI)]]; each of which can be written in any [[CLI Language]].

A program's [[Entry Point|entry point]] can be an interpreter. The interpreter could be designed for an application-specific, custom language or for a general-purpose language so that the interpreter is can be used for multiple applications.

Typically, source code is stored in a [[Version Control|version control]] system.

To produce runnable software, a complex codebase often requires building (compiling, assembling, ...) many source code files – hundreds, thousands or more. Instructions for building, such as a [[Makefile]], are often controlled with the source code in the same version control [[Repository|repository]]. These build instruction files describe the relationships among the source code files and contain information about how they are to be built separately and then combined together.

## Purposes

Source code is primarily input to an computer process that ultimately results in controlling computer behavior. In other words, it is input to a [[compiler]], [[interpreter]] or the like.

It is also used to communicate [[Algorithm|algorithms]] between people – e.g., [[Snippets|code snippets]] online or in books.

Computer programmers may find it helpful to review existing source code to learn about programming techniques.The sharing of source code between developers is frequently cited as a contributing factor to the maturation of their programming skills.Some people consider source code an expressive artistic medium.

[[Porting]] software to another [[Platforms|computer platform]] is usually prohibitively difficult and expensive without source code. One possible porting option without source code is [[Binary Translation|binary translation]]. An other is emulation of the original platform although this is often too computationally expensive; runs slowly. 

[[Decompilation]] is the process of converting machine code to a more usable form – often to [[Assembly|assembly code]] or [[Hifh-Level Language|high-level language]] source code.

[[Software Reusability]] describes the practice of using existing software in another software system via a [[Software Library|software library]]. Some may consider reuse to include adapting source code from one piece of software to another.

## Legal aspects

The situation varies worldwide, but in the United States before 1974, software and its source code was not copyrightable and therefore always public domain software.

In 1974, the US Commission on New Technological Uses of Copyrighted Works (CONTU) decided that "computer programs, to the extent that they embody an author's original creation, are proper subject matter of copyright".

In 1983 in the United States court case _[Apple v. Franklin](https://en.wikipedia.org/wiki/Apple_v._Franklin "Apple v. Franklin")_ it was ruled that the same applied to [Object Modules|object code]]; and that the Copyright Act gave computer programs the copyright status of literary works.

In 1999, in the United States court case _[Bernstein v. United States](https://en.wikipedia.org/wiki/Bernstein_v._United_States "Bernstein v. United States")_ it was further ruled that source code could be considered a constitutionally protected form of free speech. Proponents of free speech argued that because source code conveys information to programmers, is written in a language, and can be used to share humor and other artistic pursuits, it is a protected form of communication.
### Licensing

Copyright notice example:

> Copyright [yyyy] [name of copyright owner]
> 
> Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at
> 
> http://www.apache.org/licenses/LICENSE-2.0
> 
> Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.

An author of a non-trivial work like software, has several exclusive rights, among them the copyright for the source code and [[Object Modules|object code]].The author has the right and possibility to grant customers and users of his software some of his exclusive rights in form of [[Software Licensing]]. Software, and its accompanying source code, can be associated with several licensing paradigms; the most important distinction is free software vs proprietary software. This is done by including a copyright notice that declares licensing terms. If no notice is found, then the default of _All rights reserved_ is implied.

Generally speaking, a software is free software if its users are free to use it for any purpose, study and change its source code, give or sell its exact copies, and give or sell its modified copies. Software is _proprietary_ if it is distributed while the source code is kept secret, or is privately owned and restricted. One of the first software licenses to be published and to explicitly grant these freedoms was the GNU General Public License in 1989; the BSD license is another early example from 1990.

For proprietary software, the provisions of the various copyright laws, trade secrecy and patents are used to keep the source code closed. Additionally, many pieces of retail software come with an end-user license agreement (EULA) which typically prohibits [[Decompilation|decompilation]], reverse engineering, analysis, modification, or circumventing of copy protection. Types of source code protection—beyond traditional [[Compilation|compilation]] to [[Object Modules|object code]]—include code encryption, [[Obfuscation|code obfuscation]] or [[Morphing|code morphing]].

## Quality

Main article: [[Testing and Quality Assurance]]

The way a program is written can have important consequences for its maintainers. [[Conventions|Coding conventions]], which stress [[Readability|readability]] and some language-specific conventions, are aimed at the maintenance of the software source code, which involves [[Debugging|debugging]] and [[Updating|updating]]. Other priorities, such as the speed of the program's execution, or the ability to compile the program for multiple architectures, often make code readability a less important consideration, since code _quality_ generally depends on its _purpose_.