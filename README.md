# HTML5 Style Guide

WSA Internal HTML5 Coding Standards Guide

> **Note**: The purpose of these guides are to provide coding standards and conventions for the majority of WSA projects. Some elements might not be required depending on the project specifications. It also assumes you have a basic or no knowledge of Front-End technologies and Responsive Web Design. It is meant to be an on-going collaboration project.


Other Style Guides

  - [CSS & Sass](https://github.com/antonioSF/css)
  - [JavaScript](https://github.com/antonioSF)
  - [Environment / Scaffolding / Bundles / deployments](https://github.com/antonioSF)

## Table of Contents
1. [Document Structure](#document-structure)
	* [Basic structure](#structure-your-document-properly)
	* [The DOCTYPE Declaration](#the-doctype-declaration)
	* [The ```<html>``` Element](#the-html-element)
	* [The ```<head>``` Element](#the-headheader-element)
	* [The ```<body>``` Element](#the-body-element)
	* [Semantic Content Elements](#semantic-content-sectioning-elements)
2. [Responsive Elements](#responsive-images)
	* [The ```<picture>``` Element](#the-picture-element)
	* [The ```<figure>``` Element](#the-figure-element)
3. [Video & Audio](#video--audio)
	* [The ```<video>``` Element](#the-video-element)
	* [The ```<audio>``` Element](#the-audio-element)
4. [Web Forms](#web-forms)
	* [The ```<form>``` Element](#the-form-element)
	* [The ```<input>``` Element](#the-input-element)
	* [Form ```<input>``` types](#form-input-types)
	* [Latest Form Elements](#latest-html5-form-elements-introduced)
5. [Accessibility](#accessibility)
	* [Checklist](#accessibility-checklist)
	* [ARIA](#aria)
6. [Best Practices](#best-practices)

## Document structure
#### Structure your document properly
Use HTML5 semantic block level Elements to define areas of your website.

```html
<!DOCTYPE html>
<html lang="en">
	<head>

		<!-- Character encoding for the document -->
		<meta charset="utf-8">

		<!-- Document Title -->
		<title>Eg. Today's feed | The Feeder</title>

		<!-- Document metadata / CSS external links / favicons -->

	</head>
	<body>

		<!-- Document main header used across all website pages -->
		<header>
			<!-- Eg. logo of website here -->

			<nav>
				<li><a href="#">about</a></li>
				<li><a href="#">services</a></li>
				<li><a href="#">contacts</a></li>
			</nav>
		</header>
		
		<!-- Page main content -->
		<main role="main">

			<!-- A section contains a thematic grouping of content with a heading -->
			<section>
				<!-- Main page Heading -->
				<h1>Eg. Your news feed aggregator page</h1>
			</section>
			
			<!-- Another example of a section -->
			<section>
				<!-- The section always contains a heading -->
				<h2>Eg. News Feed For today</h2>

				<!-- An article containing related individual standalone pieces of content  -->
				<article>
					<h2>Eg. 10 things you didn't knew about HTML</h2>
					<p>Lorem ipsum dolor sit amet...</p>
				</article>

				<!-- Another example of an article -->
				<article>
					<h2>Eg. 10 things you didn't knew about CSS</h2>
					<p>Lorem ipsum dolor sit amet...</p>
				</article>

			</section>

			<!-- The aside is complementary/related to the document's content 
			(it can be nested if directly related to the main content.
			If not, leave it outside the main content) -->
			<aside>
				<h2>Eg. Upcaming News</h2>
				<ul>
					<li><a href="#">Eg. News 1</a></li>
					<li><a href="#">Eg. News 2</a></li>
					<li><a href="#">Eg. News 3</a></li>
				</ul>
			</aside>

		</main>

		<!-- Document main footer used across all website pages -->
		<footer>
			<p>&copy; Copyright 2018. All rights reversed.</p>
		</footer>

		<!-- JavaScript files -->
	</body>
</html>
```
---

**[Back to top](#table-of-contents)**

#### The DOCTYPE Declaration
In HTML, the Document Type Declaration is required at the beginning of a document. Its sole purpose is to prevent a browser from switching into so-called "quirks mode" when rendering a document.

```html
<!-- Case insensitive -->
<!DOCTYPE html>

<!-- Lowercase is valid -->
<!doctype html>
```
> **Note**: The DOCTYPE originates from HTML’s SGML lineage and, in previous levels of HTML, was originally used to refer to a Document Type Definition (DTD). As HTML5 is no longer formally based upon SGML, the DOCTYPE no longer serves this purpose, and thus no longer needs to refer to a DTD. HTML5 defines three modes: quirks mode, limited quirks mode and no quirks mode. To ensure the most standards compliant rendering, it is important to ensure no-quirks mode is used.

##### References
> * [W3C - HTML5 Reference](https://dev.w3.org/html5/html-author/)
> * [MDN web docs - DOCTYPE](https://developer.mozilla.org/pt-PT/docs/Glossary/Doctype)
> * [HTML Standard - Definition of the DOCTYPE](https://html.spec.whatwg.org/multipage/syntax.html#the-doctype)

---

**[Back to top](#table-of-contents)**

#### The ```<html>``` Element
Represents the root (top-level Element) of an HTML document, so it is also referred to as the root Element.All other Elements must be descendants of this Element.

```html
<!-- html with dir global attribute -->
<html dir="rtl">
	<head>
	</head>
	<body>
	</body>
</html>
```
> **Note**: This Element includes the global attributes.
##### References
> * [MDN web docs - HTML Global attributes](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes)
> * [MDN web docs - HTML Root element](https://developer.mozilla.org/pt-PT/docs/Web/HTML/Element/html)

---

**[Back to top](#table-of-contents)**

#### The ```<head>```(header) Element
Provides general information (metadata) about the Document.

```html
<!-- <head> with title and required Document metadata -->
<head>
		<!-- Character encoding for the Document -->
		<meta charset="utf-8">

		<!-- Instruct IE to use its latest rendering engine -->
		<meta http-equiv="x-ua-compatible" content="ie=edge">

		<!-- Viewport for responsive -->
		<meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
		
		<!-- Document Title -->
		<title>Page title less than 55 characters</title>
		
		<!-- Description of the page -->
		<meta name="description" content="description of the web page less than 150 characters">

		<!-- Favicon (put the favicons on the root of the folder) -->
		<link rel="icon" type="image/png" href="/favicon.png">
		<!-- for IE -->
		<!--[if IE]>
			<link rel="shortcut icon" type="image/x-icon" href="/favicon.ico">
		<![endif]-->

		<!-- Link CSS -->
		<link rel="stylesheet" href="/styles/main.css">

</head>
```
> **Note**: This Element includes the global attributes.
##### References
> * [MDN web docs - head: The Document Metadata (Header) Element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/head)

---

**[Back to top](#table-of-contents)**

#### The ```<body>``` Element
Represents the content of an HTML document. There can be only one ```<body>``` Element in a document.

```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="utf-8">
		<title>Document Title</title>
	</head>
	<body>
		<p>This is a paragraph.</p>
	</body>
</html>
```
> **Note**: Avoid adding complex styling to the body Element
##### References
> * [```<body>```: The Document Body Element - HTML | MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/body)

---

**[Back to top](#table-of-contents)**

#### Semantic Content Sectioning Elements
Content sectioning elements allow you to organize the document content into logical pieces. A semantic element is an element that has intrinsic meaning  improving the markup available for documents. That being said, they can seriously improve websites accessibility.

###### The ```<header>``` Element
Represents introductory content, typically a logo and a nav menu, or a title. Sometimes you may have more than one header. At the beginnig of an article or section, for example, if there's a case for it.
```html
<header>
	<h2>Introductory content</h2>
</header>
```
###### The ```<nav>``` Element
Represents a section of a page whose purpose is to provide navigation links like a menu.
```html
<nav>
	<ul>
		<li><a href="#">link 1</a></li>
		<li><a href="#">link 2</a></li>
		<li><a href="#">link 3</a></li>
	</ul>
</nav>
```
###### The ```<h1>–<h6>``` Elements
Represents six levels of section headings. ```<h1>``` is the highest section level and ```<h6>``` is the lowest. If several are used together, they can be grouped into an ```<hgroup>```
```html
<hgroup>
	<h2>First title</h2>
	<h3>Subtitle</h3>
	<h4>another subtitle</h4>
</hgroup>
```
###### The ```<main>``` Element
Represents content unique to the document. Use it only once per page.
```html
<main role="main">
	<p>the main content</p>
</main>
```
###### The ```<section>``` Element
Represents a standalone section — which doesn't have a more specific semantic element to represent it.
```html
<section>
	<h2>A Standalone section</h2>
</section>
```
###### The ```<article>``` Element
Represents an independent self-contained composition in a document (Eg. blog post, etc...).
```html
<article>
	<h2>Article title</h2>
	<p>Article content</p>
</article>
```
###### The ```<aside>``` Element
Represents represents content indirectly related to the main content.
```html
<aside>
	<h2>Aside title</h2>
</aside>
```
###### The ```<footer>``` Element
Represents a footer for its nearest sectioning content or sectioning root element. Tipically, it will be present at the end of the document containing contact info, copyrights, etc. Sometimes you may have more than one footer. At the end of an article, for example, if there's a case for it.
```html
<footer>
	<p>&copy; 2018. All rights reserved.</p>
</footer>
```
###### The ```<address>``` Element
Provides contact information for a person or people, or for an organization.
```html
<address>
	<p>Here you can put contact info eg. <a href="mailto:info@example.com">info@example.com</a></p>
</address>
```
> **Note**: The ```<div>``` Element is a  non-semantic element. It has no effect on the content or layout until styled using CSS. Use it when you can't find an ideal semantic element to group some items together or wrap some content.

```html
<section>
	<!-- use the div element for styling purposes -->
	<div class="wrapper">
		<p>This is a paragraph.</p>
	</div>
</section>
```
##### References
> * [Document and website structure - Learn web development | MDN](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Document_and_website_structure)
> * [HTML elements reference - HTML | MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)

---

**[Back to top](#table-of-contents)**

## Responsive Images
Images often account for most of the downloaded bytes on a web page.
The very first question you should ask yourself is whether an image is, in fact, required to achieve the effect you are after. Good design is simple and will also always yield the best performance. That said, as a rule, you should sacrifice image quality over performance.
With the plethora of devices and different screen sizes and resolutions nowadays, it is imperative to implement responsive images.

* Use the picture element.
* Use relative sizes (%) for images to prevent them from accidentally overflowing the container.
* Use srcset and the x descriptor in the img element.
* Use SVG when possible (logos, icons, etc.).
* Use Font icons.
* Always compress your images (use progressive JPEG, remove metadata, use software as PHOTOSHOP, ImageAlpha, ImageOptim).

#### The ```<picture>``` Element
Serves as a container for zero or more ```<source>``` elements and one ```<img>``` element to provide versions of an image for different display device scenarios.

```html
<!-- use the picture element -->
<picture>
	<source media="(min-width: 64rem)" srcset="images/example-large-screens1x.jpg, images/example-large-screens2x.jpg 2x">
	<source media="(min-width: 40rem)" srcset="images/example-medium-screens1x.jpg, images/example-medium-screens2x.jpg 2x">
	<img src="images/example-small-screens1x.jpg" srcset="images/example-small-screens2x.jpg 2x" alt="Responsive Image Example">
</picture>

<!-- art direction. Give diferent images with diferent sizes based on browser dimensions -->
<img src="images/example-small-screens1x.jpg" sizes="(min-width: 64rem) 50vw, 25vw" srcset="images/example-small-screens2x.jpg 900w, images/example-large-screens1x.jpg 1024w, images/example-large-screens2x.jpg 2000w"  alt="Responsive Image Example 2">
```
#### The ```<figure>``` Element
Represents self-contained content, frequently with a caption (```<figcaption>```), and is typically referenced as a single unit that can be moved away from the main flow of the document without affecting the document's meaning. It can contain images, charts, tables, code snippets, etc.

```html
<!-- using the figure element -->
<figure>
	<picture>
		<source ...>
		<source ...>
		<source ...>
		<img...>
	</picture>

	<figcaption>A Caption</figcaption>
</figure>
```

> **Note**: It is semantically correct to use any of the examples shown above. It is up to you, and the use case to decide which is the best method to implement.

##### References
> * [Responsive Images | Udacity](https://eu.udacity.com/course/responsive-images--ud882)
> * [Image Optimization | Web Fundamentals | Google Developers](https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/image-optimization)
> * [Images | Web Fundamentals | Google Developers](https://developers.google.com/web/fundamentals/design-and-ux/responsive/images)
> * [The picture element | HTML Standard](https://html.spec.whatwg.org/multipage/embedded-content.html#embedded-content)
> * [Getting Started | WebP | Google Developers](https://developers.google.com/speed/webp/docs/using)
> * [```<figure>``` - HTML | MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/figure)

---

**[Back to top](#table-of-contents)**

## Video & Audio
In the early days, native web technologies such as HTML didn't have the ability to embed video and audio on the Web, so proprietary (or plugin-based) technologies like Flash (and later, Silverlight) became popular for handling such content. A few years later the HTML5 specification had such features added, with the ```<video>``` and ```<audio>``` elements.

#### The ```<video>``` Element
It serves to embed video content in a document. This element supports the global attributes (controls, autoplay, loop, preload, etc.)

```html
<!-- simple video with poster image -->
<video src="video.webm" autoplay poster="posterimage.jpg">
Sorry, your browser doesn't support embedded video...
</video>

<!-- Video with different sources for the media format. 
	This allows for supported fallbacks with different browsers -->
<video controls preload="metadata">
	<source src="video.mp4" type="video/mp4">
	<source src="video.webm" type="video/webm">

	<!-- with subtitles -->
	<track kind="subtitles" src="foo.en.vtt" srclang="en" label="English">
  	<track kind="subtitles" src="foo.sv.vtt" srclang="sv" label="Svenska">
	<p>Sorry, your browser doesn't support embedded video...</p>
</video>
```
> **Note**: Use the source element to specify the different media format. The browser will choose the most suitable one.

#### The ```<audio>``` Element
Used to embed sound content in documents. This element supports the global attributes (controls, buffered, loop, preload, volume, etc.).

```html
<!-- Simple audio -->
<audio src="audio.ogg" autoplay>
  Your browser does not support the <code>audio</code> element.
</audio>

<!-- Audio with source -->
<audio controls preload="metadata">
	<source src="audio.mp3" type="video/mp3">
	<source src="audio.ogg" type="video/ogg; codecs=vorbis">
	Your browser does not support the <code>audio</code> element.
</audio>
```

> **Note**: Use the source element to specify the different media format. The browser will choose the most suitable one.

##### References
> * [Video and audio content - Learn web development | MDN](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Video_and_audio_content)
> * [```<video>``` - HTML | MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/video)
> * [The video element | HTML Standard](https://html.spec.whatwg.org/#the-video-element)
> * [Audio and video manipulation - App Center | MDN](https://developer.mozilla.org/en-US/Apps/Fundamentals/Audio_and_video_manipulation)
> * [```<audio>``` - HTML | MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/audio)
> * [The Web Audio API - Web APIs | MDN](https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API)

---

**[Back to top](#table-of-contents)**


## Web Forms
The creation of web forms has always been a complex task, particularly when you have to validate data.  HTML5 introduced new mechanisms for forms: it added new semantic types for the ```<input>``` element and constraint validation to ease the work of checking the form content on the client side.

* Choose the most appropriate input type for your data to simplify input.
* When suitable, offer suggestions as the user types with the datalist element.
* Provide real-time input validation as it might be frustrating for the user otherwise.
* Use placeholders to provide usefull hints about the input type.
* Use high contrast and large input fields for Accessibility reasons.
* Organize your form, it must be concise and understandable.

#### The ```<form>``` Element
Represents a document section that contains interactive controls to submit information to a web server. This element includes the global attributes: action, enctype, method, autocomplete, etc.

```html
<!-- Simple form will send a GET request and first name input is required -->
<form action="" method="GET">
	<label for="js-fname">First name</label>
	<input type="text" id="js-fname" name="fname" required>
</form>

<!-- Form will send a POST request to data.php and accepts files -->
<form action="data.php" method="POST" enctype="multipart/form-data">
	<label for="js-file">Upload files:</label>
	<input type="file" id="js-file" name="file" multiple>
	
	<button type="submit">Submit file</button>
</form>
```

#### The ```<input>``` Element
Used to create interactive controls for web-based forms in order to accept data from the user.
How an ```<input>``` works varies considerably depending on the value of its type attribute.

* Always use labels on form inputs, and ensure they're visible when the field is in focus.
* Use placeholders to provide guidance about what you expect.
* To help the browser auto-complete the form, use established name's for elements and include the autocomplete attribute.
* Always validate inputs with the required attribute as well as the pattern, min, max, step, etc. 

```html
<!-- Label attribute "for" accepts the id of the targeted input. -->
<label for="js-name">Your Full Name:</label>
<input type="text" id="js-name" name="name" placeholder="Marty Mcfly" required autocomplete="name">
<!-- Always use the name attribute on inputs as well as 
	if its required and provide autocomplete parameters. 
	Autocomplete attribute accepts different values as: 
	off, on, email, username, etc. -->

<!-- Always use the right type attribute for the required data -->
<label for="js-email">Email:</label>
<input type="email" id="js-email" name="email" placeholder="marty@gmail.com" autocomplete="email" required>

<!-- Validate inputs with proper attributes -->
<label for="js-tel">Telephone:</label>
<input type="tel" id="js-tel" name="phone" autocomplete="tel" placeholder="910000000" minlength="9" maxlength="15">

<!-- Offer suggestions as the user types with the datalist element  -->
<label for="js-city">City:</label>
<input type="text" id="js-city" type="text" list="cities" name="city" placeholder="Lisbon">
<datalist id="cities">
	<option value="Lisbon"></option>
	<option value="Oporto"></option>
	<option value="New York"></option>
	<option value="London"></option>
	<option value="Sydney"></option>
</datalist>

<!-- Use the pattern attribute (regular expressions) to validate input  -->
<label for="js-postal-code">Postal code:</label>
<input type="text" id="js-postal-code" pattern="[0-9]{4}[\-]?[0-9]{3}" autocomplete="postal-code">
```
#### Form ```<input>``` types
* [button](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/button): A push button with no default behavior.
* [checkbox](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/checkbox): A check box allowing single values to be selected/deselected.
* [color](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/color): A control for specifying a color. A color picker's UI has no required features other than accepting simple colors as text.
* [date](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/date): A control for entering a date (year, month, and day, with no time).
* [datetime-local](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/datetime-local): A control for entering a date and time, with no time zone.
* [email](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/email): A field for editing an e-mail address.
* [file](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/file): A control that lets the user select a file. Use the accept attribute to define the types of files that the control can select.
* [hidden](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/hidden): A control that is not displayed but whose value is submitted to the server.
* [image](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/image): A graphical submit button. You must use the src attribute to define the source of the image and the alt attribute to define alternative text. You can use the height and width attributes to define the size of the image in pixels.
* [month](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/month): A control for entering a month and year, with no time zone.
* [number](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/number): A control for entering a number.
* [password](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/password): A single-line text field whose value is obscured. Use the maxlength and minlength attributes to specify the maximum length of the value that can be entered.
* [radio](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/radio): A radio button, allowing a single value to be selected out of multiple choices.
* [range](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/range): A control for entering a number whose exact value is not important.
* [reset](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/reset): A button that resets the contents of the form to default values.
* [search](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/search): A single-line text field for entering search strings. Line-breaks are automatically removed from the input value.
* [submit](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/submit): A button that submits the form.
* [tel](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/tel): A control for entering a telephone number.
* [text](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/text): A single-line text field. Line-breaks are automatically removed from the input value.
* [time](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/time): A control for entering a time value with no time zone.
* [url](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/url): A field for entering a URL.
* [week](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/week) A control for entering a date consisting of a week-year number and a week number with no time zone.

#### Latest HTML5 Form elements introduced
* [```<datalist>```](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/datalist): The HTML Datalist element contains a set of ```<option>``` elements that represent the values available for other controls.
* [```<output>```](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/output): The HTML Output element is a container element into which a site or app can inject the results of a calculation or the outcome of a user action.

> **Note**: Before submitting any data to the server, do client-side form validation with JavaScript: use the [Constraint Validation API](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5/Constraint_validation) for this purpose.

##### References
> * [Create Amazing Forms | Web Fundamentals | Google Developers](https://developers.google.com/web/fundamentals/design-and-ux/input/forms/)
> * [HTML forms - Learn web development | MDN](https://developer.mozilla.org/en-US/docs/Learn/HTML/Forms)
> * [```<form>``` - HTML | MDN](https://developer.mozilla.org/pt-PT/docs/Web/HTML/Element/form)
> * [```<input>``` - HTML | MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input)
> * [HTML5 Pattern](http://html5pattern.com/)
> * [Form data validation - Learn web development | MDN](https://developer.mozilla.org/en-US/docs/Learn/HTML/Forms/Form_validation)
> * [Client-Side Form Validation with HTML5 — SitePoint](https://www.sitepoint.com/client-side-form-validation-html5/)
> * [Constraint validation - Web developer guides | MDN](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5/Constraint_validation)

---

**[Back to top](#table-of-contents)**


## Accessibility
Accessibility means that a website's content is available, and its functionality can be operated, by literally anyone. It ranges from a user's slow network and device capabilities to users with physical impairments. 
As Web Applications become increasingly powerful enabling users to improve their daily habits, developers have an amazing power. That said, with power cames great responsability. Accessibility concerns must be a priority while developing new Web Applications. 
[WCAG](https://www.w3.org/TR/WCAG20/) is organized around four principles often called by the acronym POUR:

* **Perceivable**: Can users perceive the content? This helps us keep in mind that just because something is perceivable with one sense, such as sight, that doesn't mean that all users can perceive it.
* **Operable**: Can users use UI components and navigate the content? For example, something that requires a hover interaction cannot be operated by someone who can't use a mouse or touch screen.
* **Understandable**: Can users understand the content? Can users understand the interface and is it consistent enough to avoid confusion?
* **Robust**: Can the content be consumed by a wide variety of user agents (browsers)? Does it work with assistive technology?

#### Accessibility Checklist
**With that in mind, you should follow the below list while developing a website:**

* Organize your content and keep it logical and concise (navigation, etc.).

* Implement [skip navigation](https://webaim.org/techniques/skipnav/) if necessary.

* Provide high contrast and good font sizes from low-vision users to read.

* Have a specified foreground and background color.

* Minize the use of fonts and variants, keep design clean and performance optimal.

* Blocks of text over one sentence in length are no more than 80 characters wide.

* Do not justify text.

* Provide HTML5 Semantic Elements that screen readers can understand.
```html

<!-- bad -->
<div class="main">
</div>

<!-- good -->
<main role="main">
</main> 
```

* Use HTML5 native elements when possible.
```html

<!-- bad -->
<span class="button">click me</span>

<!-- good -->
<button>click me</button>

<a href="#">click me</a>
```

* Use [tabindex](https://developers.google.com/web/fundamentals/accessibility/focus/using-tabindex) when you'll need to modify the tab order.
```html

<!-- bad (avoid adding other value greater then 0 since its an anti-pattern) -->
<button tabindex="5">Press Tab to Focus Me first!</button>

<!-- good -->
<span tabindex="0">Press Tab to Focus Me!</span>
```

* Use the ```alt``` attribute to describe important content images. Otherwise leave the ```alt```empty.
```html

<!-- bad -->
<image src="my-name.jpg">

<!-- good -->
<image src="my-name.jpg" alt="My Name">
``` 

* Form buttons have a descriptive value.

* Form inputs have associated text labels.
```html

<!-- bad -->
<input type="text" name="fname" placeholder="Marty">

<!-- good -->
<label for="fname">First name:</label>
<input type="text" id="fname" name="fname" placeholder="Marty">
```

* Keep interactive elements focusable.

* All page functionality is available using the keyboard.

* No page content flashes more than 3 times per second or it may cause seizures.

* Compress and optimize images and resources (CSS, JavaScript).

* Provide support for different browsers and, if requested, to legacy browsers (IE).

* Always check your website against the [WebAIM checklist](https://webaim.org/standards/wcag/checklist).

#### ARIA
Accessible Rich Internet Applications (ARIA)  is a set of attributes that define ways to make Web content and Web applications. ARIA is a set of special accessibility attributes which can be added to any markup, but is especially suited to HTML. 
Adding an ARIA role overrides the native role semantics in the accessibility tree which is reported via the accessibility API, and therefore ARIA indirectly affects what is reported to a screen reader or other assistive technology. The ```role``` attribute defines a specific role for type of object (such as an article, alert, slider or a button).

* If you can't use an HTML5 element, implement ARIA on the element so it becames accessible.

* Do not change native semantics, unless you really have to.
```html

<!-- bad -->
<h2 role="tab">tab</h2>

<!-- good -->
<div role="tab">tab</div>
```

* All interactive ARIA controls must be usable with the keyboard.
```html

<!--  this element must be focusable and the 
	user has to be able to interact using the keyboard (tab/enter/space) -->
<span role="button">Click me!</span>
```

* Do not use role="presentation" or aria-hidden="true" on a visible focusable element.

```html

<!-- bad -->
<button role="presentation">press me</button>

<!-- bad -->
<button aria-hidden="true">press me</button>
```

* Use ```aria-labelledby``` and ```aria-describedby``` properly
```html

<!--- a tooltip example   -->
<div aria-describedby="awesome-tooltip">text</div>
     
<div id="awesome-tooltip" role="tooltip">Assistive text tooltip</div>  

<!--- an input with multiple references --> 
<label id="l1" for="f3">label text</label>
<input type="text" id="f3" aria-labelledby="l1 l2">
<p>other content</p>
<span tabindex="-1" id="l2">more label text</span>
```

##### References
> * [ARIA - Accessibility | MDN](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA)
> * [Web Accessibility | Udacity](https://eu.udacity.com/course/web-accessibility--ud891)
> * [Accessibility | Web Fundamentals | Google Developers](https://developers.google.com/web/fundamentals/accessibility/)
> * [Web Accessibility | Udacity](https://eu.udacity.com/course/web-accessibility--ud891)
> * [Using tabindex | Web Fundamentals | Google Developers](https://developers.google.com/web/fundamentals/accessibility/focus/using-tabindex)
> * [WebAIM: "Skip Navigation" Links](https://webaim.org/techniques/skipnav/)
> * [WebAIM: WebAIM's WCAG 2.0 Checklist - for HTML documents](https://webaim.org/standards/wcag/checklist)
> * [Using ARIAm | W3C](https://w3c.github.io/using-aria/)

---

**[Back to top](#table-of-contents)**

## Best Practices
The goal is not to restrict you in any way, but to outline the coding standards and best practices in building HTML documents. With this, as long as your project meets the outlined criteria, your users should have a positive experience accessing your content.

* Reduce the Number of DOM Elements.

* Clean up HTML comments.

* Minify the HTML document.

* Meta data is included and appropriate.

* Unless there's a very explicit reason for it, always make JavaScript and CSS External. 

* Put Stylesheets at the top.

* Put Scripts at the Bottom.

* Minize the use of fonts and variants.

* Webfont sizes don't exceed 2 MB (all variants included).

* Minimize HTTP Requests (combine CSS files as well as JavaScript files): refer to [HTTP/2](https://http2.github.io/faq/).

* Avoid Redirects.

* The fastest and best optimized resource is the one not sent.

* Aim at 1MB per page weight.

* HTML5 Semantic Elements are used appropriately.

* Website meets appropriate level of WCAG compliance.

* Reduce to number of images.

* Optimise and Compress images.

* Responsive images have been implemented.

* Colour contrast tested.

* Forms have logical layout.

* Associated label for all form controls.

* Forms have apropriate client-side and real-time validation.

* Always Test your website on several different browsers and devices.

* Always Test your website with different networks (regular 3G, slow 3G, etc).

* All pages need to be tested with the W3C validator.

* Clean up your code with [DirtyMarkup Formatter](https://www.10bestdesign.com/dirtymarkup/).

* Website passed the [WSA Checklist](http://wsa.pt/checklist/).

---

**[Back to top](#table-of-contents)**

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

---

**[Back to top](#table-of-contents)**

## License

This project is licensed under the MIT License - see the [LICENSE](https://github.com/antonioSF/html/blob/master/LICENSE) file for details
