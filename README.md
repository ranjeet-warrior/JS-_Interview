# JS-Interview Question and Answers

1. Differnce between '==' and '===' operators ?


. Ans. Both are comparison opeartors.Main differnce between == and === operator in javascript is that == opeator does the type conversion
       of the operands before comparison whereas === operator compares the values as well as data types of operands
       
2. What is spread Opearator?

Ans. Spread syntax(...) allows an iterable such as array expression or string to be expanded in place where zero or more arguments(for function calls)
     or elements (for array literals) are expected,or an object expresssions to be executed in place where zero or more key value are expected
     
3. Differnce between var,let and const?

Ans. In Javascript users can declare variables using 3 keywords that are var,let and const. var keywor is the oldest keyword introduced in ES-6.
     var declarations are globally scoped or function scoped while let and const are block scoped. var variables can be updated and re-declared within its
     scope,let  variables can be updated but not redeclared,const variables can neither be updated nor redeclared.They are hoisted to top of their scope 
     but var variables are initialized with undefined,let and const variables are not initialized but var and let can be declared without being initialized
     const must be initialized during declaration
     
 4. What is Execution context?

Ans. Execution context is the concept of describing internal working of a code.In javascript, the environment that enables the javascript code to get
     executed is what we call javascript execution context.It is the execution context that decides which code section has access to functions,variables
     and objects used in the code during the execution context the specific code gets passed line by line the variables and functions are stored in the 
     memory.An execution context is similar to container that store variables and the code get evalauted and executed 
     
5.  What is meant by First class function in Javascript ?

Ans. A programming language is said to have first class function if function in that language are treated like other variables a function can be passed
     as an argument to other functions,can be returned by another function and can be assigned as a value to a variable.
     
6.  What are closures ?

Ans. A closure is the combination of a function bundled together(enclosed) with reference to its surrounding state(the lexical environment).In other words,
     a closure gives you access to an outer's function scope from an inner function.
     
7. Give an example of closures ?


Ans.     eg..  function outer(){
               var a = 10;
               function inner(){                  //outer function has access to its inner function
               console.log(a);
               }
              return inner; 
      }
      outer()();
    
8.  Explain call(),apply(),and bind() methods ?

Ans. call() :- call is a function that helps you change the context of invoking function
     
     apply() :- apply is very similar to call function,only differnce is that in apply you can pass an array as an argument list
     
     bind()  :- bind is a function that helps us create another function that we can execute with the new context of this keyword



