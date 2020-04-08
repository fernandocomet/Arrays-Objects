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
