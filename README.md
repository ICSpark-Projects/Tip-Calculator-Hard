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
- Math Functions
- Arithmetic

## Setup
1. Create the following files:
  - index.html
  - style.css
  - script.js

2. In your index.html file (remember to link your css and js files), initialize the following code:
 ```<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width">
  <link rel="stylesheet" href="style.css">
  <title>Tip Calculator</title>
</head>
<body>

  <script src="script.js"></script>
</body>
</html>
```
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
     - variable
     - variable
     - variable
     - variable
     - update blah
     - update blah
     - ```return tipPerPerson``` 

When this function is called, it will return the value in tipPerPerson.

2. Create a function called calculateBill that takes in no parameteres. This will calculate the total bill each person has to pay. In this function create the following:
     - var
     - var
     - var
     - var
     - update blah
     - update blah
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
       - Call the ```calculateTip``` function and set that to equal the previous line
       - Example:
       ```javascript
       documeent.getElementId(yourelementid) = function call
       ```
       - ```document.getElementId("perPersonBill").innerHTML```
       - call the ```calculateBill``` function and set that to equal the previous line
     
## Completed Screenshot
*TO DO~~~~**
     
## Stretch Goals
1. Create an option where you can input your own custom tip percentage where the user can type in a number that is not already in the options list.
2. Sometimes people will put in the negative numbers or leave a section blank. Create error messages of these invalid inputs by using if statements and conditions.

## Credits
This tip calculator is a variation of: https://codepen.io/cphemm/pen/reNwWd
