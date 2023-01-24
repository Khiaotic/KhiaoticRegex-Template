
# Match HEX Values (REGEX)

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

Example: `2{3}` means that 2 `MUST` be repeated 3 times therefore, the  matching string would be `333`<br>

In /^#?(`[a-f0-9]{6}`|`[a-f0-9]{3}`)$/ , the {6} indicates that [a-f0-9] will have 6 instances. This will allow 6 characters in the string to contain `lower case` characters between `a-f` and/or integer between 0-9. The same logic will be applied to the preceding bracket {3}
expression.<br>

### Grouping Constructs
Grouping Construct: `()` (parenthesis: `capturing group`)<br>
Code snippet: `([a-f0-9]{6}|[a-f0-9]{3})` <br>

The () groups the regex inside. Multiple characters will be conduct itself as a `single unit`. The group of data will be in the form of an array, with the an index allows `values to be accessed on the result of the match`.<br>

Example: `(code)`{5} matched `codecodecodecodecode`. Code needs to repeat 5 times  indicated by {5} (quantifier)<br>

In `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`  <br> the grouped expression is `([a-f0-9]{6}|[a-f0-9]{3})` is grouped as a single unit with the end string anchor $
<br>


### Bracket Expressions
Anchor: `[]` (bracket)<br>
Code snippet: `[a-f0-9]` <br>
Bracket expression is a regex that will match a pattern of characters (`integers, alphabetic, symbols, special characters, etc`) inside the []. <br>

Example: `[d-q0-7]` indicates that the string `MUST` include a  character that is between `d-q or 0-7`<br>

In /^#?(`[`a-f0-9`]`{6}|`[`a-f0-9`]`{3})$/ the expression indicates matching a string that has a `lower case`  character between `a-f` and/or integer between `0-9`


### Character Classes
Code snippet: `a-f0-9` <br>
Character classes match one out of the multiple characters `defined in the character set`. <br> `-`(hyphens) are used inside a character class to determine a range of characters. Multiple ranges can be used<br>

Example: `[3-9]` matches a single integer between 3 and 9

In `/^`#?([a-f0-9]{6}|[a-f0-9]{3})`$/`, [a-f0-9] is a character class with the range between `lower case` a-f and integer 0-9.

### The OR Operator
OR Operator: `|` (vertical pipe: `alternation/OR operand` )<br>
Code snippet: `[a-f0-9]{6}|[a-f0-9]{3}` <br>
The | OR indicator is a boolean that matches the expression before or after.<br>

Example: `22|33` means either 22 `or` 33 `or` both integers are allowed in the string. `33` is an acceptable sample match<br>

In /^#?([a-f0-9]{6}`|`[a-f0-9]{3})$/ the OR operator implies a matching string has to have 3 `OR` 6 characters defined in the character set  with  the specified pattern. `[a-f0-9]{3}` suggest match 3 character string with a character a-f/or integer0-9 (same logic applied to `[a-f0-9]{6}`).<br>


### Flags
N/A <br>

### Character Escapes
N/A<br>

## Author

My name is Khiaotic. I inspire to to be more proficient in JavaScript, Express JS, CSS, HTML, and other application technologies. 
<br>Github: https://github/com/khiaotic