# Responsify.js

`A jquery plugin that makes images truly responsive, without sacrificing anyone's face :D`

When images are used in a responsive container on web design, because of the container can change to any width:height ratio, a group shot could end up being cut off on people's faces, a nice photograph following "rule of third" could end up with no object in view. Responsive images face the challenge of how to keep the focused objects/area in view, this jquery plugin is here to solve the problem.

### Download
* [responsify.js](https://raw.githubusercontent.com/wentin/ResponsifyJS/master/responsify.js)
* [responsify.min.js](https://raw.githubusercontent.com/wentin/ResponsifyJS/master/responsify.min.js)

### Demo

[https://responsify.typedetail.com](https://responsify.typedetail.com)

### App

[https://responsify.typedetail.com/app](https://responsify.typedetail.com/app)

Use this interactive web app to generate the focus area data

### What it does

Responsify.js does the following:
 1. It allows you define a focus area on an image using `data-focus-xxx` tag
 2. It takes in the focus area data from the image, calcuate the image's container's size, resize and position the image accordingly, make sure the focus area is always in view and in the best position possible.

* Responsive image **with** responsify.js

![with-s](https://cloud.githubusercontent.com/assets/2474904/11459461/dccd59b6-96a4-11e5-81c6-5b16c7d30a23.gif) [play it yourself](http://wentin.github.io/ResponsifyJS/comparison/with-responsify-js/)

* Responsive image **without** responsify.js

![without-s](https://cloud.githubusercontent.com/assets/2474904/11459460/dccd53bc-96a4-11e5-8a33-bea161ef60a9.gif) [play it yourself](http://wentin.github.io/ResponsifyJS/comparison/without-responsify-js/)

### How to use
 1. Use this interactive web app to generate the focus area data [http://responsifyjs.space/app/](http://responsifyjs.space/app/)
 
 ```
    <img src="image.png" alt="" 
    data-focus-left=".30" data-focus-top=".12" data-focus-right=".79" data-focus-bottom=".66" />
 ```
`data-focus-left` is the focus area's left position comparing to the image's full width, in decimal. For example, if the full width is 300px, the focus area's left is 90, then the `data-focus-left` should be 90/300 = `0.3`. Same logic applies to other three data attributes.

 2. Embed the responsify.js in the html
 
 ``` 
    <script src="responsify.js"></script>
 ``` 
 3. Call responsify function when window object is loaded
 
 ``` 
    $(window).load(function() {
      $('img').responsify();
    });
 ```
 4. Call responsify function again when the window is being resized (optional)
 
  ```
    $(window).resize(function(){
      $('img').responsify();
    })
  ```
  

###Contact Me
* Follow [@DesignJokes](http://twitter.com/DesignJokes) on Twitter
* Email <zhangwenting111@gmail.com>

###Other Project by Wentin
* [Type Detail](http://typedetail.com/)
* [underline.js](https://github.com/wentin/underlineJS)
