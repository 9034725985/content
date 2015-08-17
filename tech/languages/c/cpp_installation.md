---
title: C++
page: c++
---

## C++

Like C, C++ is also a compiled language. It has many similarities with C and to some extent it is safe to say that C is
subset of C++ and C++ supports every programming technique supported by C. Next command shows how to install C++ compiler:

### G++ installation

```
# sudo dnf install gcc-c++
```

To compile and link your program you can do the same as was described above with C:
```
# g++ -std=c++14 your_source.cpp -o your_binary
```
Again in the command above there are a few examples of possible options which can be used. 
`-std=c++14` states the version of standard used when compiling your code. `-o name` again states the name of your binary program. 
You can than run your program by typing:

```
# ./your_binary
```

To view all the options that g++ can use, visit the man page by typing:
```
# man g++
```
You will see that the man page is identical with the one shown for gcc.

### CLANG installation
Clang works both for C++ and C and the installation is the same as for C:

```
# sudo dnf install clang
```

The only difference when compiling is that you need to use the command `clang++`:

```
# clang++ -std=c++14 your_source.cpp -o your_binary
```

This will produce the same result as the command with g++ above does. To see more clang options see the manual page:

```
# man clang
```