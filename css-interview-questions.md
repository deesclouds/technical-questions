# CSS - Technical Interview Questions

## Questions:

- [x] What is a CSS selector specificity and how does it work?
- **Explanation:** A CSS selector specificity determines which CSS elements are applied based on the specificity level of the individual selectors.
- **Use:** When an element's styling conflicts, specificity is taken into account and helps control which styles are applied to the HTML element. 
- **Example:** An example would be applying a higher specificity like another class or ID to target an individual element.

- [x] What's the difference between "resetting" and normalizing CSS? Which would you choose, and why?
- **Explanation:** Resetting is meant to strip all default browser styling on elements. Normalizing preserves useful default settings.
- **Use:** I would use reset when customizing site and normalize when I want the default styles. 
- **Example:** I would use reset when making a custom design and normalize when I want the use the default styles. 

- [x] Describe floats and how they work.
- **Explanation:** Float is a positioning property.
- **Use:** Removing an element from the flow of the page.
- **Example:** An example would be if I would float text around an image.

- [x] Describe z-index and how stacking context is formed.
- **Explanation:** z-index controls the vertical stacking order of elements that overlap. z-index only affects elements that have a position value which is not static.
- **Use:** for overlaying elements or images on a page.
- **Example:** I would use z-index to stack images on top of each other z-index 2 would be on top of an element with z-index 1.

- [x] Describe BFC (Block Formatting Context) and how it works.
- **Explanation:**  to display things nicely within a container.
- **Use:** one use would be the scrollbar
- **Example:** News article when we would want text to wrap around an image.

- [x] What are the various clearing techniques and which is appropriate for what context? {come back to this one}
- **Explanation:** clearfix would automatically clear the child element. overflow used when expanding over what's spilling out the container. clear property used to not allow an element to float on the page.
- **Use:** clear would be used we want an element to stay put while floating another element. clearfix we would use to if align an element within a container. overflow we would use to fix an element that is spilling out a div. 
- **Example:** use clear when we want text to not float over some text, clearfix moves the box to make room for our image, overflow used to make room for an image within the container

- [x] Explain CSS sprites, and how you would implement them on a page or site.
- **Explanation:** Allows several images to be rendered within one image.
- **Use:** To allow less http requests 
- **Example:** gmail app icons uses css sprites

- [x] How would you approach fixing browser-specific styling issues?
- **Explanation:** Using a separate stylesheet for specific browsers, adding vendor prefixes to our code, Bootstrap, normalize or reset for our css, or postcss.
- **Use:** If our design breaks within a specific browser we can implement additional solutions targeting that specific browser. 
- **Example:** When my personal site wasn't rendering properly in safari I used webkit- within my css stylesheet. 

- [x] How do you serve your pages for feature-constrained browsers? What techniques/processes do you use?
- **Explanation:** Graceful degradation - the practice of building an application for modern browsers while ensuring it remains functional in older browsers.
Progressive enhancement - practice of building an application for a base of user experience, but adding functional enhancements when a browser supports it. 

Techniques we can use are caniuse.com to check feature support, autoprefixers for automatic vendor prefix insertion, using Modernizr feature detection and using the @support css feature queries.
- **Use:** we would use these techniques to make sure users with a slower network or older devices, have the ability to still access our applications.
- **Example:** how when apple updates their ios older devices are still able to use the new ios updates as well.

- [x] What are the different ways to visually hide content (and make it available only for screen readers)?
- **Explanation:** WAI-ARIA tag, display:none, or visibility: hidden, width: 0 height 0;
- **Use:** to allow users who use a screen reader for example to have an easier time navigating the web
- **Example:** an example would be adding an ARIA tag to a label within a form so the user knows where they are when filling out a form

- [x] Have you ever used a grid system, and if so, what do you prefer?
- **Explanation:** Yes
- **Use:** CSS grid is better than flex 
- **Example:** Would use this when building grid layouts

