# Arrays-Objects
A compilation of Javascript methods to deal with Array and Objects

# Mutating an Array


## Push
arr.push(...items) – Adds items to the end of an Array

    let arr = ["Juan", "Fer", "Santi", "Luis"]
    arr.push("Mamen");
    // ["Juan", "Fer", "Santi", "Luis", "Mamen"]
    
## Pop
arr.pop() – Extracts an item from the end of an Array

    let arr = ["Juan", "Fer", "Santi", "Luis", "Mamen", "Teresa"]
    arr.push("Teresa");
    // ["Juan", "Fer", "Santi", "Luis", "Mamen"]

## Shift
arr.shift() – Extracts an item from the beginning of the Array

    let arr = ["Perico", "Juan", "Fer", "Santi", "Luis", "Mamen"]
    arr.unshift("Perico");
    // ["Juan", "Fer", "Santi", "Luis", "Mamen"]

## Unshift
arr.unshift(...items) – Adds items to the beginning of the Array

    let arr = ["Juan", "Fer", "Santi", "Luis", "Mamen"]
    arrNew.unshift("Carlos");
    // ["Carlos", "Juan", "Fer", "Santi", "Luis", "Mamen"]
    
# Working with items in Arrays
## Slice
slice()     ---  It returns a new array copying to it all items from index start to end (not including end). 
Both start and end can be negative, in that case position from array end is assumed.*/

    let arr7 = ["t", "e", "s", "t", "s"];
    console.log(arr7.slice(1, 3)); 
    // e,s (copy from 1 to 3)
    console.log(arr7.slice(-2)); 
    // s,t (copy from -2 till the end)

## Splice
Splice --- The splice() method adds/removes items to/from an array, and returns the removed item(s).

    let arr4 = ["I", "study", "JavaScript"];
    arr4.splice(1, 1); // from index 1 remove 1 element
    console.log(arr4); 
    // ["I", "JavaScript"]

    let arr5 = ["I", "study", "JavaScript", "right", "now"];
    // remove 3 first elements and replace them with another
    arr5.splice(0, 3, "Let's", "dance");
    console.log( arr5 ) 
    // now ["Let's", "dance", "right", "now"]

    let arr6 = ["I", "study", "JavaScript"];
    // from index 2, delete 0, then insert "complex" and "language"
    arr6.splice(2, 0, "complex", "language");
    console.log(arr6); 
    // "I", "study", "complex", "language", "JavaScript"

## Concat
Concat --- creates a new array that includes values from other arrays and additional items. */

    let arr8 = [1, 2];
    // create an array from: arr and [3,4]
    console.log(arr8.concat([3, 4])); 
    // 1,2,3,4
    // create an array from: arr and [3,4] and [5,6]
    console.log(arr8.concat([3, 4], [5, 6])); 
    // 1,2,3,4,5,6
    // create an array from: arr and [3,4], then add values 5 and 6
    console.log(arr8.concat([3, 4], 5, 6)); 
    // 1,2,3,4,5,6

## Join
join() --- Converts Array into String

    let arr = ["Pedro", "Juan", "Perico"];
    console.log( arr.join(' ') );
    //"Pedro Juan Perico"

    arr = [1, 2, 3, 4]
    console.log( arr.join('') );
    //"1234"

## Split
Split() --- Converts String into Array

    let str = "The quick brown fox jumps over the lazy dog";
    let strConverted = str.split("");
    console.log(strConverted);
    // ["T", "h", "e", " ", "q", "u", "i", "c", "k", " ", "b", "r", "o", "w", "n", " ", "f", "o", "x", " ", "j", "u", "m", "p", "s", " ", "o", "v", "e", "r", " ", "t", "h", "e", " ", "l", "a", "z", "y", " ", "d", "o", "g"]

    let strConverted2 = str.split(" ");
    console.log(strConverted2);
    // ["The", "quick", "brown", "fox", "jumps", "over", "the", "lazy", "dog"]

## Array.from
 Array.from --- This is a static method that creates an array based on another array or string.

    const newArray = Array.from('hello');
    console.log(newArray);
    // ["h", "e", "l", "l", "o"]

