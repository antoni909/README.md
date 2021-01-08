# Class 01

## Reading Assignment is as follows

### For your assignment, go through these resources, and create a markdown file titled class-01.md in your reading notes repo that summarizes the topics. Then ACP your master branch to create a rendered web page on github pages. Here are the chapters to read/skim before Class 1

    1.   From the Duckett HTML book:
        -   Introduction (pp.2-11)
        -   HTML Chapter 1: “Structure” (pp.12-39)
        -   HTML Chapter 8: “Extra Markup” (p.176-199)
        -   HTML Chapter 17: “HTML5 Layout” (pp.428-451)
        -   HTML Chapter 18: “Process & Design” (pp.452-475)

    2.  From the Duckett JS book:
        -   Introduction
        -   JS Chapter 1: “The ABC of Programming” (pp.11-52)

## To Summarize the information I will create a quiz for each chapter and provide an outline of what information I deemed most important during the reading 

## HTML Chapter 1: Structure

## Summary Type: Paraphrasing Chapters

### HTML describes the structure of pages by using containers called Elements that store content. Elements and tags have attributes that provide additional information about the contents of said Element. HTML stands for Hypertext Markup Language and it allows you to annotate the document. Elements are composed of an opening tage + content + closing tag. Attributes are added inside the opening tag and provide extra information about an element. An attribute consists of a name and a value. The name addresses the type of extra informaiton you are supplying and the value refers to the information or setting for the attribute

    - Quiz Questions
        1. What does HTML stand for and what is a markup language?
        1. Elements are usualy made up of 2 ___ an opening ___ and a closing ____
        1. HTML ____ tells the browser something about the information that sits between its opening and closing ____ 
        1. Even though the terms element and tag are used interchangeably, how is an element more strictly defined?
        1. An ___ of an HTML Element is made up of 2 parts, the ____ and the ____ which are seperated by an equals sign.
        1. This part of the Attribute is the information or setting for the attribute and should be placed in double quotes
        1. This particular part of the Attribute indicate what kind of extra information you are supplying about the elements content and should be written in lower case.
        1. Everything inside this particular Element is shown inside the main browser window
        1. The contents of the ____ Element are either shown at the top of the browser or the tab for that page

    - Quiz Answers
        1. Hypertext Markup Language, markup means you are allowed to annotate text and in turn annotations allows you to provide additional meaning to the contents of the document.
        1. Begore the body Element you will see the ____ Element and contains information about the page and you will usually find the ____ Element inside 
        1. tag
        1. HTML Element, tags
        1. An element comprises the openind tag and the closing tag and any content that lies between them
        1. Attribute, name , value
        1. value
        1. name
        1. Body Element 
        1. Head Element
        1. Title Element

## HTML Chapter 8: Extra Markup

## Summary Type: Paraphrasing Chapter 8

### Because there have been several verions of HTML, it is best to start an HTML document with the doctype declaration <!DOCTYPE html> (used for HTML 5). You can also create comments in your HTML doc using t<!--comment here--> which will only be visible in the code but not in the user browser. An id attribute is called a global attribute because it can be used on all elements. It is used to uniquely identify one element amongst all others and allows you to target it for special styling for CSS or interactivity with JavaScript. A class attribute is also a global attribute available to all elements. The idea is that instead of targetting a single element you can group together type/class of elements that require special attention for styling or simply because the chosen elements are more special than others on the page

### There is a subtle and important distinction between In-line and Block Elements. Block elements will always form a new code line while In-Line Elements will always appear to continue on the same code line with neighboring elements. Examples of block elements are h1, p, ul, and li. Examples of inline elements are a, b, em, and img. Div and Span elements are used to "group" together block and inline elements. The div element allows you to group inline and block elements in one block-level box. An example of its use is if you want to create a div for all the elements for the header of a site or to contain comments from users. The span element is like an inline element and is used to contain a section of text where there is no other suitable element to differentiate it from surrounding text or contain a number of inline elements

### The meta element will always be found inside the head element and will contain information about the page. It is considered an empty element because it does not have a closing tag and uses attributes to carry information. Some commonly named values are description, keywords, robots, author, pragma and expires. It is also important to note that HTML has special reserved characters such us <>, &, ", etc

## HTML Chapter 17: HTML 5 Layout

## Summary Type: Link to HTML Doc with Sample HTML outline with Comments on each element being used

[click here to be redirected to a sample HTML5 page](/CF201/sample.html)

### In HTML 5, instead of using multiple div elements like in the tradional older versions, you can use new elements that provide clearer code

## HTML Chapter 18: Process and Design

## Summary Type: Barebones Outline of the important concepts in the reading

1. What needs to be on your site:
    1. know the target audience
    1. the purpose your website will serve to the users
    1. what will the users gain from visiting your website
    1. what subject matter knowledge will the users need if any?
    1. probe how often users traffic your website
1. Organize the information to be displayed on your site:
    1. create a site map
    1. create a wire frame
        - Note: [this is an online tool for creating wireframes](https://gomockingbird.com/projects/1we38mv/4gXVnC)
    1. Implement website designs based on the following:
        - content
        - prioritizations
        - organizations
        - visual hierarchy
            - size
            - color
            - style
        - grouping 
            - proximity
            - closure
            -continuance 
            - white space
            - color
            - borders
        - similarity
    1. Design the site navigation

## JavaScript Chapter 1