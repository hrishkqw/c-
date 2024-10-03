// copy constructor deep copy
#include <iostream>
using namespace std;
class A{
    public:
    int a=1;
    int b=4;
    int *p= new int;
    
    A(){
    }
    
  A(A &o){
      a= o.a;
      b= o.b;
      p= new int(*o.p);
  }  
};

int main() {
    A o1;
   A o2= o1;
   *o2.p=66;
   cout<<o2.a<<endl;
   cout<<*o2.p;
    
}
