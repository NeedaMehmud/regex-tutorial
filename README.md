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
- And/or dots (`.`)
- And/or underscores (`_`)
- And/or digits 
- Hyphens (`-`)
- The `@` sign 
- The domain name that can be a string of characters and/or digits
- The extension preceeded by a dot (`.`)

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

## ⚓ Anchors
Anchors do not match any character at all. Instead, they match a position before, after, or between characters. They can be used to “anchor” the regex match at a certain position. The caret `^` matches the position before the first character in the string. Applying `^a` to abc matches `a`. `^b` does not match `abc` at all, because the `b` cannot be matched right after the start of the string, matched by `^`. Similarly, `$ `matches right after the last character in the string. `c$` matches `c` in abc, while a `$` does not match at all.

| Symbol      | Description | Example | E-mail regex example
| ----------- | ----------- |-----------|-----------|
| `^`          | By default, the match must occur at the beginning of the string; in multiline mode, it must occur at the beginning of the line.       |`^a` means starts with `a` | `^([a-z0-9_\.-]+)` means starts with `([a-z0-9_\.-]+)`
| `$`          | By default, the match must occur at the end of the string or before \n at the end of the string; in multiline mode, it must occur at the end of the line or before \n at the end of the line        |`b$` means ends with `b` | `([a-z\.]{2,6})$` means ends with `([a-z\.]{2,6})`

## ❓ Quantifiers
Quantifiers specify how many instances of a character, group, or character class must be present in the input for a match to be found. The quantifier `?` makes the preceding token optional. In other words, it repeats the token between zero or one times. If the `*`, `+`, `?`, `{`, and `}` characters are encountered in a regular expression pattern, the regular expression engine interprets them as quantifiers or part of quantifier constructs unless they are included in a character class. To interpret these as literal characters outside a character class, you must escape them by preceding them with a backslash. For example, the string `\*` in a regular expression pattern is interpreted as a literal asterisk `("*")` character.

| Symbol      | Description | Example   |E-mail regex example|
| ----------- | ----------- |-----------|-----------|
|`+`| Matches a string that has the anterior followed by one or more of the last character| `ne+` will match any set of characters that contains the string "`ne`" with at least one occurence of "`n`" and more, for example : "`nee`d", "`need`le" or "`ne`t". In the last 3 examples, "`nee`", "`nee`" and "`ne`" will be the corresponding matchings. | `[a-z0-9_\.-]+` means any characters of `[a-z0-9_\.-]` and more will be a matching record
|`\d`| Matches a single digit, is equivalent to `[0-9]`|`[\d]` in the zipcode `90210`, there will be 5 matching records|`[\da-z\.-]` would be equivalent to `[0-5a-z\.-]` meaning will find all the digits between 0 and 5, as well as any letter between `a` and `z`, dots `.` and hypens `-` . Example: needa `-`mehmud @gmail.com
|`{}`| Matches a string that has the anterior followed by how ever many the number in the brackets of the last character in the string | Here we can use  `max and min` within the curly brackets. That would simply mean that  preceding characters is matched at least "min" times and "max" times and would look something like this `{min,max}`| `\.([a-z\.]{2,6})$` means at least 2 occurences of a string `[a-z\.]` and no more than 6. Example: mehmudneeda@gmail`.com` and mehmudneeda@`us.gov`




### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
