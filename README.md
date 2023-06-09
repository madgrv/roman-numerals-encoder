# Roman Numeral Converter

This is a simple web application with a basic frontend that converts decimal numbers to their Roman numeral equivalent. It is built using HTML, CSS, and JavaScript.
I created this project as an exercise to learn JavaScript and DOM manipulation.

## Usage



To use the application, simply enter a decimal number in the input field and the Roman numeral equivalent will be displayed in real-time. The input field only accepts numeric values.

## Installation

To install and run the application locally, follow these steps:

1. Clone this repository using `git clone https://github.com/madgrv/roman-numeral-converter.git` or download the ZIP file.
2. Open `index.html` in your web browser.

Alternatively, you can view a live demo of the application [here](https://madgrv.github.io/roman-numeral-converter).

## The original function

```
function convert(num) {
  // Define an array of Roman numeral values and symbols
  let romanNumerals = [
    { value: 1000, symbol: "M" },
    { value: 900, symbol: "CM" },
    { value: 500, symbol: "D" },
    { value: 400, symbol: "CD" },
    { value: 100, symbol: "C" },
    { value: 90, symbol: "XC" },
    { value: 50, symbol: "L" },
    { value: 40, symbol: "XL" },
    { value: 10, symbol: "X" },
    { value: 9, symbol: "IX" },
    { value: 5, symbol: "V" },
    { value: 4, symbol: "IV" },
    { value: 1, symbol: "I" }
  ];

  // Initialize an empty string to hold the Roman numeral equivalent of the number
  let result = "";

  // Loop through the Roman numeral array, starting with the highest value
  for (let i = 0; i < romanNumerals.length; i++) {
    // While the current value is less than or equal to the input number, subtract the value from the input number and add the corresponding symbol to the result string
    while (num >= romanNumerals[i].value) {
      result += romanNumerals[i].symbol;
      num -= romanNumerals[i].value;
    }
  }

  // Return the result string
  return result;
}


```
