# Algorithms

### Print an Array 
 Write a function, call it whatever seems appropriate, and have it print all the items in an array. 

<details>
 <summary><strong>hints ...</strong></summary>

* pseudocode!
* I need a function that iterates through my array one by one
* while iterating through the array it will be put into a string 
* it needs to be returned/logged into the console
</details>

**Inputs** ['christina', 'nando', 'kenny']

**Output**
```javascript
    christina
    nando
    kenny
```

#### Solutions 
<details>
    <summary><strong>Click to Reveal...</strong><summary>

    ```javascript
    function printArr(param){
        var string = ""
        for(let i = 0; i < param.length; i++){
            console.log(string += `${param[i]} \n`)
        }
    }
    ```

</details>