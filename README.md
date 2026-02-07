# FNV Hashing Library

NOTE: This is not versioned yet and needs unit tests. Probably safe, but no garuntees!

This is an implemntation of the public domain [FNV Non-Cryptographic hash function](https://www.ietf.org/archive/id/draft-eastlake-fnv-21.html) created by Glenn Fowler, Landon Curt Noll, and Klem-Phong Vo.

The FNV algorithm is great if you want to make a hashmap in C. [Read here](https://craftinginterpreters.com/hash-tables.html) to see how.

This project is based on the [official fnv library](https://github.com/lcn2/fnv) with changes:

* This library is contained within a single header file, which can be copied directly into your project.
* It is also possible to generate a static library target using the CMake script.
* This library assumes you are using at least C99, and it uses fixed sized integer types from `stdint.h`.
* This library only contains fnv32-1a and fnv64-1a versions of the FNV algorithm, since these are the best for real-world usage.
