# WebAssembly_CHAM
<hr>
<h3>To build example file</h3> <br>

$mkdir example // make folder <br>
$cd example // enter example folder <br>
$nano example.c //make c example file <br><br>
#include <stdio.h> <br>
int main(int argc, char ** argv) {<br>
  printf("github by kyu\n"); //**waring** Have to put '\n'. if not, can make error <br>
  return 0;<br>
}<br><br>
$emcc example.c -s WASM=1 -o example.html
<hr>
<h3>How to run Web Assembly</h3> <br>
$cd emsdk <br>
$./emsdk activate --build=Release sdk-incoming-64bit binaryen-master-64bit <br>
$source ./emsdk_env.sh --build=Release <br>
$emcc example.c -s WASM=1 -o example.html <br><br>

  &nbsp;&nbsp;&nbsp;->If want to include some files(ex, txt or img etc.), you need to use other command line <br>
  &nbsp;&nbsp;&nbsp;emcc can not access to files on disks. You just have block of memory. WASM code could be called from JS and also WASM could call JS function. <br>
  &nbsp;&nbsp;&nbsp;So, if want to include some files use under command line without above.
<h5>$emcc example.c -s WASM=1 -o example.html --preload-file /Users/kyu/Desktop/WebAssembly/emsdk/WebTest/</h5>
  &nbsp;&nbsp;&nbsp;'/Users/kyu/Desktop/WebAssembly/emsdk/WebTest/' is the directory path that you want to include.<br><br>
$emrun --no_browser example.html --port 8080 //the browser will run 6931 port. 8080 extends to 6931. <br><br>

Once the HTTP server is running, you can access http://localhost:6931/example.html this link. <br>
If you see 'github by kyu' on console, you are success complie Web Assembly!
