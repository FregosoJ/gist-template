Regex Reader 

This tutorial explains how to use regular expressions (regex) to validate email addresses using the pattern /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/. This method is useful in applications/technologies like Node (Inquirer) and MongoDB.

## Summary

A regular expression, or regex, is a set of characters defining a search pattern. It is often utilized for searching for patterns in strings, replacing characters, and validating input. This tutorial will cover the basics of regex and its use in matching email addresses.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors
In this regex expression for email matching, the anchors used are ^ and $. The ^ signifies the start of the string, while $ denotes the end of the string. The m or multiline option is not activated, so the regex will conclude at $.
### Quantifiers
Quantifiers in this regex includes the + operator, which will connect the users email name + email service + .com. Another quantifier for this regex includes {2,6}, which will allow a match range of 2-6 characters for the character set of [a-z\.].
### Grouping Constructs
In this expression, the first capturing group is ([a-z0-9_\.-]+) which matches the email username. The second capturing group, ([\da-z\.-]+), matches the email service provider. Lastly, the third capturing group, ([a-z\.]{2,6}), captures the domain extension such as .com.
### Bracket Expressions
The bracket expressions used for email validation in this expression are:

[a-z0-9_\.-]: This matches any letter a-z (case sensitive), digits 0-9, "_", "-", and ".".
[\da-z\.-]: This matches a single digit from 0-9, any letter a-z (case sensitive), and the characters "." and "-".
[a-z\.]: This matches any letter a-z (case sensitive) and the character ".".
### Character Classes
Character classes are a set of defined characters in a regex. In this instance \d is used, which causes this regex to match with single digit characters such as 0-9.

### Greedy and Lazy Match
This is a greedy regex, typical of most regex, indicated by the two + characters at the end of the first two subexpressions ([a-z0-9_.-]+) and ([\da-z.-]+). This means that the regex will match all the string patterns that satisfy the criteria defined in the bracket expressions [].

The quantifier {2,6} further sets the parameters for matching, in this case requiring a match to be 2 to 6 characters long.

## Author
Jonathan Fregoso has been working on achieving 1 of his goals of becoming a software engineer/coder and is attempting to achieve this by enrolling in the UCLA Extension Coding Bootcamp to further his knowledge and create a different and better career path. 
