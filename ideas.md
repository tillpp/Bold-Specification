Syntax should be a bit like Zig.

# Lifetime specified

Any data or part of data can become invalid after a certain time.
At which point it is not allowed to be used:

```zig
const x = IntArray();
x.push(8);
const y = &x[0]; // y is attached to x.innerdata lifetime.
y = 7; // valid
x.push(10); // x.innerData lifetime runs out.
y = 1; // invalid



```

# Don't allow global variables 

Maybe make every file be a class

# Acyclic file imports (Layers of abstraction)

To ensure simple code, code build up in levels, each level being able to access all the previous levels.
Files may define Parameters, that can be set by upper layers.

# Version control system

more context sensitiv, to notice change moves in code.

# syntax highlighting

should also work for comptime values