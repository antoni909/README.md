# Class 02

## Reading Assignment is as follows

## For your assignment, go through these resources, and create a markdown file titled class-02.md in your reading notes repo that summarizes the topics. Then ACP your master branch to create a rendered web page on github pages

## Reading

    1. From the Duckett HTML book:

        - Chapter 2: “Text” (pp.40-61)
        - Chapter 10: Ch.10 “Introducing CSS” (pp.226-245)
    1. From the Duckett JS book:

        - Chapter 2: “Basic JavaScript Instructions” (pp.53-84)
        - Chapter 4: “Decisions and Loops” only up to the section on switch statements (pp.145-162)

## Additional Resources

This link is a reading on how git message conventions and how to submit[git messages](https://chris.beams.io/posts/git-commit/)

## HTML Chapter 2: Text

## Summary Type: Notes in Outline Form

## The main objectives of this chapter are: Headings and Paragraphs, Bold, Itilics, Emphasis, Structural and Semantic markup

### The content of this chapter covers Structural Markup are the elements that you can use to describe both headings and paragraphs and Semantic Markup is not intended to affect the structure of a page, but to provides extra information such as where emphasis is placed in a sentence

    1. Structural Elements (Markup)
        - Headings (h1,h2,h3,h4,h5,h6)
        - Paragraph(p)
        - Bold and Itilics (b, i)
        - Subscript/Superscript (sub, sup)
        - Whitespace = default is no whitespace
        - Line Breaks <br /> start a new code line 
        - Horizontal Rule <hr /> create a hor line on page as a page break
    2. Semantic Elements (Markup)
        - Strong <strong> turns text to bold
        - Emphasise <em> turns text to itilics
        - Blockquote <blockquote> used for longer quotes that take up a paragraph
        - Quotes <q> used for shorter quotes
        - Abbreviations <abbr> 
        - Cite <cite> used to reference
        - Define <dfn> used to identify new term 
        - Address <address> contains contact details of author of the page
        - Inserted <ins> will underline the newly inserted content
        - Delete <del> strikes out deleted content
        - Strike Line <s> creates a line striking out content that is no longer accurate/relavent

## HTML Chapter 10: Introducting CSS

## Summary Type: Notes in outline form

## The main objectives of this chapter are what CSS does, how CSS works, Rules, Properties, and Values

    1. Understanding CSS: Thinking inside the Box
        - CSS allows you to CREATE rules that control the way each individual box (surrounding each element) is presented
        - Block Level Elements span L to R on the page and Inline Elements have other elements neighboring them
        - Example Style types: 
            - Boxes 
                -background color and images
                - position in browser, 
                - width and height, 
                - borders 
                    - color
                    - width
                    - style
            - Text 
                - Typeface
                - Size
                - Color
                - Itilcs, Bold, Uppercase
                - Lowercase
                - Smallcaps
            - Specefic
                - Tables, lists, and forms
    1. CSS Syntax 
        - Selector: indicate which element the rule applies to.   
        - Declaration: indicate how the elements should be styled. 
            - Declaration Properties: indicate the aspects of the element you want to change, i.e color,font,width,height and border.
            - Declarartion Value: specify the settings you want to use for the chosen properties.

        p {
            font-family: Ariel;}
    1. External vs Internal CSS
        - External CSS: create a link to HTML page from a CSS page using <link>
            - <link> is an empty element and lives int the <head> element in an HTML page. This element has 3 attributes:
                - href:"" : specifies the path to the CSS file
                - type:"" : specifies the type of document being linked and should be: "text/css" for a CSS page
                - rel:"" : specifies the relationship between the HTML page the file being linked and should be: "stylesheet"
        - Internal CSS: includes inline CSS rules inside HTML page using the <style> element.
            - <style> usually lives inside the head element
    1. CSS Selectors (indicate which element the CSS rules apply to)
        - Are case sensative, must match name and attribute values exactly
        - Common Selectors are:
            - * (Universal Selector: Applies to all Elements in the doc)
            - h1, h2, h3 {} (targets all <h1>,<h2>,<h3> elements)
            - .x {} (targets elements whose CLASS attribute has a value of any assigned value x)
            - p.x {} (targets only <p> class attributes with assigned value of x)
            - #x {} (targets elements with id attribute of assigned value x)
    1. How CSS Rules Cascade and Rule Precedence
        - Last Rule: it two selectors are identical, the latter will override the former
        - Specificity: The more specific rule will overried the more ambiguous rule
        - Important: you can add:  !important  after any property value to be considered more important than other rules that apply to the same element
            - Example:
                - p b {
                    color: pink;}
                - p b {
                    color: blue !important;}
click on the following link to head back to the [homepage](../README.md)

## JavaScript Chapter 04: Decisions and Loops

## Summary Type: Notes in Outline form

## The main objectives of to understand evaluations, decisions(conditional statements) and loops in JavaScript. There are 2 components to a Decision

    1. Expression is evaluated, returning a value
    2. Conditional Statement says what to do in give situation

### Comparison Operators: Evaluating Conditions

    - You can evaluate a situation by comparing one value to what you migh expect to get, resulting in a boolean value of True or False
        - Comparison Operators
            - == "is equal to", compares 2 values (numbers, strings, booleans) to see if they are the SAME
            - === "strict equal to", compare 2 values to check that both the data type and value are the same
            - != "is not equal to", compares 2 values(numbers, strings, booleans) to see if they are NOT the same
            - !== "strict not equalt to", compares 2 values to check that both that data type and value are NOT the same
        - Typical Syntax
            - Example:            
              ( Operand | comparison operator | Operand) 
              (    A              ===             B    )
        - Logical Operators
            - Allow you to compare the results of more than one comparison operator
                - && "Logical And", tests more than 1 condition. 
                    - If both expressions eval to T the expressions returns T
                    - If One espression evals to F then the expression returns F
                - || "Logical Or", tests at least one condition
                    - If either expression evals to T then expression returns T
                    - If both eval to F then expression returns F
                - ! "Logical Not", takes single boolean val and inverts it
                    - Example:
                        !(2 less than 1) returns T
    - If Statements
        - evaluate a condition, if the condition evals to T, any statements in the subsequent code block are executed. If the condition resolves to F, statements in that code block will NOT run.
    - If...else Statements
        - if it resolves to T, the first code block is executed, if F teh second code block is run instead.
        - code blocks are contained within curly braces: { code block}
