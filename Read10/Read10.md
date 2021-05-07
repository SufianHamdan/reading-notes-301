#  JavaScript Call Stack

### What is a ‘call’?

At the most basic level, a call stack is a data structure that uses the Last In, First Out (LIFO) principle to temporarily store and manage function invocation (call).


### How many ‘calls’ can happen at once?

one 

### What does LIFO mean?

Last In, First Out.

### Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.

![Example](/Read10/s.png)

### What causes a Stack Overflow?

A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error.

Here is an example:

```js
function callMyself(){
  callMyself();
}

callMyself();
```

The callMyself() will run until the browser throws a “Maximum call size exceeded”. And that is a stack overflow.

**In summary**

The key takeaways from the call stack are:

1. It is single-threaded. Meaning it can only do one thing at a time.
2. Code execution is synchronous.
3. A function invocation creates a stack frame that occupies a temporary memory.
4. It works as a LIFO — Last In, First Out data structure.

We have used the call stack article to lay the foundation for a series we will be looking at on Asynchronous JavaScript (which we will be looking at in another article).