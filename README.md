# The LLVM Compiler Infrastructure
## LLVM Overview
#### The LLVM Project is a collection of modular and reusable compiler and toolchain technologies. Despite its name, LLVM has little to do with traditional virtual machines. The name "LLVM" itself is not an acronym; it is the full name of the project.

#### LLVM began as a research project at the University of Illinois, with the goal of providing a modern, SSA-based compilation strategy capable of supporting both static and dynamic compilation of arbitrary programming languages. Since then, LLVM has grown to be an umbrella project consisting of a number of subprojects, many of which are being used in production by a wide variety of commercial and open source projects as well as being widely used in academic research. Code in the LLVM project is licensed under the "Apache 2.0 License with LLVM exceptions"

### The primary sub-projects of LLVM are:

#### The LLVM Core libraries provide a modern source- and target-independent optimizer, along with code generation support for many popular CPUs (as well as some less common ones!) These libraries are built around a well specified code representation known as the LLVM intermediate representation ("LLVM IR"). The LLVM Core libraries are well documented, and it is particularly easy to invent your own language (or port an existing compiler) to use LLVM as an optimizer and code generator.

#### Clang is an "LLVM native" C/C++/Objective-C compiler, which aims to deliver amazingly fast compiles, extremely useful error and warning messages and to provide a platform for building great source level tools. The Clang Static Analyzer and clang-tidy are tools that automatically find bugs in your code, and are great examples of the sort of tools that can be built using the Clang frontend as a library to parse C/C++ code.

#### The LLDB project builds on libraries provided by LLVM and Clang to provide a great native debugger. It uses the Clang ASTs and expression parser, LLVM JIT, LLVM disassembler, etc so that it provides an experience that "just works". It is also blazing fast and much more memory efficient than GDB at loading symbols.

#### The libc++ and libc++ ABI projects provide a standard conformant and high-performance implementation of the C++ Standard Library, including full support for C++11 and C++14.

#### The compiler-rt project provides highly tuned implementations of the low-level code generator support routines like "__fixunsdfdi" and other calls generated when a target doesn't have a short sequence of native instructions to implement a core IR operation. It also provides implementations of run-time libraries for dynamic testing tools such as AddressSanitizer, ThreadSanitizer, MemorySanitizer, and DataFlowSanitizer.

#### The MLIR subproject is a novel approach to building reusable and extensible compiler infrastructure. MLIR aims to address software fragmentation, improve compilation for heterogeneous hardware, significantly reduce the cost of building domain specific compilers, and aid in connecting existing compilers together.

#### The OpenMP subproject provides an OpenMP runtime for use with the OpenMP implementation in Clang.

#### The polly project implements a suite of cache-locality optimizations as well as auto-parallelism and vectorization using a polyhedral model.

#### The libclc project aims to implement the OpenCL standard library.

#### The klee project implements a "symbolic virtual machine" which uses a theorem prover to try to evaluate all dynamic paths through a program in an effort to find bugs and to prove properties of functions. A major feature of klee is that it can produce a testcase in the event that it detects a bug.

#### The LLD project is a new linker. That is a drop-in replacement for system linkers and runs much faster.

#### The BOLT project is a post-link optimizer. It achieves the improvements by optimizing application's code layout based on execution profile gathered by sampling profiler.

#### In addition to official subprojects of LLVM, there are a broad variety of other projects that use components of LLVM for various tasks. Through these external projects you can use LLVM to compile Ruby, Python, Haskell, Rust, D, PHP, Pure, Lua, Julia, and a number of other languages. A major strength of LLVM is its versatility, flexibility, and reusability, which is why it is being used for such a wide variety of different tasks: everything from doing light-weight JIT compiles of embedded languages like Lua to compiling Fortran code for massive super computers.

#### As much as everything else, LLVM has a broad and friendly community of people who are interested in building great low-level tools. If you are interested in getting involved, a good first place is to skim the LLVM Blog and join LLVM Discourse. For information on how to send in a patch, get commit access, and copyright and license topics, please see the LLVM Developer Policy.
