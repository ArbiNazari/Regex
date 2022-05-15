# 17. Computer Science for JavaScript Challenge: Regex Tutorial 


  ## Table-of-Contents
  * [Description and Task](#description)
  * [Anchors](#anchors)   
  * [Quantifiers](#quantifiers)   
  * [OR Operator](#OR)  
  * [Character Classes](#classes)
  * [Flags](#flags)   
  * [Grouping and Capturing](#grouping)
  * [Bracket Expressions](#bracket)   
  * [Greedy and Lazy Match](#greedy)
  * [Boundaries](#boundaries)
  * [Back-references](#back)   
  * [Look-ahead and Look-behind](#look)  
  * [Questions](#questions)
  * [Contributing](#table-of-contents)
  * [Questions](#table-of-contents)


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
  
  
## [Character Classes](#table-of-contents)
  
- Character Classes ensure that a given sequence of characters matches a Larger set of characters.

- [a-z]          Matches lowercase alphabetic characters between a and z
- \w             Matches a single word
- \d             Matches a single character that is a digit 0-9
- .              Matches any character

  
## [Flags](#table-of-contents)
  
  
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
  
  
## [Look-ahead and Look-behind](#table-of-contents)
  
  
## [Bracket Expressions](#table-of-contents)


    
## [Contributing](#table-of-contents)
  
    Feel free to contact me if there are any issues or ideas to implement.
    
  ## [Questions](#table-of-contents)
  Contact Information Below:
  [GitHub](https://github.com/arbinazari)

  [Email: arbinazari@hotmail.com](mailto:arbinazari@hotmail.com)
