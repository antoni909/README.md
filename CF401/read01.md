# Node Ecosystem, TDD, CI/CD

## The Assignment

Review, Research, and Discussion
In your reading notes page for this class, provide answers to the following prompts. Cite any external sources

### Map

1. Describe (in plain English) what Array.map() does

### .map() Syntax

  someArr.map(
    (element,
    index,
    array)=>{
      //
    },
    this
  )

### What it does

The JS Array Map method takes in a callback function and an optional 'this' parameter.

### The Params

The callback will take in three parameters of which only the element or index is required. The element is the current element mapped in the array. The index is the index of the current element mapped in the array. The array is the array that the map method is being used on. the value of 'this' can be set after the callback param and will be used whithin the context of the callback itself.

### Why use .map()

We can use the built-in array-method to mutate each individual element in an array and produce a NEW array with desired changes. The element can be of any data-type such as object, string, number. Therefore the return value of each item will be explicitly made inside the code block of the arrow function.

### The anti-pattern

Per the MDN docs,[Array.prototype.map()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map), it is an anti-pattern use of map if :

- will not be using the new array it returns
- will not be returning a value from callback

### Reduce

1. Describe (in plain English) what Array.reduce() does

### .reduce() Syntax

per the MDN docs [Array.prototype.reduce()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce)

  someArr.reduce((accumulator,currentValue,index,array) => {//resulting single val},initialValue)

### The Params

  someArr.reduce(
    (accumulator, // stores initialValue(if provided) and subsequent return values
    currentValue, // the current element in the array being processed by the callback
    index,        // the current index of the element in the arr being processed by the callback
    array)=>{     // the array being acted on by the reduce method
      // code block which returns single value
    },
    initialValue  // if provided as arg, it will be stored in the accumulator as the start value, if not provided the first element is used as the accumulators start value and will be skipped by the callback
  )

### Why use .reduce()

  This array method uses a so called reducer-function as its callback and an optional intialValue to be used at initiation, which if provided, provides a value for the callback to use as the start value at initiation. If no value is provided as the initialValue, then the function accumulator will use the value of the first element as its start value and the reducer callback function will skip the first element and use the second element as the argument to the currentValue parameter.

  This being said, the reduce method will output a single value as its return value after the reducer callback is applied to each element in the array. If it is executed on an empty array, the method will throw an error.

### Superagent

1. Provide code snippets showing how to use superagent() to fetch data from a URL and log the result

- With normal Promise .then() syntax

Using the cat facts API to get cat facts

      const getCatFacts = () => {
      const url = 'https://cat-fact.herokuapp.com/facts'
      superagent
        .get(url)
        .then( result => {
          let catsArray = result.body;
          let catQuotes = catsArray.map( catObject => {
            return catObject.text
          });
          console.log(catQuotes);
        })
        .catch( error => console.error(error));
      };
      getCatFacts();

- Again with async / await syntax

const getCatFacts = async() => {
      const url = 'https://cat-fact.herokuapp.com/facts'
        try{
          let catData = await superagent.get(url);
          let catQuotes = catData.body.map( catObject => {
              return catObject.text
            });
          console.log(catQuotes)
        }catch(e){
        console.error(e)
        }
      };
      getCatFacts();

- Both respond with the following output, an array of cat quotes:

      Promise { <pending> }
      Hint: hit control+c anytime to enter REPL.
      [
        'Wikipedia has a recording of a cat meowing, because why not?',
        'When cats grimace, they are usually "taste-scenting." They have an extra organ that, with some breathing control, allows the cats to taste-sense the air.',
        'Cats make more than 100 different sounds whereas dogs make around 10.',
        "Most cats are lactose intolerant, and milk can cause painful stomach cramps and diarrhea. It's best to forego the milk and just give your cat the standard: clean, cool drinking water.",
        'Owning a cat can reduce the risk of stroke and heart attack by a third.'
      ]

1. Explain promises as though you were mentoring a Code 301 level student

A promise is itself an object that is either in the pending state  or rejected state or resolved state. Once the Promise is either rejected or resolved, you use a callback function that will take that promise and handle it accordingly using .then() or .catch().

1. Are all callback functions considered to be Asynchronous? Why or Why Not?

I used the following reading as a reference to Synchronous and Asynchronous Callback functions in my explanation.

[Are Callbacks Always Asynchronous?](https://dev.to/marek/are-callbacks-always-asynchronous-bah)

I would argue that whether to call a callback  synchronous or asynchronous depends on the order in which it and the parent function are being returned respectively. For example, in an synchronous callback, the parent function has a child callback function as a parameter/argument. In order for the parent function to return, it must wait for the child callback function to return. For example, using array methods as an example where the parent functions are forEach,filter,map,etc, the child callback functions must return a value for each item in the array, then and only then, allowing the parent function to return its expected value.

In asynchronous code, the parent function need not wait for the child callback function to return before it itself can return a value (Promise). This allows the JavaScript Callstack to execute the parent function and refer the respective child callback to be handled by the browser then the callback queue then the eventloop and finally pushed into the JavaScript Callstack.
