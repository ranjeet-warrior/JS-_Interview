41. Create a button , on click of which new Heading tag h1 should be added with text as "MERN stack" on the screen above button
    
Ans.   <button>Click</button>
       

42. Write code to get 1st H1 element from a webpage using DOM

Ans. var h1Text = document.querySelector(".entry-title").textContent;

43. Write code to implement timer clock using JS -- display HH:MM:SS -- the time should keep updating every second

Ans.         const Digital_Clock = () => {
             const date = new Date();
             let hrs = time.getHours();
             let min = time.getMinutes();
             let sec = time.getSeconds();     
            }

44. Create an HTML page having content as Hello world and a button named Replace Text. When user will click on this button page content should be changed             to "Welcome to Elevation academy"

Ans. <body>
    <h1 id = "heading">Hello World</h1>
    <button id = "btn">Replace Text</button>
    </body>
    document.getElementById("btn").onclick="Elevation Academy";



45.Create an HTML page having content as Hello world and a button named "Hide Text." When user will click on this button hide the "Hello World" text

Ans. <body>
  <h1 id = "heading">Hello World</h1>
  <button id = "btn"> Hide Text </button>
  </body>
  document.getElementById("btn").onclick =" ";
  
46.Given an array of 0's and 1's find out number of 0's

Ans.            

                     <script>
                        // A divide and conquer solution to find count of zeroes in an array
                       // where all 1s are present before all 0s
 
                        /*
                    * if 0 is present in arr then returns the index of FIRST occurrence of 0 in
                    * arr[low..high], otherwise returns -1
                    */
                    function firstZero(arr , low , high) {
                    if (high >= low) {
         
                  // Check if mid element is first 0
                  var mid = low + parseInt((high - low) / 2);
                 if ((mid == 0 || arr[mid - 1] == 1) && arr[mid] == 0)
                  return mid;
 
               if (arr[mid] == 1) // If mid element is not 0
                return firstZero(arr, (mid + 1), high);
               else // If mid element is 0, but not first 0
                return firstZero(arr, low, (mid - 1));
        }
        return -1;
    }
 
         // A wrapper over recursive function firstZero()
         function countZeroes(arr , n)
         {
     
        // Find index of first zero in given array
        var first = firstZero(arr, 0, n - 1);
 
        // If 0 is not present at all, return 0
        if (first == -1)
            return 0;
 
        return (n - first);
    }
 
    // Driver program to test above functions
 
        var arr = [ 1, 1, 1, 0, 0, 0, 0, 0 ];
        var n = arr.length;
        document.write("Count of zeroes is " + countZeroes(arr, n));
 
      // This code is contributed by gauravrajput1
      </script>

47.Given an array find out total no. of odd and even nos.

Ans.                                      

                            function CountingEvenOdd(arr, arr_size)
                            {
                              let even_count = 0;
                              let odd_count = 0;
 
                           // loop to read all the values in the array
                           for (let i = 0; i < arr_size; i++) {
         
                          // checking if a number is completely
                          // divisible by 2
                          if (arr[i] & 1 == 1)
                         odd_count++;
                      else
                         even_count++;
                       }
 
    document.write("Number of even elements = " + even_count
        + "<br>" + "Number of odd elements = " + odd_count);
                      }


48.Given a string find out number of vowels 

                         


                             const findVowels = str => {
                                let count = 0
                              const vowels = ['a', 'e', 'i', 'o', 'u'] 
                             for(let char of str.toLowerCase()) {
                           if(vowels.includes(char)) { count++
                              } }
                            return count }



49.Write a code to create two objects with 2 properties each, one will be string and other will be an array. Create a function to check if all the elements of the arrays in both the objects are same

                                         const obj1 = {
                                         firstname = "Ranjeet",
                                         lastname. = "Kumar",
                                         }
                                         const obj2 = {
                                         new_array = [1,2,3,4,5],
                                         new_array2=[6,7,8,9,10]
                                         }
                                         function check(){
                                         
                                         
                                         }
                                         
                                         
                                         
