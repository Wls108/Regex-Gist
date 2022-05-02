# Regex-Gist (Regex Tutorial)

This Tutorial will break down Regex (Regular Expression) down into more basic and easier 
to understand parts for specificly email Regex.

## Summary

Regex (short of Regular Expression) is a string that allows you to create a search pattern that finds and manages
text.

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

^ A Regular expression used for Email address.

## Table of Contents

- [Anchors](#Anchors)
- Quantifiers
- OR Operator
- Charecter Classes
- Flags
- Grouping and Capturing
- Bracket Expressions
- Greedy and Lazy Match
- Boundries
- Back-References


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

- Examples of Quantifiers :

* `*` - matches a group of charecters followed by zero or more of last character
* `+` - matches a group of charecters followed by one or more of last character
* `?` - matches a group of charecters followed by zero or one of last character
* `{}` - matches a group of characters based on the numbers placed inside of the last character
* `()` - matches a group of characters followed by zero or more copies in the parentheses

* Examples

- ENA*  matches EN followed by zero or more A
- ENA+  matches EN followed by one or more A
- ENA?  matches EN followed by zero or one A
- ENA{2} matches EN followed by 2 A
- ENA {2,} matches EN followed by 2 or more A
- ENA {2,8} matches EN followed by 2 to 8 A
- E(NA)* matches E followed by zero or more copies of NA

### OR Operator
OR Operators (Alternation Operation) matches alternation of ethier two charecters listed.

* Example of OR opt :

* `(|)` - matches to eitehr side of vertical bar
* `[]` - matches to anything without whats in the brackets

- Examples

- E(N|A) matches E with N or A
- E[NA] matches E without NA

### Character Classes
Tess regex to match only one serveral Characters such as digits,words, or whitespace

-Example of Character Classes :

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

Flags are optinal parameters to a plain expression to make searches different.

- Examples of Flags :

* `g` - Global (Searches for all occurences)
* `m` - Multi-Line (when used with anchors to with search based on line not whole string
* `i` - Insensitive, makes the search case sensetive

- Examples

- /ENA/g matches all ENA in test
- /ENA/m matches all ENA at start and end of lines
- /ENA/i matches all ENA despite case (Ena, eNA, EnA, etc)


### Grouping and Capturing
Grouping unifies a string r pattern that is matched

- Examples of Grouping :

Examples :
* `()` - parentheses creates a capture group
* `(?:)` - using `?:` disables the capturing group
* `(?<>)` - using `?<>` puts a name to the group

- Examples:

- E(NA)           parentheses create a capturing group with value NA
- E(?:NA)*        using ?: we disable the capturing group
- E(?<bar>NA)     using ?<bar> we put a name to the group

### Bracket Expressions
Are used to match and characters inside the bracket

Examples of Bracket Expressions : 
* `[]` - matches the characters in brakets
* `[]%` - matches the characters in brakets before a %
* `[^]` - matches any character not in brakets

- Examples:

[ENA]   matches any string with E or N or A        
[E-N]   similar to case above
[u-zU-Z0-9]  a string that represents a single hexadecimal digit, case insensitively
[0-9]%        a string that has a character from 0-9 before a %
[^a-zA-Z]    a string that has not a letter from a to z or from A to Z


### Greedy and Lazy Match
Greedy and lazy are quantifies that expand the match as far as possible through the text.

Examples of Greedy and/or Lazy Matching :
* `* + {}` - anyone of these could be used
 -Examples:

*<.+?>  matches any charecter one or more times of whats inside the <> and expands as needed   
*<[^<>]+>   matches any charecter one or more times of whats inside the <>   


### Boundaries
Thier are two types word and non-word and are denoted by specific charecter
 
Examples of Boundaries :
* `\b` - positions that bounds a word, or where a word starts or ends, anmd place between word and non-word
* `\B` - does the exact oppisite of the last
* `*` - will match a word to word or non-word to non-word
* Examples :
```
`ENA` has 4 total Boundaries with 3 Word Boundaries as seen below:
|E|N|A|
^ ^ ^ ^ 
N W W N  -  N = Nonword Boundary \ W = Word Boundary
\bxyz\b     matches a "whole words only search" for the string `xyz`
\Bxyz\B     matches only if the pattern is fully surrounded by word characters `txyzt` would match the string `xyz` because it only has word boundaries
```

### Back-references
When grouping it may capture and be saved for later use, Backrefrencing is the action of using these matches
 
Examples are a follows:

- ([ENA])\1              using \1 it matches the same text that was matched by the first capturing group
- ([uwx])([yz])\2\1      we can use \2 (\3, \4, etc.) to identify the same text that was matched by the second (third, fourth, etc.) capturing group
- (?<bar>[ENA])\k<bar>   we put the name bar to the group and we reference it later (\k<foo>). The result is the same of the first regex
```

## Writer
  
Wyatt Smith cuurently in coding boot camp at Pennsalvania
  
Github link below to checkout other projects
  
https://github.com/Wls108

