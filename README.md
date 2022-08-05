# Regex_tutorial

Regex is the simplified version Regular expression. Regex is best known as a series of characters that identfies a sequenced pattern. They have used these characters in email addresses by using these  characters:

/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/

## Summary
In this tutorial, we will break down the specification of regular expressions which will help connect emails to the usesr through verifications.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping_constructs)

## Regex Components

### Anchors

Regex anchors assert something about the string or the matching process. They do not match any character, but they do match a position before or after characters. The two anchors in regex are ^ and $, where:
```
    ^ means that the following code must appear at the beginning of the string, and

    $ means that the preceding code must appear at the end of the string.
```
Our regex contains both anchors, so therefore a given string must match all the given specifications exactly. If not, the stringit won't be a match.

### Quantifiers

Quantifiers are used to communicate how many characters are expected. Quantifiers specify how many instances of a character must be present in the input for a match to be found. They often include the minimum and maximum number of characters that your regex is looking for. Our regex is using two quantifiers: + and {2,6}.

The "+" quantifier in our regex (as used in the expression [a-z0-9_.-]+ above), means that any character matching the characters inside the brackets is expected to appear at least once. The second instance of our + quantifier (the expression [\da-z.-]+), means the same is true.

The "{2, 6}" quantifier in our regex specifies the lower and upper bounds of the number of characters expected. Thus, the expression [a-z.]{2,6} means that we expect 2 to 6 characters matching those inside the brackets.

### Grouping Constructs

Capturing an expression is accomplished with the expression "( )" in regex. Anything within the set of parentheses is taken as a single group, and it allows all the information inside to be treated as a single unit.

Considering our expression (/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/), there are three unique character groups, being defined by the ( ). The groups are:

```
([a-z0-9_.-]+),

([\da-z.-]+), and

([a-z.]{2,6}).
```

Since these are single units, you can think about the expression as meaning "(Unit 1) @ (Unit 2).(Unit 3)" . This scheme is more intelligible, and corresponds to how email addresses are always formed, the "(string)@(site).(com)" template.

### Bracket Expressions

An integral piece of our regex analysis are the bracket expressions, of which we have three: [a-z0-9_.-], [\da-z.-], and [a-z.]. A bracket expression represents a single character, which can be anything as long as it is specified within the brackets. For example in our expression [a-z0-9_.-], this character will be matched by any lowercase letters from a-z, any digit from 0-9, or a period. As our quantifier "+" has no upper limit, any number of characters matching those specified within the brackets will match.

### Character Classes

A character class in a regex defines a set of characters, which can be used to fulfil a match by matching types of characters. In our expression above, \d is used to match any digit character.

## Author 

Andrew Nguyen

Email:
```
Blueandyn@gmail.com
```

Github:
```
BlueAndyn
```