- [x] Have you used or implemented media queries or mobile specific layouts/CSS?
- **Explanation:** Yes 
- **Use:** To condense a site for smaller screens
- **Example:** For example min-width & max-width, and implementing a hamburger menu to take up less space on mobile devices.

- [x] Are you familiar with styling SVG?
- **Explanation:** Yes
- **Use:** I use inline styling changing the style of the icons on my site.
- **Example:** Font awesome uses svgs and can change the colors for the fill stroke, fill-opacity, stroke-opacity and sizing for the height, width properties as well.

- [x] Can you give an example of an @media property other than screen?
- **Explanation:** Yes. All, print & speech.
- **Use:** All for all media type devices, print for printers, speech for screenreaders
- **Example:** we can set the media property to print out a site in black.

@media print{
    body {
        color: black;
    }
}

- [x] What are some of the "gotchas" for writing efficient CSS?
- **Explanation:** margin collapse affecting block formatting, 
- **Use:** Making sure to be specific with our css stylings so that things go as we expect them to.
- **Example:** using a universal selector will style everything and lead to more work when determining why a certain style is not rendering properly

- [x] What are the advantages/disadvantages of using CSS preprocessor?
- **Explanation:** 
Advantages:

CSS is made more maintainable.
Easy to write nested selectors.
Variables for consistent theming. Can share theme files across different projects.
Mixins to generate repeated CSS.
Sass features like loops, lists, and maps can make configuration easier and less verbose.
Splitting your code into multiple files. CSS files can be split up too but doing so will require an HTTP request to download each CSS file.

Disadvantages:

Requires tools for preprocessing. Re-compilation time can be slow.
Not writing currently and potentially usable CSS. For example, by using something like postcss-loader with webpack, you can write potentially future-compatible CSS, allowing you to use things like CSS variables instead of Sass variables. Thus, you're learning new skills that could pay off if/when they become standardized.


- [x] Describe what you like and dislike about the CSS preprocessor you have used?
- **Explanation:**
Likes are: CSS is more maintainable, Easy to nest selectors, 
Mostly the advantages mentioned above.
Less is written in JavaScript, which plays well with Node.
Dislikes:

I use Sass via node-sass, which is a binding for LibSass written in C++. I have to frequently recompile it when switching between node versions.
In Less, variable names are prefixed with @, which can be confused with native CSS keywords like @media, @import and @font-face rule.
- **Use:** 
Can be used to make computational logic within CSS
- **Example:**
For example like if, else, statements or giving our colors variables within our CSS stylesheet.

- [x] How would you implement a web design comprehensive that uses non-standard fonts?
- **Explanation:**

- **Use:**
Use @font-face and define font-family for different font-weights to implement custom fonts.
- **Example:**
Using beautiful typography created 

- [x] Explain how a browser determines what elements match a CSS selector.
- **Explanation:**
Browsers filter out elements in the DOM according to the key selector and traverse up its parent elements to determine matches. The shorter the length of the selector chain, the faster the browser can determine if that element matches the selector.
- **Use:**

- **Example:**

- [x] Describe pseudo-elements and discuss what they are used for.

- **Explanation:**
A CSS pseudo-element is a keyword added to a selector that lets you style a specific part of the selected element(s). 

- **Use:**
They can be used for decoration (:first-line, :first-letter) or adding elements to the markup (combined with content: ...) without having to modify the markup (:before, :after).
- **Example:**
:first-line and :first-letter can be used to decorate text.
Used in the .clearfix hack as shown above to add a zero-space element with clear: both.
Triangular arrows in tooltips use :before and :after. Encourages separation of concerns because the triangle is considered part of styling and not really the DOM.

- [x] Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.
- **Explanation:**
The box model describes how elements are visually formatted on the webpage.
The content is the object within the box.
The padding is the tissue paper that surrounds the content within the box.
The margin controls the space around the box.
- **Use:**
We use the box model to create borders and change the sizing of a box element on the web page.
- **Example:**
We can target the border for an image and calculate how much space it takes up. We can change the border for the image and make it thicker, we can make the image wider, or taller based on the dimensions of the image.


