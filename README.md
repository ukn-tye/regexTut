# regexTut
This is my module 17 assignment and in this assignment it is my job to show you how to use a ``regex function``. The expression I will be showing you how to use today will be an Email matching regex function. Here is what it looks like..
```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```
It might look confusing and hard now but by the end of this tutourial you'll be a regex Pro. I will go through each component of this expressing and touch on what they look like, mean, and do.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Boundaries](#boundaries)

## Regex Components

### Anchors
the anchors match a position a character is in. for ex.
- The ``^`` in this bit of code matches the begginning of the text
- The ``$`` would be mathcing the ending of the text
```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```
There's one thing you know about this expression now, so lets move on to our `Quantifiers` .
##

### Quantifiers
Quantifiers are exactly what you probably think it is.... NUMBERS! A quantifier sets the amount of characters you would like to match. It's a number inside curly brackets just like this `/\d{n}/` . This example it would be matching a 4 digit code. The `\d` stands for "digits" so it knows to look for numbers instead of text. In our expression we have acouple of different Quantifiers.

```
{2,6}
```
This is a range quantifier, and it gives you the ability to match more than one specific digit. This example we have in our code snippet is stating that it will match any number that is `2` to `6` digits long. There is also a `Quantifier Shorthand` in this expression and it would be the `+` . This can be placed at the end of an expression or character class to allow more than one return value. For example...
```
let phone = "+1-(408)-555-0105";
let result = phone.match(/\d+/g);

console.log(result);
```
This would retun...
```
["1", "408", "555", "0105"]
```
Giving you 4 different numbers of any amount because there is no set number or range just the `\d` .
in our 

### Character Classes
A character class. Matches any one of the enclosed characters. You can specify a range of characters by using a hyphen, but if the hyphen appears as the first or last character enclosed in the square brackets, it is taken as a literal hyphen to be included in the character class as a normal character. Here's what it looks like in our expression...
```
'[a-z0-9_\.-]' '[\da-z\.-]' '[a-z\.]'
```
We have 3 different character classes. The first one `[a-z0-9_\.-]` is stating that it will match any letter from `a` through `z`, any number from 0 to 9, and all 4 of the special characters that are displayed after the 9. The second is stating that it will match any digit because of the `\d` in front of the `a-z` and will also match any character from a through z, and all the displayed special characters. I think you can do the last one on your own with your knowledge.

### Boundaries
The `()` in this expression are our boundaries an din between them we have a `@`, `\.` which is a dot. This makes the format of an Email.
```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

## Author
Thanks for coding with me! I hope you were able to learn something new. My name is Luacs Polk, and I have many different helpful Repositiries.
- Github: https://github.com/ukn-tye
- Email: Lucas.polk04@gmail.com
Heres some of my resources to reach me
