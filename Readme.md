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

## CSS Update

```html
<section class="chapter-section">
    <h2>Discover the Ocean's Mysteries</h2>
    <!-- This is a paragraph section -->
    <p>
        Sail with us as we explore untouched islands, crystal clear waters, and breathtaking sunsets. Every tour is a curated experience, ensuring you witness the beauty and tranquility of the sea. Join us on a voyage of discovery and indulge in the luxury that only Elegant Yachting Tours can offer.
    </p>
</section>
```

```css
.chapter-section {
    background-color: rgba(255, 255, 255, 0.2);
    border-radius: 8px;
    padding: 20px;
    margin: 80px auto;
    max-width: 800px;
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
}

.chapter-section h2 {
    font-family: "Montserrat", sans-serif;
    font-size: 24px;
    color: #e6e6e6;
    margin-bottom: 5px;
    border-bottom: 2px solid #e6e6e6;
    display: inline-block;
    padding-bottom: 5px;
}

.chapter-section p {
    font-family: "Montserrat", sans-serif;
    font-size: 18px;
    color: #e6e6e6;
    line-height: 1.6;
}
```

The updated CSS code adds styling to the HTML section with the class "chapter-section". The section has a background color with transparency, rounded corners, padding, margin, and a box shadow to give it a visually appealing appearance. The maximum width is set to 800px and it is centered on the page.

The heading `<h2>` within the section has a custom font, font size, color, and a bottom border to separate it from the paragraph.

The paragraph `<p>` within the section has a custom font, font size, color, and line height to ensure readability.

These CSS styles enhance the visual presentation of the HTML section, making it more attractive and engaging for readers.

---

## Text Formatting

```html
<p>
    <ins>Sail</ins> with us as we explore <small>untouched</small> islands, crystal clear H<sub>2</sub>O, and <b>breathtaking</b> sunsets. <q cite="https://google.com"><em>Every tour</em> is a curated &nbsp;experience, <i>ensuring</i> you witness the <mark>beauty and tranquility</mark> of the sea.</q> <del>Join us on a voyage of discovery</del> and indulge in the luxury that only <strong>Elegant Yachting Tours</strong><sup>®</sup> can offer! We also offer tours to the <abbr>NASA</abbr> Space Center
    <br><br>
    <cite>The Hobbit</cite> by J.R.R Tolkien
     <br><br>
    <address>123 Yacht Street, Ocean City, OC 12345</address>
    <br><br>
    <bdo dir="rtl">This text has been reversed</bdo>
    <br><br>
    <code>
        // Sample code
        <br>
        function greet() {
            console.log("Hello, world!");
        }
    </code>
</p>
```

This markdown content demonstrates various text formatting options in HTML. It includes examples of:

- Inserted text using the `<ins>` tag
- Small text using the `<small>` tag
- Subscript text using the `<sub>` tag
- Bold text using the `<b>` tag
- Quoted text using the `<q>` tag with a citation
- Deleted text using the `<del>` tag
- Strong emphasis using the `<strong>` tag
- Superscript text using the `<sup>` tag
- Abbreviations using the `<abbr>` tag
- Citations using the `<cite>` tag
- Addresses using the `<address>` tag
- Reversed text using the `<bdo>` tag with the `dir="rtl"` attribute
- Code snippets using the `<code>` tag

These formatting options allow you to add emphasis, provide additional information, and style your text in various ways within your HTML content.

---

## Semantic Elements

```html
<body>
    <nav>
        <ul>
            <li><a href="home.html">Home</a></li>
            <li><a href="tours.html">Tours</a></li>
            <li><a href="gallery.html">Gallery</a></li>
            <li><a href="about.html">About</a></li>
            <li><a href="contact-us.html">Contact</a><li>
        </ul>
    </nav>
    <!-- This is the header section -->
    <header>
        <h1>Elegant Yachting Tours</h1>
        <h2>An experience that will sail your dreams into reality</h2>
        <button>Book Now</button>
    </header>

    <!-- This is the main section -->
    <section class="discovery-section">
        <h2>Discover the Ocean's Mysteries</h2>
        <!-- This is a paragraph section -->
        <p>
            Sail with us as we explore untouched islands, crystal clear waters, and breathtaking sunsets. Every tour is a curated experience, ensuring you witness the beauty and tranquility of the sea. Join us on a voyage of discovery and indulge in the luxury that only Elegant Yachting Tours can offer!
        </p>
    </section>

    <!-- This is an article -->
    <article>
        <h2>Our Tours</h2>
        <p>
            Our tours are designed to cater to your every need. Whether you are looking for a romantic getaway, a family vacation, or a solo adventure, we have the perfect tour for you. Our experienced crew will ensure that you have a safe and enjoyable journey, while our luxurious yachts will provide you with the comfort and relaxation you deserve.
        </p>
    </article>

    <!-- Aside -->
    <aside>
        <h2>Why Choose Us?</h2>
        <p>
            At Elegant Yachting Tours, we are committed to providing you with an unforgettable experience. Our tours are designed to cater to your every need, ensuring that you have a safe and enjoyable journey. Our experienced crew will take care of all the details, so you can relax and enjoy the beauty of the sea. Book your tour today and discover the magic of Elegant Yachting Tours!
        </p>
    </aside>

    <!-- Figure -->
    <figure>
        <img src="images/image.png" alt="Yacht"  width="800px"/>
        <figcaption>Image of a yacht</figcaption>
    </figure>

    <!-- This is the footer section -->
    <footer>
        <p>&copy; 2021 Elegant Yachting Tours</p>
    </footer>

</body>
```

This markdown content represents a web page structure using semantic HTML elements. It includes:

- A navigation bar (`<nav>`) with links to different pages.
- A header section (`<header>`) with a heading, subheading, and a button.
- A main section (`<section>`) with a heading and a paragraph.
- An article (`<article>`) with a heading and a paragraph.
- An aside (`<aside>`) with a heading and a paragraph.
- A figure (`<figure>`) with an image and a caption.
- A footer section (`<footer>`) with a copyright notice.

By using semantic elements, the HTML structure becomes more meaningful and easier to understand for both humans and search engines. It also helps with accessibility and allows for better styling and organization of the content.

---
