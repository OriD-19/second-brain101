![[Pasted image 20221216151132.png]]

## 1. Algorithm

*I don't know if this algorithm already has a name. Look it up (maybe) and then come here and update this message!*

Select an item that is the least on the array subset of already ordered elements (So, at the first iteration, we can safely say that such sub array is of length 0)

After that, we insert the element at the correct index, by keeping a key through each iteration of which element we are looking for so far.

So, our first task would be to select the element with the minimum value, and place it at index key = 0.

After that, we increase the value of key.

However, we need to have a copy of the value that we are substituting with each iteration, so what we could do is simply swap both items inside the same array, so that we can keep a single data structure through the whole program.


Keep repeating this process until all the elements are sorted (i.e., when the value of the "key" index is equal to the length of the array).

## 2. Pseudocode for the algorithm

Search for the minimum values in the range of the array ($Key$, $lengthArr - 1$), where $Key$ is a value starting at 0.

Within this range, search for the minimum value, and swap it with the value that is at position $Key$. Repeat this process until the value of $Key$ is equal to the value of $lengthArr - 1$.


```js
function cheap_sort(arr) {
	let key = 0;
	let n = arr.length;
	
	while(key < n - 1) {
		const subArr = arr.slice(key);
		const minVal = Math.min(...subArr);
		
		const indexOfMinVal = subArr.indexOf(minVal) + key;
		
		const temp = arr[key];
		
		arr[key] = arr[indexOfMinVal];
		arr[indexOfMinVal] = temp;
		
		key++;
	}
	
	return arr;
	
}

console.log(cheap_sort([4, -6, 7, 10, 8, 32]));
console.log(cheap_sort([3, 6, 1, -1, 2, 2]));
```