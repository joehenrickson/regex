Regex Tutorial - Email Search

Introductory paragraph (replace this with your text)

## Summary

This Regular Expression or RegEx will be defining a search pattern to look for different expressions of an email address within a document. The RegEx code that will be discussed is as follows:

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

## Regex Components

There are 3 components in the RegEx that will be discussed in the tutorial.

1. Username = beginning of the email prior to the "@" symbol.
2. Domain Name = string represented after the "@" symbol and before the ".".
3. Suffix = After the "." such as .com, .au, or .home, etc.

### Anchors

Our first snip of code after the forward slash is the ^ symbol and is the anchor. This anchor defines where the search parameter starts. In the case of this example, the search parameter is either a letter, a-z or a number 0-9 and/or a symbol as follows: /^([a-z0-9_\.-] Inside the brackets are the search parameters.

The end of our code has the closing anchor $.  The code before the $ is looking for anything that ends with those parameters.  In this ([a-z\.]{2,6})$/ anthing that ends with a-z, a backslash or period and is a minimum of 2 characters but up to 6.

### Quantifiers

The quantifiers used in this RegEx are the {} symbols. In this case, the {2,6} is telling us that there shold be a minimum of 2 characters and up to 6 characters of the previously selected values as explained above.

### OR Operator

There are no OR operators in this regex.

### Character Classes

There are no character classes either, although the "." is normally a character class, because it is followed by "\" it is telling the "." to be taken literally. Without the "\" a period would be a class definer that would mean it could match any character.

### Flags

Flags are at the beginning and the end of each search parameter and are forward slashes. The anchors would be in between each forward slash if needed.

### Grouping and Capturing

Using parenthesis we can group expressions together as you can see in the example. "a-z" as well as "0-9" and symbols are all grouped in a square bracket together and outside the square bracket, still in parenthesis you have a "+" sign. This plus sign is part of the group that tells the search query to look for one or more instances of the previous characters. In this case, the previous characters are a-z. 0-9 and underscore, dash or period.

### Bracket Expressions

Process of combining multiple character classes together. [A-Za-z0-9] would be a bracket expression.

### Greedy and Lazy Match

There are no lazy matches in this portion of RegEx, however, the "+" operator is a greedy operator. This means that the search parameters can be anything from the selected group until it returns a value that is not in the group. Then it will check the group 2 parameters. If the perameters just simply checked for anything before an "@" symbol and there were more than one, the search would continue through the first symbol and also give you everything before the second. Adding a lazy match with a ? would stop when it reached the first symbol.

### Boundaries

Boundaries are for putting boundaries on words. If you wanted to do a search of a class list and wanted to find everyone with the first name John but didn't want to also retrieve everyone with the last name Johnson, you could add the \b boundary tag like, \bJohn\b

## Author

Joe Henrickson - Github: https://github.com/joehenrickson
Email address: joehenrickson@gmail.com
