# Matching an Email: A regex tutorial. 
Expression used:
` /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ `

This is a tutorial explaining the usage of regex to match emails. A regex is a series of characters within two slashes  
`/ characters here /`.
The expression used for this is `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`.
This is most widely used when validating email data for a specific user on a website. 

## Summary
A regular expression can be summed up as a sequence of seemingly random characters, but these characters are varying patterns
that help to match a string. Most commonly, these patterns are used to find characters within a string, replace a character within a string, or validate input. The following will go over the basics of a regular expression, and how it can be used to match an email.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

### Anchors

There are two anchors, or otherwise beginning and end points in this regular expression. The `^` notates the beginning of the string,
and the `$` sign notates the ending of the string. A multiline regex expression is notated with `(m)`, which is not used for this string, therefore the `$` sign will notate the ending of the expression completely. 

### Quantifiers

A Quantifier in regular expression's notate how many instances of a character should be present for a match to be identified.
This regex provides a `+` operator, which connects the users email data with the email client, and its domain type (.com/.net etc).
It also includes the `{2,6}` quantifier, which will allow a match range of 2-6 characters, notated by the `[a-z\.]`. 

### Character Classes

Character classes help distinguish what the character type is (example: numbers, letters etc). The character class for this expression is
`\d` which matches a single integer from 0-9. This character class is used for just one integer, so for example a "7" would match, whereas "77" would not. 

### Grouping and Capturing

Group capturing in regex is a way to capture groups as a single unit. This expression has 3 capturing groups associated. The first
is `([a-z0-9_\.-]+)` matches the users email. The second is `([\da-z\.-]+)` which matches the email client. The third is `([a-z\.]{2,6})`
which matches the email domain.

### Bracket Expressions

A bracket expression is essentially a set of characters to match. The email validation regex we are using has 3 different bracket expressions for matching and validating the input data. The character set `[a-z0-9_\.-]` is matching a-z and is case sensitive, 0-9, and the `_`, `-`, `.` (underscore, dash, and period characters). Similarly, the next bracket expression `[\da-z\.-]` matches a single character a-z and is case sensitive, an integer from 0-9, and the special characters included (`.` and `-`). Finally `[a-z\.]` matches any character a-z and is case sensitive, and the `.` character. 

### Greedy and Lazy Match

The regular expression used for matching an email uses only greedy match. A greedy match essentially means to match the longest possible string, while a lazy would mean to match the shortest possible string. These are written as quantifiers like `+`, `*`, `?`, `{}` and so on. The `+` quantifier after the first set of brackets means it will match as many times as possible. The `{2,6}` at the end of the expression is a quantifier, allowing a match between 2-6 characters for the final group (the domain for the email).

## Author

I am a full stack web developer from St. Louis, MO.
Github Repository Link: https://github.com/Hmndtyphn
