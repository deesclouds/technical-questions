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
- **Use:**
- **Example:**

- [x] Describe what you like and dislike about the CSS preprocessor you have used?
- **Explanation:**
- **Use:**
- **Example:**

- [x] How would you implement a web design comp that uses non-standard fonts?
- **Explanation:**
- **Use:**
- **Example:**

- [x] Explain how a browser determines what elements match a CSS selector.
- **Explanation:**
- **Use:**
- **Example:**

- [x] Describe pseudo-elements and discuss what they are used for.
- **Explanation:**
- **Use:**
- **Example:**

- [x] Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.
- **Explanation:**
- **Use:**
- **Example:**

- [x] What does *{box-sizing: border-box} do? What are its advantages?
- **Explanation:**
- **Use:**
- **Example:**

- [x] What is the CSS display property and can you give a few examples of its use?
- **Explanation:**
- **Use:**
- **Example:**

- [x] What's the difference between inline and inline-block?
- **Explanation:**
- **Use:**
- **Example:**

- [x] What's the difference between a relative, fixed,, absolute and statically positioned element?
- **Explanation:**
- **Use:**
- **Example:**

- [x] What existing CSS frameworks have you used locally, or in production? How would you change/ improve them?
- **Explanation:**
- **Use:**
- **Example:**

- [x] Have you played around with the new CSS Flexbox or Grid specs?
- **Explanation:**
- **Use:**
- **Example:**

- [x] Can you explain the difference between coding a website to be responsive versus using a mobile-first strategy?
- **Explanation:**
- **Use:**
- **Example:**

- [x] How is responsive design different from adaptive design?
- **Explanation:**
- **Use:**
- **Example:**

- [x] Have you ever worked with retina graphics? If so, when and what techniques did you use?
- **Explanation:**
- **Use:**
- **Example:**

- [x] Is there any reason you'd want to use translate() instead of absolute positioning, or vice-versa? And why?
- **Explanation:**
- **Use:**
- **Example:**