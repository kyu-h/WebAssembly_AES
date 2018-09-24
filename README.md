# WebAssembly_CHAM
<hr>
<h3>To build example file</h3> <br>

$mkdir example // make folder <br>
$cd example // enter example folder <br>
$nano example.c //make c example file <br>
#include <stdio.h> <br>
int main(int argc, char ** argv) {<br>
  printf("github by kyu\n"); //**waring** Have to put '\n'. if not, can make error <br>
  return 0;<br>
}<br>
$emcc example.c -s WASM=1 -o example.html
$emrun --no_browser example.html --port 8080 //the browser will run 6931 port. 8080 extends to 6931. <br>

<hr>
