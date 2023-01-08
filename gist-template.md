![](images/Funk%20Coding%20Inverted%20Color.png)



**# Funky Regex Tutorial**

This is a full regex tutorial on Email Matching. I will explain functionality as well as provide examples whilst breaking down the regex piece by piece.  :wink:

## Summary

 In this tutorial I will be going over the components of a regex which matches input to a correct Email. 
 
 **<mark> (example-- /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ --) </mark>**

## Table of Contents

- [Anchors](#anchors)
- [Open and Close](#open-and-close)
- [Quantifiers](#quantifiers)
- [Character Escapes](#character-escapes)
- [Character Classes](#character-classes)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Author](#author)

## Regex Components

### Anchors

Anchors are not defined by any specific character. Their purpose is to match a position before/after characters. The up arrow or caret (^) identifies the start of the string. The dollar sign ($) anchor signifies the end of the string. For this regex matching an Email:

- The caret ^ symbol in this instance begins recognizing the start to the stringed group. **<mark>Example = ([a-z0-9_\.-]+)</mark>**

- The dollar $ symbol in this instance begins to recognize the end of the stringed group. **<mark>Example = ([a-z\.]{2,6})</mark>**

### Open and Close

Regular regex expressions will always be wrapped by two forward ( / ) slashes.

- Open: Defined as the beginning of a regex with the first forward slash to indicate the start.
- Close: Defined as the end of a regex with the second forward slash to indicate the the end of the regular expression. (None in this tutorial but this is where the start of expressions flags would occur, if any)

### Quantifiers

Quantifiers match a number of instances of a character, group, or class in a string. A quantifier can call a specific number of instances using curly brackets to search for a three digit number or a range of numbers of instances using curly brakets with two numbers with a comma in between.

**<mark> Example = \d{4} searches for a four digit number specifically. </mark>**

**<mark> Example = \d{1,6} searches for a number with anywhere from 1 to 6 digits. </mark>**

ShortHand Quantifiers Cheat Sheet

- **<mark> {1,} range of one or more. Shorthand symbol  ( + ). </mark>**
- **<mark> {0,1} range of zero or one. Shorthand symbol ( ? ). </mark>**
- **<mark> {0,} range of zero or more. Shorthand symbol ( * ). </mark>**

For this Email regex there is three quantifiers: two seperate shorthand +'s and one {2,6}.

- Here + is being used to indicate one or more instances of the previous token must match. Therefore the first two sets of brackets must appear once for the string to be in the search output.

- {2,6} indicates that the match must be between two and six characters of the previous alphabetic set.


### Character Escapes

To use a special character as a regular one in a regex, it must be prepended with a backslash **<mark> \ </mark>**. This causes the character to "escape" or lose its specific meaning. This will also allow the escapee to be searched for like any other character. If you notice in the full regex matching an email searches for four periods. A period is a class that matches any character minus line terminators.

### Character Classes

For Email matches there is only one Character Class but in some circumstances there may be more then one. CC's identify different kinds of characters and distinguish between them. One example is to seperate between letters and numbers.

- **<mark> \d - Matches any digit in Arabic numeral as well as [0-9] </mark>**

### Grouping Constructs

Grouping constructs allow you to group multiple tokens together. This creates a group to capture from for extracting a substring! This means you can include multiple character sets as customizable options for every part of your search. Groups will always be enclosed with parenthesis **<mark> ( ) </mark>**
This particular regex tutorial I am focusing on email specifically which has three groups:

- **([a-z0-9_\.-]+)**
- **([\da-z\.-]+)**
- **([a-z\.]{2,6})**

### Bracket Expressions

Brackets **<mark> [ ] </mark>** represent sets of characters that must match. The most commonly used characters to match are the **<mark> alphabet [A-Za-z] or numbers [0-9] </mark>**

Curly Brackets **<mark> { } </mark>** indicates how many times specifically the match must occur. Single characters return one option, while two or more numbers returns said amount. **<mark> Example = {4} vs {2,4,7} </mark>**. Knowing this we can look at the complete regex and at the end what do we notice? Two characters in the curly brackets which means the match must occur more than once. 

- **<mark> [a-z0-9_\.-] </mark>**  - Matches any lowercase alphebtical character input a-z. Also matches any number from 0-9, a dash, period and underscore.

- **<mark> [\da-z\.-] </mark>** - - Matches any digit, any lowercase letters, a dash and a period.

- **<mark> [a-z\.] </mark>** - Like the first set of the regex but simpler. Matches any lowercase letter and a period.

- **<mark> {2,6} </mark>** - Parameters of matching between 2 and 6 of the token.



## Author

:computer: Max Lanfear aka DaFunk is a new web developer and avid video game streamer. Nothing is more pleasing to me than completing an app and seeing that "Build Complete" :). :musical_score:

**<mark> Github = https://github.com/MLanfear </mark>**