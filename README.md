# clang-no-skip

# Setup
```
$ mkdir clang-test
$ cd clang-test
```
## Dependencies
```
$ brew install cmake
```

### Get all the codes
```
$ wget http://releases.llvm.org/4.0.0/llvm-4.0.0.src.tar.xz
```
Unzip it and rename the folder to `llvm`.
Next get all the other tools.
```
$ cd llvm/tools
$ git clone https://github.com/Deadlyelder/clang-no-skip.git
$ mv clang-no-skip clang
$ cd clang/tools
$ wget http://releases.llvm.org/4.0.0/clang-tools-extra-4.0.0.src.tar.xz
```
Unzip it and rename to `clang-tools-extra-4.0.0` to `clang-tools-extra`

```
$ cd ../../..
$ cd projects
$ wget http://releases.llvm.org/4.0.0/compiler-rt-4.0.0.src.tar.xz
$ mv compiler-rt-4.0.0.src compiler-rt
```

### Building the project
```
$ mkdir build
$ cd build
$ cmake -DCMAKE_BUILD_TYPE=Release -DCMAKE_EXPORT_COMPILE_COMMANDS=ON -DCMAKE_INSTALL_PREFIX=$HOME/local -G "Ninja" .
```
    
