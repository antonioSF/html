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
	* 1.2 [DOCTYPE Declaration](#doctype-declaration)
	* 1.3 [HTML Element](#html-element)
	* 1.4 [HEAD element](#head-header-element)
	* 1.5 [BODY element](#)
	* 1.6 [Semantic tags](#)
2. [RESPONSIVE IMAGES](#)
3. [VIDEO & AUDIO](#)
4. [WEB FORMS](#)
5. [ACCESSIBILITY](#)

## Document structure
#### Structure your document properly
Use HTML5 semantic block level elements to define areas of your website.

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
#### DOCTYPE Declaration
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

#### HTML Element
The HTML <html> element represents the root (top-level element) of an HTML document, so it is also referred to as the root element. All other elements must be descendants of this element.

```html
<!-- html with dir global attribute -->
<html dir="rtl">
	<head>
	</head>
	<body>
	</body>
</html>
```
> **Note** This element includes the global attributes.
##### References
> * [MDN web docs - HTML Global attributes](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes)
> * [MDN web docs - HTML Root element](https://developer.mozilla.org/pt-PT/docs/Web/HTML/Element/html)

#### HEAD (header) element
The HEAD element provides general information (metadata) about the document.

```html
<!-- <head> with title and required metadata -->
<head>
		<!-- Character encoding for the document -->
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
> **Note** This element includes the global attributes.
##### References
> * [MDN web docs - head: The Document Metadata (Header) element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/head)

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors


## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments
