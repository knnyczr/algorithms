# Algorithms

For Developer's it's important to practice thinking critically, and coming up with solutions with the language you want to practice with. The following problems can be solved with any programming language you can think of. For this Repo we'll be using javascript. 

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
    <summary><strong>Click to reveal...</strong><summary>

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