# 17. Computer Science for JavaScript Challenge: Regex Tutorial 


  ## Table-of-Contents
  * [Description and Task](#description)
  * [Explanation and Examples](#explanation)
  * [Anchors](#anchors)   
  * [Quantifiers](#quantifiers)   
  * [OR Operator](#OR-Operator)  
  * [Character Classes](#Character-Classes)
  * [Flags](#flags)   
  * [Grouping and Capturing](#Grouping-and-Capturing)
  * [Bracket Expressions](#bracket-expressions)   
  * [Greedy and Lazy Match](#Greedy-and-Lazy-Match)
  * [Boundaries](#boundaries)
  * [Back-references](#Back-references)   
  * [Look-ahead and Look-behind](#Look-ahead-and-Look-behind)  
  * [Contributing](#Contributing)
  * [Questions](#questions)


 ## [Description](#table-of-contents)
 
Application Design and Function
As a web development student I want a tutorial explaining a specific regex
so that I can understand the search pattern the regex defines


 # My Task and Application Requirments

  - GIVEN a regex tutorial when I open the tutorial I want see a descriptive title and introductory paragraph   
    explaining the purpose of the tutorial, a summary describing the regex featured in the tutorial, a table of contents linking to different sections that break down each component of the regex and explain what it does, and a section about the author with a link to the author’s GitHub profile

  - WHEN I click on the links in the table of contents then I am taken to the corresponding sections of the   
    tutorial.

  - WHEN I read through each section of the tutorial then I find a detailed explanation of what a specific      
    component of the regex does

  - WHEN I reach the end of the tutorial then I find a section about the author and a 
    link to the author’s GitHub profile

## [Explanation](#table-of-contents)

  # Regex Tutorial

   - A regular expression (Regex/Regexp), is a special text string for describing a search pattern. When
     included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string.

  # Character Examples:

    - /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/ 

  # Explanation: 

   - -/ Begins Regex -^ This is always at the begining of the string, to position the anchors. -( 
      Groups together multiple "tokens" to create a capture group. This can be used to retrieve 
      a substring or backreference. -https This indicates a sub-expression string that should
      be matched. "s" .

 -  ? This is a Greedy quantifier, which is basically denoting 0 or 1 occurrence of previous 
      character (s) either http or https ^^ not 100% on this, pretty sure it takes a way 
      the 's' from http.

-  \/\/ This is an escaped character.

-  ) This Ends the capture grouped.

- ? Greedy quaintifier indicating the entire previous section wrapped in () is optional. You 
      can have it or not.

- ( Begins captured group.

- [ Begins bracket list.

-  /d Is a metacharacter indicating any one digit character (0-9).

-  a-z Indicates lower case letters between a-z.

-  \. Escape sequence denoting the character.

-  Indicates - character.

- ] Ends bracket list.

- (+) Because its outside the brackets the Greedy quantifier is denoting that the 
    previous bracket list characters, may occur one or more times.

- ) Ends captured group.

- \.Escape sequence denoting the character.

- ( Begins captured group.

- [ Begins bracket list.

- a-z. Indicates lower case letters between a-z.
    
- ] Ends bracket list. {2,6} Occurence indicator denoting the previous bracket list characters 
    may occur from 2 to 6 times.

- ) Ends captured group.

- ( Begins captured group.

- [ Begins bracket list.

- / Escapes regex to match the character /

- \w Is a character class indicating any dingle Word Characters. Those are any characters 
  including a-z, A-Z, 0-9, and _.

- . Escape sequence denoting the character.

- (-) Indicates - character.

-  ] Ends bracket list.

-  The Greedy quantifier denoting that the previous bracket list characters may occur zero 
   or more times.

-  ) Ends captured group.

-  Greedy quantifier indicating that the entire previous captured group may occur zero or 
      more times.

-  / Escapes regex to denote a regular / character.

-  ? Greedy quantifier indicating previous / character may have 0 or 1 occurrences.

-  $ Position acnhoring that ends the string.
    
-  / Ends Regex.



## [Anchors](#table-of-contents)
 -  The Anchors are always at the begining and end of the string. For the example above, ^ is the symbol for the 
    begining and $ is for the end.

   * ^               Matches any string that starts with
   * $               Matches a string that ends with


## [Quantifiers](#table-of-contents)
    
   - Quantifiers communicate to the regex engine that it MUST match the Quanity of the character or expression  
    to its LEFT. There are two types of Quantifiers; Greedy and Lazy, each type has the same description.

    * and *? Matches Zero or more times.
    + and +? Matches One or more times.
    ? and ?? Matches Zero or One times.
    {n} and {n}? Matches exactly n times.
    {n,} and {n,}? Matches atleast n times.
    {n,m} and {n,m}? Matches from n to m times.

  
## [OR Operator](#table-of-contents)
  
* It is not present in the code for the given matching email code, but in order to talk about the 
  OR Operator, we will look at the following code for matching a hex code.

- /^#?([a-f0-9]{6}|[a-f0-9]{3})$/

- This is a regex for matching a hex code that uses the OR Operator. What this will 
  do is it will match where it starts with the # and that has to come first followed by 
  one of the following:

- [a-f0-9]{6} which will match a 6 character long string that contains a 
   combination of a-f letters and 0-9 numbers.

- | OR Operator

- [a-f0-9]{3} it will match a 3 character long string that contains a combination of a-f 
  letters and 0-9 numbers.
  
## [Character Classes](#table-of-contents)
  
- Character Classes ensure that a given sequence of characters matches a Larger set of characters.

- [a-z]          Matches lowercase alphabetic characters between a and z
- \w             Matches a single word
- \d             Matches a single character that is a digit 0-9
- .              Matches any character

  
## [Flags](#table-of-contents)

- A regex flag is not used in the matching email code that is being used for this tutorial. A regular expression
  typically comes in the form:

- /regex/
  
  
## [Grouping and Capturing](#table-of-contents)
  
* Grouping expressions allows us to keep things more organized and easier to exact the characters of a given  
    group. This is used with parentheses "()".

- (https?:\/\/) This group is basically saying it allows the URL code to being with "http://", "https://" or  
   none of them.
- ([\da-z\.-]+)     This group which is the domain name. It matches 1 or more numbers, letters, dots or hypens 
   Ending it with a "+" linking it to the following line.
- ([a-z\.]{2,6})    Withe the + connecting this group together, this matches 2-6 copies of the sequences "[a-z\"
- ([\/\w \.-]*)     This group is is being matched as many times as they want because of the "*" at the end. 


  
## [Bracket Expressions](#table-of-contents)
  
* Bracket expressions are expressions between "[]" brackets. In the example above, we have the following 
  Bracket Expressions.

  - [\da-z\.-]
  - [a-z\.]
  - [\/\w \.-]
  
## [Greedy and Lazy Match](#table-of-contents)

  * Greedy and Lazy Quantifers allow you to find the Greedy and the Lazy match. "Greedy" being the longest
    "Lazy" being the shortest.
  
  - ([\da-z\.-]+) The "+" operator is greedy as it allows character matching from one to an infinite amount of 
    times.

## [Boundaries](#table-of-contents)
  
- If in a string, the coder is looking for for specific words. Boundaries are not used in the given 
  matching an email code.

## [Back-references](#table-of-contents)
  
- Back-references are not included in the given code..
  
## [Look-ahead and Look-behind](#table-of-contents)

- If using a look-ahead or look-behind, then it has to match in a certain order. It is not being used in the 
  given matching an email code.
  
## [Bracket Expressions](#table-of-contents)

- Back-references are not included in the given code.
    
## [Contributing](#table-of-contents)
  
    Feel free to contact me if there are any issues or ideas to implement.
    
## [Questions](#table-of-contents)
- Contact Information Below:
  [GitHub](https://github.com/arbinazari)

  [Email: arbinazari@hotmail.com](mailto:arbinazari@hotmail.com)
