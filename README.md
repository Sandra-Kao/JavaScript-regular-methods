# JavaScript-regular-methods

對於幾個常用的方法做個筆記


> //Meth.floor()
> //returns the largest integer less than or equal to a given number, not a NaN.

Math.floor(5.914) //5

Math.floor(-5.914) //-6

Math.floor(null) //0

> /Set()
> //Store unique values of any type, whether primitive values or object references.

let mySet = new Set()

mySet.add(1)           // Set [ 1 ]

mySet.add(5)           // Set [ 1, 5 ]

mySet.add(5)           // Set [ 1, 5 ]

mySet.add('some text') // Set [ 1, 5, 'some text' ]

let o = {a: 1, b: 2}

mySet.add(o)              // Set [ 1, 5, 'some text', {...}]

mySet.add({a: 1, b: 2})   // o is referencing a different object, so this is okay
                          // Set [ 1, 5, 'some text', {...}, {...}]

mySet.has(5)              // true

mySet.has(3)              // false, since 3 has not been added to the set

mySet.has(Math.sqrt(25))  // true

mySet.has('Some Text'.toLowerCase()) // true

mySet.has(o)       // true

mySet.size         // 5

> //Array.pop()
> //Removes thr last element from an array and returns that element. This method changes the length of the array.

const plants = ['broccoli', 'cauliflower', 'cabbage', 'kale', 'tomato'];

console.log(plants.pop()); // "tomato"

console.log(plants); // Array ["broccoli", "cauliflower", "cabbage", "kale"]

plants.pop();

console.log(plants); // Array ["broccoli", "cauliflower", "cabbage"]

> //Array.shift()
> //Returns the first element from an array and returns that removed element or undefind if the array is empty. This method changes the length of the array.

const arrayShift = [1, 2, 3];

const firstElement = arrayShift.shift();

console.log(arrayShift); // Array [2, 3]

console.log(firstElement); // 1

> //Array.unshift()
> //Adds one or more elements to the beginning of an array and returns the new length of the array.

const arrayUnshift = [1, 2, 3];

console.log(arrayUnshift.unshift(4, 5)); // return length = 5

console.log(arrayUnshift); // Array [4, 5, 1, 2, 3]

> //Array.includes()
> //Whether an array includes a certain value among its entrues, returning true or false ad appropriate.

const array1 = [1, 2, 3];

console.log(array1.includes(2)); // true

const pets = ['cat', 'dog', 'bat'];

console.log(pets.includes('cat')); // true

console.log(pets.includes('at')); // false

> //Set.has()
> //Returns a boolean indicating whether an element with the specified value exists in a Set object or not.

const set1 = new Set([1, 2, 3, 4, 5]);

console.log(set1.has(1)); // true

console.log(set1.has(5)); // true

console.log(set1.has(6)); // false

> //Array.slice()
> //Returns a shallow copy of into a new array object selected from start to end (start stay and end gone). The original array will not be modified.

const animals = ['ant', 'bison', 'camel', 'duck', 'elephant'];

console.log(animals.slice(1));
> // expected output: Array ['bison', "camel", "duck", "elephant"]

console.log(animals.slice(2, 4));
> // expected output: Array ["camel", "duck"]

console.log(animals.slice(2, 5));
> // expected output: Array ["camel", "duck", "elephant"]

> //Array.splice()
> //Changes the contents of an array by removing or replacing existing elements and/or adding new elements in place.

const months = ['Jan', 'March', 'April', 'June'];

months.splice(1, 0, 'Feb'); // remove no element at index 1 and inserts 'Feb' at index 1 

console.log(months); // ["Jan", "Feb", "March", "April", "June"]

months.splice(4, 1, 'May');// replaces 1 element at index 4

console.log(months); // ["Jan", "Feb", "March", "April", "May"]

> //String.split()
> //Divides a String into an ordered list of substrings, puts these substrings into an array, and returns the array.

const str = 'The quick brown fox jumps over the lazy dog.';

const words = str.split(' ');

console.log(words[3]); // "fox"

const chars = str.split('');

console.log(chars[4]); // "q"

> //Array.reverse()
> //Reverses an array in place. Thr first arrat elemrnt becomes the last, and the last array becomes the first.

const arrayReverse = [[1,1,1],[2,2,2],[3,3,3]]

arrayReverse.reverse(); // [[3,3,3],[2,2,2],[1,1,1]]

> //Array.join()
> //Creats and returns a new string by concatenating all of the elements in an array (or an array like object), separated by a specified separtor string.
> //If the array has only one item, them that item will be returned without using the separator.

const elements = ['Fire', 'Air', 'Water'];

elements.join('-'); //Fire-Air-Water

elements.join(' '); //Fire Air Water

elements.join('');  //FireAirWater

const elementOne = ['Fire'];

elements.join('-'); //Fire

elements.join(' '); //Fire

elements.join('');  //Fire


> //Array.concat()
> //The concat() method is used to merge two or more arrays. This method does not change the existing arrays, but instead returns a new array.

const array1 = ['a', 'b', 'c'];

const array2 = ['d', 'e', 'f'];

array1.concat(array2); // Array ["a", "b", "c", "d", "e", "f"]
