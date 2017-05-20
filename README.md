# callbackPromiseAsyncAwait
difference between callback, promise and async/await calling

callbacks in the general definition are just functions that you pass to other functions

a `promise` object allows us to handle success and error cases separately and also allow us to chain multiple asynchronous calls instead of nesting them

But a more recent alternative to working with async code is to use the `async` function, which allows us to treat async code as if it was linear, making it a lot more readable when we need to process things in loops. In my current node version, this feature is behind a harmony flag.

 To consume our readFileAsArray method with `async/await`, we first create an async function, which is just a normal function with the word async before it. Inside the async function, we call the readFileAsArray function as if it returns the lines variable, and to make that work, we use the keyword await. After that, we continue the code as if the readFileAsArray call was synchronous. And to get things to run, we execute the async function. Very simple and more readable. However, to work with errors, we also need to wrap everything in a try/catch call

