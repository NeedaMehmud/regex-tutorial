# Regex Tutorial

Welcome to Regex Tutorial! What is Regex? Let's hop on to the summary section below to get to know it more.

## Summary

Regex stands for a regular expression. It is a special text string for describing a search pattern. You can think of regular expressions as wildcards on steroids. You are probably familiar with wildcard notations such as `*.txt` to find all text files in a file manager. The regex equivalent is 
`^.*\.txt$.`

 Cool, right? 🤯

In this tutorial we will be using the most common regular expression: an e-mail address.
How can we write a regular expression of mehmudneed@gmail.com? Let's break this down line by line.

My e-mail address can be broken down into groups below:

- String of characters 
- And/or dots
- And/or underscores
- And/or digits 
- Hyphens 
- The at sign (@)
- The domain name that can be a string of characters and/or digits
- The extension preceeded by a dot (.)

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

# Regex Components

## Anchors
Anchors do not match any character at all. Instead, they match a position before, after, or between characters. They can be used to “anchor” the regex match at a certain position. The caret `^` matches the position before the first character in the string. Applying `^a` to abc matches `a`. `^b` does not match `abc` at all, because the `b` cannot be matched right after the start of the string, matched by `^`. See below for the inside view of the regex engine. Similarly, $ matches right after the last character in the string. c$ matches c in abc, while a$ does not match at all.

| Symbol      | Description | Example | E-mail regex example
| ----------- | ----------- |-----------|-----------|
| `^`          | Starts with the following character(s), usually placed at the beginning of the regex       |`^a` means starts with `a` | `^([a-z0-9_\.-]+)` means starts with `([a-z0-9_\.-]+)`
| `$`          | Ends with the preceeding character(s), usually placed at the end of the regex        |`b$` means ends with `b` | `([a-z\.]{2,6})$` means ends with `([a-z\.]{2,6})`


## Quantifiers

### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
