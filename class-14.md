[Home](README.md)

# CSS Transforms
- CSS3 comes with new transform ability, including 2d and 3d
- transform syntax 
  ```
      div {
        -webkit-transform: scale(1.5);
        -moz-transform: scale(1.5);
            -o-transform: scale(1.5);
          transform: scale(1.5);
        }
  ```

- transform properties include multiple vendor prefixes to support multiple browsers 


**2d Transform**
- rotate value allows 0 to 360 degrees, +value clockwise, -value anticlockwise
- ```
        .box-1 {
         transform: rotate(20deg);
        }
  ```
- scale: <1 makes element smaller, >1 makes it greater, you can scale in only x or y, scaleX
- ```
     .box-1 {
    transform: scale(.75);
    }
  ```
- translate: moves an element similar to relative positioning, use translateX, translateY or translate(x,y)
- skew, similar to scale and translate
- transforms can be combined 
- ```
        .box-1 {
          transform: rotate(25deg) scale(.75);
        }
   ```
 - default transform origin is the dead center of element, can be changed with transform-origin property   
 - use perspective to change the perspective view of the element

**3d Transforms**
- for changing element on z axis
- rotate
- scale
- translate
- if an transformed element is a child of transformed parent, use transform-style to preserve to transforms on parent

# CSS Transitions and Animations
**Transition**
- transition: an element has a change in state, different styles in each style
- :hover, :focus, :active, and :target pseudo-classes.
- transition related properties: transition-property, transition-duration, transition-timing-function, and transition-delay
-  transition-property property determines exactly what properties will be altered in conjunction with the other transitional properties.
- ```
    .box {
        background: #2db34a;
        border-radius: 6px
        transition-property: background, border-radius;
        transition-duration: 1s;
        transition-timing-function: linear;
    }
    .box:hover {
        background: #ff7b29;
        border-radius: 50%;
    }



- not all properties can be transitioned, they must have a half-way point in value
- transition-duration, use seconds or ms
- transition-timing-function  sets the speed at which a transition will occur
  - linear, easein, easeout, cubic bezier
- transition-delay to set a delay for the transition
- shorthand: `transition: background .2s linear, border-radius 1s ease-in 1s;`
**Animation**
- if more control and multiple transition states are need, use animation
- To set multiple points at which an element should undergo a transition, use the @keyframes rule.
- ```       @keyframes slide {
            0% {
            left: 0;
            top: 0;
            }
            50% {
            left: 244px;
            top: 100px;
            }
            100% {
             left: 488px;
            top: 0;
            }
            }

- once the keyframe has been declared, the animation must be assigned to an element
- ```
        .stage:hover .ball {
        animation-name: slide;
        }

- animation-duration
- animation-timing-function: ease-in-out;
- animation-delay: .5s;
- animation-iteration-count: infinite;
- animation-direction property include normal, reverse, alternate, and alternate-reverse.
- animation-play-state property allows an animation to be played or paused using the running and paused keyword values respectively. 
- shorthand: animation: slide 2s ease-in-out .5s infinite alternate;


