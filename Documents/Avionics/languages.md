**[Back to Avionics](https://und-arc.github.io/research/avionics/index.html)**

# Programming Languages

This aims to be a catalog of most of the different programming languages that would have applications at ARC, what sets them apart, and some qualities that might make one language better for some function than another.

[C](#c)  
[Python](#python)  
[Java](#java)  
[Ada](#ada)  

## C

Low(er) level code that compiles into machine code.  Very fast, but will blow up in your face if you use it wrong.  Functional programming.

## Python

High level language that is interpreted rather than compiled.  Easy to debug, useful error messages, easy to write and read.  "Batteries-included" philosphy -- 90% of needed libraries (networking, multithreading, reflection) are already included.  Runs anywhere.  Relatively quite slow and due to [implementation details](https://softwareengineering.stackexchange.com/questions/186889/why-was-python-written-with-the-gil) can only have 1 thread running at a time.  Object-oriented.

Downside: has two different versions (py 2 and py 3) with different syntax.  Semantics is nearly identical, and due to this any work at ARC done in Python should use the most recent version of Python 3.

## Java

High level language, compiles to JVM bytecode.  Would likely be an unfortunate choice for anything that has to interface with metal on a rocket, as escaping the JVM can be difficult (it's not designed with that in mind).  Fairly fast and java bytecode will run on anything with a JVM, but not all things have a JVM and if there isn't a port for the machine we'd have to make one.  Object-oriented.

## Ada

Falls somewhere between [C](#c) and [Python](#python), more towards the [C](#c) end.  Ada is linked using the same linker as C code, but is compiled in a different manner.  Very fast, and while slightly more taxing to write, if it compiles, it will run.  Commonly used in rocketry (see Arianne 5 -- programming error, not language failure).  Most unique semantics and likely harder to learn on the fly.  Not a commonly known language.  
