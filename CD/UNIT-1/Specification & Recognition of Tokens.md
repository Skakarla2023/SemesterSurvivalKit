# Specification & Recognition of Tokens

- In compiler design, tokens are the basic building blocks.

- A token = pair of (token-name, attribute-value)

- Token-name → general category (e.g., identifier, number, keyword).

- Attribute-value → points to symbol table entry for more info.

## 1. Specification of Tokens

1. This is about describing tokens formally.

2. Tokens are specified using patterns.

3. A pattern is a rule describing how a token looks.

4. Usually expressed with regular expressions.

#### 🧠 Examples:

```
Identifier → letter (letter | digit)*

Number → digit+

Whitespace → (space | tab | newline)+

Keyword if → just the string "if"
```

## 2. Recognition of Tokens

1. This is the actual process of finding tokens in the source program.

2. Done by the Lexical Analyzer (scanner).

3. Reads the input, matches characters with patterns, and produces tokens.

4. Uses finite automata (DFA/NFA) to recognize regular expression patterns.

#### 🧠 Example:

Input: int a = 25;

Lexical Analyzer recognizes:

```
"int" matches keyword pattern.

"a" matches identifier pattern.

"=" matches assignment operator pattern.

"25" matches number pattern.

";" matches semicolon pattern.
```
