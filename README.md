# Hate it or love it - regular expressions

```
  \_\_\_   \_\_\_   \_\_   \_\_\_  \_  \_
   \_  \_   \_     \_       \_      \_  \_
    \_\_     \_\_   \_  \_   \_\_      \_
     \_  \_   \_     \_  \_   \_      \_  \_
      \_  \_   \_\_\_   \_\_   \_\_\_  \_  \_
      
             \_\_\_    \_     \_\_    
              \_      \_  \_   \_  \_  
               \_\_    \_  \_   \_\_    
                \_      \_  \_   \_  \_   
                 \_        \_     \_  \_  
          
 \_\_     \_  \_   \_  \_   \_  \_   \_   \_\_\_    \_\_
  \_  \_   \_  \_   \_\_\_   \_\_\_   \_   \_      \_
   \_  \_   \_  \_   \_  \_   \_  \_   \_   \_\_      \_
    \_  \_   \_  \_   \_  \_   \_  \_   \_   \_          \_
     \_\_       \_     \_  \_   \_  \_   \_   \_\_\_  \_\_
      
     By Kamil Mikolajczyk and Krystian Przybyla-Warmuzinski
                          23.04.2020
  
```

## Agenda
* Intro
* Basic symbols
* Any/None
* Quantifiers (occurence and repetition)
* Grouping
* Lookahead and lookbehind
* Modifiers
* Advanced usage and examples

## Introduction
### Overview
* Allows to find patterns in the text
* Helpful in find-and-replace operations
* Helpful in text values validation
* Very widely known and standarized
* Available in most of technologies
* Implemented in IDEs and text editors

### Useful tools
* https://www.regexpal.com/
* https://regex101.com/
* https://www.debuggex.com/

### Crazy example
http://www.ex-parrot.com/~pdw/Mail-RFC822-Address.html

## Basic symbols
### Wildcards
```
. (dot) - any char
\s - a white-space char
\w - a word (alphanumeric) char (letters, digits, underscore) 
\d - a digit
\b - a word boundary
```

### Negative wildcards
```
\S - anything else than a white-space char
\W - anything else than a word char
\D - anything else than a digit
\B - anything else than a word boundary
```

### Others
```
^ - beginning of a string/line
$ - end of a string/line
\xZZ - a hex char ZZ
\0 - null
```

### Special characters
`.^$\[]{}()?*+|`

## Any/None
```
[] - any of matches
[^] - none of matches

[ab] - a or b
[abc] - a or b or c
[c-r] - any of c,d,e,f,....,p,q,r
[a-zA-Z] - any letter
[^a-z] - anything but a lowercase letter
[^79h] - anything else than 7, 9 and h
```

## Quantifiers
```
? - 0 or 1 occurrence
+ - at least 1 occurrence
* - 0 or more occurrence

{4} - something occurs exactly 4 times
{5,10} - something occurs between 5 and 10 times
{2,} - something occurs at least 2 times
```

## Grouping
* can be used to reference chunks for substitution
* can be combined with quantifiers
* can be joined with `|` operator to create an alternative

## Lookahead and lookbehind
### Positive lookahead
`foo(?=bar)` will match `foo` only if it's followed by `bar`
### Negative lookahead
`foo(?!bar)` will match `foo` followed by anything but `bar`
### Positive lookbehind
`(?<=foo)bar` will match `bar` only if it follows `foo`
### Negative lookbehind
`/(?<!foo)bar/` will match `bar` only if it NOT follows `foo`

## Modifiers
They change global behavior of matching
```
\g - global - causes NOT stopping matching after first occurrence
\i - case insensitivity
\m - multi-line - handles ^$ per line, instead of whole input
\y - sticky - matches only beginning of the input in sequence
\u - unicode - extra handling of unicode chars
```
