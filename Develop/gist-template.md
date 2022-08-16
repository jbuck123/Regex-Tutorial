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

(/^\w+([\.-]?\w+)*@\w+([\.-]?\w+)*(\.\w{2,3})+$/) 
  
         in the exmaple: \w{2,3}  it is looking of the character w 2 - 3 times 
         this is looking for .com .co or something
  
### OR Operator
The or operator is this: "|". Exmaple: (desk1|desk2|desk3) matches desk1, desk1 desk2, desk1 desk2 desk3. needs to be in order like that 
### Character Classes

throught out the email validator you can see \w which is looking for a pattern of letters

Character classes:
- \d is the character class for digits
- \s is the character class for spaces 
- \w is the character class for words which is actually just letters
- \t is the character class for tab 
- \n is the character class for new line 
### Flags
regular expressions may have flags that affect the search 
- "i" this flag means the search is case-insensitive
- "g" looks for all matches, without it - only the first match is returned
- "m" multiline mode
- "s" enables dotall, which allows a dot to match newline character
- "u" enables full Unicode support.
- "y" sticky mode: searchign at the exact position in the text

### Grouping and Capturing
example of email validation:   (/^\w+([\.-]?\w+)*@\w+([\.-]?\w+)*(\.\w{2,3})+$/) 
in the begining of the expression you can see the w+... this means w which is a class of letters repeated 1 or more times.
at this point the Email Regex is starting to make sense,.. with our knowledges on classes, quantifiers, anchors and now grouping
we can start to read what is happening in the code above.
### Bracket Expressions
Bracekts indicate a set of characters to match. 
[] any individual character between the brackers will match 

example of email validation:   (/^\w+([\.-]?\w+)*@\w+([\.-]?\w+)*(\.\w{2,3})+$/) 

looking at: [\.-] in the begining is meant to match the username before the @ symbol.
it begins with at least one word character, followed by more word characters or "." or "-". cannot contain ".." "--" ".-" or "-."


### Greedy and Lazy Match
Greedy search: for ever position in the string - try to match the pattern at that position. if theres no match, go to the next position.

lazy search: the opposite to the greed mode meaning repeat minimal number of times. Lazy search is enable by putting a question mark after the quantifier.


### Boundaries
boundaries are like anchors in a way that it sets "boundaries" for the pattern search. 
for example: /b\d\d\d\d/b matches a 4-digit number. so with the example of MN 2022 b\d\d\d\d/b outputs 2022 because its only looking for numbers

### Back-references
Back refrences is getting into advanced but in simple english back refrencing is used to look for repeated text. A backrefrence in a regular expression identifies a previously matched group and looks for exactly the same text again. 

### Look-ahead and Look-behind

## Author

Solo assignment by James Buchmann 
Github : https://github.com/jbuck123
