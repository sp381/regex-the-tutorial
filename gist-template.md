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

    Examples of Anchors: 
    - ^ matches the position before the first character in a string.
    - $ matches right after the last character in the string.   
    - \A matches at the start of the string 
    - \Z matches at the end of the string 
    - \b matches the created word boundry 


### Quantifiers
    Quantifiers indicate how many of a single character must be present in the input for a match to be found. 

### The following is a list of quantifiers: 

* = Match zero or more times. 
+ = Match 1 or more times.
? = Match zero or one time.
{ n } = Match an exact number amount of times.
{ n, } = Match at least a certain number amount of times. 
{ n, m } = Match from n to m times.

Here are some examples for the list of quantifiers:

### * example: 
string pattern = @"\b91*9*\b";
string input = "99 95 919 929 9119 9219 999 9919 91119";
foreach (Match match in Regex.Matches(input, pattern))
   Console.WriteLine("'{0}' found at position {1}.", match.Value, match.Index);

// The example displays the following output:
//       '99' found at position 0.
//       '919' found at position 6.
//       '9119' found at position 14.
//       '999' found at position 24.
//       '91119' found at position 33.

### + example:
string pattern = @"\ban+\w*?\b";

string input = "Autumn is a great time for an annual announcement to all antique collectors.";
foreach (Match match in Regex.Matches(input, pattern, RegexOptions.IgnoreCase))
   Console.WriteLine("'{0}' found at position {1}.", match.Value, match.Index);

// The example displays the following output:
//       'an' found at position 27.
//       'annual' found at position 30.
//       'announcement' found at position 37.
//       'antique' found at position 57.

? example: 
string pattern = @"\ban?\b";
string input = "An amiable animal with a large snount and an animated nose.";
foreach (Match match in Regex.Matches(input, pattern, RegexOptions.IgnoreCase))
   Console.WriteLine("'{0}' found at position {1}.", match.Value, match.Index);

// The example displays the following output:
//        'An' found at position 0.
//        'a' found at position 23.
//        'an' found at position 42.

### { n } example:
string pattern = @"\b\d+\,\d{3}\b";
string input = "Sales totaled 103,524 million in January, " +
                      "106,971 million in February, but only " +
                      "943 million in March.";
foreach (Match match in Regex.Matches(input, pattern))
   Console.WriteLine("'{0}' found at position {1}.", match.Value, match.Index);

//  The example displays the following output:
//        '103,524' found at position 14.
//        '106,971' found at position 45.

### { n, } example:
string pattern = @"\b\d{2,}\b\D+";
string input = "7 days, 10 weeks, 300 years";
foreach (Match match in Regex.Matches(input, pattern))
   Console.WriteLine("'{0}' found at position {1}.", match.Value, match.Index);

//  The example displays the following output:
//        '10 weeks, ' found at position 8.
//        '300 years' found at position 18.

### { n, m } example: 
string pattern = @"(00\s){2,4}";
string input = "0x00 FF 00 00 18 17 FF 00 00 00 21 00 00 00 00 00";
foreach (Match match in Regex.Matches(input, pattern))
   Console.WriteLine("'{0}' found at position {1}.", match.Value, match.Index);

//  The example displays the following output:
//        '00 00 ' found at position 8.
//        '00 00 00 ' found at position 23.
//        '00 00 00 00 ' found at position 35.

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
