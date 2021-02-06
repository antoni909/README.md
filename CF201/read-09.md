# Reading-08

## If you wish to exit to the homepage click on the following link to head back to the [homepage](../README.md)

## Reading Assignment is as follows

    From the Duckett HTML book:

    Chapter 1 “Forms” (p.1-1)
    Chapter 1: “Lists, Tables & Forms” (pp.330-357)
    From the Duckett JS book:

    Chapter 1: “Events” (pp.243-292)

## JS Chapter 06: “Events” 

Events- browsers way of monitoring user activity and the script responding to those events. In summary, interactions create events → events trigger code → code responds to user

1. Event Types pg 246-247
        1. Ui - when user interacts with UI vs web page 
        1. Keyboard - user interacts with keyboard
        1. Mouse -  user interacts with mouse
        1. Focus - when ELEMENT gains/loses focus
        1. Form - user interacts with a form
        1. mutation - when DOM structure is changed by script
1. Event Handling Process
    1. Select ELEMENT → Specify EVENT (‘binding’) → call code
    1. 1Types of Event Handlers:
        1. HTML *do not ever use*
        1. DOM 
            1. One function per each event handler only
            1. Event Handler Syntax: element + event = code
                    1. element.onevent = functionName;
                    1. element is usually stored in a var
            1. Event listeners - can use more than One function 
                    1. Syntax: element + addEventListener : ‘event’+functionName+boolean(f)
                    1. element.addEventListener(‘event’.functionName [false]);
            1. Using Parameters for Event handlers/listeners
                1. you must wrap the function call in an anonymous function
                1. anonymous function gets placed before the event function
                1. Arguments are passed to the event functions in its parenthesis like normal
            1. Fallback code for older versions that do not support parameters
                1. Pg 258
        1. DOM level 1 Event FLOW - 
    1. Event Bubbling - event starts at specific node and flows to the least specific 
    1. Event Capturing - event starts at least specific node and flows to most specific 
1. The Event Object - tells you information about the event and the element it happened to
    1. The event object = has parameter name ‘e’ and gets passed to any function that is event listener/handler
    1. Event Delegation - due to event flow, ‘container’ elements can use event handlers that use the target property to find out which child element an event happened to. This eliminates having to place event listeners to every source element. Other benefits:	
        1. Works with new elements
        1. Solves limitations with _this_ keyword
        1. Simplifies code
    1. Using Event Delegation - pg 268 flow chart
1. Changing default behavior
    1. Event object has methods that change default behavior of elements and how the container elements respond to events
        1. preventDefault()
        1. stopPropagation()
            1. Stops the bubbling up after event to further container elements
        1. return false;
            1 Prevents default behavior of element, but stops processing subsequent code within that function
1. Using an Event Delegation - pg 268
1 Which Element Did an Event Occur on? pg 270
1 Different types of events - pg 2711 User Interface Events - user interacts with Browser Window not HTML page pg 272
1. Load event - used to trigger scripts that access the content of the page
    1. Raised by the window object after the page has loaded
        1. HTML+resources
        1. Images
        1. Scripts/CSS
        1. 3rd party content
    1. Focus / Blur Events - fire when they gain/lose focus, used mostly on forms and helpful when:
        1. You want to show tips/feedback to user as they interact with an individual element in a form
        1. Trigger form validation as user moves one control to the next
    1. Mouse Events - fire when mouse moved/buttons clicked. Pg 276
        1. Where Events Occur - Can tell you where cursor was positioned when event was triggered using screenX/screenY, pageX/pageY, clientX/clientY properties
    1. Keyboard Events - pg 281    1. Form Events - pg 282, 
    1. Mutation Events and Observers - 
        1. Mutation Event - when elements add/del from dom
        1. Mutation Observer - report changes as a batch before reacting, specify type of DOM changes to react to
    1. HTML 1events pg 286

## Chapter 1: “Lists, Tables & Forms”

## To exit to the homepage click on the following link to head back to the [homepage](../README.md)

CSS properties made for HTML tables, lists, forms

1. Bullet Styles
    1. List-style-type
        1. Control shape of bullet
    1. List-style-image
        1. Use an img for bullet
    1. List-style-position
        1. Indent style of the bullet
    1. List-style
        1. Shorthand for all
