# Regex Tutorial

In this tutorial, we will analyze a given snippet of Regex code in order to extropolate some of the guiding principles of regex. The table of contents below will help a user navigate to an explanation of the Regex component used in the given Regex code.  

## Summary

In this tutorial, we will be going through a snppet of code meant to find an email address.  Email addresses can take several forms, with letters, numbers and symbols all possibly coming before the @ symbol, then several letters, numbers or symbols could be used in the domain name immediately following the @ symbol, and finally a domain suffix that can be any combination of letters (of a limited length) following a dot (.) symbol.  The code we have for this is as follows:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

 ^                                             $

Anchors are used to open and close off the string. Used in conjunction with eachother, the ^ and $ symbol are saying that we are looking for something that starts and ends with what is specified between the two symbols. Ie. This is the beginning and end of the string we are looking for.  Find any text that begins and ends with what is between these two symbols.

### Quantifiers
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

                                         {2,6}



### OR Operator
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

### Character Classes
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

### Flags
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

### Grouping and Capturing
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

### Bracket Expressions
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

### Greedy and Lazy Match
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
