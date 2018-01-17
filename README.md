# HTML5 Style Guide

WSA Internal HTML5 Coding Standards Guide

> **Note**: The purpose of these guides are to provide coding standards and conventions for the majority of WSA internal projects. Some elements might not be required depending on the project specifications. It also assumes you have a basic knowledge of Front-End technologies and Responsive Web Design.


Other Style Guides

  - [CSS & Sass](https://github.com/antonioSF)
  - [JavaScript](https://github.com/antonioSF)
  - [Environment / Scaffolding / Bundles / deployments](https://github.com/antonioSF)

## Table of Contents
1. [Document & website structure](#document--website-structure)

## Document & website structure
#### Structure your document properly:
* Use HTML5 semantic block level elements to define areas of your website


```html
<!DOCTYPE html>
<html>
	<head>
		<!-- Document metadata / CSS external links / favicons -->

		<!-- Document Title -->
		<title>Eg. Today's feed | The Feeder</title>

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
				<h2>Eg. Upcaming events</h2>
				<ul>
					<li><a href="#">Eg. Event 1</a></li>
					<li><a href="#">Eg. Event 2</a></li>
					<li><a href="#">Eg. Event 3</a></li>
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

### Prerequisites

What things you need to install the software and how to install them

```
Give examples
```

### Installing

A step by step series of examples that tell you have to get a development env running

Say what the step will be

```
Give the example
```

And repeat

```
until finished
```

End with an example of getting some data out of the system or using it for a little demo

## Running the tests

Explain how to run the automated tests for this system

### Break down into end to end tests

Explain what these tests test and why

```
Give an example
```

### And coding style tests

Explain what these tests test and why

```
Give an example
```

## Deployment

Add additional notes about how to deploy this on a live system

## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone who's code was used
* Inspiration
* etc