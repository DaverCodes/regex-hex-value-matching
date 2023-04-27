# Matching Hex Values Using Regex

## Summary

Matching a Hex value using regular expression can sound like a daunting task. In this tutorial we will break down the process to make it easier to get our heads around. 
Before we get started, the regular expression we will take on looks like this:
/^#?([a-f0-9]{6}|[a-f0-9]{3})$/
Join me and we will break down this topic into easily understood segements. 


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

The regular expression contains a grouping construct which is represented by the parentheses (). It is used to group a subpattern so that it can be treated as a single unit.
the quantifier we just talked about lives in the construct! this is how our code looks so far ({6})

### Bracket Expressions

The bracket expression "[]" is where most of the magic happens. It lives in the grouping construct and goes before the quantifier like so ([]{6}). 
here is a bracket expression '[a-f0-9]' lets tango with whats going on here. Here, a-f matches any lowercase alphabet from a to f and 0-9 matches any digit from 0 to 9.
with no repeats this is quite easy to hash out, our regex is starting to tie itself together ([a-f0-9]{6})

### Character Classes

The regular expression contains two character classes represented by \d and \w. The \d matches any digit from 0-9, and \w matches any word character which includes alphabets, digits, and underscores.

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
