## Functions in Memory (Stack)

Checkout my twitter thread explaining how functions work in memory (stack).

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Here&#39;s how functions behave in the stack (aka memory)<br><br>A thread 🧵<a href="https://twitter.com/hashtag/programming?src=hash&amp;ref_src=twsrc%5Etfw">#programming</a> <a href="https://twitter.com/hashtag/DSA?src=hash&amp;ref_src=twsrc%5Etfw">#DSA</a> <a href="https://twitter.com/hashtag/ALGO?src=hash&amp;ref_src=twsrc%5Etfw">#ALGO</a> <a href="https://twitter.com/hashtag/recursions?src=hash&amp;ref_src=twsrc%5Etfw">#recursions</a> <a href="https://twitter.com/hashtag/stack?src=hash&amp;ref_src=twsrc%5Etfw">#stack</a> <a href="https://twitter.com/hashtag/memory?src=hash&amp;ref_src=twsrc%5Etfw">#memory</a> <a href="https://twitter.com/hashtag/functions?src=hash&amp;ref_src=twsrc%5Etfw">#functions</a></p>&mdash; Khushal Bhardwaj (@CeleronCoder) <a href="https://twitter.com/CeleronCoder/status/1571901815616344065?ref_src=twsrc%5Etfw">September 19, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

Things to keep in mind to understand functions behavior
- When a function is called, it gets in the stack, and stays there until its execution.
- When the function completes executions, it gets off the stack and returns to the program flow.

Here's a program with a main function that call some other functions and that function call some other function. As they get called, they are loaded into the memory stack.
![function_in_stack.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1663609326862/ZjY7jHbnC.png align="left")

When the function, completes execution the functions gets off the stack and the program returns to the previous program flow, aka to the previous function that called that function.
![stack_get_off_1.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1663609353456/J1A2VXHgR.png align="left")
![stack_get_off_2.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1663609358194/WMSIGMGJ5.png align="left")

When there is nothing left in the stack, even the main function that is loaded by default, gets off the stack, the program finishes execution.
![empty_stack.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1663609379835/790Fmj28P.png align="left")

**Takeaways**:
- When the function is called, it is loaded on the stack with its arguments.
- When it completes execution, it gets off the stack and the program returns to its previous program flow.

> If "A" function calls "B" function, "A" function will remain in the stack (and in scope also) until the "B" function returns. It means that not only the currently executing function remains in the function but also all the parent function that called it.