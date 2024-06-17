# My Personal CPP Style Guide

My style guide uses Google formatting and naming conventions, and CPP core guidelines for other style decisions. Personal rules are listed below. Included here as well are the standard tools I use.

## Code Standards

### CPP Standard

Use any version after CPP 11 you like, but newer is better. CPP 11 is as old as anyone wants to maintain.

### Line Length

I use a line length of 120. This is promotes descriptive variable names and prevents the splitting of certain logic that is more understandable on one line. It still still preferable to use shorted lines when possible.

### Boost

Whenever there is an alternative available in the standard library prefer using that over Boost. (ex. Boost::hash) Otherwise there are no limits on the use of Boost.

### Documentation

Every non trivial public function or class should have a doxygen style comment with the following style.

``` cpp
/**
 * Comments here
 */
 ```

Other than that follow cpp core guide lines suggestions.

## Tools

### Clang Format

Included here is my .clang-format file. It uses Google's style guide with an extended line length.

Include ordering is also disabled as it doesn't recognize external libraries correctly.

### Clang Tidy

Included here is my .clang-tidy file. It has default clang-tidy rules, and cppcoreguidlines rules enabled.

LLVM 19 is required for the include .clang-tidy file to work correctly.

### CLion

I use CLion for my development environment. It is cross platform, and does not require a continued subscription (you just lose updates). For the most part I let CLion include its default code checks next to clang-tiday

### Compilers

All code should be portable. Use the most popular compiler for your system. GCC for linux, MSVC for windows, clang for mac.

### CMake

Use Cmake for the build system. If compiling libraries, compile the library and include it in all the targets to prevent recompiling files over and over again.

### Unit Testing

So far I use the Boost testing framework, though future work may switch to GTest. All tests should be able to run with CTest.
