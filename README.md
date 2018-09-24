# WebAssembly_CHAM
<hr>
<h3>How to run Web Assembly</h3> <br>
$cd emsdk <br>
$ ./emsdk install --build=Release sdk-incoming-64bit binaryen-master-64bit <br>
$ ./emsdk activate --build=Release sdk-incoming-64bit binaryen-master-64bit <br>
$ source ./emsdk_env.sh --build=Release <br>

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
$emcc example.c -s WASM=1 -o example.html <br>
$emrun --no_browser example.html --port 8080 //the browser will run 6931 port. 8080 extends to 6931. <br><br>

Once the HTTP server is running, you can access http://localhost:6931/example.html this link. <br>
If you see 'github by kyu' on console, you are success complie Web Assembly!