1. Table Properties 
    1. Give Cells Padding
        1. empty-cells: (val: show,hide, inherit); 
        1. Border-spacing: (val: num px)
        1. border-collapse: (val: collapse, separate);
    1. Unique Headings
    1. Shade Alternate Rows
    1. Align Nums
1. Styling Forms
    1. Styling Text Inputs {css rules}
        1. font-size: num%;
        1. cssSelector:focus - is a pseudo class to change background color of text input when used
            1. cssSelector:hover - pseudo class applies same styles when user hovers over 
    1. Styling Submit Buttons
        1. color: change color of text on button
        1. text-shadow: give 3d look
        1. background-color: color in button
        1. cssSelector: hover changes button appearance

## HTML Chapter 1: “Forms”

1. How to collect info from site visitors
1. Types of Form Controls
    1. Several types used to collect info:
        1. For adding text
            1. Text input
            1. Password input
            1. Text box
        1. For Making choices
            1. Radio buttons
            1. Check Boxes
            1. Drop-down Boxes
        1. For Submitting forms
            1. Submit Buttons
            1. Image Button
            1. File Upload Box+Button
1. How Forms Work
            1. User Provides Input via form as name:value pair
            1. Server Process Data + Store Info in DataBase
            1. Server Creates new Page for User based on data received
1. Form Controls Gather bits of Data
1. HTML elements used for Form Structure
    1. Form Element
        1. \<form>
        1. carries action attributes
        1. Usually has method/id attribute 
            1. Action attribute
                1. action=”url”
                1. Attribute of every form element, value is some url
            1. Method attribute
                1. method=”get/post”
                1. “Get” - vals from form added to end of url in action attribute
                    1. Used for short forms (search boxes)
                    1. Retrieving data from web server
                    1. If method
                1. “Post” - vals sent as HTTP headers
                    1. Used for user upload a file
                    1. Long forms
                    1. Contains sensitive data
                    1. add/del info from database
            1. Size attribute
                1. NOT USED ANYMORE
    1. Input Element
        1. \<input>
        1. Creates several form controls. Vals of type attribute determines the kind of input they create
            1. Type vals
                    1. type=”text”
                    1. Creates  a _\<span> style="text-decoration:underline;">single-line</span>_ of text input
                    1. type=”password”
                    1. Creates textbox that acts like single-line input + characters are hidden
            1. Input attributes
                1 Name attribute
                    1. name=”some-val”
                    1. Identifies the form control + sent with info users enter to server
                    1. Indicates the name of the input
                1. Max-length attribute
                    1. maxlength=”some-val”
                    1. Limit the number of characters user enter to textfield
            1. Other Type Vals
                    1. type=”radio”
                        1. Lets user pick just one bubble bullet
                        1. Val of name=”val” attribute should be same for all opts
                        1. checked=”val” used to indicate which vals should be selected when page loads
                    1. type=”checkbox”
                        1. User can select more than 1 answer 
                        1. name=”val” val should be the same for all possible answers
                        1. checked=”val” its val should be checked when page loads
                    1. type=”file”
                        1. Allows user to upload a file from their comp
                    1. type=”submit”
                        1. Send a form to the server
                    1. type=”image”
    1. Text Area Element
        1. \<textarea>
        1. Used to create multi-line text input / not an empty element
    1. Select Element
        1. \<select>
        1. Shows a drop down list and allows users to pick one option
            1. name=”val” attribute
                1. Indicates name of form control being sent to server + val selected
        1. Option Element
                1. \<option>”option x”\<option>
                1. Specify the options the user can select from
                    1. value=”val” attribute
                    1. Indicates name of control used 
    1. Button Elements
        1. \<button>
            1. Allows customization of button appearance by placing images and text inside element
1. Labeling Form Controls
    1. \<label>
        1. Used to:
            1. Wrap the text description + form input
    1. \<fieldset>
        1. Group related form controls together
            1. \<legend>
                1. Contains the caption for related form controls

## To exit to the homepage click on the following link to head back to the [homepage](../README.md)

## [Top  of page](#Reading-08)
