# The Call Stack

In Javascript, when a funciton is called it gets sent to the Call Stack. The call stack is the part of memory the browser or enginer dedicates just to these functions. Well some part of JS are asychronous, the call stack is not. It can only deal with one function at a time, part of JS having a single thread. This means that when a function alls another function is added to the stack.

The call stack uses the principle of Last In, First Out. The last function to be called, the one on the top of the list, is the first one taken of the list. This happens when the program his the the return in the function. This takes it off the stack and sends the return value to function that called it. This process goes down the call stack until all the fuctions have hit their returns.

If you have a case where a function calls itself, or the chain of functions returns to the intial function, the call stack will keep growing and growing and growing. Due to this, browsers have a set limit for call stacks. Go past this size, and the program will crash.