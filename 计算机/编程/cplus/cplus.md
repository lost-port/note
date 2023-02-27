
##字节对齐方法
    
__attribute__((aligned (n)))，让所作用的结构成员对齐在n字节自然边界上。
如果结构中有成员的长度大于n，则按照最大成员的长度来对齐。
    
    __attribute__:用来设置字节对齐 
    aligned(n):需要对齐的字节数

__alignof__ 
    `alignof 值是结构中的最大元素的对齐大小`

    例子
    #include <iostream>
    struct abc{   
    char a;
    double b;
    int c;
    
    } __attribute__ ((aligned(8)));
    int main()
    {
    std::cout <<__alignof__(struct abc) <<std::endl;
    }