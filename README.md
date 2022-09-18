# Regex Tutorial: Matching a Email

The meaning of regex, or really it's regular expression, is a sequence of characters used to match patterns in a text. These expressions are very useful for extracting the data from things like emails, phone numbers and countless other things, and it follows a specific pattern from text. It's used in all of programming.

## Summary

This tutorial wil explain the regex for matching a email  /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ in a way you will better understand, and how versatile it can be.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Author](#author)

## Regex Components

### Anchors
Anchors match a position before, after or between characters. The caret, ^ matches the position before the first character in the string, and thedollar symbol, $ basically contain the parameters of the regex.
### Quantifiers
Qauntifiers specify how many instances if a character, group, or character class must be present for a match to be found. So, for a regex that is meant to match an email adress, you'd want to use the plus sign, + , operator. The + on its own is known as a greedy operator, as it will match as many occurances as possible. In [a-z0-9_\.-]+@ from our email matching regex, the expression will look for at least one or more instances of everything in the brackets "lowercase a through z" and of "zero through nine" a period and a dash. After the + is the @ so it will stop this part of the search once it gers to the @.
Finally, the {2,6} at the end will look for a range of 2-6 characters. For a email address that works because they end in something like .com or .net which is 2 and 6 characters long.
### Character Classes
The \d used in the email matching regex is looking for any single digit. Since it is wrapped in brackets followed by the + sign, it can be one or more digits If it was just on its own it would only allow a single digit, or something like \d\d\d that would mean only three digits.
### Flags
The / is used to de-limit the expression, and will come before the caret and after the dollar sign. After the closing /g = global search, i = case sensitive search, m= multi-line search, are come flags that may be used.
### Grouping and Capturing
Paraenthases are used to group parts of the expression together. In /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ the username is grouped, then its provider name is grouped,and between them is a @ symbol so that nothing may be affecting these groups affect the @ symbol and the regex will just look for a single @ symbiol between those two groups.
### Bracket Expressions
Using Brackets allows a regex to match speficic characters in a range. So, [a-z] is not looking for a or -, and z. Acutally it's looking for any letters "a" through "z". Also, in the brackets the dash is not taken litterally in the case of a-z or 0-9. After, the / to escape the period it is recognized as a literal "-".
### Greedy and Lazy Match
A greedy match will match as much as possible while the lazy match will try to match as little as possible. In the matches in a email regex are greedy and will match as much as possible.
## Author

I'm Nic Verdi, a aspiring web developer.
https://github.com/Verdster98