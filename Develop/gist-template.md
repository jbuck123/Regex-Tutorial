# Regualr expressions!

in this project I will be explaining and giving a tutorial on a simple regular expression. In this tutorial I will be diving deep into a variety of topics including Achors, Flags, back-references and more. 

## Summary

The regular expression I will be using as an example will be the emmail validator. I will be using this example as a reference throughout the tutorial.
code snippet: (/^\w+([\.-]?\w+)*@\w+([\.-]?\w+)*(\.\w{2,3})+$/)

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
A list of compenents often found in a regular expression
- "." matches any single character. for example, boo.camp matches bootcamp, boofcamp, boorcamp ect
- " $ "  matches any string where a specific pattern occurs at the END of the string. example: ooth$ matches smooth, booth, tooth but not smooths 
- "^" matches any string where the pattern occurs at the BEGINNING of the string. example: ^red matches reds, reddit, but not unred.
- "[]" matches any single character in the range or set enclosed in the brackets. [aeiou] matches any vowel [0-9] matches any decimal digit
- "|" indicates an "OR" operator
- "()" used for grouping expressions. (desk[0-9]) matches desk23 but not just desk
- "*" matches 0 or more occurences  of the element that precedes it. Example : bed_[a-z0-9] matches bed_aaaa, bed_. bed_0123
- "+" siimilar to the one above but it matches 1 or more occurnces of the element it folows. example bed_[a-z0-9] matches bed_1, bed_a but not bed_
- "?" matches 0 or 1 occurences of the element it follows. Example: bed_[a-z0-9] matches bed_0, bed_, bed_aa
### Anchors
    (/^\w+([\.-]?\w+)*@\w+([\.-]?\w+)*(\.\w{2,3})+$/) 

    the line of code above is started with a ^ to signal a pattern occuring at the beginning of the string. 
    The line of code ends with an $ signalling a pattern occuring at teh end of the string.
### Quantifiers
Quantifiers specifiy how many instances of a character, gorup, or character class must be present in the input for a match to be found.

### OR Operator
The or operator is this: "|". Exmaple: (desk1|desk2|desk3) matches desk1, desk1 desk2, desk1 desk2 desk3. needs to be in order like that 
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
