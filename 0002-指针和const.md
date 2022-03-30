判读const和pointer的关系一直是一个十分烦人的话题  

C++ Primer 5e上有一种很不错的方法判断复合类型的含义，那就是从右往左阅读，离对象最近的符号对对象的类型有最直接的影响：  
e.g.：  
int const \*         pointer to const int  
int const \*const    const pointer to const int  
int \*const          const pointer to int  
int \*const \*        pointer to const pointer to int  
如果读不懂，可以尝试把星号读作Pointer to  

这里有一个规律，星号左边的标识符可以任意调换顺序，右边亦是这样，但是左右边不能乱换。
所以int const\*和const int\*没有什么本质区别
