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

## Regex Components

### Anchors
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

 ^                                             $

<!-- Anchors are used to open and close off the string. Used in conjunction with eachother, the ^ and $ symbol are saying that we are looking for something that starts and ends with what is specified between the two symbols. Ie. This is the beginning and end of the string we are looking for.  Find any text that begins and ends with what is between these two symbols. -->

Anchors can be used to specify where in a string we want to start.  In the case of the two we are using here, a caret (^) and a dollar sign ($), we are told to look for a string that begins and ends with what is specified in between the two symbols.

### Quantifiers
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

                                         {2,6}

Quantifiers are used to determine how many times to look for the component called before it.  The component called before in this case is the OR operator looking for any letter a-z lowercase or a dot (.).  Therefore, the quantifier will look for a string that calls those characters between 2 and 6 times. Ie, the domain suffix can only between 2 and 5 characters (characters specified in the OR operator).

### OR Operator
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

   [a-z0-9_\.-]    [\da-z\.-]     [a-z\.]

OR Operators are used to select any character that falls within a set of different character types.  In our example, we see 3 OR Operators: one for the address, one for the domain name, and one for the domain suffix.  The first says to look for any character that is either: a through z lowercase, 0 through 9, an underscore (_), a dot (.) or a dash (-). The plus sign (+) that follows is a Greedy Operator that tells us that it is looking for every instance where that occurs. Ie. looking for one or many characters that fit the constrainst specified by the OR operator.  The second OR Operator is looking for either a digit (\d),  a letter a through z lowercase, a dot (.) or a dash (-). Again, this is modified by the Greedy Operator, and therefore will look for as many occurances of these specifications as occur.  The final OR Operator looks for any letter a through z lowercase or a dot (.). This is modified by the Quantifier as discussed in the [Quantifiers](#quantifiers) section.  

### Character Classes
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

                    \d

The only character class we see comes in our second OR operator, looking for a single character that is a digit.  Character classes could also search words, whitespaces, or any character. We don't see any here, however, one could imagine that if email address didn't have a restriction on the types of character that they could hold, that we could use the dot (.) character class, and therefore select any character.

### Flags
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

/                                               /

The flags used above are meant to encapasulate the string we are looking at.  

### Grouping and Capturing
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

  (             ) (           )  (            )

The parentheses above are used to "group" sections of the string that we want to look at.  Each group contains our OR Operators and their related quantifiers.  

### Bracket Expressions
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

   [          ]    [        ]     [     ]

The bracket expressions used above are another version of the syntax for an OR Operator, discussed in detail here: [OR Operator](#or-operator). Conversely, one could also have used: (a-z|0-9|_|\.|-) for our first OR operator.  

### Greedy and Lazy Match
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

               +             +

As discussed in the section about our OR operators, [OR Operator](#or-operator), the Greedy Match operators are a way to specify that we want to look for every instance of what occurs immediately before the plus signs (+).  Ie, it runs the search for characters specified until those cases are no longer fufilled.  

## Author

My name is Anthony Geritano.  I am a 24 year old student in Columbia's Coding Bootcamp.  I currently work for the genomics company, Sema4, in their lab informatics team.  In my spare time, I play for New Haven Rugby as a prop.  I live in New Haven, where I did my undergraduate study at Yale University in Ecology and Evolution Biology and History.  My Github account is github.com/antger78
