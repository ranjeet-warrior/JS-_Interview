32. What is a Temporal Dead Zone ?

Ans. Temporal Dead Zone is the area of block where the variables are inaccessible until the moment the computer completely initializes 
     the value.
     
     
           x = 23; // Gives reference error
           let x;
       function anotherRandomFunc(){
       message = "Hello"; // Throws a reference error
       let message; }
       anotherRandomFunc();
     
33. What is for in loop in JavaScript.Give its Syntax

Ans. for in statement iterates over all enumerable properties of an object that are keyed by strings( ignoring ones keyed by symbols)
     including inherited enumerable properties
     
     const object = { a: 1, b: 2, c: 3 };
     for (const property in object) {
    console.log(`${property}: ${object[property]}`);
    }
     // expected output:
     // "a: 1"
     // "b: 2"
     // "c: 3"
     
34. Write a code to explain map and filter in arrays ?
     
Ans.   map() is used to create a new  
