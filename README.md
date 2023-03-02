# Tip Calculator

Create a simple tool to calculate tip/gratuity at a restaurant or for a service.

## Difficulty
Easy

## Prerequisites
- HTML structures and attributes
- Basic CSS styling
- Changing Elements in HTML using DOM
- JS Functions
- Variables
- Return Statements
- JS Math Methods
- Arithmetic

## Setup
1. Create the following files:
  - index.html
  - style.css
  - script.js

2. In your index.html file link your css and js files in their respective lines, initialize the following code:

```<link rel="stylesheet" href="style.css">```
```<script src="script.js"></script>```
## Part I: HTML
1. Create the following HTML elements between the ```body``` tags with the following nested structure:
     - ```div``` with the id of "container" 
       - ```h1``` tag with the inner HTML "Tip Calculator".
       - ```p``` tag with the inner HTML "Tip your waiters!" (You can customize this message).
       - ```div``` with the ```id``` of "boxes". This div will hold the squares of each input section
          - ```div``` with the ```class``` of "input-section". This div will hold the bill amount input.
            - ```h3``` tag with the inner HTML "Bill Amount".
            - ```p``` tag with the inner HTML "Enter the total amount on your bill" (You can customize this message).
            - ```input``` with the ```id``` of "bill", ```type``` of "number", ```placeholder``` of "$"
          - ```div``` with the ```class``` of "input-section". This div will hold tip percentage.
            - ```h3``` tag with the inner HTML "Rate the Service".
            - ```p``` tag with the inner HTML "How was your experience?" (You can customize this message).
            - ```select``` with the ```id``` of "rating" *Note: You can customize the following option tags to whatever percentages and inner HTML to whatever you want :)*
              - ```option``` tag with ```disabled selected value``` of "0" and the inner HTML "--- Rating ---"
              - ```option``` tag with ```value``` of "0.10" and the inner HTML "Bad - 10%"
              - ```option``` tag with ```value``` of "0.18" and the inner HTML "OK - 18%"
              - ```option``` tag with ```value``` of "0.35" and the inner HTML "Good - 35%"
              - ```option``` tag with ```value``` of "0.50" and the inner HTML "0.50 - 50%"
          - ```div``` with the ```class``` of "input-section". This div will hold the amount of people splitting the bill.
             - ```h3``` tag with the inner HTML "Splitting the Bill?
             - ```p``` tag with the inner HTML "How many people are sharing the bill?" (You can customize this message).
             - ```input``` with the ```id``` of "people", ```type``` of "number", ```value``` of "0"
       - ```div``` with the ```id``` of "calculate-button"
         - ```button``` tag with the ```id``` of "calculate" and inner HTML of "Calculate!"
       - ```div``` with the ```id``` of "totalTip".
         - ```h2``` tag with the inner HTML "Tip Per Person".
         - ```h3``` tag
            - ```sup``` tag with the inner HTML of "$"
            - ```span``` tag with the ```id``` of "tip" and inner HTML of "0.00" 
       - ```div``` with the ```id``` of "billPerPerson"
         - ```h3``` tag
           - ```sup``` tag with the inner HTML of "$"
           - ```span``` tag with the ```id``` of "perPersonBill" and inner HTML of "0.00"          
                    
## Part II: CSS
1. Target the ```body``` element
     - set ```text-align``` to ```center```
     - set ```background-color``` to a color of your choice
    
2. Target the ```container``` id
     - set ```max-width``` to ```800px```
     - set ```margin``` to ```16px auto```
     - set ```background``` to ```white```
     - set ```padding``` to ```30px```
     - set ```border-radius``` to ```10px```
     
3. Target the ```boxes``` id
     - set ```display``` to ```flex```
     
4. Target the ```input-sections``` class 
     - set ```padding``` to ```16px```
     - set ```border``` to ```1px solid black```
     - set ```margin-right``` to ```16px```
     - set ```border-radius``` to ```16px```
     
5. Target the ```calculate-button``` id
     - set ```margin-top``` to ```16px```

