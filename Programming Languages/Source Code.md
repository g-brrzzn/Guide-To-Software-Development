In [computing](https://en.wikipedia.org/wiki/Computing "Computing"), **source code**, or simply **code**, is text (usually [plain text](https://en.wikipedia.org/wiki/Plain_text "Plain text")) that conforms to a [human-readable](https://en.wikipedia.org/wiki/Human-readable "Human-readable") [programming language](https://en.wikipedia.org/wiki/Programming_language "Programming language") and specifies the behavior of a [computer](https://en.wikipedia.org/wiki/Computer "Computer"). A [programmer](https://en.wikipedia.org/wiki/Programmer "Programmer") writes code to produce a [program](https://en.wikipedia.org/wiki/Computer_program "Computer program") that runs on a computer.

Since a computer, at base, only understands [machine code](https://en.wikipedia.org/wiki/Machine_code "Machine code"), source must be translated in order to be used by the computer and this can be implemented in a variety of ways depending on available technology. Source code can be converted by a [compiler](https://en.wikipedia.org/wiki/Compiler "Compiler") or an [assembler](https://en.wikipedia.org/wiki/Assembler_(computing) "Assembler (computing)") into machine code that can be directly [executed](https://en.wikipedia.org/wiki/Execution_(computing) "Execution (computing)"). Alternatively, source code can be processed without conversion to machine code via an [interpreter](https://en.wikipedia.org/wiki/Interpreter_(computing) "Interpreter (computing)") that performs the actions prescribed by the source code via the interpreter's machine code. Other technology (i.e. [bytecode](https://en.wikipedia.org/wiki/Bytecode "Bytecode")) incorporates both mechanisms by converting the source code to an intermediate form that is often _not_ human-readable but also _not_ machine code and an interpreter executes the intermediate form.

Most languages allow for [comments](https://en.wikipedia.org/wiki/Comment_(computer_programming) "Comment (computer programming)"). The programmer can add comments to [document](https://en.wikipedia.org/wiki/Software_documentation "Software documentation") the source code for themself and for other programmers reading the code. Comments cannot be represented in machine code, and therefore, are ignored by compilers, interpreters and the like.

Often, the source code of [application software](https://en.wikipedia.org/wiki/Application_software "Application software") is not distributed or publicly available since the producer wants to protect their [Intellectual property](https://en.wikipedia.org/wiki/Intellectual_property "Intellectual property") (IP). But, if the source code is available ([open source](https://en.wikipedia.org/wiki/Open_source "Open source")), it can be useful to a [user](https://en.wikipedia.org/wiki/User_(computing) "User (computing)"), programmer or a [system administrator](https://en.wikipedia.org/wiki/System_administrator "System administrator"), any of whom might wish to study or modify the program.

## Definitions

[Richard Stallman's](https://en.wikipedia.org/wiki/Richard_Stallman "Richard Stallman") definition, formulated in his [1989 seminal license](https://en.wikipedia.org/wiki/GPL "GPL"), proposed source code as whatever form in which software is modified:

> The "source code" for a work means the preferred form of the work for making modifications to it.[[2]](https://en.wikipedia.org/wiki/Source_code#cite_note-2)

Some classical sources define source code as the text form of programming languages, for example:

> Source code (also referred to as source or code) is the version of software as it is originally written (i.e., typed into a computer) by a human in [plain text](https://en.wikipedia.org/wiki/Plain_text "Plain text") (i.e., human readable alphanumeric characters).[[3]](https://en.wikipedia.org/wiki/Source_code#cite_note-3)

This responds to the fact that, when [program translation](https://en.wikipedia.org/wiki/Program_translation "Program translation") first appeared, the contemporary form of software production were textual programming languages, thus source code was text code while [machine code](https://en.wikipedia.org/wiki/Assembly_language "Assembly language") was target code. However, as programming pipelines started to incorporate more intermediate forms, some in languages like JavaScript that could be either source or target, text code stopped being synonymous with source code.

Stallman's definition thus contemplates JavaScript and HTML's source-target ambivalence, as well as contemplating possible future forms of software production, like visual programming languages, or datasets in Machine Learning.[[4]](https://en.wikipedia.org/wiki/Source_code#cite_note-4)[[5]](https://en.wikipedia.org/wiki/Source_code#cite_note-5)

Other broader interpretations, however, consider source code to include the machine code along with all the high level languages that produce it, this definition undoes the original machine/text distinction by considering each step in the program translation to be source code.

> For the purpose of clarity "source code" is taken to mean any fully executable description of a software system. It is therefore so construed as to include machine code, very high level languages and executable graphical representations of systems. [[6]](https://en.wikipedia.org/wiki/Source_code#cite_note-6)[[7]](https://en.wikipedia.org/wiki/Source_code#cite_note-7)

This approach allows for a much more flexible approach to system analysis, dispensing with the requirement for designer to collaborate by publishing a convenient form for understanding and modification. It can also be applied to scenarios where a designer is not needed, like DNA. However, this form of analysis does not contemplate a costlier machine-to-machine code analysis than human-to-machine code analysis.

The earliest programs for [stored-program computers](https://en.wikipedia.org/wiki/Stored-program_computer "Stored-program computer") were entered in binary through the [front panel](https://en.wikipedia.org/wiki/Front_panel "Front panel") switches of the computer. This [first-generation programming language](https://en.wikipedia.org/wiki/First-generation_programming_language "First-generation programming language") had no distinction between source code and [machine code](https://en.wikipedia.org/wiki/Machine_code "Machine code").

When IBM first offered software to work with its machine, the source code was provided at no additional charge. At that time, the cost of developing and supporting software was included in the price of the hardware. For decades, IBM distributed source code with its software product licenses, until 1983.[[8]](https://en.wikipedia.org/wiki/Source_code#cite_note-8)

Most early computer magazines published source code as [type-in programs](https://en.wikipedia.org/wiki/Type-in_program "Type-in program").

Occasionally the entire source code to a large program is published as a hardback book, such as _Computers and Typesetting_, vol. B: _TeX, The Program_ by [Donald Knuth](https://en.wikipedia.org/wiki/Donald_Knuth "Donald Knuth"), _PGP Source Code and Internals_ by [Philip Zimmermann](https://en.wikipedia.org/wiki/Philip_Zimmermann "Philip Zimmermann"), _PC SpeedScript_ by [Randy Thompson](https://en.wikipedia.org/wiki/Randy_Thompson "Randy Thompson"), and _µC/OS, The Real-Time Kernel_ by Jean Labrosse.

## Organization

The source code which constitutes a [program](https://en.wikipedia.org/wiki/Computer_program "Computer program") is usually in one or more [text files](https://en.wikipedia.org/wiki/Text_file "Text file") stored on a computer [file system](https://en.wikipedia.org/wiki/File_system "File system"). A larger [codebase](https://en.wikipedia.org/wiki/Codebase "Codebase") may be organized in a [directory tree](https://en.wikipedia.org/wiki/Directory_(file_systems) "Directory (file systems)") known as a _source tree_. Source code can also be stored in a [database](https://en.wikipedia.org/wiki/Database "Database"), as is common for [stored procedures](https://en.wikipedia.org/wiki/Stored_procedure "Stored procedure"), or elsewhere.

[![](https://upload.wikimedia.org/wikipedia/commons/thumb/7/75/CodeCmmt002.svg/220px-CodeCmmt002.svg.png)](https://en.wikipedia.org/wiki/File:CodeCmmt002.svg)

A more complex [Java](https://en.wikipedia.org/wiki/Java_(programming_language) "Java (programming language)") source code example. Written in [object-oriented programming](https://en.wikipedia.org/wiki/Object-oriented_programming "Object-oriented programming") style, it demonstrates [boilerplate code](https://en.wikipedia.org/wiki/Boilerplate_code "Boilerplate code"). With prologue comments indicated in red, inline comments indicated in green, and program statements indicated in blue.

A program's source code can be written in multiple programming languages.[[9]](https://en.wikipedia.org/wiki/Source_code#cite_note-9) For example, it is not uncommon for a program written primarily in [C](https://en.wikipedia.org/wiki/C_(programming_language) "C (programming language)") to have portions written in [assembly language](https://en.wikipedia.org/wiki/Assembly_language "Assembly language") for optimization purposes.

Some languages allow multiple languages in the same file. For example, a block of assembly embedded in a C file.

[Library linking](https://en.wikipedia.org/wiki/Library_(computing)#Linking "Library (computing)") allows for components to be written and compiled separately, sometimes in multiple languages, and later integrated into a program. For example, with [Java](https://en.wikipedia.org/wiki/Java_(programming_language) "Java (programming language)"), classes are compiled into separate files that are linked together by the interpreter at [runtime](https://en.wikipedia.org/wiki/Runtime_(program_lifecycle_phase) "Runtime (program lifecycle phase)"). [Microsoft Windows](https://en.wikipedia.org/wiki/Microsoft_Windows "Microsoft Windows") supports programs built from [DLLs](https://en.wikipedia.org/wiki/Dynamic-link_library "Dynamic-link library"); each of which can be written in any language that can be compiled to a DLL. Similarly, [Microsoft .NET](https://en.wikipedia.org/wiki/Microsoft_.NET "Microsoft .NET") supports programs built from [.NET assemblies](https://en.wikipedia.org/wiki/.NET_assemblies ".NET assemblies"); each of which can be written in any [.NET language](https://en.wikipedia.org/wiki/.NET_language ".NET language").

A program's [entry point](https://en.wikipedia.org/wiki/Entry_point "Entry point") can be an interpreter. The interpreter could be designed for an application-specific, custom language or for a general-purpose language so that the interpreter is can be used for multiple applications. [[10]](https://en.wikipedia.org/wiki/Source_code#cite_note-10)

Typically, source code is stored in a [version control system](https://en.wikipedia.org/wiki/Version_control_system "Version control system").

To produce runnable software, a complex [codebase](https://en.wikipedia.org/wiki/Codebase "Codebase") often requires building (compiling, assembling, ...) many source code files – hundreds, thousands or more. Instructions for building, such as a [Makefile](https://en.wikipedia.org/wiki/Makefile "Makefile"), are often controlled with the source code in the same version control [repository](https://en.wikipedia.org/wiki/Repository_(version_control) "Repository (version control)"). These build instruction files describe the relationships among the source code files and contain information about how they are to be built separately and then combined together.

## Purposes

Source code is primarily input to an computer process that ultimately results in controlling computer behavior. In other words, it is input to a [compiler](https://en.wikipedia.org/wiki/Compiler "Compiler"), [interpreter](https://en.wikipedia.org/wiki/Interpreter_(computing) "Interpreter (computing)") or the like.

It is also used to communicate [algorithms](https://en.wikipedia.org/wiki/Algorithm "Algorithm") between people – e.g., [code snippets](https://en.wikipedia.org/wiki/Code_snippets "Code snippets") online or in books.[[11]](https://en.wikipedia.org/wiki/Source_code#cite_note-Spinellis-11)

[Computer programmers](https://en.wikipedia.org/wiki/Programmer "Programmer") may find it helpful to review existing source code to learn about programming techniques.[[11]](https://en.wikipedia.org/wiki/Source_code#cite_note-Spinellis-11) The sharing of source code between developers is frequently cited as a contributing factor to the maturation of their programming skills.[[11]](https://en.wikipedia.org/wiki/Source_code#cite_note-Spinellis-11) Some people consider source code an expressive [artistic medium](https://en.wikipedia.org/wiki/Media_(arts) "Media (arts)").[[12]](https://en.wikipedia.org/wiki/Source_code#cite_note-12)

[Porting](https://en.wikipedia.org/wiki/Porting "Porting") software to another [computer platform](https://en.wikipedia.org/wiki/Computer_platform "Computer platform") is usually prohibitively difficult and expensive without source code. One possible porting option without source code is [binary translation](https://en.wikipedia.org/wiki/Binary_translation "Binary translation"). An other is emulation of the original platform although this is often too computationally expensive; runs slowly. [[13]](https://en.wikipedia.org/wiki/Source_code#cite_note-13)

[Decompilation](https://en.wikipedia.org/wiki/Decompilation "Decompilation") is the process of converting machine code to a more usable form – often to [assembly code](https://en.wikipedia.org/wiki/Assembly_code "Assembly code") or [high-level language](https://en.wikipedia.org/wiki/High-level_programming_language "High-level programming language") source code.

[Software reusability](https://en.wikipedia.org/wiki/Software_reusability "Software reusability") describes the practice of using existing software in another software system via a [software library](https://en.wikipedia.org/wiki/Software_library "Software library"). Some may consider reuse to include adapting source code from one piece of software to another.

## Legal aspects

See also: [History of free and open-source software](https://en.wikipedia.org/wiki/History_of_free_and_open-source_software "History of free and open-source software")

The situation varies worldwide, but in the United States before 1974, software and its source code was not [copyrightable](https://en.wikipedia.org/wiki/Copyright "Copyright") and therefore always [public domain software](https://en.wikipedia.org/wiki/Public_domain_software "Public domain software").[[14]](https://en.wikipedia.org/wiki/Source_code#cite_note-14)

In 1974, the US Commission on New Technological Uses of Copyrighted Works (CONTU) decided that "computer programs, to the extent that they embody an author's original creation, are proper subject matter of copyright".[[15]](https://en.wikipedia.org/wiki/Source_code#cite_note-15)[[16]](https://en.wikipedia.org/wiki/Source_code#cite_note-sail_book-16)

In 1983 in the United States court case _[Apple v. Franklin](https://en.wikipedia.org/wiki/Apple_v._Franklin "Apple v. Franklin")_ it was ruled that the same applied to [object code](https://en.wikipedia.org/wiki/Object_code "Object code"); and that the Copyright Act gave computer programs the copyright status of literary works.

In 1999, in the United States court case _[Bernstein v. United States](https://en.wikipedia.org/wiki/Bernstein_v._United_States "Bernstein v. United States")_ it was further ruled that source code could be considered a constitutionally protected form of [free speech](https://en.wikipedia.org/wiki/Free_speech "Free speech"). Proponents of free speech argued that because source code conveys information to programmers, is written in a language, and can be used to share humor and other artistic pursuits, it is a protected form of communication.[[17]](https://en.wikipedia.org/wiki/Source_code#cite_note-17)[[18]](https://en.wikipedia.org/wiki/Source_code#cite_note-18)[[19]](https://en.wikipedia.org/wiki/Source_code#cite_note-19)

### Licensing

Main article: [Software license](https://en.wikipedia.org/wiki/Software_license "Software license")

Copyright notice example:[[20]](https://en.wikipedia.org/wiki/Source_code#cite_note-20)

> Copyright [yyyy] [name of copyright owner]
> 
> Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at
> 
> http://www.apache.org/licenses/LICENSE-2.0
> 
> Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.

An author of a [non-trivial work](https://en.wikipedia.org/wiki/Threshold_of_originality "Threshold of originality") like software,[[16]](https://en.wikipedia.org/wiki/Source_code#cite_note-sail_book-16) has several [exclusive rights](https://en.wikipedia.org/wiki/Exclusive_right "Exclusive right"), among them the copyright for the source code and [object code](https://en.wikipedia.org/wiki/Object_code "Object code").[[21]](https://en.wikipedia.org/wiki/Source_code#cite_note-fsm-21) The author has the right and possibility to grant customers and users of his software some of his exclusive rights in form of [software licensing](https://en.wikipedia.org/wiki/Software_licensing "Software licensing"). Software, and its accompanying source code, can be associated with several licensing paradigms; the most important distinction is [free software](https://en.wikipedia.org/wiki/Free_software "Free software") vs [proprietary software](https://en.wikipedia.org/wiki/Proprietary_software "Proprietary software"). This is done by including a [copyright notice](https://en.wikipedia.org/wiki/Copyright_notice "Copyright notice") that declares licensing terms. If no notice is found, then the default of _[All rights reserved](https://en.wikipedia.org/wiki/All_rights_reserved "All rights reserved")_ is implied.

Generally speaking, a software is free software if its users are free to use it for any purpose, study and change its source code, give or sell its exact copies, and give or sell its modified copies. Software is _proprietary_ if it is distributed while the source code is kept secret, or is privately owned and restricted. One of the first software licenses to be published and to explicitly grant these freedoms was the [GNU General Public License](https://en.wikipedia.org/wiki/GNU_General_Public_License "GNU General Public License") in 1989; the [BSD license](https://en.wikipedia.org/wiki/BSD_license "BSD license") is another early example from 1990.

For proprietary software, the provisions of the various copyright laws, [trade secrecy](https://en.wikipedia.org/wiki/Trade_secret "Trade secret") and [patents](https://en.wikipedia.org/wiki/Patent "Patent") are used to keep the source code closed. Additionally, many pieces of [retail software](https://en.wikipedia.org/wiki/Retail_software "Retail software") come with an [end-user license agreement](https://en.wikipedia.org/wiki/End-user_license_agreement "End-user license agreement") (EULA) which typically prohibits [decompilation](https://en.wikipedia.org/wiki/Decompilation "Decompilation"), [reverse engineering](https://en.wikipedia.org/wiki/Reverse_engineering "Reverse engineering"), analysis, modification, or circumventing of [copy protection](https://en.wikipedia.org/wiki/Copy_protection "Copy protection"). Types of source code protection—beyond traditional [compilation](https://en.wikipedia.org/wiki/Compiler "Compiler") to [object code](https://en.wikipedia.org/wiki/Object_code "Object code")—include code encryption, [code obfuscation](https://en.wikipedia.org/wiki/Code_obfuscation "Code obfuscation") or [code morphing](https://en.wikipedia.org/wiki/Code_morphing "Code morphing").

## Quality

Main article: [Software quality](https://en.wikipedia.org/wiki/Software_quality "Software quality")

The way a program is written can have important consequences for its maintainers. [Coding conventions](https://en.wikipedia.org/wiki/Coding_conventions "Coding conventions"), which stress [readability](https://en.wikipedia.org/wiki/Readability "Readability") and some language-specific conventions, are aimed at the maintenance of the software source code, which involves [debugging](https://en.wikipedia.org/wiki/Debugging "Debugging") and [updating](https://en.wikipedia.org/wiki/Patch_(computing) "Patch (computing)"). Other priorities, such as the speed of the program's execution, or the ability to compile the program for multiple architectures, often make code readability a less important consideration, since code _quality_ generally depends on its _purpose_.