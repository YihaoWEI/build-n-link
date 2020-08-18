# build-n-link
A good programmer should know how to build and link correctly.

### 关于MT MD
以前还有ML，单线程版本。目前VS已不使用。  
/MT是 "multithread, static version ”  
/MD是 "multithread- and DLL-specific version”   
实际使用时候遇到的是OpenCV编译时候的问题
OpenCV默认shared libs时是MT而非shared libs是MD，但某些项目的CMakeList里指定了我们是/MD的，所以我们调用的windows的静态库也需要是MD生成得到的
批量更改modules/属性/c/c++/代码生成/运行时库  MD 就好  
运行时库是代码运行的时候加载的vc++，需要提前确定是dynamic还是static的方式。  