- [x] What does *{box-sizing: border-box} do? What are its advantages?
- **Explanation:**
border-box changes the width and height of the elements that includes the border and padding with the content
- **Use:**
taking account of the padding and border helps to image in the content without throwing off the calculations
- **Example:**
using border box would make it easier to calculated the content and the borders at the same time. 

- [x] What is the CSS display property and can you give a few examples of its use?
- **Explanation:**
Is a property that we use to control how an element is displayed
- **Use:**
none, block, inline, inline-block, flex, grid, table, table-row, table-cell, list-item
- **Example:**
We can use the CSS display property to target how an element behave like a block element which consumes the whole line in the block direction horizontally.

- [x] What's the difference between inline and inline-block?
- **Explanation:**
Inline blocks adds spaces between its self and another element while inline does not add space between itself and another element. Block elements take up the whole available space.
- **Use:**
Inline spans 
Inline block would be used for long forms of written content
- **Example:**
When we insert an img within out html, we can't really change the height or width because it's default is inline. When we place the img within a container we can then change the width and height sizing because then the img has been converted into inline-block.

- [x] What's the difference between a relative, fixed, absolute and statically positioned element?
- **Explanation:**
relative - when it is relative to the parent's container
fixed -  doesn't move when scrolled
absolute - taken out of the normal flow
statically - normal flow
- **Use:**
to customize how our elements are moved within the webpage
- **Example:**
to have a fixed navbar within a webpage so users can always have access to the navbar while scrolling

- [x] What existing CSS frameworks have you used locally, or in production? How would you change/ improve them?
- **Explanation:**
Yes, I've used Bootstrap. 
What I would improve is being able to easily customize the theme designs.
- **Use:**
I would Bootstrap to quickly style a website.
- **Example:**
Instagram

- [x] Have you played around with the new CSS Flexbox or Grid specs?
- **Explanation:**
Yes. Flexbox for using columns or rows while Grid is meant for using both columns and rows.
- **Use:**
Grid for structure. Flexbox for flow.
- **Example:**
Flexbox for twitter on m and Grid for a product page. 

- [x] Can you explain the difference between coding a website to be responsive versus using a mobile-first strategy?
- **Explanation:**
Responsive is starting off big and then condensing it.

Mobile first strategy  is starting off with a more simplified design and then gets bigger.
- **Use:**
Social media sites using mobile first since they are accessed most strategy. 
- **Example:**


- [x] How is responsive design different from adaptive design?
- **Explanation:**
Responsive design changes the layout & appearance based on screen size of the device used to access the site. 

Adaptive design requires the creation of different layouts for each device the website will be based on.
- **Use:**
Responsive design = less work for UX designer to create & works with developer hand in hand

Adaptive design = more work + more optimization for every device.
- **Example:**
Responsive works best for larger sites being done from scratch. 

Adaptive designs work best for smaller sites being refreshed.

- [x] Have you ever worked with retina graphics? If so, when and what techniques did you use?
- **Explanation:**
Yes. Retina graphics is a marketing term made up by Apple for high resolution displays. 
- **Use:**
Using jQuery to pin point images and half their widths  and height declarations, media queries, svgs. 

- **Example:**
Let’s say you had three major breakpoints in a design. This design also had a large background graphic and you wanted it looking it’s best on any screen (retina or not) and not waste any bandwidth. You’d set up 6 media queries, one for each breakpoint and one for each one of those breakpoints on retina. Then you’d override the background image all the way down.

- [x] Is there any reason you'd want to use translate() instead of absolute positioning, or vice-versa? And why?
- **Explanation:**
 translate() is more efficient and will result in shorter paint times for smoother animations.

absolute positioning triggers the repaint or DOM reflow. 

transform causes the browser to create a GPU layer for the element but changing absolute positioning properties uses the CPU

- **Use:**
use for changing the placement of an image for animations

- **Example:**
Using translate would give a better performance like a cursor hover using javascript can perform translate. 