## Part III: JS
1. Create a function called calculateTip that takes in no parameters. This will calculate the tip per person. In this function create the following:
     - Set the value of the ```bill``` element in a ```var``` variable called "bill" using the DOM method ```document.getElementById("yourelementid").value```
     - Set the value of the ```rating``` element in a ```var``` variable called "serviceRating" using the DOM method ```document.getElementById("yourelementid").value``` 
     - Set the value of the ```people``` element in a ```var``` variable called "numOfPeople" using the DOM method ```document.getElementById("yourelementid").value```
     - ex. var variableName = document.getElementById("yourelementid").value`
     - Now that we have the values of the 3 things we need to calculate the tip each person owes, we can use arithmetics to calculate that. Do the following:
       -  Create a ```var``` variable called "tipPerPerson"
       -  Set that variable to equal to ```(bill * serviceRating) / numOfPeople```
       -  How would we deal with numbers that are more than 2 decimal places? We will use JS math methods to round to the nearest hundredth and then make them 2 decimal places with the following code:
       - ```javascript
         //round to nearest hundredth
         tipPerPerson = Math.round(tipPerPerson * 100) / 100;
         // 2 decimal plaes
         tipPerPerson = tipPerPerson.toFixed(2);
         ```
     - Return the final value that we want by: ```return tipPerPerson``` 

When this function is called, it will return the value in tipPerPerson.

2. Create a function called calculateBill that takes in no parameteres. This will calculate the total bill each person has to pay. In this function create the following:
     - Set the value of the ```bill``` element in a ```var``` variable called "bill" using the DOM method ```document.getElementById("yourelementid").value```
     - Set the value of the ```people``` element in a ```var``` variable called "numOfPeople" using the DOM method ```document.getElementById("yourelementid").value```
     - ex. var variableName = document.getElementById("yourelementid").value`
     - Create a ```var``` variable called "tipPerPerson"
     - Call the ```calculateTip``` function and set that equal to the tipPerPerson variable.
     - Use the ```parseFloat``` method on tipPerPerson
     -  ```javascript
          tipPerPerson = parseFloat(tipPerPerson); //converts string into float :)
        ```
     - Now that we have the values of the 3 things we need to calculate the total bill each person owes, we can use arithmetics to calculate that. Do the following:
       -  Create a ```var``` variable called "billPerPerson"
       -  Set that variable to equal to ```(bill / numOfPeople) + tipPerPerson```
       -  How would we deal with numbers that are more than 2 decimal places? We will use JS math methods to round to the nearest hundredth and then make them 2 decimal places with the following code:
       - ```javascript
         //round to nearest hundredth
         billPerPerson = Math.round(billPerPerson * 100) / 100;
         // 2 decimal plaes
         billPerPerson = billPerPerson.toFixed(2);
         ```
 
     - ```return billPerPerson```

When this function is called, it will return the value in billPerPerson.

3. Create an onlick event function when the calculate button is clicked. This will display the results of the calculations.
     ``` javascript
     document.getElementById("calculate").onclick = function() {
       //code here
     };
     ```
     - Inside the function, do the following:
       - ```document.getElementId("tip").innerHTML```
       - Call the ```calculateTip``` function and set that to equal to the line above
       - ```document.getElementId("perPersonBill").innerHTML```
       - call the ```calculateBill``` function and set that to equal to the line above
       - Example:
       ```javascript
       documeent.getElementId(yourelementid) = function call
       ```
     
## Completed Screenshot
https://github.com/yhanessaanne/tip-calculator/blob/main/Screen%20Shot%202023-01-20%20at%207.53.51%20PM.png?raw=true
     
## Stretch Goals
1. Create an option where you can input your own custom tip percentage where the user can type in a number that is not already in the options list.
2. Sometimes people will put in the negative numbers or leave a section blank. Create error messages of these invalid inputs by using if statements and conditions.

## Credits
This tip calculator is a variation of: https://codepen.io/cphemm/pen/reNwWd
