# HTML - Technical Interview Questions

## Questions:

- [x] What does a doctype do?

- **Explanation:** A doctype tells our browser what version of HTML we should use to render a HTML document.

- **Use:** Every HTML document starts with a doctype declaration.

- **Example:** The latest version of HTML is HTML 5, and we should add the doctype for that version on the first line of our index.html file with <!DOCTYPE html>.

- [x] How do you serve a page with content in multiple languages?

- **Explanation:** A page can be served content in a different language by modifying the lang attribute, metadata and content-language http header.

- **Use:** There are two ways a page can be served content in multiple languages. One way is by modifying the lang attribute within the html document. Another way is by adding the google translate button to the page.

- **Example:** To change the lang attribute within the opening html tag we can set the language to english <html lang="en">. Then adding different languages within the html document within a span tag <span lang="fr">Bonjour</span>. To add a google translate button the page is by adding a div element, adding the google translate api reference and then add the Javascript function. <div id="google_translate_element"></div> , <script type="text/javascript" src="//translate.google.com/translate_a/element.js?cb=googleTranslateElementInit"></script> , <script type="text/javascript"> function googleTranslateElementInit() { new google.translate.TranslateElement ({pageLanguage: 'en'}, google_translate_element'); 
}</script>

- [x] What kind of things must you be wary of when designing or developing for multilingual sites?

- **Explanation:** Using a default language based on location of the user, color choices, having set character counts, formatting dates, currencies  and the direction languages are read.

- **Use:**  Providing a simple way for a user to change their location and language. Having an understanding of how colors are perceived in other cultures. Using template strings with parameter substitution for each language. Language reading direction. 

- **Example:** Users may be located in a location and are not able to speak the native language fluently so a user should be provided with an easy way of changing the language and origin if needed. Some cultures like China perceive the color red as good luck while in the US the color red can be perceived as danger. Some parts of the world have different formatting for currencies, dates (ie. June 05, 2022 vs 05 June 2022). Using template strings for each language would avoid breaking if there's a different order for how the sentences are formed. Languages like Japanese and Arabic are read from right to left while in the English language words are read from left to right. 

- [x] What are data- attributes good for?

- **Explanation:** configure elements to our needs

- **Use:** assigning values to properties within our code by using their values.

- **Example:** library database, database pulling json api

- [x] Consider HTML5 as an open web platform. What are the building blocks of HTML5?

- **Explanation:** semantics, connectivity, offline and storage, multimedia, 2d/3d graphics & effects, performance and integration, device access, styling

- **Use:** to allow more user to have access to your website.

- **Example:** https://motherfuckingwebsite.com it loads lightweight, loads fast, responsive and has the information that a user needs.

- [x] Describe the difference between a cookie, sessionStorage and local Storage.

- **Explanation:** local storage stores data on the client side device until the user clears it and never touches the server. sessionStorage stores data until browser is closed. cookies is data stored on the server.

- **Use:** cookies used by web servers to identify and track users as they navigate different pages on a site and identifies users when they return. sessionStorage would be a great use for maintaining data safety localStorage would be used to play games in the browser. 

- **Example:** a real-world example of localStorage is Wordle.
sessionStorage would be used on a public device or guest account. cookie use would be a user not having to login again when returning to a website. 


- [x] Describe the difference between <script>, <script async> and <script defer>.
- **Explanation:** <script> is tag used to insert a Javascript file to a page.
 <script async> runs in the background and runs when ready. 
 <script defer> only executes.

- **Use:** we use the script tag when we need to inject js. 
<script async> is used when need to wait for something to respond and bring back information. script def is used when we need the whole DOM

- **Example:** script used for adding animations and behavior.
<script async> tag we use for google analytics or api
<script defer> if we want the content to show up immediately 

- [x] Why is it generally a good idea to position CSS <link>s between <head></head> and JS <script>s just before </body>? Do you know any exceptions?

- **Explanation:** so that the html and css renders first and the javascript then can render the DOM.
The exception would be if we worked Amazon and would lose millions of dollars on slow page load we would remove the body and head tags since they are optional.

- **Use:** to provide a great user experience and a faster page load to also provide a lower bounce rate. 

- **Example:** google site 

- [x] What is progressive rendering?

- **Explanation:** technique used to improve the performance of a site to render content fast

- **Use:** used to improved load times

- **Example:** Prioritizing content we would like rendered with the least amount of styling, content and scripts to display them as quickly as possible like using Vue or React. 

- [x] Why would you use a srcset attribute in an image tag?
 Explain the process the browser uses when evaluating the content of this attribute.

- **Explanation:** scrset is how we can display various image sizing  based on the size of the user's display and resolution.
 The browser chooses the best quality graphic to display to the user. 

- **Use:** we would use this to choose the best quality image to display to the user based on what screen and device they are using.

- **Example:** older displays & smaller devices would be served smaller images while devices with retnia displays and larger devices would have larger and higher quality images

- [x] Have you used different HTML templating languages before?

- **Explanation:** Yes. 

- **Use:** to escaping content and helpful filters for manipulating data

- **Example:** I've use Handlebars and EJS.