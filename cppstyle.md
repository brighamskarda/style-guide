# My Personal CPP Style Guide

Except in the instances listed below I follow the Google C++ style guide found [here](https://google.github.io/styleguide/cppguide.html). As I program and more fully understand Google's style guide I will make updates to this style guide.

## CPP Standard

Use any version you like, but newer is better.

## File Naming

Use .cpp file extension for source files. This file extension seems to be more broadly used than the .cc file extension Google uses.

Use .hpp file extension for header files. I like the differentiation this makes from C header files.

## Exceptions

Google doesn't use exceptions because of the difficulty of implementing them with existing code. All the code I'm writing is new and thus should use exceptions.

## Boost

Whenever there is an alternative available in the standard library prefer using that over Boost. (ex. Boost::hash) Otherwise there are no limits on the use of Boost, there is no need to stick to the approved libraries from Google.

## Enums

Prefer use of scoped enums over unscoped enums. Use static casts if necessary to convert to integer type.