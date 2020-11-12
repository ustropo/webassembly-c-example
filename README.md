# WebAssembly in C - Example

A simple example to create a WebAssemby code using C.

## Environment setup

To compile, you must install Emscripten compiler.

```bash
cd ~/
git clone https://github.com/emscripten-core/emsdk.git
cd emsdk
./emsdk install latest
./emsdk activate latest
```

Add variables to PATH:

```bash
source ./emsdk_env.sh
```

## Compiling

To compile the code: 

```bash
emcc add.c -o add.js
```

This will create two files: `add.js` and `add.wasm`.

## Serving

Install the package `http-server` for the node application to be able to serve the html file:

```bash
npm install -g http-server
```

And start it:

```bash
http-server
```

Now, open the browser and access `http://localhost:8080/add.html` and you will see the page.

## More information

To know more details about it, check the article [here](https://medium.com/vacatronics/how-to-write-a-webassembly-app-in-c-c-6c560438a844?source=friends_link&sk=5aa4c2bd68fb6295c7cd7209052d2357).
