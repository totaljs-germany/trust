# OpenTrust 
TRust is coming from the interoprabilty of the popular programming language Rust and superset webassembly to build high secure and performant app-container.
Just one isolated process with the modules the app just needs.

In a century of Unikernel and NanoVMs, we do need a runtime environment, running legacy total.js apps.
The speedup of reacting on requests was the point why it made scence to me starting this project.

Don't hesitate getting in touch if interessted as well. just leave a message...

## Total.js
Total.js is a fantastic node.js framework i am working with since a long long time and i love it and dont wont to learn such new people i love

the following code changed everything as a developer.
Even if the webassembly file add.wasm was written with C/C++ or Golang or as mentioned Rust, the browser can now work with it.

#
But, there are plenty things to keep in mind always.
So the right pipeline is key.

So i decided in researching a bit more deeper and i found some interessting projects out there in working with low-level and high-level languages like C++ and javaScript, or even Rust and javaScript.


###Emscripten example

```cpp
#include <stdio.h>
#include <emscripten/emscripten.h>

int main() {
    printf("Hello World\n");
    return 0;
}

#ifdef __cplusplus
#define EXTERN extern "C"
#else
#define EXTERN
#endif

EXTERN EMSCRIPTEN_KEEPALIVE void myFunction(int argc, char ** argv) {
    printf("MyFunction Called\n");
}
```

###Cheerp Example

```cpp
// The cheerp/clientlib.h header contains declarations for the browser APIs
#include <cheerp/clientlib.h>

// webMain is the entry point for web applications written in Cheerp
void webMain()
{
        client::console.log("Hello, World Wide Web!");
}
```

```javascript
async function run() {
  const {instance} = await WebAssembly.instantiateStreaming(
    fetch("./add.wasm"),
    env: { abort: () => console.log("Abort!") }
  );
  const r = instance.exports.add(1, 2);
  console.log(r);
}
run();
```
