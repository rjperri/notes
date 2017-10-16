# Chapter 1: Packaging, Compiling, and Interpreting Java Code

## The Java Platform
_Exam Objective: Compare and contrast the features and components of Java, such as platform independence, objective orientation, encapsulation and so on_

### Platform Independence
- **Bytecode** compiled java code to run on JVM
- can be compiled on WINDOWS and ran on Linux

### Java's Object-Oriented Philosophy
- **Encapsulation** object that uses data prtoection and exposes only some of ts data and methods
 - The data and methods that are for internal use in the object are not exposed to other objects
- **Abstraction** the ablity to generalize algorithms.
 - Code reuse and flexability
 - _Inheritance_ and _polymorphism_ help create resuable code

### Robust and Secure
- Java was designed to not have explicit pointers
- Java variables do store references to objects but do not allow access to, or modification of, the memory address stored for refeence
- JVM periodically runs the built in **Garbage collector**
 - looks for objects that have gone out of scope, and delocates their memory
- Java automatically checks the bounds of arrays.
 - if index is out of bounds, an exception is thrown

## Understand Packages
