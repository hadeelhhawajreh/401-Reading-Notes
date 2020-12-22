
## Regular Expressions in Python
In Python, regular expressions are supported by the re module. That means that if you want to start using them in your Python scripts, you have to import this module with the help of import:
 ```
import re
```
Basic Patterns: Ordinary Characters
You can easily tackle many basic patterns in Python using ordinary characters. Ordinary characters are the simplest regular expressions. They match themselves exactly and do not have a special meaning in their regular expression syntax.

Wild Card Characters: Special Characters
Special characters are characters that do not match themselves as seen but have a special meaning when used in a regular expression. For simple understanding, they can be thought of as reserved metacharacters that denote something else and not what they look like.

Let's check out some examples to see the special characters in action...

But before you do, the examples below make use of two functions namely: search() and group().
With the search function, you scan through the given string/sequence, looking for the first location where the regular expression produces a match.
The group function returns the string matched by the re. You will see both these functions in more detail later.

Back to the special characters now.

. - A period. Matches any single character except the newline character.

re.search(r'Co.k.e', 'Cookie').group()
'Cookie'
^ - A caret. Matches the start of the string.

This is helpful if you want to make sure a document/sentence starts with certain characters.

re.search(r'^Eat', "Eat cake!").group()
'Eat'
## However, the code below will not give the same result. Try it for yourself:
# re.search(r'^eat', "Let's eat cake!").group()
$ - Matches the end of string.

This is helpful if you want to make sure a document/sentence ends with certain characters.

re.search(r'cake$', "Cake! Let's eat cake").group()
'cake'
## The next search will return the NONE value, try it:
# re.search(r'cake$', "Let's get some cake on our way home!").group()
[abc] - Matches a or b or c.
[a-zA-Z0-9] - Matches any letter from (a to z) or (A to Z) or (0 to 9).

TIP: Characters that are not within a range can be matched by complementing the set. If the first character of the set is ^, all the characters that are not in the set will be matched.

re.search(r'[0-6]', 'Number: 5').group()
'5'
## Matches any character except 5
re.search(r'Number: [^5]', 'Number: 0').group()

## This will not match and hence a NONE value will be returned
#re.search(r'Number: [^5]', 'Number: 5').group()
'Number: 0'
\ - Backslash.
Perhaps, the most diverse metacharacter!!

If the character following the backslash is a recognized escape character, then the special meaning of the term is taken (Scenario 1)
Else if the character following the \ is not a recognized escape character, then the \ is treated like any other character and passed through (Scenario 2).
\ can be used in front of all the metacharacters to remove their special meaning (Scenario 3).
## (Scenario 1) This treats '\s' as an escape character, '\s' defines a space
re.search(r'Not a\sregular character', 'Not a regular character').group()
'Not a regular character'
## (Scenario 2) '\' is treated as an ordinary character, because '\r' is not a recognized escape character
re.search(r'Just a \regular character', 'Just a \regular character').group()
'Just a \regular character'
## (Scenario 3) '\s' is escaped using an extra `\` so its interpreted as a literal string '\s'
re.search(r'Just a \\sregular character', 'Just a \sregular character').group()
'Just a \\sregular character'
There is a predefined set of special sequences that begin with '\' and are also very helpful when performing search and match. Let's look at some of them up close...
```
\w - Lowercase 'w'. Matches any single letter, digit, or underscore.
\W - Uppercase 'W'. Matches any character not part of \w (lowercase w).

print("Lowercase w:", re.search(r'Co\wk\we', 'Cookie').group())
```

## Matches any character except single letter, digit or underscore
```
print("Uppercase W:", re.search(r'C\Wke', 'C@ke').group())
```

## Uppercase W won't match single letter, digit
```
print("Uppercase W won't match, and return:", re.search(r'Co\Wk\We', 'Cookie'))
Lowercase w: Cookie
Uppercase W: C@ke
Uppercase W won't match, and return: None
\s - Lowercase 's'. Matches a single whitespace character like: space, newline, tab, return.
\S - Uppercase 'S'. Matches any character not part of \s (lowercase s).

print("Lowercase s:", re.search(r'Eat\scake', 'Eat cake').group())
print("Uppercase S:", re.search(r'cook\Se', "Let's eat cookie").group())
Lowercase s: Eat cake
Uppercase S: cookie
\d - Lowercase d. Matches decimal digit 0-9.
\D - Uppercase d. Matches any character that is not a decimal digit.
```
# Example for \d


print("How many cookies do you want? ", re.search(r'\d+', '100 cookies').group())
How many cookies do you want?  100
The + symbol used after the \d in the example above is used for repetition. You will see this in some more detail in the repetition section later on...
```
\t - Lowercase t. Matches tab.
\n - Lowercase n. Matches newline.
\r - Lowercase r. Matches return.
\A - Uppercase a. Matches only at the start of the string. Works across multiple lines as well.
\Z - Uppercase z. Matches only at the end of the string.
```
