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


# Working with texts in Arrays
## Slice
slice()     --- Returns desired elements in a new array    
