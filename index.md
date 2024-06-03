
```markdown
## Implementing Basic OOP Features in LPython

LPython is a statically typed, compiled programming language with a syntax inspired by Python. It aims to provide first-class support for working with both Python and C libraries. LPython supports multiple backend targets like C, C++, and LLVM IR, allowing for compilation to target executables using the appropriate C/C++ compiler or the LLVM compiler toolchain. Due to its static typing and ahead-of-time compilation, LPython offers significantly better performance than CPython. However, LPython is not yet feature-complete and still contains some bugs. One key feature currently missing from LPython is the Object-Oriented Programming (OOP) paradigm. My goal is to implement basic OOP features in LPython.

### Work Done So Far

I have successfully added class support to LPython. Previously, structs were used to represent classes. Now, the Abstract Syntax Tree (AST) node can also house function definitions. Additionally, I fixed a bug in the `visitClassDef` function in `python_ast_to_asr`. This function was being called twice, causing the symbol table for the class to be generated twice. This issue has now been resolved.

You can view the changes in this pull request: [PR #2721](https://github.com/lcompilers/lpython/pull/2721).

### Tasks for the Next Week

1. **Add ClassProcedure Nodes to the ASR:**
   - Extend the Abstract Syntax Representation (ASR) to include `ClassProcedure` nodes, which will represent methods within classes.

2. **Link ClassProcedure Nodes with the Correct FunctionDef Nodes:**
   - Write the logic to ensure that `ClassProcedure` nodes are correctly linked to their corresponding `FunctionDef` nodes.

3. **Make Functions Callable from Classes:**
   - Implement the functionality to allow functions (methods) to be called on class instances, enabling typical OOP method invocation.

4. **Implement Constructor Following Python Variable Storage Conventions:**
   - Ensure that the constructor (`__init__` method) adheres to Python's variable storage conventions, correctly initializing instance variables.

### Conclusion

By implementing these tasks, we aim to bring basic OOP capabilities to LPython, making it more powerful and versatile. Stay tuned for updates as we continue to enhance LPython's feature set.
```

