# Reading-14

## If you wish to exit to the homepage click on the following link to head back to the [homepage](../README.md)

## Reading

    The following reading is required for psychological safety talk:

    What Google Learned From Its Quest to Build the Perfect Team
    Read the following articles and/or review the following examples on CSS animations:

    Read this article on CSS Transforms
    Read this article on CSS Transitions & Animations
    1 simple CSS3 transitions that will wow your users
    1 Buttons animated
    CSS3 Animations: Keyframes
    404
    Pure CSS Bounce Animation

Outline from: Web Designer Depot

1. transition property has 1 vals
   1. Properties to transition
   1. Speed of transition
   1. How the acceleration is calc
1. Fade effects is 1 steps (fade in)
   1. Initial state
   1. Change state
1. Change Color
   1. Set element with pseudo class :hover
   1. Set background to some color
1. Grow/Shrink
   1. Use transform to enlarge >1 scale
   1. transform: scale(1.1);
   1. To shrink &lt;1 scale
1. Rotate elements 11. Assign rotate class(name convention) add transform 12. Add pseudo class :hover to class 13. Transform: rotateZ(+/- someNum deg);
1. Square to Circle 14. myClass:hover + border-radius: 50%
1. 3d shadows
1. Swing 15. use: @keyframes, animation, animation-iteration
1. Inset border 16. Use :hover + box-shadow to a select class

What Google learned from its quest to build the perfect team

1. Psychological Safety: generally speaking the following group dynamic increases project success regardless of individual talent:
   1. Conversational turn taking + empathy = bonding
   1. Average social sensitivity
1. The take-away from this reading: The best teams listen to each other and show sensitivity to each members feelings/needs

[top of page](#Reading-14)

## Transform Articles

Transforms - new ways to position/alter elements with CCS3

Transform Syntax

1. transform - scale(X); vals are transform type and some num

2D Transforms

1. Elements being transformed in 2D are being manipulated on a x and y axis
1. How to rotate
   1. transform: rotate(deg);
      1. vals from 0-360
      1. default of element rotation is 50% 50%
1. 2D scales 1. transform: scale(num); 1. change appeared size of elem 1. Default val = 1 1. .99 &lt;= vals &lt;= .01 elem appear smaller 1. vals >= 1.01 1. transform: scaleX(num); 1. transform: scaleY(num); 1. transform: scale(numX,numY);
1. 2D translate 1. push/pull element w/out changing doc flow. 1. transform: translateX(num); 1. transform: translateY(num); 9. transform: translate(numX,numY);
1. 2D skew 10. Distort elements on hor x/y axis 11. transform: skewX(num); 12. transform: skewY(num); 13. transform: skew(numX,numY);

Combining Transforms

1. Its common to combine skew and translate

Transform Origin

1. to change the default origin position for transform use the transform origin
   1. transform-origin

Perspective

1. Is the vanishing point for each element
1. Single vs Group of elements
   1. for single use perspective val inside transform property → great for transforming one element from one unique perspective
   1. For a group use perspective property on the parent element → great for a group with same perspective/vanishing point
1. Perspective Depth Value 1. Sets a depth value of none to length measurement of some number. 1. The ^ the val = ^ farther away perspective appears → low intensity + low 3D change 1. The lower the val = closer perspective appears → ^ intensity persp + ^ 3D change
1. Perspective Origin 1. transform origin vs perspective origin - the origin of a perspective ids the coords of vanishing point of transform

3D Transforms

1. 3D rotate
1. 3D scale
1. 3D translate
1. 3D skew - cannot skew on z axis
1. 3D shorthand

Transform Style

[top of page](#Reading-14)

## Transitions CSS

1. allow property changes in CSS vals to occur smoothly over some duration by some event (click, focus, active state, element changes).
   1. Transition happen when:
1. Element has a change in state
1. Different styles added to each change in state
   1. To select style for change in state use pseudo classes:
      1. \. className : hover
      1. \. className : focus
      1. \. className : active
      1. \. className : target
1. Transition Properties: 1. transition-property 1. Determines what properties will collectively be altered. Multiple props may be comma separated so as to be applied transition behavior 1. NOT all properties are transition able. Props must have Recognizable values between one another = midpoint. 1. Transition-duration 1. is the time for transition 1. Transition-timing-function 1. is the transition behavior of the change happening and has vals of linear, ease-in, etc 1. Transition-delay 9. stalls transition execution
1. Vendor Prefixes: 1. CSS style that accommodates all browser types

Shorthand Transitions

1. Use transition vals alone in order of transition property to use shorthand
   1. Example from: https://learn.shayhowe.com/advanced-html-css/transitions-animations/
      1. `transition: background .2s linear, border-radius 1s ease-in 1s;`
1. Useful for buttons, “card-flips”

Animations

1. For transitions that require MULTIPLE states better to use Animations
   1. \@keyframes - css rule and includes:
      1. Name
      1. animation breakpoints = frames u
      1. properties intended to animate
   1. Example from: [https://learn.shayhowe.com/advanced-html-css/transitions-animations/](https://learn.shayhowe.com/advanced-html-css/transitions-animations/)
1. Animation Names 1. animation-name property is applied to element that animation is applied to, also the property value for \@keyframes rule 1. animation-duration property is how long the animation will last
1. Animation Duration, Timing, and Delay 1. \animation-name: slide; 1. \animation-duration: xs; 1. \animation-timing-function: ease-in-out; 1. \animation-delay: xs;

Customizing Animations

1. animation iteration - the ability for an animation to be repeat itself
   1. animation-iteration-count - integer/keyword as a val
1. animation direction - lets you control the direction of animation 1. animation-direction - vals are normal, reverse,alternate and alternate-reverse
1. animation play state - animation can be played/paused using: 1. animation-play-state - running/paused val
1. animation fill mode - ids how an element should be styled before/after or before&after animation is run 1. animation-fill-mode - none/forwards/backwards/both

Shorthand Animations - Shorthand - there is a specified order of vals for shorthand

1. Animation-name
1. Animation-duration
1. Animation-timing-function
1. Animation-delay
1. Animation-iteration-count
1. Animation-direction
1. Animation-fill-mode
1. Animation-play-state

## If you wish to exit to the homepage click on the following link to head back to the [homepage](../README.md)

[top of page](#Reading-14)
