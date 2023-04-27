# Matching Hex Values Using Regex

Matching a Hex value using regular expression can sound like a daunting task. In this tutorial we will break down the process to make it easier to get our heads around. 
Before we get started, the regular expression we will need is as follows:
/^#?([a-f0-9]{6}|[a-f0-9]{3})$/
Join me and we will break down this topic into easily understood segements. 

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

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

Important anchors are '^' for the start of a string and '$' at the end of the string. Both are necessary to be certain that the regex matches the hex value.

### Quantifiers

as quantifiers do not apply, we will need to use '{}' and that is all we need as an indicator of the number of characters we need to match.
if there are 6 characters match, for example, we define that as follows {6}

### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