## Array spread operator (...)
(...) -- Spreading arrays using the spread operator (…) allows you to expand the elements in an array. It’s useful when concatenating a bunch of arrays together. 

    //Combine two arrays:
    const spreadableOne = [1, 2, 3, 4];
    const spreadableTwo = [5, 6, 7, 8];
    const combined = [...spreadableOne, ...spreadableTwo];
    console.log(combined);
    // [1, 2, 3, 4, 5, 6, 7, 8]

Also to remove an array element without mutating the original array.

    const animals = ['squirrel', 'bear', 'deer', 'salmon', 'rat'];
    const mammals = [...animals.slice(0,3), ...animals.slice(4)]
    console.log(mammals);
    // ["squirrel", "bear", "deer", "rat"]
    
    
# Iterating an Array
## forEach
forEach()  --- Works as a loop. Applies a function on each item in an array. 

    const items3 = [
        { name: `Bike`, price: 100},
        { name: `TV`, price: 200},
        { name: `Album`, price: 10},
        { name: `Book`, price: 5},
        { name: `Phone`, price: 500},
        { name: `Computer`, price: 1000},
        { name: `Skate`, price: 101},
        { name: `Keyboard`, price: 200},
        { name: `Bottle`, price: 20}
    ]
    
    items3.forEach((item) => {
        console.log(item.name);
    })
    // ["Bike", "TV", "Album", "Book", "Phone", "Computer", "Skate", "Keyboard", "Bottle"]

## Filter
filter()    --- Iterates an array and result is filtered array

    const studentsAge = [17, 16, 18, 19, 21, 17];
    const ableToDrink = studentsAge.filter(age => age > 18);
    console.log("Able to drink are: " + ableToDrink);
    //"Able to drink are: 19,21"
    
    const ableToDrink2 = studentsAge.filter((item) => {
        return item >18 
    })
    console.log(ableToDrink2);
    //[19, 21]

## Map
Map()  --- Iterates an array and result is new array

    const items2 = [
        { name: `Bike`, price: 100},
        { name: `TV`, price: 200},
        { name: `Album`, price: 10},
        { name: `Book`, price: 5},
        { name: `Phone`, price: 500},
        { name: `Computer`, price: 1000},
        { name: `Skate`, price: 101},
        { name: `Keyboard`, price: 200},
        { name: `Bottle`, price: 20},
        { name: `Keyboard`, price: 1000},
    ]
    
    let mapped = items2.map(elem => elem.price * 10)
    console.log(mapped);
    // [1000, 2000, 100, 50, 5000, 10000, 1010, 2000, 200, 10000]

    const itemNames = items2.map((item) => {
        return item.name;
    })
    console.log(itemNames);
    // ["Bike", "TV", "Album", "Book", "Phone", "Computer", "Skate", "Keyboard", "Bottle", "Keyboard"]

## Reduce
reduce()  --- "Reduces" the array into single value (accumulator). Great for calculating totals.

    const numbers = [2, 3, 4, 5];
    var sum = numbers.reduce((sum, elem) => sum + elem)
    console.log(sum)
    // 14

    const items2 = [
        { name: `Bike`, price: 100},
        { name: `TV`, price: 200},
        { name: `Album`, price: 10},
        { name: `Book`, price: 5},
        { name: `Phone`, price: 500},
        { name: `Computer`, price: 1000},
        { name: `Skate`, price: 101},
        { name: `Keyboard`, price: 200},
        { name: `Bottle`, price: 20},
        { name: `Keyboard`, price: 1000},
    ]
    const total = items2.reduce((acumulator, currentItem) => {
        return currentItem.price*10 + acumulator
    }, 0)
    console.log("total = " + total);
    // total = 3136


