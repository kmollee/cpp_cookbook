
1. compile to object

```
g++ -c -fPIC ./*.cc -I../includes
```

2. create dynamic library `johnpaul.so`

When using `-l<libname>` to specify library to link, the linker will first search for `lib<libname>.so` before searching for `lib<libname>.a`

```
g++ -shared -fPIC  -o libjohnpaul.so john.o johnpaul.o paul.o
```

3. link with it


```
g++ main.cc -ljohnpaul -L. -I../includes
```
