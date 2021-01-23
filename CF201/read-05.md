# Reading-05

## If you wish to exit to the homepage click on the following link to head back to the [homepage](../README.md)

## Reading Assignment is as follows

Go through the reading material for this class and watch/bookmark the additional resources provided. Prepare an entry for your Readings Notes Repository that summarizes the principal reading topic as though you were presenting the material to someone new to the industry.

## Reading

From the Duckett HTML book:

Chapter 5: “Images” (pp.94-125)
Chapter 11: “Color” (pp.246-263)
Chapter 12: “Text” (pp.264-299)

## HTML Chapter 05: Images

### Reasons to load images onto a page: logo, photograph, illustration, diagram, or chart.

### How to add images to pages using HTML

- Create a folder that will store your images used for your website
- How to add images:
  1. the img element is used to contain the img file and has the following 
  attributes:

    - src
    - alt
    - title
    - height
    - width

- Where to place?

  1. Before the p
  
  1. inside the start of the p

  1. in the middle of the p

- Where you place is important because browswers show HTML elements in 2 ways:

  1. BLock Elements always appear on a new line (such as h1, p )

  1. Inline Elements sit within a block level element and do NOT start on a new line (such as b, em, img)

- 3 rules for creating images:
  
  1. Save images in the right format

  1. Save images at the right size

  1. Measure images in pixels

- JPEG is for many different colors

- GIF or PNG is for few colors or large areas with same color

- Resolution is the number of pixels on the screen

- Vector Images are resolution independent and can increase dimensions without affecting quality of the image

### Choosing the Right Format

### Optimizing Images for the Web






## Chapter 11: Color

### How to specify colors

### Color Terminology and Contrast Ensure Text is readable

### Background Color

  1. Saturation - amount of gray in a color where max sat = no gray and min sat = mostly gray
  1. Brightness - amount of black in a color where max brightness = no blk and min brightness = very dark
  1. Contrast - must be present to make text legible
    a. Low Contrast- hard to read text
    b. High Contrast- easy to read text
    c. Medium Contrast- for long spans of time, improves readability

### Foreground color - specify the color of the Text inside an Element.

    - color: (values: rgb, hex code, color names);

### Background color - if no background color specified color is transparent by default

    - background-color: (values: rgb, hex code, color names || hsl, hsla);

  1. Property - HSL Colors are Hue, Saturation, Lightness in this order

    - Hue: expressed as an angle 0-360
    - Saturation is Percentage
    - Lightness is percentage
    - Alpha a decimal between 0-1
    - hsl is a value that can be used for background color

  1. Opacity
    - opacity:(value: percent or decimal from 0-1);

## Chapter 12: Text

## Size and Typeface of text

### Typeface Terms:

  1. Serif - fonts that have extra detains in the ends of the main strokes of the letters, Considered easier to read for prints, Have EXTRA details

  1. Sans-Serif - fonts that have straight ends to letters, clean look/design, Low resolution
    - Monospace - every letter is the same width
      - Code becomes more readable
  1. Text dimensions
      - Ascender - above the cap height
      - Cap Height - top of flat letters
      - X- Height - height of the letter x
      - Baseline - line the letters sit on
      - Descender - below the baseline

### CSS Typeface Properties

  1. Specifying typeface - allows you to specify the typeface that should be used for any text inside the element to which a CSS rule applies to and the value is the name of the typeface you want to use

    - font-family:(value: Courier New, Courier, monospace);
    - font-size:(px, percent, em);
    - Bold, italics, capitals, underlines
    - Spacing between lines, words, and letters

### Properties that allow you to control the Appearance of text can be split into 2 groups:

    1. Those that affect the Font/Appearance
    1. Those that have same effect on text no matter the Font type

Type Scales - scale is based on “points”, 1 pix = 1 point = 1/72 in and computers have a resolution of 72 dots / inch . Default size in a browser is 16 px, so if using %/ems, the size is relative to default size of 16px.

- 12 pixel scale
- 16 pixel scale

### Pseudo Elements / Class

Pseudo Element - acts like an extra element is in the code
Pseudo Class - acts like an extra value for a class attribute
CSS Fonts

- @font-face allows you to use a font even if it is not installed on the the computer of the person browsing by specifying the path to allow copy

- @font-face { font-family: ‘value name’; src: url;}

Font formats should appear in the script in this order:

- eot>woff>ttf/otf>svg

Bold - creates bold text

- font-weight: (normal, bold);

Italic - extra styling

- font-style: (normal, italic, oblique);

Upper/Lower case Property used to change the case of the text

- text-transform: (uppercase, lowercase, capitalize);

underline/strike property

- text-decoration: (none, underline, overline, line-through, blink);

Leading (pronounced ledding) vertical space between lines of text. Descender letter that drops below the baseline. Ascender letter the highest point of the letter. Leading is measured from desceneder bottom to ascender top.

- line-height: (ems);

Letter and Word Spacing - space between each letter, kerning. 
letter-spacing: (ems);

- word-spacing: (ems); default is .25ems

Indenting Text - indents the first line of text within an element, pos/neg val

- text-indent: (px, ems) ;

Drop Shadow - dark version of the word just behind it and slightly offset, embossed effect

- text-shadow: ();

First Letter or Line - pseudo elements/class Its as if there is an extra first letter/ first line which can have its own styles applied

- :first-letter:( );

- :first-line:( ) ;

Styling Links - allow you to set different styles for links that have/have not yet been visited

- :link
- :visited

Responding to Users - allow you to change the appearance of elements when a user is interacting with them

- :hover
- :active
- :focus
