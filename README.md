# js-functional-programming

**Map & Reduce**
- Map is a higher order function.
- Mapping data from one state, via transformation to another data. 
- First thing it does it, to create a new array. 
- Reduce is the one of the most versatile, powerful function in functional programming. 
- Reducing is basically if you have an initial empty array, and the function is to multiply all elements by two. Then in the first iteration you are combining/reducing the first element and the empty array. Next using the same array and another elemnt you combine/reduce. So basically two things are getting down to one thing. 
- The intiial array is called the accumulator, in reduce function (the result of each iteration)
- The combine function which combines arr value and accumulator, is called the reducer. 
- Our reduce, is two things to one, repeatedly through each element in the array. 
- Array is an object too. Whenever we create an array, an object is there on it with all sorts of functions. 
- Basically the object an array has, has a ____proto____ property which is pointing to the shared object which contains all functions like push, filter etc. 
- This shared object is available to all arrays. This shared object is called array.prototype
- When we do arr.reduce(func, initialVal), the arr is inserted by JS as first param, into the reduce function.

**Functional Composition**
- When we have three functions on an input, we usually go like this: fun1(fun2(fun3(12))). But we can use reduce:
- const output =  reduce([fun1, fun2, fun3], runFunOutput, 0)
- runFunOutput(input, fn){
  return fn(input)}
- Composition is basically reduction of each function with a value. 
- We can use libraries like rambda or lodash to use the compose or pipe functionality. 
- These type of functions are called point free. 


**Purity & Immutability**
- Functions must be highly predictable. 
- Functions need to be pure. 
- This means, a function which is doing something to the input, and also changing something in the global memory, then its impure and it is a side effect. 
- If for example the map functions takes an array and instead of creating the new array, mutates the original one, then its basically changing something in the global memory, this is an impure function.
- We want to ensure that any data that is passed by reference to a function is not mutated. We want to ensure our purity.  

**Closures**
- Lexical Scoping is the feature of JS, which is why closures happen. The function would pick up all data around it before getting off the call stack. This is due to lexical scoping. 
- Lexical scoping is the feature which allows backpacks (closure) to exist.
- 
