### swig example 





 

```
kitty.cc
#include <stdio.h>
#include "kitty.h"

kitty::kitty(){
  printf("Constructor\n");
  variable = 100;
}

kitty::~kitty(){
  printf("Destructor\n");
  variable = 0;
}

void kitty::speak(){
  printf("I'm a cat.\n");
}



kitty.h
#include <stdio.h>

class kitty {
 public:
  kitty();
  ~kitty();

  void speak();  
  void speak2(){ printf("totes works\n"); }

 private:
  int variable;

};




 kitty.i
%module kitty
%{
  #include "kitty.h"
%}

%include "kitty.h"



# standard compile options for the c++ executable
FLAGS = -fPIC

# the python interface through swig
PYTHONI = -I/usr/include/python2.6/
PYTHONL = -Xlinker -export-dynamic

# default super-target
all: 
	g++ -fPIC -c kitty.cc -o kitty.o
	swig -c++ -python -o kitty_wrap.cxx kitty.i 
	g++ $(FLAGS) $(PYTHONI) -c kitty_wrap.cxx -o kitty_wrap.o
	g++ $(PYTHONL) $(LIBFLAGS) -shared kitty.o kitty_wrap.o -o _kitty.so
```
