Building
--------

### Unix and MacOS X

Dependencies: GCC 4.7.3 or later, CMake 2.8.6 or later, and Boost 1.53(but don't use 1.54) or later. You may download them from:
http://gcc.gnu.org/
http://www.cmake.org/
http://www.boost.org/
Alternatively, it may be possible to install them using a package manager.

More detailed instructions for OS X (assume you’re using MacPorts (they’re, however, pretty self-explanatory and homebrew users shouldn't have troubles following it too):

* Install latest Xcode and command line tools (these are in fact MacPorts prerequisites)
* Install GCC 4.8 and toolchain selector tool: `sudo port install gcc48 gcc_select`
* Set GCC 4.8 as an active compiler toolchain: `sudo port select --set gcc mp-gcc48`
* Install latest Boost, CMake: `sudo port install boost cmake`

To build, change to a directory where this file is located, and run `make`. The resulting executables can be found in `build/release/src`.

**Advanced options**:

Parallel build: run `make -j<number of threads>` instead of just `make`.

Debug build: run `make build-debug`.

Test suite: run `make test-release` to run tests in addition to building. Running `make test-debug` will do the same to the debug version.

Building with Clang: it may be possible to use Clang instead of GCC, but this may not work everywhere. To build, run `export CC=clang CXX=clang++` before running `make`.

### Windows

Dependencies: MSVC 2012 or later, CMake 2.8.6 or later, and Boost 1.53(but don't use 1.54) or later. You may download them from:
http://www.microsoft.com/
http://www.cmake.org/
http://www.boost.org/

To build, change to a directory where this file is located, and run this commands: 
```bash
 mkdir build
 cd build
 cmake -G "Visual Studio 11 Win64" ..
```

And then do Build.
Good luck!
