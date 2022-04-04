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

- ^Example  Matches any string starting with Example
- Example$  Matches any string ending with Example
- ^Example$ Matches only the word Example

### Quantifiers
