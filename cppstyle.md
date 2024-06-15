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

### Visual Studio

I use Visual Studio as my development environment as it has the most seamless integration of cpp features. Note that this does not limit the use of other environments if you so choose.

In Visual Studio I disable Microsoft's code analysis and just use clang tidy.
You can see how this is done in the include CMakeSettings.json

Visual is configured to format with clang format on save. Modifying Visual Studio behavior to follow Google's formatting is useful.

### Compilers

I use the clang compiler as it is cross platform. Though code should be written to be portable and cross platform.

### CMake

Use Cmake for the build system. If compiling libraries, compile the library and include it in all the targets to prevent recompiling files over and over again.

### Unit Testing

So far I use the Boost testing framework, though future work may switch to Gtest. All tests should be able to run with Ctest.