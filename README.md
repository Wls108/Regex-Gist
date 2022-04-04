# Regex-Gist (Regex Tutorial)

This Tutorial will break down Regex (Regular Expression) down into more basic and easier 
to understand parts for specificly email Regex.

## Summary

Regex (short of Regular Expression) is a string that allows you to create a search pattern that finds and manages
text.

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

^ A Regular expression used for Email address.

## Table of Contents

- Anchors
- Quantifiers
- OR Operator
- Charecter Classes
- Flags
- Grouping and Capturing
- Bracket Expressions
- Greedy and Lazy Match
- Boundries
- Back-References
- Look-ahead snf look behind

## Regex Parts

### Anchors
Anchors are characters in regular expression that match strings that start, end, or both cerrtain chrecters.

Examples of Anchors :

* `^` - matches any string with start
* `$` - matches any string with end

- Examples:

- ^Example : Matches any string starting with Example
- Example$ : Matches any string ending with Example
- ^Example$ : Matches only the word Example

### Quantifiers
Qunatifiers are charecters that specify how many instances a group or charecter class must be in the input to match.

- Example

* `*` - matches a group of charecters followed by zero or more of last character
* `+` - matches a group of charecters followed by one or more of last character
* `?` - matches a group of charecters followed by zero or one of last character
* `{}` - matches a group of characters based on the numbers placed inside of the last character
* `()` - matches a group of characters followed by zero or more copies in the parentheses

* Example

- ENA*  matches EN followed by zero or more A
- ENA+  matches EN followed by one or more A
- ENA?  matches EN followed by zero or one A
- ENA{2} matches EN followed by 2 A
- ENA {2,} matches EN followed by 2 or more A
- ENA {2,8} matches EN followed by 2 to 8 A
- E(NA)* matches E followed by zero or more copies of NA

### OR Operator
OR Operators (Alternation Operation) matches alternation of ethier two charecters listed.

* Example

* `(|)` - matches to eitehr side of vertical bar
* `[]` - matches to anything without whats in the brackets

- Example

- E(N|A) matches E with N or A
- E[NA] matches E without NA

### Character Classes
Tess regex to match only one serveral Characters such as digits,words, or whitespace

-Example 

* `\d` - matches a single digit
* `\w`- matches a word with or without underscore
* `\s` - matches any whitespace including tabs and line breaks
* `.` - matches any
* Capital versions do the oppisite

- Example

- \d matches single digit 0-9
- \w matches a single charecter that is a-z
- \s matches ` `
- . matches any charecter
- \D matchess a single non-digit
- \W matches a single non a-z charecter
- \S matches any non ` ` 

### Flags
