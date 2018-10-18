# Algorithms

For developers it's important to practice thinking critically, practice problem solving, and think of clean ways to execute a task efficiently. We know our computers can run a millions, even hundreds of mathematical problems in seconds. Writing efficient clean code can help open and run our applications, thus elevating our user experience.



### Print an Array 
 Write a function, call it whatever seems appropriate, and have it print all the items in an array. 

**Inputs:** ['christina', 'nando', 'kenny']

**Output:**
```javascript
    christina
    nando
    kenny
```
<details>
 <summary><strong>hints ...</strong></summary>

* pseudocode!
* I need a function that iterates through my array one by one
* while iterating through the array it will be put into a string 
* it needs to be returned/logged into the console
</details>

#### Solutions 

<details>
    <summary><strong>Click to Reveal...</strong></summary>

```javascript
function printArr(param){
    var string = "";
    for(let i = 0; i < param.length; i++){
        console.log(string += `${param[i]} \n`);
    }
}
```
</details>

____

### Reversing a String
Write a function, name it whatever seems appropriate, and return/log in the console the reverse the the inputted string. 

**Inputs:** 'abcd'

**Output:** 'dcba'

<details>
    <summary><strong>hints...</strong></summary>

* pseudocode!
* so you know there's a new string being outputted. 
* you'll need a loop that will start at the end of the old string
* the loop should then iterate backwards simulatiously concatenating the letters into the new string 
</details>

#### Solutions

<details>
    <summary><strong>Click to reveal...</strong></summary>

```javascript
var reversedString = "";
function reverse(param){
    for(let i = (param.length - 1); i>=0; i--){
        reversedString += param[i]; 
        console.log(reversedString)
    }
}
```
</details>
 
<details>
    <summary><strong>Click to reveal...</strong></summary>

```javascript
function reverse(param) {
    const reverse = [];
    for (let i = (param.length - 1); i >= 0; i -= 1) {
        reverse.push(param[i]);
    }
    console.log(reverse.join(''))
}
```
</details>

#### Source: [leetcode](https://leetcode.com/problems/reverse-string/)
#### Reading: [10 Ways To Reverse A String](http://eddmann.com/posts/ten-ways-to-reverse-a-string-in-javascript/)
____

### Finding the Largest Number 
Write a function call it whatever you ddeem appropriate, return/log in the console the largest value from the array. 

**Input:** [1,2,3,6,9,24,12]

**Output:** 24

### Solution

<details>
<summary><strong>Click to reveal...</strong></summary>

```javascript
function largest(){
    let num = num[0]
    num.forEach((d) => {
        if( d > largest ) { largest = d }
    })
    return largest
}
```
</details>

____

### Print a chess Board 

Write a function that creates a chest board out of a string that represents an 8x8 chess board. 

**Input** 
**Output**
```javascript
 # # # #
# # # # 
 # # # #
# # # # 
 # # # #
# # # # 
 # # # #
# # # # 
```

<details>
<summary><strong>Click to reveal...</strong></summary>

```javascript
function chessBoard(){
    let size = 8;
    let board = "";

    for (let y = 0; y < size; y++) {
        for (let x = 0; x < size; x++) {
            if ((x + y) % 2 == 0) {
                board += " ";
            } else {
                board += "#";
            }
        }
    board += "\n";
    }
    console.log(board);
}
```
</details>

<span>Source:</span> [Eloquent Javascript](http://eloquentjavascript.net/code/#2.3)

____

### Palindrome

Palindromes can be a word, a number, a phrase, a series of characters that is the same forwards and backwards. 

Have a function that takes in a string, checks true or false if the word or number is a paindrome. 

**Inputs/Outputs:**

```javascript
'Anna.'
=> true
'not a palindrome'
=> false
'Civic'
=> true
'A man, a plan, a canal. Panama'
=> true
'Kayak'
=> true
'Never odd or even'
=> true
'Level'
=> true
'Almostomla'
=> false
'1 eye for of 1 eye'
=> false
'Madam'
=> true
'Mom'
=> true
'Noon'
=> true
'Racecar'
=> true
```

<details>
<summary><strong>hints...</strong></summary>

* The toLowerCase() method to return the calling string value converted to lowercase.
* The replace() method to return a new string with some or all matches of a pattern replaced by a replacement. We will use one of the RegExp we just created earlier.
* The split() method splits a String object into an array of strings by separating the string into sub strings.
* The reverse() method reverses an array in place. The first array element becomes the last and the last becomes the first.
* The join() method joins all elements of an array into a string.
* the toString() converts an interger to a string.

</details>

**Solutions**
I have seen many ways to create palindrome functions, I challenge you to think of cleaner, more efficient code than this. 

<details>
<summary><strong>Click to reveal...</strong></summary>

```javascript
function isPalindrome(s) {
  var s = s.toString().toLowerCase();
  let arr = s.split(' ').join('').split(''); 
  for (let i = 0; i < arr.length / 2; i += 1) {
    if (arr[i] !== arr[arr.length - (i + 1)]) {
      return false;
    }
  }
  return true;
}
```

</details>

<details>
<summary><strong>Click to reveal... </strong> </summary>

```javascript
function palindrome(str) {
  var re = /[\W_]/g;
  var lowRegStr = str.toLowerCase().replace(re, '');
  var reverseStr = lowRegStr.split('').reverse().join(''); 
  return reverseStr === lowRegStr;
}
```
**\W** removes all non-alphanumeric characters
* \W matches any non-word character
* \W is equivalent to [^A-Za-z0–9_]
* \W matches anything that is not enclosed in the brackets
**^_** matches anything that does not enclose _ (this is case specific please check the freecodecamp source.)
**/g** the g flag is used for global search
[Source](https://medium.freecodecamp.org/two-ways-to-check-for-palindromes-in-javascript-64fea8191fd7)
<details>