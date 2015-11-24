# responsify.js

`A jquery library that makes images truly responsive, without sacrificing anyone's face :D`

When we use full screen images or full width images on web design, often in some edge cases, a group shot with end up being cut off on people's faces, a nice photography following "rule of third" will end up with on object in view. Responsive images face the challenge of how to keep the neccessary objects/area in view? This jquery plugin is here to help.

### Demo

[http://responsifyjs.space/](http://responsifyjs.space/)

The project is currently under development. I will add more details soon!

### What it does

responsify.js does the following:
 1. it allows you define a hot area on an image using `data-focus-xxx` tag
 2. it takes the hot area info from the image, calcuate the image's container's size, resize and position the image in the right place, making sure the hot area is always in view and in the best position possible.

### How to use
 1. add focus area data to the img tag, `data-focus-left` is the focus area's left position comparing to the image's full width, in decimal. For example if the full width is 300, the focus area's left is 90, then the `data-focus-left` should be 90/300 = 0.3
 
 ```
    <img src="image.png" alt="" 
    data-focus-left=".15" data-focus-top=".12" data-focus-right=".79" data-focus-bottom=".66" />
 ```
 2. embed the responsify.js in your html
 
 ``` 
    <script src="js/responsify.js"></script>
 ``` 
 3. call responsify function when window object is loaded
 
 ``` 
    $(window).load(function() {
      $('img').responsify();
    });
 ```
 4. (optional) call responsify function again when the window is being resized
 
  ```
    $(window).resize(function(){
      $('img').responsify();
    })
  ```
  

###Contact
* Follow [@DesignJokes](http://twitter.com/DesignJokes) on Twitter
* Email <zhangwenting111@gmail.com>
* Visit [wentin.co](http://wentin.co)
