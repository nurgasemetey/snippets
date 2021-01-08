###  ctypes pass argument by reference


[Python ctypes: pass argument by reference error - Stack Overflow](https://stackoverflow.com/questions/52204971/python-ctypes-pass-argument-by-reference-error "Python ctypes: pass argument by reference error - Stack Overflow")


 

```
Here's your C++ code reworked to keep the memory around. I just created some local variables with some data since your example wasn't complete:

#define API __declspec(dllexport)  // Windows-specific export
#include <cstdlib>
#include <vector>

using namespace std;

extern "C" {
    API double* myfunction(double* &y, double* &z, int &n_x, int &n_y, int &n_z)
    {
        vector<double> _x {1.1,2.2,3.3};
        vector<double> _y {4.4,5.5};
        vector<double> _z {6.6,7.7,8.8,9.9};

        // Allocate some arrays to store the vectors.
        double* x = new double[_x.size()];
        y = new double[_y.size()];
        z = new double[_z.size()];
        memcpy(x,_x.data(),_x.size() * sizeof(double));
        memcpy(y,_y.data(),_y.size() * sizeof(double));
        memcpy(z,_z.data(),_z.size() * sizeof(double));
        n_x = static_cast<int>(_x.size());
        n_y = static_cast<int>(_y.size());
        n_z = static_cast<int>(_z.size());
        return x;
    }

    // A function to free up the memory.
    API void myfree(double* x, double* y, double* z)
    {
        delete [] x;
        delete [] y;
        delete [] z;
    }
}
Python:

from ctypes import *

dll = CDLL('test')
dll.myfunction.argtypes = (POINTER(POINTER(c_double)),
                           POINTER(POINTER(c_double)),
                           POINTER(c_int),
                           POINTER(c_int),
                           POINTER(c_int))
dll.myfunction.restype = POINTER(c_double)

dll.myfree.argtypes = POINTER(c_double),POINTER(c_double),POINTER(c_double)
dll.myfree.restype = None

# Helper function to allocate storage for return arrays
def myfunction():
    y = POINTER(c_double)() # create an instance of a C double*
    z = POINTER(c_double)()
    n_x = c_int()           # and instances of C int
    n_y = c_int()
    n_z = c_int()

    # Pass them all by reference so new values can be returned
    x = dll.myfunction(byref(y),byref(z),byref(n_x),byref(n_y),byref(n_z))

    # Copies the data into Python lists
    a = x[:n_x.value]
    b = y[:n_y.value]
    c = z[:n_z.value]

    # Free the C arrays and return the Python lists.
    dll.myfree(x,y,z)
    return a,b,c

x,y,z = myfunction()
print(x,y,z)

```
