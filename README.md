HTML

What is HTML?
HTML is the language used to create the websites you visit everyday. It provides a logical way to structure content for websites.
Let's analyze the acronym "HTML," as it contains a lot of useful information. HTML stands for HyperText Markup Language.
A markup language is a computer language that defines the structure and presentation of raw text. Markup languages work by surrounding raw text with information the computer can interpret, "marking it up" to be processed. In HTML, the computer can interpret raw text that is wrapped in HTML elements. These elements are often nested inside one another, with each containing information about the type and structure of the information to be displayed in the browser. HyperText is text displayed on a computer or device that provides access to other text through links, also known as “hyperlinks.”

!DOCTYPE:
Whether you realize it or not, when you read text, your brain must first identify the text's language. If you can understand that language, then your brain immediately begins to interpret the text. This same process happens whether you're reading a street sign, a book, or a name tag. Web browsers work in a similar way. They must know what language a document is written in before they can process its contents. You can let web browsers know that you are using HTML by starting your document with a document type declaration.
The declaration looks like this: <!DOCTYPE html>. This declaration is an instruction. It tells the browser what type of document to expect, along with what version of HTML is being used in the document. <!DOCTYPE html> must be the first line of code in all of your HTML documents. If you don't use the declaration, your HTML code will likely still work, however, it's risky. For now, the browser will correctly assume that the html in <!DOCTYPE html> is referring to HTML5, as it is the current standard. In the future, however, a new standard will override HTML5. Future browsers may assume you're using a different, newer standard, in which case your document will be interpreted incorrectly. To make sure your document is forever interpreted correctly, always include <!DOCTYPE html> at the very beginning of your HTML documents.

Preparing for HTML:
Browsers that read your code will know to expect HTML when they attempt to read your file. The <!DOCTYPE html> declaration is only the beginning, however. It indicates to the browser that you will use HTML in the document, but it doesn't actually add any HTML structure or content. To create HTML structure and content, we must add opening and closing <html> tags, like so:
<!DOCTYPE html>
<html>

</html>
Anything between the opening <html> and closing </html> tags will be interpreted as HTML code. Without these tags, it's possible that browsers could incorrectly interpret your HTML code.


HTML Anatomy:
Before we move forward, it's important that we discuss how HTML elements are structured. The diagram to the right displays an HTML paragraph element.
In this example, the paragraph element is made up of one opening tag (<p>), the “Hello world!” text, and a closing tag (</p>):
Let's quickly review each part of the tag pictured:
HTML Tag - The element name, surrounded by an opening (<) and closing (>) angle bracket.
HTML element (or simply, element) - a unit of content in an HTML document formed by HTML tags and the text or media it contains.
Opening tag - the first HTML tag used to start an HTML element. The tag type is surrounded by opening and closing angle brackets.
Element content - The information (text or other elements) contained between the opening and closing tags of an HTML element.
Closing tag - the second HTML tag used to end an HTML element. Closing tags have a forward slash (/) inside of them, directly after the left angle bracket.
Most elements require both opening and closing tags, but some call for a single self-closing tag. We'll encounter examples of both element types in the next few exercises.

The Head:
So far you've done two things:
Declared to the browser that your code is HTML.
Added the HTML element (<html>) that will contain the rest of your code.
Let's also give the browser some information about the page. We can do this by adding a <head> element.
The <head> element contains the metadata for a web page. Metadata is information about the page that isn't displayed directly on the web page. You'll see an example of this in the next exercise.
The opening and closing head tags (<head></head>) typically appear as the first item after your first HTML tag.

Page Titles:
What kind of metadata about the web page can the <head> element contain? If you navigate to the Codecademy catalog and look at the top of your browser (or at the tab you have open), you'll notice the words All Courses | Learn to code interactively | Codecademy, which is the title of the web page.
The browser displays the title of the page because the title can be specified directly inside of the <head> element, by using a <title> tag.
<!DOCTYPE html>
<html>
<title>My Coding Journal</title>
  <head>
  </html>

