# Regex the Tutorial

This tutorial will is about Regular Expression, or Regex. Regex is a sequence of characters that defines a search pattern, and it is very useful in extracting information from any text.  This tutorial will help you understand the different characters that make up an expression and how to use a Regex to find certain patterns within a text.  

## Summary

The sequence of characters I will use in this tutorial are as follows,  /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ 

This regex is for locating and matching an email. Please use the Table of Contents to follow the path I took to create this particular sequence. 




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
    Anchors match a position before, after, or between characters.

    Some examples of Anchors: 
    - Use ^ to locate the position before the first character in a string.
    - Use $ to locate right after the last character in the string.   
    - Use \A to locate the start of the string 
    - Use \Z to locate the end of the string 
    - Use \b to match the created word boundry 

    

### Quantifiers
    Quantifiers indicate how many of a single character must be present for a match to be found. 

    A list of quantifiers: 

    * = Match zero or more times. 
    + = Match 1 or more times.
    ? = Match zero or one time.
    { n } = Match an exact number amount of times.
    { n, } = Match at least a certain number amount of times. 
    { n, m } = Match the minimum and maximum amount of a certain number. 


### OR Operator
    The syntax for the OR Operator is ||

    It is a Boolean operator that will return a true value if the operands is true. If the operand is false then it will return a false value. 

### Character Classes
    Character classes are used to distinguish between different types of characters. 

    Here are just a few examples of Character Classes: 
    /d matches any digit
    /D matches any character other than a digit
    /s matches a white space character, including unicode spaces
    /S matches a single character other than white space
    /w matches uppercase A-Z, lowercase a-z, numbers 0-9
    . matches any character  

### Flags

    Flags allow for global searching and case-insensitive searching. 
    They are an integral part of regex and they cannot be removed or added later. 


### Grouping and Capturing

    Grouping and Capturing is a way of matching multiple characters as a single unit. This is done by putting the regex inside a set of parentheses. 
 
    The grouping from the sequence on line 7 is ([a-z0-9_\.-]+) and ([\da-z\.-]+) and ([a-z\.]{2,6})
    

### Bracket Expressions

    Bracket Expressions matches any character within square brackets. That could be a single character or a collating element. 

    Example using line 7's sequence:
        [a-z0-9_\.-] , [\da-z\.-] , ([a-z\.]

### Greedy and Lazy Match

    A greedy match will try and locate as many characters as possible in the pattern. That could match the longest string possible.  
    On the other hand, a lazy match will locate the shortest string. It will repeat as minimal times as possible. 

### Boundaries

    The metacharacter for boundaries is \b. It can match the first character in a string, if it is a word character. It can match the last character in a string if it is a word character. Basically, you are able to locate and match whole words. 

### Back-references

    Back references are regex commands that are locating a previous part of the matched regex. They are specifed using a backslash and a single digit. 
    Example: \2

### Look-ahead and Look-behind

    Look-ahead and Look-behind are regex used to match a pattern that is followed or preceded by another pattern. 

    The syntax for Look-ahead is X(?=Y) and it's saying to locate "X", but only if it's followed by Y. 

    The syntax for Look-behind is (?<=Y)X and it's saying to locate "X", but only is there is Y before it. 

## Author

    Hi! My name is Sarah and I am a Fullstack Developer. I love the way coding allows the whole brain to be used through artistic design and critical thinking and problem solving. There has not been a dull moment yet and I look forward to new challenges that will help me grow as a developer. 

    Follow me on GitHub https://github.com/sp381 ❤️