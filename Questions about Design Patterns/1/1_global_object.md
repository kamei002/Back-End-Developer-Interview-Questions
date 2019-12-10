# Why are global and static objects evil? Can you show it wi th a code example?
----

## Because it increases the complexity of the code.
If all of variable are written as global, you must check all of the flow relate to the variable so as to know what is in it.

If the program work asynchronous?　

If the program get huge?

It's too difficult to change code without bug because of the complexity.

However, I don't think all of global and static objects are evil.

It'll work properly if you treat completely controllable number of global object