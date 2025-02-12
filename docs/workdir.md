# workdir structure
```
$workdir
- $pkg-$ver   pointed by $pkgworkdir
  - env       list of environment variables
  - state     current state of building
  - src       unpacked source files
    - src[0]
    - src[1]
    ...
  - build     build directory, pointed by $builddir
  - image     temporal install destination
```
