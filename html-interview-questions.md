# HTML - Technical Interview Questions

## Questions:

- [x] What does a doctype do?
- **Explantaion:** A doctype tells our browser what version of HTML we should use to render a HTML document.
- **Use:** Every HTML document starts with a doctype declaration.
- **Example:** The latest version of HTML is HTML 5, and we should add the doctype for that version on the first line of our index.html file with <!DOCTYPE html>.

- [x] How do you serve a page with content in multiple languages?
- **Explanation:** A page can be served content in a different language by modifying the lang attribute, metadata and content-language http header.
- **Use:** There are two ways a page can be served content in multiple languages. One way is by modifying the lang attribute within the html document. Another way is by adding the google translate button to the page.
- **Example:** To change the lang attribute within the opening html tag we can set the language to english <html lang="en">. Then adding different languages within the html document within a span tag <span lang="fr">Bonjour</span>. To add a google translate button the page is by adding a div element, adding the google translate api reference and then add the Javascript function. <div id="google_translate_element"></div> , <script type="text/javascript" src="//translate.google.com/translate_a/element.js?cb=googleTranslateElementInit"></script> , <script type="text/javascript"> function googleTranslateElementInit() { new google.translate.TranslateElement ({pageLanguage: 'en'}, google_translate_element'); 
}</script>

- [x] What kind of things must you be wary of when designing or developing for multilingual sites?
- **Explanation:**
- **Use:**
- **Example:**

- [x] What are data- attributes good for?
- **Explanation:**
- **Use:**
- **Example:**

- [x] Consider HTML5 as an open web platform. What are the building blocks of HTML5?
- **Explanation:**
- **Use:**
- **Example:**

- [x] Describe the difference between a cookie, sessionStorage and local Storage.
- **Explanation:**
- **Use:**
- **Example:**

- [x] Describe the difference between <script>, <script async> and <script defer>.
- **Explanation:**
- **Use:**
- **Example:**

- [x] Why is it generally a good idea to position CSS <link>s between <head></head> and JS <script>s just before </body>? Do you know any exceptions?
- **Explanation:**
- **Use:**
- **Example:**

- [x] What is progressive rendering?
- **Explanation:**
- **Use:**
- **Example:**

- [x] Why would you use a srcset attribute in an image tag? Explain the process the browser uses when evaluating the content of this attribute.
- **Explanation:**
- **Use:**
- **Example:**

- [x] Have you used different HTML templating languages before?
- **Explanation:**
- **Use:**
- **Example:**