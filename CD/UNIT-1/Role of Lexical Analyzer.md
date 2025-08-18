# Role of Lexical Analyser

1. The Lexical Analyzer (Scanner) is the first phase of a compiler.
2. It reads the source code character by character and groups them into meaningful units called tokens.
3. It acts as a bridge between the source program and the syntax analyzer (parser).

<img width="364" height="138" alt="image" src="https://github.com/user-attachments/assets/03b75a02-8321-4271-9d83-29b49c272467" />

## Functions of a Lexical Analyser

### 1. Token Generation

- Converts sequence of characters into tokens.

- A token is a meaningful unit → keyword, identifier, operator, literal, punctuation.


1. Token Generation
2. Removes Whitespaces
3. Error detection
4. Acts as an interface
5. Symbol table


### 1. Token Generation

- Converts sequence of characters into tokens.

- A token is a meaningful unit → keyword, identifier, operator, literal, punctuation.

Example: a = b + c; → tokens: id(a), =, id(b), +, id(c), ;.

### 2. Removing Whitespaces & Comments

- Skips unnecessary characters like spaces, tabs, newlines.

- Removes comments (not useful for compilation).

### 3. Error Detection

- Detects errors in tokens such as invalid identifiers, illegal characters.

Example: Variable name starting with a digit is invalid.

### 4. Communicates with Symbol Table

- Stores information about identifiers (variables, constants, functions).

- Passes attributes like type, scope, memory location to the symbol table.

### 5. Acts as an Interface

- Simplifies the job of the parser by providing tokens instead of raw characters.

- Parser works on tokens, not on individual characters.
