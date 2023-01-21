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
            - ```p``` tag with the inner HTML "Enter the total amount on your bill (You can customize this message).
            - ```input``` with the ```id``` of "bill", ```type``` of "number", ```placeholder``` of "$"
          - ```div``` with the ```class``` of "input-section". This div will hold the bill amount input.
            - ```h3``` tag with the inner HTML "Bill Amount".
            - ```p``` tag with the inner HTML "Enter the total amount on your bill (You can customize this message).
            - ```input``` with the ```id``` of "bill", ```type``` of "number", ```placeholder``` of "$"



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

## Stretch Goals
