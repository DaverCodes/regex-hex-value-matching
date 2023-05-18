# Matching Hex Values Using Regex

## Introduction

Hello and welcome to this tutorial on matching Hex values using regular expressions! In this tutorial, we will explore the regex pattern and deconstruct its components to understand how it works. By the end, you'll have a solid understanding of how to match Hex values with regex.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)
- [Examples](#examples)
- [Author](#author)

## Regex Components

### Anchors

Anchors are essential in regex, and we use the `^` symbol at the start and `$` symbol at the end of the string to ensure a complete match for the Hex value.

### Quantifiers

For our Hex value pattern, we use the `{}` quantifier to specify the number of characters we need to match. For example, `{6}` indicates a six-character Hex value.

### Grouping Constructs

The grouping construct in regex is denoted by parentheses `()`. It allows us to treat a subpattern as a single unit. In our case, the quantifier lives within the grouping construct, like this: `({6})`.

### Bracket Expressions

The bracket expression `[]` is where the magic happens. Placed within the grouping construct and before the quantifier, it allows us to define the valid characters for the Hex value. For instance, `[a-f0-9]` matches lowercase alphabets from 'a' to 'f' and digits from '0' to '9'.

### Character Classes

Our regex pattern includes two character classes: `\d` and `\w`. The `\d` matches any digit from '0' to '9', and `\w` matches any word character, including alphabets, digits, and underscores.

### The OR Operator

The OR operator is represented by the pipe character `|`. In our regex, it allows us to match Hex values that are either six characters or three characters in length. This is expressed as `([a-f0-9]{6}|[a-f0-9]{3})`.

### Flags

Flags in regex modify the matching behavior. However, for our Hex value pattern, we don't require any flags.

### Character Escapes

Character escapes are used to match special characters in regex. They are denoted by a backslash `\` followed by the character to match. In our regex, we use two character escapes:

- `#` matches the "#" character
- `\d` matches any digit from '0' to '9'

These character escapes are used to match the optional "#" character at the beginning of the Hex value and the digits within the Hex value.

## Examples

Let's take a look at some examples to understand how the regex pattern works:

```javascript
const hexPattern = /^#?([a-f0-9]{6}|[a-f0-9]{3})$/;

console.log(hexPattern.test("#3a7b42"));  // true
console.log(hexPattern.test("#abc"));     // true
console.log(hexPattern.test("a2c"));      // true
console.log(hexPattern.test("#12345"));   // false (invalid length)
console.log(hexPattern.test("#xyz"));     // false (invalid characters)
```

## Author

This tutorial was created by David Simpson. You can find more of my work on [GitHub](https://github.com/DaverCodes) and reach me via email at DaverCodes@gmail.com.

