# crafting-interpreters-vm

Part III of https://craftinginterpreters.com. This follows the book when implementing a compiler and a virtual machine for the Lox language. This part is implemented in C.

The code for the first part (building an interpreter) can be found [here](https://github.com/pin3da/CraftingInterpreters). This part is implemented in Kotlin.

## Compiling 

``` sh
bazelisk build :all
```

## Running

``` sh
./bazel-bin/main [filename]
```

