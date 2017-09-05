/* String & Array methods exercise
*/

//#1-Function returns first letter of the string that is passed to it, if it receives no parameter or an invalid parameter, it returns 'undefined'

function firstLetter (inputString) {
  if (inputString) {
    return inputString[0]
  } else {
    return undefined
  }
}

//#2-Function returns last letter of the string that is passed to it, if it receives no parameter or an invalid parameter, it returns 'undefined'

function lastLetter (inputString) {
  if (inputString) {
    return inputString[inputString.length - 1]
  } else {
    return undefined
  }
}

//#3- Function returns the letter at a specific position, it takes the string and an index number as a parameter, returns undefined if it receives invalid parameters

function letterAtPosition (inputString, indexNumber) {
  if(inputString) {
    return inputString[indexNumber]
  } else {
    return undefined
  }
}

//#4- Function returns the sum of the two numbers that are passed as an argument. If one of the numbers is not passed or if it's not a number, return undefined

function addTwoNumbers (num1, num2) {

  if (typeof num1 === 'number' && typeof num2 === 'number') {
    return num1 + num2
  } else {
    return undefined
  }
}

//#5 Function returns the product of the two numbers that are passed as an argument. If one of the numbers is not passed or if it's not a number, return undefined

function multiplyTwoNumbers (num1, num2) {

  if (typeof num1 === 'number' && typeof num2 === 'number') {
    return num1 * num2
  } else {
    return undefined
  }
}

//#6- Calculator: Use 'operation' argument to decide what this function will return; if 'add', return the sum of two numbers, if 'sub' return the difference, if 'mult' or 'div', you get the idea. if anything else return undefined

function calculator (operation, num1, num2) {

  if (operation == 'add') {
    return num1 + num2
    } else if (operation == 'sub') {
      return num1 - num2
    } else if (operation == 'mult') {
      return num1 * num2
    } else if (operation == 'div') {
      return num1 / num2
    } else {
      return undefined
    }
}


//#7- Function that repeats input string as number of times specified. If negative number or zero is specified, return empty string, if any invalid parameters, return undefined

function repeatString (inputString, count) {

  if (typeof inputString === 'string' && typeof count === 'number' && count > 0) {
    return inputString.repeat(count);
  } else if (typeof inputString === 'string' && typeof count === 'number' && count <= 0)  {
    return ''
  } else {
    return undefined
  }
}

//#8- Function reverses an input string

function reverseString (inputString) {
  return inputString.split('').reverse('').join('');
}

//#9- Function that returns the longest word in an input string. If the input string is empty, return an empty string. If multiple words have the same length, return the last one that matches

function longestWord (inputString) {

  var strSplit = inputString.split(' ');

  if (strSplit === '') {
    return ''
  } else {
    var longestWord = strSplit.sort(function(a, b) {
    return b.length - a.length;
  });
  return longestWord[0]
  }
}

//#10- Function returns an input string capitalized (using for loop, and using map function)

function capitalize (inputString) {

  var splitString = inputString.toLowerCase().split(' ');

  for (i = 0; i < splitString.length; i++) {
    splitString[i] = splitString[i].charAt(0).toUpperCase() + splitString[i].substring(1);
  }
  return splitString.join(' ');
}

//using map function (cleaner)

function titleCase (inputString) {
  return inputString.toLowerCase().split(' ').map(function(word) {
    return word[0].toUpperCase() + word.substr(1);
  })
  .join(' ');
}


//#11- Function returns the sum of all numbers in the input array, if any element is not a number, skip it, if empty, return 0

function sumOfNumbers(arrayOfNumbers) {
   var sum = 0;

    for (var j = 0; j < arrayOfNumbers.length; j++) {
        if (typeof arrayOfNumbers[j] !== "number") {
            return
        }
    }
     for (var i = 0; i < arrayOfNumbers.length; i++) {
           sum = sum + arrayOfNumbers[i];
     }
    return sum;
}

//#12- Function returns the elements that are unique to array1 and array2, if no unique elements, return empty array, if inputs are not arrays, return undefined

function uniqueElements(array1, array2) {

  if (typeof array1 === 'object' && typeof array2 === 'object') {
    var uniqueArray = [];

    array1.forEach(function(value) {
      if (array2.indexOf(value) < 0) uniqueArray.push(value);
    });

    array2.forEach(function(value) {
      if (array1.indexOf(value) < 0) uniqueArray.push(value);
    });
    return uniqueArray
  }
}


//using filter methods

function uniqueArrayElements (array1, array2) {
  var uniqueArray = [];
  if (!Array.isArray(array1) || !Array.isArray(array2)) {
  return undefined
  }
  var uniqueArray = array1.filter(function (value) {
    return array2.indexOf(value) == -1;
  });
  return uniqueArray
}

uniqueArrayElements('test', [1,3,6,10]);


//#13- Function checks if the string is a palindrome and returns true or false

function isPalindrome (inputString) {
  return inputString === inputString.split('').reverse('').join('');
}


//#14- Function returns the string of characters wrapped to 40 characters per line (do not display spaces after the cut)

function wrapCharacter (inputString) {
  var wordWrapped = [];
  var characters = inputString.split("");

  while (characters.length > 0) {
    //removes white spaces
    if (characters[0] == " ") characters.shift();
    //puts the limit at 40 chars and joins them back to words
    wordWrapped.push(characters.splice(0,40).join(""));
  }
  return wordWrapped.join("\n");
}

wrapCharacter("You are one uglyassmothafuckingcuntscabsonofabitch, you know that?");


//#14- Function returns a string of characters wrapped to 40 chars per line, but the line is split up by word, if a word is longer than 40 chars, move it to the next line

function wrapWord(inputString){
    var ret = ""; // to return
    var line = ""; // line
    var words = inputString.split(" ");
    words.forEach(function(word) {
        if (word.length > 40){
            ret += line + '\n';
            line = word;
            ret += line + '\n';
            line = ""
        }
        else if (line.length + word.length < 40){
            line += " " + word;
        } else {
            ret += line + '\n';
            line = word;
        }
    }, this);
    ret += line;
    return ret;
}

wrapWord("You are one uglyassmothafuckingcuntscabsonofabitch, you know that?");



/* #15- Function bubbleSort will: Loop through all the elements in the array from left to right. For each element:
  a. Compare it to the one right next to it.
  b. If the current number is larger than the one next to it, then they are clearly not in the right order. Swap the two numbers.
  c. Otherwise, do nothing.
2. Once the loop is over, make a simple decision:
  a. If you swapped any numbers during the loop, then you need to loop again. Go back to step #1
  b. If you did not swap any numbers during the loop, then the array is in order. You can return it.
  */


  function bubbleSort(array) {
    var swaps = true;
    while (swaps == true){
        // PASS
        swaps = false;
        var n = 0;
        while (n + 1 < array.length){
            if (array[n] > array[n + 1]){
                // do a swap
                var temp = array[n];
                array[n] = array[n + 1];
                array[n + 1] = temp;
                swaps = true;
            }
            n++;
        }
    }
}
bubbleSort([3,4,2,1,10,23]);
