# Regular Expression Tutorial

Regular expressions (regex) are tools for matching pattern in string and they are useful for vaildating user input. My tutorial will break down a regex designed for vaildation email addresses explaining each component to help you understand how it functions.

## Summary

^([a-z0-9._%+-]+)@([a-z0-9.-]+)\.([a-z]{2,6})$

The above regex checks for a valid email format. The email format should contain a local part, an @ symbol, domain name and a Top Level Domain (TLD). 

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors

*   Anchors are used to assert the position in the string where the match must occur.

*   Caret  ^ : Asserts the start of the string.

*   Example: In ^([a-z0-9._%+-]+), it ensures that the matching begins at the start of the email.

*   Dollar Sign  $ : Asserts the end of the string.

*   Example: In ([a-z]{2,6})$, it ensures that the match ends with a valid Top Level Domain (TLD).

### Quantifiers

*   Quantifiers specify how many times a character or group must occur for a match.

*   Plus  + : Indicates that the preceding element must occur one or more times.

*   Example: ([a-z0-9._%+-]+) ensures that the local part must contain at least one valid character.

*   Curly Braces  {} : Specify a range for occurrences.

*   Example: ([a-z]{2,6}) ensures the TLD is between 2 and 6 characters long.

### Grouping Constructs

*   Grouping constructs allow you to group parts of the regex for applying quantifiers or capturing matched text.

*   Parentheses  () : Create a group for capturing or applying quantifiers.

*   Example: ([a-z0-9._%+-]+) groups all characters valid for the local part

### Bracket Expressions

*   Bracket expressions define a set of characters that can match at a specific position.

*   Square Brackets  [] : Match any single character within the brackets.

*   Example: [a-z0-9._%+-] matches any character that is a lowercase letter, digit, or special character.

### Character Classes

*   Character classes are shorthand notations for common sets of characters.

    Predefined Classes:
    \d: Matches any digit (equivalent to [0-9]).
    \w: Matches any word character (equivalent to [a-zA-Z0-9_]).
    \s: Matches any whitespace character.

*   In our regex, \d is used in the domain part ([a-z0-9.-]+) to include digits.

### The OR Operator

*   The OR operator is represented by the pipe symbol | . It allows you to specify alternatives or options, meaning the pattern can match either of the options separated by the | .

*   Example: cat|dog will match either "cat" or "dog" or (red|blue) car will match either "red car" or "blue car".

*   The | works within parentheses to group alternatives and can be used at any level in the regex pattern to specify different matching possibilities.

### Flags

*   Flags modify the behavior of the regex engine.

*   Case Insensitivity: The  i  flag can be used to ignore case differences.

*   Example: /^([a-z0-9._%+-]+)@([a-z0-9.-]+)\.([a-z]{2,6})$/i 

*   The  i  makes the regex case insensitive, allowing uppercase letters.

### Character Escapes

*   Character escapes are used to match special characters that have a specific meaning in regex.

*   Backslash \ = Escapes special characters.

*   In regex, the dot . must be escaped when used to match a literal dot. In the domain part, it is used as \., indicating that we want to match an actual dot rather than any character.

## Author

My name Is Caliph Ferguson, a junior web developer student passionate about coding and gaining and sharing knowledge.
(https://github.com/Cue4)
