6. What are closures ? give an example of closures ?

Ans. Closures are an ability of a function to remember the variables and functions that are declared in its outer scope.

    example.     var Person = function(pName){
                 var name = pName;
                 
                 this.getName = function() {
                 return name;
                 }
                 }
                 var Person = new Person("Ranjeet");
                 console.log(Person.getName());
                 
7. Explain call(), apply() and, bind() methods. Give an example of call(), apply(), bind()

Ans. 1. call():
                It’s a predefined method in javascript.
                This method invokes a method (function) by specifying the owner object. 
                
                Example 1:  function sayHello(){
                            return "Hello " + this.name;
                           }
                           var obj = {name: "Sandy"}; sayHello.call(obj);
                           // Returns "Hello Sandy"
  call() method allows an object to use the method (function) of another object.
              
              Example 2:    var person = {
                            age: 23,
                           getAge: function(){
                          return this.age; }
                       }
                     var person2 = {age: 54}; person.getAge.call(person2); // Returns 54
    
   2. apply():
                 The apply method is similar to the call() method. The only difference is that,
                 call() method takes arguments separately whereas, apply() method takes arguments as an array.  
                 
           Example 1:    function saySomething(message){ 
                         return this.name + " is " + message;
                            }
                        var person4 = {name: "John"}; 
                        saySomething.apply(person4, ["awesome"]);
   3. bind():  
               This method returns a new function, where the value of “this” keyword will be bound to the owner object, which is provided as a parameter.
               
               
          Example with arguments:     var bikeDetails = {
                                displayDetails: function(registrationNumber,brandName){
                             return this.name+ " , "+ "bike details: "+ registrationNumber + " , " + brandName;
                          } }
                          var person1 = {name: "Vivek"};
                  var detailsOfPerson1 = bikeDetails.displayDetails.bind(person1, "TS0122", "Bullet"); // Binds the displayDetails function to the person1              
             detailsOfPerson1();
           // Returns Vivek, bike details: TS0452, Thunderbird    
           
  8. What is creation phase and execution phase ?
  
  Ans.  Creation phase : Compiler runs through the entire code for 2 time before actually executing the code,
        In the first run, It picks all function declarations and stores them in memory with their reference.
        In the second run, It picks all variables and assign undefined to them. In the event of a conflict between variable
        and function declaration name then that variable is ignored.
        
  Execution Phase :
                 Variables assigned with values
                 Functions executed
 9.What are objects in javascript ?
 
 Ans. The Object type represents one of JavaScript's data types. It is used to store various keyed collections and more complex entities. Objects can be        created using the Object() constructor or the object initializer / literal syntax.
     
    const person = {
     firstName: "John",
     lastName: "Doe",
     age: 50,
    eyeColor: "blue"
     };
     
10. What are function constructors ?

Ans. The function constructors create a new function object, calling the constructor directly and can create functions dynamically,but suffer from security
     and similar issues.However unlike eval,function constructors creates functions which executes in global scope only
     
    // constructor function
      function Person () {
    this.name = 'John',
    this.age = 23,

     this.greet = function () {
        console.log('hello');
    }
    }

    // create objects
    const person1 = new Person();
    const person2 = new Person();

    // access properties
     console.log(person1.name);  // John
     console.log(person2.name);  // John
     
11. Explain prototypes ?

Ans. Prototypes is an object that is associated with every functions and objects by default in javascript where function's prototypes properly is
     accessible and modifiable and object's prototypes is not visible. Every function includes prototype objects by default
     
            function Person () {
    this.name = 'John',
    this.age = 23
     }

    const person = new Person();

    // checking the prototype value
    console.log(Person.prototype); // { ... }   
    
12. What is prototype chain ?

Ans. Every object has a prototype including prototype object. This chain gives all the way back until it reads the object that has no prototype
     usually object's prototype
     
     
         function Dog(name) {
         this.name = name;
         }
         
         / Returns true
      Object.prototype.isPrototypeOf(Dog.prototype);
      
13. Give an example of inheritance using function constructor

Ans.     function human(name, age, money) {
         animal.call(this, name, age);
         this.money = money;
        }  
        
  human.prototype = Object.create(animal.prototype);

14.What are callbacks?

Ans. callback function is a function passed into another function as an argument, which is then invoked inside the outer function to complete
     some kind of routine or action.
     
     
         // function
      function greet(name, callback) {
    console.log('Hi' + ' ' + name);
    callback();
     }

     // callback function
     function callMe() {
    console.log('I am callback function');
     }

    // passing function as an argument
     greet('Peter', callMe);     
     
 15. What is the use of setTimeout

Ans The setTimeout() method executes a block of code after the specified time.The method executes the code only once.The commonly used 
    syntax of javascript setTimeout is 
                     setTimeout(function,milliseconds);
                     
                     
                     
                             // program to display a text using setTimeout method
                function greet() {
              console.log('Hello world');
              }
            setTimeout(greet, 3000);
           console.log('This message is shown first');

16. What is an event loop and call stack?

Ans. The event loop is the secret behind JavaScript’s asynchronous programming. JS executes all operations on a single thread, but using a few smart data structures, it gives us the illusion of multi-threading. Let’s take a look at what happens on the back-end.

call stack :  A call stack is a mechanism for an interpreter (like the JavaScript interpreter in a web browser) to keep track of its place in a script that calls multiple functions — what function is currently being run and what functions are called from within that function, etc.

When a script calls a function, the interpreter adds it to the call stack and then starts carrying out the function.
Any functions that are called by that function are added to the call stack further up, and run where their calls are reached.
When the current function is finished, the interpreter takes it off the stack and resumes execution where it left off in the last code listing.
If the stack takes up more space than it had assigned to it, it results in a "stack overflow" error.

           function greeting() {
      // [1] Some code here
       sayHi();
      // [2] Some code here
     }
     function sayHi() {
     return "Hi!";
    }

     // Invoke the `greeting` function
      greeting();

    // [3] Some code here

 


     

     


           
                        
                        
                        
                        
                        
