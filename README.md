# HTML5 Style Guide

WSA Internal HTML5 Coding Standards Guide

> **Note**: The purpose of these guides are to provide coding standards and conventions for the majority of WSA projects. Some elements might not be required depending on the project specifications. It also assumes you have a basic knowledge of Front-End technologies and Responsive Web Design.


Other Style Guides

  - [CSS & Sass](https://github.com/antonioSF)
  - [JavaScript](https://github.com/antonioSF)
  - [Environment / Scaffolding / Bundles / deployments](https://github.com/antonioSF)

## Table of Contents
1. [DOCUMENT STRUCTURE](#document-structure)
	* 1.1 [Basic structure](#structure-your-document-properly)
	* 1.2 [The DOCTYPE Declaration](#the-doctype-declaration)
	* 1.3 [The ```<html>``` Element](#the-html-element)
	* 1.4 [The ```<head>``` Element](#the-headheader-element)
	* 1.5 [The ```<body>``` Element](#the-body-element)
	* 1.6 [Semantic Content Elements](#semantic-content-sectioning-elements)
2. [RESPONSIVE IMAGES](#responsive-images)
3. [VIDEO & AUDIO](#video--audio)
4. [WEB FORMS](#)
5. [ACCESSIBILITY](#)

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

#### Responsive Images
Images often account for most of the downloaded bytes on a web page.
The very first question you should ask yourself is whether an image is, in fact, required to achieve the effect you are after. Good design is simple and will also always yield the best performance. That said, as a rule, you should sacrifice image quality over performance.
With the plethora of devices and different screen sizes and resolutions nowadays, it is imperative to implement responsive images.

* Use the picture element.
* Use relative sizes (%) for images to prevent them from accidentally overflowing the container.
* Use srcset and the x descriptor in the img element.
* Use SVG when possible (logos, icons, etc.).
* Use Font icons.
* Always compress your images (use progressive JPEG, remove metadata, use software as PHOTOSHOP, ImageAlpha, ImageOptim).

###### The ```<picture>``` Element
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
###### The ```<figure>``` Element
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

#### Video & Audio
In the early days, native web technologies such as HTML didn't have the ability to embed video and audio on the Web, so proprietary (or plugin-based) technologies like Flash (and later, Silverlight) became popular for handling such content. A few years later the HTML5 specification had such features added, with the ```<video>``` and ```<audio>``` elements.

###### The ```<video>``` Element
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

##### References
> * [Video and audio content - Learn web development | MDN](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Video_and_audio_content)
> * [```<video>``` - HTML | MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/video)
> * [The video element | HTML Standard](https://html.spec.whatwg.org/#the-video-element)



## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors


## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments
