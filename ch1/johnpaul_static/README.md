1. compile to object

```
g++ -c ./*.cc -I../includes
```

2. create static library `johnpaul.a`

```
ar rvs johnpaul.a john.o johnpaul.o paul.o
```

3. link with it


```
g++ main.cc johnpual.a  -I../includes
```