

# Overview

### Author: Trevor J. Puckett

The goal of this project is to great a webpage that randomly displays some of my favorite quotes. 

# Prompt

For this first project, you'll create an app that displays random famous quotes each time a button is clicked. You will select your own quotes from famous historical figures, artists, scientists, celebrities, etc.

##### Example:

> "Every great developer you know got there by solving problems they were unqualified to solve until they actually did it." - _Patrick McKenzie_

You'll locate and select your own quotes. Please select tasteful, positive, and uncontroversial quotes, for the sake of this project. Thank you.
<br>
You'll use your growing knowledge of basic JavaScript syntax, variables, loops, conditionals, and object literals to:
<br>

- Build the array of quote objects to store the quotes.
- Write your own functions for selecting random quotes from the array and printing them to the screen.


This project is a fun and effective way for you to practice basic JavaScript skills while also creating a simple interactive portfolio piece to showcase your understanding of JavaScript fundamentals.
<br>
After completing this project, you'll have a tremendous sense of accomplishment, an awesome example of your hard work to show off, and you'll be one important step closer to your goals. Best of luck and happy coding!
<br>
To complete each part of this project, use ONLY the concepts and techniques listed in the project instructions and what we have covered in the courses so far.

# Requirements Overview

- atleast 5 `quotes`
- `source` is provided for each quote
- optional quote properties: `citation`, `date` ( presented when known )
- `getRandomQuote()`: function should create a random number, and use that random number to return a random quote object from the quotes array.
- `printRandomQuote()`: perform three tasks: call the getRandomQuote function, use the returned quote object to build a string of HTML and quote properties, then use that string to display a random quote in the browser


## Create an Array of objects to store the data for your quotes

A data structure is necessary to store and organize the quotes in your app. A basic array of objects is a lightweight way to store information.

##### In your js/script.js file:
- Create a variable named `quotes` and set it equal to an empty array.
- Add a minimum of five empty objects to your `quotes` array.

## Add data to your quote objects
The objects in the quotes array store the individual properties of the quotes.

- **Add the following properties to each quote object:**
    - `quote` - string - the actual quote
    - `source` - string - the person or character who said it
- **Add a `citation` property to at least one quote object.** The value should be a string holding a reference to the source of the quote, like the book, movie, or song where the quote originates.
- **Add a `year` property to at least one quote object.** The value should be a string or number representing the year the quote originated.


# Create the `getRandomQuote` function
The `getRandomQuote` function should create a random number, and use that random number to return a random quote object from the `quotes` array.

- **Project Warm Up:** Dealing with functions, arrays, and random numbers can be confusing at first. For some helpful practice, check out the project Warm Up Random Array Index.
- **Create a function named `getRandomQuote`.**
- In the function body, **create a variable to store a random number** ranging from zero to the index of the last item in the `quotes` array.
- Lastly, the function should **return a random quote object** using the random number variable above and bracket notation on the `quotes` array.



# Create the `printQuote` function
The app should display a new quote each time the user clicks the "Show another quote" button using a printQuote function.

- **1 - Create a function named printQuote.**

    > You will program the printQuote function to perform three tasks: call the getRandomQuote function, use the returned quote object to build a string of HTML and quote properties, then use that string to display a random quote in the browser.

- 2 - In the body of the `printQuote` function, **create a variable to store a random quote object from the `getRandomQuote()` function.**

- **Create another variable to store the HTML string.** Set it equal to a string containing two `<p>` elements. Use this code snippet as a guide for what the HTML string should look like at this point:

    ```html
    <p class="quote"> A random quote </p>
    <p class="source"> quote source </p>
    ```
  - The first `<p>` element should have a class equal to “quote”, and the random quote object’s `.quote` property nested between the opening and closing `<p>` tags.
  - The second `<p>` element should have a class equal to “source”, and the random quote object’s `.source` property nested between the tags.

    > ###### Important Notes:
    > - Do not include the second closing `</p>` tag for now – you will add it at the end of this step.
    > - You can use template literals here if you’re comfortable with that approach. But if you use traditional strings instead, be sure to wrap the strings in single quotes, so that the HTML classes can use their recommended double quotes.

- 4 - **Create two separate `if` statements below the variables.** You will need to add decision-making to this function:
    > - Project Warm Up: Using conditionals to test if objects or elements exist before trying to do something with them is a common developer task. For some helpful practice, check out the project Warm Up Conditional String.
    > - If the random quote object has a citation property, concatenate a `<span>` element with the class "citation" to the HTML string.
    > - If the random quote object has a year property, concatenate a `<span>`element with the class "year" to the HTML string.
  
    Use the following code snippet as a guide for what the HTML string should look like with the added "citation" and "year" `<span>` elements (like earlier, omit the second closing `</p>` tag for now):

    ```html
    <p class="quote"> A random quote </p>
    <p class="source"> quote source
    <span class="citation"> quote citation </span>
    <span class="year"> quote year </span>
    </p>
    ```


- 5 - Below the `if` statements, **complete the string by concatenating a closing `</p>` tag to the HTML string.** This is the closing tag for the second paragraph with the class `source`.

- 6 - Lastly, **set the `printQuote` function to change the HTML string by using the `innerHTML` property.**

    > Use the following code snippet, along with the variable storing the string you’ve assembled, to update your project’s HTML with a random quote:

    ```javascript
    document.getElementById('quote-box').innerHTML = yourStringHere;
    ``` 
    
    > Note: You'll learn all about document.getElementById() and .innerHTML in an upcoming course, in this project it's going to help you select the 'quote-box' div and update its HTML content with the random quote markup.