If we were to open a file containing the HTML code in the example above, the browser would display the words My Coding Journal in the title bar (or in the tab's title).

The Body:
We've added some HTML, but still haven't seen any results in the web browser to the right. Why is that?
Before we can add content that a browser will display, we have to add a body to the HTML file. Only content inside the opening and closing body tags can be displayed to the screen.
Once the file has a body, many different types of content – including text, images, and buttons – can be added to the body.
<!DOCTYPE html>
<html>
  <head>
    <title>I'm Learning To Code!</title>
  </head>
  <body>

  </body>
</html>

In the example above, the opening body tag (<body>) is placed directly below the closing head tag (</head>), and the closing body tag (</body>) is placed directly above the closing html tag (</html>).

Self-closing Tag:
Thus far we have only seen HTML elements with an opening and a closing tag. A few types of elements, however, require only one tag.
Self-closing elements contain all the information the browser needs to render the element inside a single tag. Also, because they are single tags, they cannot wrap around raw text or other elements.
The line break element <br /> is one example of a self-closing tag. You can use it anywhere within your HTML code. The result is a line break in the browser.
<p>line one<br />line two</p>
In the example above, the paragraph tags (<p>) enclose two phrases, split by a break tag (<br />). Note that single tags, unlike elements with two tags, can't wrap around raw text or other elements.

The code in the example above will result in an output that looks like the following:
line one
line two
Without the break tag, the browser would render line one and line two on the same line.

HTML Structure:
The rest of this lesson will focus on how HTML is structured and some tools developers use to make code easier to interpret.
HTML documents are organized as a collection of parent-child relationships. When an element is contained inside another element, it is considered the child of that element. The child element is said to be nested inside of the parent element.
<body>
  <p>Paragraph</p>
</body>
In the example above, the <p> element is nested inside the <body> element. The <p> element is considered a child of the <body> element, the parent.
Since there can be multiple levels of nesting, this analogy can be extended to grandchildren, great-grandchildren and beyond. Let's consider a more complicated example:
<body>
  <div>
    <h1>Student</h1>
    <p>Get Started</p>
  </div>
</body>
In this example, the <body> element is the parent of the <div> element. Both the <h1> and <p> elements are children of the <div> element. Because the <h1> and <p> elements are in the same level, they are considered siblings, and are both grandchildren of the <body> element.
Understanding this hierarchy is important, because child elements can inherit attributes from their parent element.

Whitespace:
As the code in an HTML file grows, it becomes increasingly difficult to keep track of how elements are related. Programmers use two tools to visualize the relationship between elements: whitespace and indentation.
Both tools take advantage of the fact that the position of elements in a browser is independent of the amount of whitespace or indentation in the index.html file. For example, if you wanted to increase the space between two paragraphs on your web page, you would not be able to accomplish this by adding space between the paragraph elements in the index.html file. The browser ignores whitespace in HTML files when it renders a web page, so it can be used as a tool to make code easier to read and follow. What makes the example below difficult to read?
<body><p>Paragraph 1</p><p>Paragraph 2</p></body>
You have to read the entire line to know what elements are present. Compare the example above to this:
<body>
<p>Paragraph 1</p>
<p>Paragraph 2</p>
</body>
This example is easier to read, because each element is on its own line. While the first example required you to read the entire line of code to identify the elements, this example makes it easy to identify the body tag and two paragraphs.
A browser renders both examples the same way:
Paragraph 1
Paragraph 2
In the next exercise you will learn how to use indentation to help visualize nested elements.

Comments:
HTML files also allow you to add comments to your code.

Comments begin with <!-- and end with -->. Any characters in between will be ignored by your browser.

<!-- This is a comment that the browser will not display. -->
Including comments in your code is helpful for many reasons:

They help you (and others) understand your code if you decide to come back and review it at a much later date.
They allow you to experiment with new code, without having to delete old code.
<!-- Favorite Films Section -->
<p>The following is a list of my favorite films:</p>
In this example, the comment is used to denote that the following text makes up a particular section of the page.

<!-- <p> Test Code </p> -->
In the example above, a valid HTML element (a paragraph element) has been "commented out." This practice is useful when there is code you want to experiment with, or return to, in the future.

Review:

Let's review what you've learned so far:

HTML stands for HyperText Markup Language and is used to create the structure and content of a webpage.
Most HTML elements contain opening and closing tags with raw text or other HTML tags between them.
Single-closing tags cannot enclose raw text or other elements.
Comments are written in HTML using the following syntax: <!-- comment -->.
HTML elements can be nested inside other elements. The enclosed element is the child of the enclosing parent element.
Whitespace between HTML elements helps make code easier to read while not changing how elements appear in the browser.
Indentation also helps make code easier to read. It makes parent-child relationships visible.
The <!DOCTYPE html> declaration should always be the first line of code in your HTML files.
The <html> element will contain all of your HTML code.
Information about the web page, like the title, belongs within the <head> of the page.
You can add a title to your web page by using the <title> element, inside of the head.
A webpage's title appears in a browser's tab.
Code for visible HTML content is placed inside of the <body> element.


