## GSOC'24 : Implementation of classes and OOP features.

### Week 1:
LPython is a compiled language with static typing, drawing inspiration from Python's syntax. Designed to seamlessly integrate with both Python and C libraries, LPython features multiple backend targets, including C, C++, and LLVM IR. This enables compilation into executable files using the respective C/C++ or LLVM compiler toolchains. Thanks to its static typing and ahead-of-time compilation, LPython delivers performance that significantly surpasses that of CPython. However, LPython is not yet feature-complete and still contains some bugs. One key feature currently missing from LPython is the Object-Oriented Programming (OOP) paradigm. My goal is to implement basic OOP features in LPython.

### Work Done So Far

I have successfully added class support to LPython. Previously, structs were used to represent classes. Now, the Abstract Syntax Representation (ASR) node can also house function definitions. Additionally, I fixed a bug in the `visitClassDef` function in `python_ast_to_asr`. This function was being called twice, causing the symbol table for the class to be generated twice. This issue has now been resolved.

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

