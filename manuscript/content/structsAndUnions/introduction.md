# Structs and Unions
Encapsulation of other types into more complex data structures can be done by using structs/unions and classes. These enable a unit of work or purpose to be associated with a group of information within memory.
There are advanced topics associated with types, specifically type information which is also introduced.

## Type information
**Summary:**

Type information is the run time information regarding types that is derived from compile time information.

**Theory:**

During the compilation, the compiler has access to large amounts of information regarding any type declarations. Some of this gets filtered into what is known as run time information. Run time information is a limited subset that most provides information for e.g. the garbage collector.

It is an advanced topic and one that D could very easily remove as compile time reflection via traits is preferred.
The difference between run time reflection (which type information provides for) and compile time reflection is one occurs during compilation. Because of this the assembly produced can be highly optimized unlike run time reflection.
Other languages such as Java, C# and PHP provide run time reflection as it is the only means to do so.

Reflection is the means to gain information about types during run time. It can also be used to find all symbols/modules within a program.

All types in the D programming language have type information, including primitives. Which is accessed by using:

{line-numbers=off}
```D
writeln(typeid(int).name);
```