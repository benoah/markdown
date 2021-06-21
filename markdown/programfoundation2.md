# Undefined and null

- We saw that an uninitialised variable (a variable that has been declared but not assigned a value), like myVar above, receives a value of undefined.

- undefined is a valid value in JavaScript, but you can think of it as an empty value - we can't do much with it.

- JavaScript has another empty value called null which you will often see too. In practical terms, there is not really any difference between undefined and null, they are both empty value types.

- So why have two empty value types and confuse everyone?

- The original version of JavaScript was written in ten days in the 1990s on a tight deadline. Some of the decisions made by the developer were not too great, but we have to live with them as there is an enormous amount of code written that takes into account these decisions.

# Arrays

Here is an empty array:

            var emptyArray = [];

Here is an empty array:

            var numbers = [6, 54, 17, 108];

Here is an array of booleans:

        var booleans = [true, false, false, true];

They can also hold different types of values:

        var mixedValues = ["blue", 17, false, 108, null];

## Array properties and methods

#### Counting items in an array using length

      var colours = ["red", "blue", "green", "yellow"];
        var numberOfColours = colours.length;
        console.log(numberOfColours);
        // 4


    console.log(colours.length);
    // 4

## Adding items to an array using push

         // here is the empty array
            var myArray = [];

         // its length will be 0 as there are no items in it
            console.log(myArray.length);
            // 0

        // let's add a number to the array
        myArray.push(19);

        // now the length will be 1
        console.log(myArray.length);
        // 1

        console.log(myArray)
        // [19]

        Let's add a colour to the colour array:
        var colours = ["red", "blue", "green", "yellow"];

        // add purple to the colours array
        colours.push("purple");

        // now colours includes purple
        console.log(colours);
        // ["red", "blue", "green", "yellow", "purple"]

        // now the length property will be 5
        console.log(colours.length);
        // 5

## So what are arrays used for?

But almost every website you visit uses arrays for the data they display. Some examples would be:

- posts on an Instagram page
- articles on a news site
- a Twitter feed

All of those would be fetched from the server as an array, and the browser would loop through the array to display them on the page.

# Objects and arrays of objects

- Objects are used to store related variables. Variables inside objects are called properties. Everything in an object lives inside curly braces: {}

- Objects can have none or many properties.

- Here is an empty object with no properties:

        var emptyObject = {};

- It can be useful to compare objects in JavaScript to objects in the real world.

- A dog in the real world has certain properties like name, breed and numberOfLegs.

- We can represent these properties in an object in JavaScript like this:

            var dog = {
        name: "Tripod",
        breed: "labrador",
        numberOfLegs: 3

  };

### We've created a variable called dog with a value type of object. The object has three properties, name, breed and numberOfLegs.

#### Each property has a key and a value. The key is on the left; it's the variable name. The value is on the right and is the... value.

Each value can be any of the JavaScript value types we've covered so far:

- string
- number
- boolean
- undefined
- null

             var dog = {
               name: "Tripod", // name is the key, "Tripod" is the value, a string value
                breed: "labrador", // breed is the key, "labrador" is the value, a string value
                numberOfLegs: 3, // numberOfLegs is the key, 3 is the value, a number value
                };

# Objects continued

            var postItem = {
            imageUrl: "https://path/to/bee-picture",
            likeCounter: 80,
            likedByUser: true
        };

- Because we want an array of items to loop through, we'll store this object in an array.

- If we had no items in our Norogram posts, the array would be empty:

        var posts = [];

- When we store objects in arrays, we don't need the variable name:

        // we can remove the variable name
        {
            imageUrl: "https://path/to/bee-picture",
            likeCounter: 80,
            likedByUser: true
        }

- First, let's just log the whole object.

        for(var i = 0; i < posts.length; i++) {

            // we access each item in the array using its index
            // we use the i variable as the index
            console.log(posts[i]);
        }

This will log the whole object:

      for(var i = 0; i < posts.length; i++) {

        // we access each item in the array using its index
        // we use the i variable as the index
        console.log(posts[i]);
    }
        This will log the whole object:

        // {
        //     imageUrl: "https://path/to/bee-picture",
        //     likeCounter: 80,
        //     likedByUser: true
        // }

        Now let's get the imageUrl property value of the item using dot . notation:
        for(var i = 0; i < posts.length; i++) {

    // we use . and then the property name to access it
    var image = posts[i].imageUrl;
    console.log(image);
    // "https://path/to/bee-picture"

    // or we can log it directly without the variable
    console.log(posts[i].imageUrl);
    // "https://path/to/bee-picture"

}  
 Let's log all the properties' values:
for(var i = 0; i < posts.length; i++) {

        console.log(posts[i].imageUrl);
        // "https://path/to/bee-picture"

        console.log(posts[i].likeCounter);
        // 80

        console.log(posts[i].likedByUser);
        // true
    }

# A REST API is one way to fetch data from a server.

- API stands for Application Programming Interface.

- An API is a way for programs to communicate with each other.

- REST stands for Representational state transfer.

- A REST API gives us URLs that allow a browser to communicate with a server and fetch data that it can use JavaScript to loop over and display.

- The data that a REST API sends to the browser will look a lot like the arrays of objects that we've been discussing.

# Functions

- To use a function, we first need to declare it. Declaring a function means writing the code for what we want it to do. We use the function keyword and a name of our choice to declare it.

            // declare the function
                function logWord() {
        // the code we want the function to run goes here
            }

We call a function using its name and round brackets ().

    logWord();

// Inside js/script.js call the function after declaring it:

        function logWord() {
            console.log("one");
        }

        logWord();

        it will return
        // one
