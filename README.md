
# Match HEX Values(REGEX)

This file is intended to explain how <br> `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/` (a regular expression) works. This regex is utilized to `match a HEX value`.

## Summary

A detailed evaluation for the following regex used to match HEX values: <br>
`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/` <br>

 will be displayed in the contents table of contents. 

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
Anchor: `^` (caret: `beginning of string` or line)<br>
**Code snippet: `/^#` <br>**

Anchors assert something about the strings or the `matching` process based on the expressions/matching pattern along side them, however, they belong in the family regex tokens that don't match characters. <br> 

Example: `^yellow` indicates that the string must begin with `yellow`<br>

`^` is an anchor at the beginning of the string `must match` the character `#` (which differentiates a decimal number from a hexadecimal number) It;s great to keep in mind that `#` is optional. <br>
<br>
<space> 
Anchor: `$` (dollar: `end of string` or line) <br>
**Code snippet: `$/`** <br>

Similar to the ^ (caret), `$` is also used check if a string entirely matches a pattern at the '`end of the string`. <br>

Example: `$endGoal` indicates that the string must end with `endGoal`
<br>
<br>
In `/^`#?([a-f0-9]{6}|[a-f0-9]{3})`$/` the end of the string must match with the 3 or 6 character pattern before the $ anchor.


### Quantifiers
Quantifier: `?` <br>
**Code snippet:** `/^#?`<br>
The quantifier ? matches 0 or 1 occurrence of the pattern; it imples a boolean value (0 or 1). This quantifier typically makes the preceding character `optional`.<br>

Example: ? can distinguish between the spelling of `color` vs `colour` -- the regex would be `colou?r` indicating the `u` is optional. <br>

In `/^#?`([a-f0-9]{6}|[a-f0-9]{3})`$/` the quantifier indicates that the # (character) preceding the `?` is optional.

Quantifier: `{}` (brackets) <br>
**Code snippet:** `[a-f0-9]{6}`<br>
**Code snippet:** `[a-f0-9]{3}`<br>
The qualifier {} indicates the number of occurrences the preceding pattern matches. Quantifiers a typically greedy causing the regex to match as many occurrences of a pattern as possible, but when `?` is attached, the regex will then match as few times as possible becoming `lazy`. <br>

Example: `2{3}` means that 2 `MUST` be repeated 3 times therefore, the  matching string would be `333`

### Grouping Constructs
Anchor: `^` (caret: `beginning of string` or line)<br>
Code snippet: `/^#` <br>








### Bracket Expressions
Anchor: `^` (caret: `beginning of string` or line)<br>
Code snippet: `/^#` <br>
### Character Classes
Anchor: `^` (caret: `beginning of string` or line)<br>
Code snippet: `/^#` <br>
### The OR Operator
Anchor: `^` (caret: `beginning of string` or line)<br>
Code snippet: `/^#` <br>
### Flags
Anchor: `^` (caret: `beginning of string` or line)<br>
Code snippet: `/^#` <br>
### Character Escapes
Anchor: `^` (caret: `beginning of string` or line)<br>
Code snippet: `/^#` <br>
## Author

My name is Khiaotic. I inspire to to be more proficient in JavaScript, Express JS, CSS, HTML, and other application technologies. 
<br>Github: https://github/com/khiaotic