# Calling Conventions

## stdcall

1. The calling function pushes the parameters for the called function in reverse order, so the first parameter will be pushed last.
2. Push the current address of ebp and transfer execution to the called function.
3. Set ebp to be equal to esp.
4. Subtract from esp to make space for the called functions parameters.
5. Once the function is done make esp equal to ebp.
6. Pop and return ebp to its location before the function call.
7. The called function does one last action and pops the stack back to where it was before the function was called.

