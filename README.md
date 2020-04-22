# Hate it or love it - regular expressions

```
  \_\_\_  \_\_\_   \_\_  \_\_\_  \_  \_
   \_  \_  \_     \_      \_      \_  \_
    \_\_    \_\_   \_  \_  \_\_      \_
     \_  \_  \_     \_  \_  \_      \_  \_
      \_  \_  \_\_\_   \_\_  \_\_\_  \_  \_
      
             \_\_\_   \_    \_\_    
              \_     \_  \_  \_  \_  
               \_\_   \_  \_  \_\_    
                \_     \_  \_  \_  \_   
                 \_       \_    \_  \_  
          
  \_\_    \_  \_  \_  \_  \_  \_  \_  \_\_\_    \_\_
   \_  \_  \_  \_  \_\_\_  \_\_\_  \_  \_      \_
    \_  \_  \_  \_  \_  \_  \_  \_  \_  \_\_      \_
     \_  \_  \_  \_  \_  \_  \_  \_  \_  \_          \_
      \_\_      \_    \_  \_  \_  \_  \_  \_\_\_  \_\_
      
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
