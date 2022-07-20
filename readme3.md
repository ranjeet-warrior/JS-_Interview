21. What are promises and why do we need them ?

Ans. promises are used to handle asynchronous operations in javascript.
     Before promises,callbacks were used to handle asynchronous operations.But due to limited functionality of callbacks,using multiple
     callbacks to handle asynchronous code can lead to unmanageable code.
    promise object has four states :- 
    1. pending :- Initial state of promise.This state represents that the promise has neither been fulfilled nor been rejected,it is in the
                  pending state
   2. fulfilled :- This state represents that promise has been fulfilled, meaning the async operation is completed
   3. Rejected :- This state represents the promise has bee rejected for some reason, meaning the asunc opearation is failed
   4. Settled  :- This opeartion represents that promose has been either rejected or fulfilled.
   
   A promise is created using promise constructor which takes in a callback function with two parameters resolve and reject respectively
   
   resolve() is a function that will be called when the async operation has been successfully Completed
   
   reject() is a function that will be called, when the async operation fails or if some error occurs.
   Example of a promise
   
              function sumOfThreeElements(...elements){ return new Promise((resolve,reject)=>{
             if(elements.length > 3 ){
           reject("Only three elements or less are allowed");
           } else{
          let sum = 0;
        let i = 0;
        while(i < elements.length){
        sum += elements[i];
         i++; }
       resolve("Sum has been calculated: "+sum); }
       }) }
  In the code above, we are calculating the sum of three elements, if the length of the elements array is more than 3, a promise is rejected, or else the promise is resolved and the sum is returned.
  We can consume any promise by attaching then() and catch() methods to the consumer. 
 then() method is used to access the result when the promise is fulfilled.
  catch() method is used to access the result/error when the promise is rejected. In the code below, we are consuming the promise:
  
        sumOfThreeElements(4, 5, 6)
      .then(result=> console.log(result))
      .catch(error=> console.log(error));
     // In the code above, the promise is fulfilled so the then() method gets executed
     sumOfThreeElements(7, 0, 33, 41)
    .then(result => console.log(result))
    .catch(error=> console.log(error));
    // In the code above, the promise is rejected hence the catch() method gets executed
    
22. what is the purpose of async/await keywords ?

Ans.  The async/await keywords enable asynchronous,promise based behaviour to be written in a cleaner style,avoiding the need to explicitly
      configure promise chains.
      
23. What is hoisting ?

Ans. Javascript hoisting refers to the process whereby the interpreter appears to move the declaration of functions,variables or closure to 
     top of their scope,prior to execution of code.
     Hoisting allows functions to be safely used in code before they are declared. variables and class declarations are also hoisted,
     so they can be referenced before they are declared
     
          // using test before declaring
          var test;
         console.log(test); // undefined
         
         // program to display value
         a = 5;
       console.log(a);
       var a; // 5
       
 24. What is DOM ?

Ans.  DOM stands for Document Object Model. DOM is a programming interface for HTML and XML documents.
      When the browser tries to render an HTML document, it creates an object based on the HTML document called DOM. Using this DOM, we can manipulate or change various elements inside the HTML document.
     Example of how HTML code gets converted to DOM :
     
     
                                      <html>
                                     <head>
                                    <title>
                                  DOM Example
                                 </title>
                                </head>
                                <body>
                         <p id = "para1" > Hello </p>
                         <p id = "para2" > Hey   </p>
                        </body>
                        </html>
                        
 25. Differnce between undefined vs not defined vs NaN
 
 Ans. 
     
