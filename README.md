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
	* 1.6 [Semantic Content Sectioning Elements](#semantic-content-sectioning-elements)
2. [RESPONSIVE IMAGES](#)
3. [VIDEO & AUDIO](#)
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
**[⬆ back to top](#table-of-contents)**

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

**[⬆ back to top](#table-of-contents)**

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

**[⬆ back to top](#table-of-contents)**

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

**[⬆ back to top](#table-of-contents)**

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

**[⬆ back to top](#table-of-contents)**

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

**[⬆ back to top](#table-of-contents)**

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors


## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments
