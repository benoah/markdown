# Variables

#### Variables are how a programming language stores information in a computer's memory. We can think of them as containers for data and once stored there, we can act on and use this data in other parts of our program.

## Declaring variables

        var pet;

## Strings

    var pet = "dog";

We can now use that variable in our code:

        console.log(pet);

## Joining strings together

            var letters = "a" + "b";

            console.log(letters);
            // "ab"

## Let's assign those string values to variables and then join them:

          var letter1 = "a";
            var letter2 = "b";

            var letters = letter1 + letter2;

            console.log(letters);
            // "ab"

## Numbers

                    var integer = 8;
                    var decimal = 7.1;

<!-- tabell  -->

| Operator | Name           | Example |
| -------- | -------------- | ------- |
| +        | addition       | 3 + 2   |
| -        | subtraction    | 2-1     |
| \        | multiplication | 6 \* 4  |
| /        | division       | 3/4     |
| %        | modulus        | 5%2     |

## Booleans

- Boolean values are either true or false.

            var isLoggedIn = true;

## Checking data types

        var colour = "red";

            typeof(colour);
            // "string"

            typeof("blue");
            // "string"

            typeof 14;
            // "number"

            typeof false;
            // "boolean"

# Comparison operators

| Operator | description              | Example | results |
| -------- | ------------------------ | ------- | ------- |
| ===      | equal to                 | 3 === 2 | false   |
| !==      | not equal to             | 3 !== 2 | true    |
| >        | greater than             | 6 \ 4   | true    |
| > =      | greater than or equal to | 5 >= 5  | true    |
| <        | less than                | 5 > 4   | false   |
| < =      | less than or equal to    | 3 > 4   | true    |

                    var myNumber = 7;
                        var myString = "dog";

                        // is myNumber greater than 8?
                        (myNumber > 8) // false

                        // is myNumber less than or equal to 7?
                        (myNumber <= 8) // true

                        // is myString exactly equal to "dog">
                        (myString === "dog") // true

                        // is myString not equal to "cat">
                        (myString !== "cat") // true

# Conditional statements

### if...else

- When we need to make decisions in our code, we use conditional statements.

- If it is false, we run different code.

**Perhaps you need to check whether a user is logged in:**

            var isLoggedIn = true;

                if(isLoggedIn === true) {
                    console.log("The user is logged in");
                }
                else {
                 console.log("The user is logged out");
                }

**Or whether a user has entered valid data into an input field in a form:**

            var inputIsValid = false;

                if(inputIsValid === false) {
                    // show error message
                }
                else {
                    // hide error message
                }

### Sometimes you'll need to check multiple conditions.

                var colour = "red";

                if(colour === "blue") {
                    console.log("The colour is blue");
                }
                else if(colour === "red") {
                    console.log("The colour is red");
                }
                else {
                    console.log("The colour is neither blue nor red");
                }

### switch

        var colour = "red";
        var colour = "red";


    switch(colour) {
        case "blue":
            console.log("The colour is blue");
            break;
        case "red":
            console.log("The colour is red");
            break;
        case "green":
            console.log("The colour is green");
            break;
        case "yellow":
            console.log("The colour is yellow");
            break;
        default:
            console.log("The colour is not blue, red, green or yellow");

# Assignment vs comparison

### A common mistake is to accidentally use the = operator instead of a comparison operator when peforming a check. When that happens the comparison will always return true:

            var myPet = "pig";

        if(myPet = "sheep") {
            console.log("My pet is a sheep");
        }
        else {
            console.log("My pet is not a sheep");
        }

## Loops

#### Loops are used to do the same thing over and over again.

- If we wanted to console log a number value from 1 to 3, we could do something like this:

            console.log(1);
            console.log(2);
            console.log(3);

#### for loop

       for(var count = 1; count <= 10; count++) {
    console.log(count);

}

- Inside for's brackets, we first have var count = 1;. This is the counter variable. It's just a variable so we could call it anything. Often the variable is called i.

- var count = 1 is the starting value for the loop. We've set it to start at 1.

- Next is count <= 10. This is the condition that gets checked each time the loop runs. Each pass through the loop, the code will check if count is less than or equal to 10. If it is, the code inside the curly braces {} will run. If not, the loop will stop.

- The count++ part is the iterator. On each loop, it adds a value to the count variable. count++ is shorthand for count = count + 1.

So we could rewrite the loop like this:

     for(var count = 1; count <= 10; count = count + 1) {
        console.log(count);
        }

Some developers prefer to declare the variable outside the loop without initialising it:

            var count;

            for(count = 1; count <= 10; count++) {
            console.log(count);
            }

Let's write a loop that counts from 5 to 25:

        for(var i = 5; i <= 25; i++) {
            console.log(i);
        }

We're calling the variable i this time. We've set it to start at 5. The loop will run until the condition (i <= 25) returns false.

We could write the condition differently:

                for(var i = 5; i < 26; i++) {
            console.log(i);
        }

### Looping through arrays

Here is an array of string variables, a list of colours. An array's variables live inside square brackets [].

        var colours = ["red", "blue", "green", "yellow"];

    var firstItem = colours[0]; // the first item in the array is at index 0

### We can get the amount of items in an array using its length property:

        var numberOfColours = colours.length;
            console.log(numberOfColours)
            // 4

We are going to start the loop at 0, since that is the first index of the array:

        for(var i = 0; i < numberOfColours; i++) {
        console.log(colours[i]);
    }
