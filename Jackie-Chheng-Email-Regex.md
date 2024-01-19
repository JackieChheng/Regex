# Regex Tutorial Emails (replace with your title)

Hello, this is an introduction to regex matching an email. Which will be mentioned down below as we get started.

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

This matching specific regex is used to validate emails. This tutorial will give you a rundown on each regex component and how it applies to match an email.

## Summary

Regular expressions, or regex, are encoded text strings created to identify patterns within other strings. They prove useful when searching for character sequences that adhere to specific patterns. These patterns may range from simple exact matches to more intricate rules governing the strings they match.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Author](#author)

## Regex Components

### Anchors
Anchors don't stand for actual characters; instead, they mark positions before or after characters. In the code below, you'll notice the ^ at the beginning and the $ at the end, representing these positions.

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` 
               
The `^` symbol means the regex string will match the start of the text.

The `$` symbol means the regex string will match the end of the text.
 

### Quantifiers
Quantifiers in a regex match how many times a character, group, or character class appears in a string. In this expression below, you'll find the + and {2,6} as quantifiers.

 `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` 

  Quantifiers indicate the certain amount of characters the regex will match. 
 
 The `+` quantifier will match  1 or more characters. 
 
 The `*` quantifier will match 0 or more characters.
 
 The `?` quantifier will match 0 or 1 character.
 
 The `{n}` quantifier will match `n` character(s).
 
 The `{a,b}` quantifier will match an expression that is at least `a` character(s) but no more than `b` character(s).

### Character Classes
A character class, also known as a character set, lets you match symbols from a specific set in a string. It's a fundamental element in regex, coming right after character matches. For example, in the regex for matching an email 
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`:

`[a-z0-9_\.-]+`: This indicates the string must have at least one letter from 'a' to 'z', one or more digits from 0 to 9, an underscore '_', or a dot '.', and it can include a hyphen '-'.

`[\da-z\.-]+`: This matches a string with digits from 0 to 9 (using \d) or a letter from 'a' to 'z'. The pattern can repeat due to the quantifier '+'.

`[a-z\.]{2,6}`: Here, the pattern should include a letter from 'a' to 'z' or a dot '.'. This section must repeat between 2 to 6 times.

### Grouping and Capturing

Capturing groups allow you to treat several characters as a single unit, and they are formed by enclosing the characters in parentheses. The regex 
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` uses parentheses for grouping. In this regex, grouping is applied to distinguish meta characters from literal characters. The specific groups in this regex are:

- `([a-z0-9_\.-]+)`
- `([\da-z\.-]+)`
- `([a-z\.]{2,6})`

### Bracket Expressions
Finally, our regex includes bracket expressions, which are expressions enclosed in square brackets.

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` 

There are three within our code:
- `[a-z0-9_\.-]`
- `[\da-z\.-]`
- `[a-z\.]`

For instance, in `[a-z0-9_\.-]`, this part of the regex will match any lowercase letters from a to z, any digits from 0 to 9, or a period.

## Author

Jackie Chheng
Github Profile: https://github.com/JackieChheng
