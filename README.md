About Emscripten
Emscripten is a complete Open Source compiler toolchain to WebAssembly. Using Emscripten you can:

Compile C and C++ code, or any other language that uses LLVM, into WebAssembly, and run it on the Web, Node.js, or other Wasm runtimes.

Compile the C/C++ runtimes of other languages into WebAssembly, and then run code in those other languages in an indirect way (for example, this has been done for Python and Lua).

Practically any portable C or C++ codebase can be compiled into WebAssembly using Emscripten, ranging from high-performance games that need to render graphics, play sounds, and load and process files, through to application frameworks like Qt. Emscripten has already been used to convert a very long list of real-world codebases to WebAssembly, including commercial codebases like the Unreal Engine 4 and the Unity engine. For examples and demos, see the community-maintained list on the wiki.

Emscripten generates small and fast code! Its default output format is WebAssembly , a highly optimizable executable format, that runs almost as fast as native code, while being portable and safe. Emscripten does a lot of optimization work for you automatically, by careful integration with LLVM, Binaryen, Closure Compiler, and other tools.


Porting code to use Emscripten
Emscripten support for portable C/C++ code is fairly comprehensive. Support for the C standard library, C++ standard library, C++ exceptions, etc. is very good, as is SDL2 and other APIs. OpenGL support in Emscripten support is excellent for OpenGL ES 2.0-type code, and acceptable for other types.

There are differences between the native and Emscripten Runtime Environment, which mean some changes usually need to be made to the native code. That said, many applications will only need to change the way they define their main loop, and also modify their file handling to adapt to the limitations of the browser/JavaScript.

There are also limitations that can make some code easier to port — read Portability Guidelines to determine where you may need to spend more effort.