# More Array methods
## Find 
find() --- useful to find a particular item in array if it returns true then the item exist or else not. Similar to .map() and .filter() it also takes item as a parameter and it checks for an item with name ‘Album’. If there are two items with same then it will only print out the first occurrence of the item.

     const items3 = [
            { name: `Bike`, price: 100},
            { name: `TV`, price: 200},
            { name: `Album`, price: 10},
            { name: `Book`, price: 5},
            { name: `Phone`, price: 500},
            { name: `Computer`, price: 1000},
            { name: `Skate`, price: 101},
            { name: `Keyboard`, price: 200},
            { name: `Bottle`, price: 20}
        ]
    const filteredItems4 = items3.find((item) => {
          return item.name === 'Album' 
    })
    console.log(filteredItems4);
    
    // Object {
    // name: "Album",
    // price: 10
    //}


## Some
Some() --- Checks if any item in an array passes the condition. 
It can also be used similarly to a .forEach() where you would perform an action on each array item and break out of the loop once a truthy value is returned.

    const items = [
        { name: `Bike`, price: 100},
        { name: `TV`, price: 200},
        { name: `Album`, price: 10},
        { name: `Book`, price: 5},
        { name: `Phone`, price: 500},
        { name: `Computer`, price: 1000},
        { name: `Skate`, price: 101},
        { name: `Keyboard`, price: 200},
        { name: `Bottle`, price: 20}
    ]
    const hasInexpensiveItems = items.some((item) => {
        return item.price <= 100;
    })
    console.log(hasInexpensiveItems);
    // true

## Every
Every() --- Similar to .some(), but checks if all items in an array pass a condition.

    const items = [
            { name: `Bike`, price: 100},
            { name: `TV`, price: 200},
            { name: `Album`, price: 10},
            { name: `Book`, price: 5},
            { name: `Phone`, price: 500},
            { name: `Computer`, price: 1000},
            { name: `Skate`, price: 101},
            { name: `Keyboard`, price: 200},
            { name: `Bottle`, price: 20}
        ]
    const hasExpensiveItems = items.every((item) => {
        return item.price >= 100;
    })
    console.log(hasExpensiveItems);
    // false


## Includes
 Includes --- Checks if an array contains a certain value. 
It’s similar to .some(),but instead of looking for a condition to pass, it looks if the array contains a specific value.*/

    //Check if the array includes an item with the string ‘waldo’.
    const names = ['sophie', 'george', 'waldo', 'stephen', 'henry'];
    const includesWaldo = names.includes('waldo');
    console.log(includesWaldo);
    // true
    
    //Includes - Returns true/false
    const items5 = [1, 2, 3, 4, 5];
    const includesTwo = items5.includes(2);
    console.log(includesTwo);
    //true

## Sort
Sort --- sorts the array items into an alphabetical order.*/

    const ages2 = [33, 12, 20, 16, 5, 54, 21, 44, 61, 13, 15, 45, 25, 64, 32];
    const sortAges = ages2.sort((a, b) => a - b);
    console.log(sortAges);
    // [5, 12, 13, 15, 16, 20, 21, 25, 32, 33, 44, 45, 54, 61, 64]

    const names2 = ["Zulema", "Soraya", "Desiree", "Anaconda", "Iloveny"]
    const namesSorted = names2.sort();
    console.log(namesSorted);
    // ["Anaconda", "Desiree", "Iloveny", "Soraya", "Zulema"]

    //Sort companies by start year
    const companies= [
      {name: "Company One", category: "Finance", start: 1981, end: 2004},
      {name: "Company Two", category: "Retail", start: 1992, end: 2008},
      {name: "Company Three", category: "Auto", start: 1999, end: 2007},
      {name: "Company Four", category: "Retail", start: 1989, end: 2010},
      {name: "Company Five", category: "Technology", start: 2009, end: 2014},
      {name: "Company Six", category: "Finance", start: 1987, end: 2010},
      {name: "Company Seven", category: "Auto", start: 1986, end: 1996},
      {name: "Company Eight", category: "Technology", start: 2011, end: 2016},
      {name: "Company Nine", category: "Retail", start: 1981, end: 1989}
    ];
    
    const sortedCompanies  = companies.sort(function(c1, c2) {
      if(c1.start > c2.start) {
        return 1;
      } else {
        return -1;
      }
    });
    console.log(sortedCompanies);

    const sortedCompanies2 = companies.sort((a, b) => (a.start > b.start ? 1 : -1));
    console.log(sortedCompanies2);
    
   # Arrays & Objects
