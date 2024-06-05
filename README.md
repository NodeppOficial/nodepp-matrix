# NODEPP-MATRIX

A simple Linear algebra library for Nodepp

## Build & Run
- 🐧: `g++ -o main main.cpp -I ./include ; ./main`
- 🪟: `g++ -o main main.cpp -I ./include -lws2_32 ; ./main`

## Usage
```cpp
#include <nodepp/nodepp.h>
#include <matrix.h>

using namespace nodepp;

void onMain(){

    matrix_t<int> A ( 3, 3 );
    A.set({
        1, 2, 3,
        4, 5, 6,
        7, 8, 9
    });

    matrix_t<int> B ( 1, 3 );
    B.set({ 0, 1, -1 });

    auto C = A * B;

    for( auto &x: C )
         console::log(x);

}
```