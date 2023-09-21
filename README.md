# Horiseon Refactor

## Technology Used 

| Technology Used         | Resource URL           | 
| ------------- |:-------------:| 
| HTML    | [https://www.w3schools.com/html/](https://www.w3schools.com/html/) | 
| CSS     | [https://www.w3schools.com/css/default.asp](https://www.w3schools.com/css/default.asp)      |   
| Git | [https://git-scm.com/](https://git-scm.com/)     |    

## Description 

[Visit the Deployed Site] https://jamessahunter.github.io/horiseon-refactor/

The project was to refactor the given code for the Horiseon website. The main reason was to make the website follow accessiblity standards such as using semantic HTML elements, header size decreasing sequetially, add alt attributes to images and have the code follow a logical structure. This was done by changing out the div elements and replacing them with their relevant semantic counterparts as shown in the example below. The images had alt attributes added the provides a brief descrpiton of the image. The CSS file was also reorganized and consolidated so the elements appeared in the same order as in the HTML file and reduced any clutter by combining duplicates into one class also shown below.  

## Code Refactor HTML Example

What are the steps required to install your project? Provide a step-by-step description of how to get the development environment running.

 The given HTML file uses the div element which is non-semantic. To learn more about semantic elements use this link (https://www.w3schools.com/html/html5_semantic_elements.asp).
```html
<div class="header">
        <h1>Hori<span class="seo">seo</span>n</h1>
        <div>
            <ul>
                <li>
                    <a href="#search-engine-optimization">Search Engine Optimization</a>
                </li>
                <li>
                    <a href="#online-reputation-management">Online Reputation Management</a>
                </li>
                <li>
                    <a href="#social-media-marketing">Social Media Marketing</a>
                </li>
            </ul>
        </div>
    </div>
```

Converting the above non-semantic div with the class of 'header' to use the semantic element of header as well as adding in the nav element to replace the second div element

```html
    <header>
        <h1>Hori<span id="seo">seo</span>n</h1>
            <nav>
                <ul>
                    <li>
                        <a href="#search-engine-optimization">Search Engine Optimization</a>
                    </li>
                    <li>
                        <a href="#online-reputation-management">Online Reputation Management</a>
                    </li>
                    <li>
                        <a href="#social-media-marketing">Social Media Marketing</a>
                    </li>
                </ul>
            </nav>
    </header>
```

Due to the change in the HTML file the CSS file need to be changed as the section was no longer using a class selector  one can just use the element selector of header.

```css
.header {
    padding: 20px;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    background-color: #2a607c;
    color: #ffffff;
}
```
This change is seen by the removal of the '.' before header.
```css
header {
    padding: 20px;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    background-color: #2a607c;
    color: #ffffff;
}

```
## Code Refactor CSS Example
The provided code below has multiple classes that are unessecary as they are repetitive. The classes are also not in the order they appear in the HTML file
```css

.benefit-lead img {
    display: block;
    margin: 10px auto;
    max-width: 150px;
}

.benefit-brand img {
    display: block;
    margin: 10px auto;
    max-width: 150px;
}

.benefit-cost img {
    display: block;
    margin: 10px auto;
    max-width: 150px;
}

.search-engine-optimization {
    margin-bottom: 20px;
    padding: 50px;
    height: 300px;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    background-color: #0072bb;
    color: #ffffff;
}

.online-reputation-management {
    margin-bottom: 20px;
    padding: 50px;
    height: 300px;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    background-color: #0072bb;
    color: #ffffff;
}

.social-media-marketing {
    margin-bottom: 20px;
    padding: 50px;
    height: 300px;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    background-color: #0072bb;
    color: #ffffff;
}
```
The classes have been consolidated and renamed. They classes have also been reorder to appear as they do in the HTML file.
```css
/* sets height of images */
.content-sections img {
    max-height: 200px;
}
/* sets margins and font size for h2 */
h2 {
    margin-bottom: 20px;
    font-size: 36px;
}
/* has benefits fill 20% and floats right with margin and sets font and color */
.benefits {
    margin-right: 20px;
    padding: 20px;
    clear: both;
    float: right;
    width: 20%;
    height: 100%;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    background-color: #2589bd;
}
```

## Usage 
 The website should load and scroll up and down. The links in the header take you to the correct sections. 

 An example of how the website should perform is in the gif below.

![Usage Example](./assets/Horiseon.gif)

## Learning Points 

Learned about semantic HTML elements and how to link to a different part of the website

## Author Info

### James Hunter
* [LinkedIn](https://www.linkedin.com/in/james-hunter123/)
* [Github](https://github.com/jamessahunter)

## Credits

Jerome Chenette for providing the original code
* [Github](https://github.com/jeromechenette)
