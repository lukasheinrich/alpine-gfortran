# cmplopes/alpine-gfortran
Docker GNU Fortran, gdb and make over Alpine Linux

```
$ docker pull -t cmplopes/alpine-gfortran:[TAG]
```

## Suported Tags

[edge - (gfortran 6.4.0-r8 over alpine:edge) (Dockerfile)](https://github.com/cmplopes/alpine-gfortran/blob/master/edge/Dockerfile)

[6.4, latest - (gfortran 6.4.0-r8 over alpine:3.8) (Dockerfile)](https://github.com/cmplopes/alpine-gfortran/blob/master/6.4/Dockerfile)

[6.3 - (gfortran 6.3.0-r4 over alpine:3.6) (Dockerfile)](https://github.com/cmplopes/alpine-gfortran/blob/master/6.3/Dockerfile)

[6.2 - (gfortran 6.2.1-r1 over alpine:3.5) (Dockerfile)](https://github.com/cmplopes/alpine-gfortran/blob/master/6.2/Dockerfile)

[5.3 - (gfortran 5.3.0-r0 over alpine:3.4) (Dockerfile)](https://github.com/cmplopes/alpine-gfortran/blob/master/5.3/Dockerfile)


## Check GNU Fortran version
```
$ docker run --rm -it -v $(pwd):/source cmplopes/alpine-gfortran:6.3
```
or
```
$ docker run --rm -it -v $(pwd):/source cmplopes/alpine-gfortran:6.3 gfortran --version
```

## Compile, link and run a Fortran program
```
$ docker run --rm -it -v $(pwd):/source cmplopes/alpine-gfortran:6.3 gfortran -Wall -o test /source/test.f90
$ docker run --rm -it -v $(pwd):/source cmplopes/alpine-gfortran:6.3 ./test
```
