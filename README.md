# Limesharp test

Fork this repo, commit changes after each task and send us the link to your repo (don't do a Pull Request, just send us the link).
We will get back to you shortly. 
Languages accepted: Javascript or PHP. 

### Task 1: 
Make this work (repeat 3 times the contents of an array):
```javascript
repeat([1,2,3]) //[1,2,3,1,2,3,1,2,3]
```
Your solution:
function repeat(array) {
  var arr = [];
  for(var i = 0; i < 3; i++) {
    arr = arr.concat(array);
  }
  return arr;
}

###### if we type in our console your function and repeat([1,2,3]) then the result should be [1,2,3,1,2,3,1,2,3] 

### Task 2:
Make this work (no vowels, lowercase except the first letter):
```javascript
reformat("liMeSHArp DeveLoper TEST") //Lmshrp dvlpr tst
```
Your solution:
function reformat(str) {
    var fixCase = str.charAt(0).toUpperCase() + str.slice(1).toLowerCase();
    var remVowels =  fixCase.replace(/[aeiou]/gi, '');
    return remVowels;
}

###### if we type in our console your function and reformat("liMeSHArp DeveLoper TEST") then the result should be Lmshrp dvlpr tst


### Task 3 (optional, for bonus points):
Make this work (without using any built in functions, only a `for` loop, return the next binary number in a string or as an array)
```javascript
next_binary_number([1,0]) // [1,1]

// possible test cases:
// [1,0] => [1,1]
// [1,1] => [1,0,0]
// [1,1,0] => [1,1,1]
// .......
// [1,0,0,0,0,0,0,0,0,1] => [1,0,0,0,0,0,0,0,1,0]
```
Your solution:
function next_binary_number(array) {
    var i;
	for (i = array.length - 1; i >= 0; i--) {
		if (array[i] === 0) {
        	break;
        }
    }
    if (i === -1) {
      	array.push(0);
      	return array;
    } else {
      	array[i] = 1;
		for (i = i + 1; i < array.length; i++) {
			array[i] = 0;
		}
		return array;
	}
}

###### if we type in our console your function and next_binary_number([1,0,0,0,0,0,0,0,0,1]) then the result should look like 1,0,0,0,0,0,0,0,1,0 (or as an array).

###### If you get invited to the first interview read the What to expect.md file.
