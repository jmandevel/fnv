# FNV Hashing Library

This is an implemntation of the public domain [FNV Non-Cryptographic hash function](https://www.ietf.org/archive/id/draft-eastlake-fnv-21.html) created by Glenn Fowler, Landon Curt Noll, and Klem-Phong Vo.

## Differences from Official Library

The code in this repository is based on the [official fnv library](https://github.com/lcn2/fnv) with changes. This version of the fnv library is designed for ease of use.

* This library contained within a single header file, which can be copied directly into your project.
* It is also possible to generate a static library target using the CMake script.
* This library assumes you are using at least C99, and it only uses fixed sized integer types from `stdint.h`.
* This library includes only includes fnv32-1a and fnv64-1a versions of the FNV algorithm, since these are the best for real-world usage.