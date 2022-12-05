# Matching An Email Regex Tutorial

A Regex, or regular expression, is a string of text that helps search for, validate, find, or format text input by searching within the text for matching criteria. These are often used within multiple programming languages and can be used within search engines.

## Summary

Matching an Email in Regex: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

To simplfy the above expression, this Regex is seaching for a character group of any number of characters, followed by the '@' symbol, then another character group set, followed by a ".", then finally ending with a third character group between 2 and 6 characters total. The following guide has been created to help budding developers understand each section of code, what it does, and how it is implemented. 

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components



### Anchors
Anchors are special characters that are used to specify the beginning and/or end of the searchable text.   
For matching an email Regex, you'll notice the anchors `^` and `$`.  
The `^` is used to match the beginning of the text while `$` is used to match the ending of the text.  
Everything within the `^` and `$` is searched for matching criteria.  




### Quantifiers
Quantifiers are used to match the number of instances a character or group in a string of text.   
`*` is used to match 0 or more times within the string  
`+` is used to match 1 or more times within the string  
`?` is used to match only 0 or 1 time within the string  
`{}` are used to match within a set limit  
Placing a number alone within `{}` will match exactly that number of times within the string  
A number followed by a comma within `{}` will match AT LEAST that number of times within the string  
Two numbers separated by a comma within `{}` will match AT LEAST the first number of times and AT MOST the second number 


As you can see in the Regex there are two quantifiers: `+` and `{2,6}`  
The `+` will match will match an email with 1 or more of the characters or sequence listed immediately before it  
`{2,6}` will match an email that has a minimum of 2 but no more than 6 of the previous listed characters or sequence at the end of the address    




### Character Classes
Character classes are used to match any character or symbol from a certain set of characters  
`\d` is used to match any digits between 0-9
`\s` is used to match a space or tab  
`\w` is used to match a word including lowercase and capital letters, numbers, and underscores  


Within the matching an email Regex, we can see `\d` being used after the `@` symbol to signify any digit found here would match  




### Grouping and Capturing
Grouping is done using `()` to group certain parts of the string together for independent matching  
In the email Regex there are 3 groups:  
`([a-z0-9_\.-]+)`  
`([\da-z\.-]+)`  
`([a-z\.]{2,6})`  
Each group has their own quantifiers, bracket expressions, and character classes to match within the email string as a whole  




### Bracket Expressions
Brackets are used to indicate a strict set of characters to match. Typically these will be done using a range of digits `[0-9]`, letters `[a-z]`, or both `[a-z0-9]`  They may also include special characters `[a-z0-9_\.-]`. This will match any letters, numbers, underscore, period, or hyphen.  


### Greedy and Lazy Match
All quantifiers listed within this Regex are greedy. This means that it will search for a match the maximum number of times specified. See [Quantifiers](#quantifiers) for match criteria.  




## Author

My name is Davey Douglas. I'm currenly enrolled as a student at UT Austin's Full Stack Developer Bootcamp. To check out my other projects on GitHub, click [here](https://github.com/ddouglas86) 
