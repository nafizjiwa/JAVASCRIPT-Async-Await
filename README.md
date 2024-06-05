# JAVASCRIPT-Async-Await



async...await is syntactic sugar built on promises and generators. (not new functionality). <br>
Declare an async function with the keyword async. <br>
Inside an async function we use the await operator to pause execution of our function until an asynchronous action completes .<br>
await returns the resolved value of the awaited promise. <br>
We can write multiple await statements to produce code that reads like synchronous code. <br>
We use try...catch statements within our async functions for error handling. <br>
Usingawait Promise.all take advantage of concurrency by writing async functions that allow asynchronous actions to happen in concurrently. <br>
To declare an async function:

    async function funcName() {
    
    }
This is the syntax for using the await operator: <br>

    const variableName = await returnsPromise(); 

Promise.all takes in an array of promises and returns a single array of resolved promises<br>

    async function myFunction() {
      let myArray = await Promise.all([returnsPromise1(), returnsPromise2(), returnsPromise3() ]);
    }
  console.log(`Dinner is served. We're having ${myArray[0}}, ${myArray[1]}, ${myArray[2}}, ${myArray[3]}.`);

`await` halts the execution of our async function. This allows us to conveniently write synchronous-style code to handle dependent promises <br>
A function with a try catch statement

    async function functionName() {
        try {
           let dinner = await cookBeanSouffle();
           console.log(`${dinner} is served!`);
        }
        catch (error) { //specifies and identifier error
          console.log(error);
          }
    }

the async...await version more closely resembles synchronous code, which helps developers maintain and debug their code. <br>
The async...await syntax also makes it easy to store and refer to resolved values from promises further back in our chain which is a much more difficult task with native promise syntax. <br>

