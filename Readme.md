# HTML Essentials

This guide is designed to introduce you to the basics of HTML, the standard markup language used to create web pages. You'll learn how to structure an HTML document, add images and hyperlinks, insert comments, and style your content with CSS.

---

## Creating an HTML document

An HTML document is structured between the `<html>` tags. It mainly consists of two parts: the `<head>` and the `<body>`. The `<head>` contains meta-information about the document, like its title, while the `<body>` contains the content that is displayed on the web page.

```html
<!DOCTYPE html>
<html>
    <head>
        <title>This is a great title</title>
    </head>
    <body>
        <h3>This is a Heading</h3>
        <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. This is a sample text to demonstrate the paragraph element in HTML.
        </p>
    </body>
</html>
```

The `<!DOCTYPE html>` declaration defines this document to be HTML5, which is the latest standard.

---

## Adding Images

To add images to your HTML document, use the `<img>` tag. The `src` attribute specifies the path to the image you want to display, while the `alt` attribute provides alternative information for an image if a user for some reason cannot view it.

```html
<img src="images/image.png" alt="This is an image of a Yacht sailing in a wide sea" style="height: 500px; float: right" />
```

The `style` attribute is used here to adjust the image's appearance directly in the HTML document, setting its height and floating it to the right.

---

## Adding Hyperlinks

Hyperlinks are defined with the `<a>` tag. The `href` attribute specifies the link's destination. You can link to another page within your website, an external website, an email address, or a file.

```html
<a href="otherpage.html">Click here!</a>
<a href="http://www.bbc.com" target="_blank">Click here!</a>
<a href="https://en.wikipedia.org/wiki/Yacht">
    <img src="images/image.png" alt="This is an image of a Yacht sailing in a wide sea" style="height: 500px; float: right" />
</a>
<a href="mailto:dave@elegantyachting.com">Mail us!</a>
```

The `target="_blank"` attribute in the second link opens the linked document in a new window or tab.

---

## Adding Comments

Comments in HTML are added with the `<!--` and `-->` tags. They are not displayed in the browser but can help document your HTML source code.

```html
<!-- This is a paragraph section -->
```

---

## Adding CSS

CSS can be added to HTML documents in three ways: inline, internal, and external. Here, we focus on inline and internal CSS.

### Inline CSS

Inline CSS is used to apply a unique style to a single HTML element, using the `style` attribute.

```html
<p style="font-size: 40px; color: red">
    We provide the best yachting experience in the world. Our yachts are the most luxurious and our staff are the most professional.
</p>
```

### Internal CSS

Internal CSS is defined within the `<style>` element, inside the `<head>` section of an HTML page. It applies styles to elements within that page.

```html
<style>
    p {
        font-size: 20px;
        color: blueviolet;
    }

    h1 {
        font-size: 80px;
        color: red;
    }

    #orangeparagraph {
        font-size: 20px;
        color: orange;
    }
</style>
```

### CSS with ID

The `id` attribute is used to specify a unique style for an individual element.

```html
<p id="orangeparagraph">
    We provide the best yachting experience in the world. Our yachts are the most luxurious and our staff are the most professional.
</p>
```

### External CSS

External CSS is a method of adding CSS styles to an HTML document by linking an external CSS file. This allows for better organization and separation of concerns in web development.

To use external CSS, you need to create a separate CSS file, typically with a .css extension, and link it to your HTML document using the `<link>` tag. The `rel` attribute specifies the relationship between the HTML document and the linked file, and the `href` attribute specifies the path to the CSS file.

Here is an example of how to link an external CSS file named "style.css":

```html
<link rel="stylesheet" type="text/css" href="style.css" />
```

In the example above, the CSS file "style.css" is located in the same directory as the HTML document. If the CSS file is in a different directory, you need to provide the correct path in the `href` attribute.

The CSS code in the external file can define styles for various HTML elements. In the example below, the CSS file "style.css" defines styles for `<p>`, `<h1>`, and an element with the `id` "orangeparagraph":

```css
p {
    font-size: 40px;
    color: blueviolet;
    font-family: 'Courier New', Courier, monospace;
}

h1 {
    font-size: 80px;
    color: #955d02f2;
}

#orangeparagraph {
    font-size: 20px;
    color: orange;
    font-family: Verdana, Geneva, Tahoma, sans-serif;
}
```

In this CSS code, the `p` selector selects all `<p>` elements and applies the specified styles. The `h1` selector selects all `<h1>` elements, and the `#orangeparagraph` selector selects the element with the `id` "orangeparagraph". The styles defined in the CSS file will be applied to the corresponding HTML elements when the HTML document is rendered in a web browser.

Using external CSS allows for easy maintenance and reusability of styles across multiple HTML documents. It also promotes a separation of concerns between the structure (HTML), presentation (CSS), and behavior (JavaScript) of a web page.

---

## The Division Element

The `<div>` element is a container that is used to group and organize other HTML elements. It does not have any semantic meaning on its own, but it is commonly used to create sections or divisions within a web page.

```html
<div>
    <h1>Elegant Yachting Tours</h1>
    <hr />
    <!-- This is a paragraph section -->
    <p>
        We provide the best yachting experience in the world. Our yachts are the most luxurious and our staff are the most professional. We guarantee that you will have the best time of your life.
    </p>
</div>
```

In the example above, the `<div>` element is used to group the heading `<h1>`, horizontal rule `<hr>`, and paragraph `<p>` elements together. This helps to organize the content and apply styles or manipulate the group as a whole using CSS or JavaScript.

The `<div>` element is a versatile and commonly used element in HTML, providing a way to structure and organize the content of a web page.

---

## Navigation

The navigation section of a website is crucial for providing easy access to different pages. Here is an example of HTML and CSS code for creating a navigation bar.

```html
<nav>
    <ul>
        <li><a href="home.html">Home</a></li>
        <li><a href="tours.html">Tours</a></li>
        <li><a href="gallery.html">Gallery</a></li>
        <li><a href="about.html">About</a></li>
        <li><a href="contact-us.html">Contact</a></li>
    </ul>
</nav>
```

The HTML code above represents a navigation bar with a list of links. Each link is represented by an `<a>` tag within an `<li>` tag. The `href` attribute specifies the destination of each link.

```css
/* Navigation styles */
nav {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    padding: 10px 0px;
    z-index: 1000;
    background-color: rgba(50, 50, 60, 0.95);
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.52);
}

nav ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
    align-items: center;
}

nav li {
    margin: 0 15px;
}

nav a {
    font-family: "Montseratt", sans-serif;
    font-size: 16px;
    color: #e6e6e6;
    text-decoration: none;
    transition: color 0.3s, border-bottom 0.3s;
    padding-bottom: 5px;
    position: relative;
}

nav a:hover {
    color: #1b1b20;
    border-bottom: 2px solid #e6e6e6;
}
```

The CSS code above provides styling for the navigation bar. The `nav` selector targets the `<nav>` element and sets its position to fixed, making it stay at the top of the page. The `nav ul` selector targets the `<ul>` element inside the navigation and applies flexbox properties to horizontally align the list items. The `nav li` selector targets the `<li>` elements and adds margin to create spacing between them. The `nav a` selector targets the `<a>` elements and sets their font, color, and transition properties. The `nav a:hover` selector changes the color and adds a bottom border to the links when hovered over.

By combining the HTML and CSS code, you can create a visually appealing and functional navigation bar for your website.

---
