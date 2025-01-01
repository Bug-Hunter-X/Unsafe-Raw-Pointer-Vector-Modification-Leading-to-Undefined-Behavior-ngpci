# Rust Raw Pointer Vector Modification Bug

This repository demonstrates a common error in Rust involving the unsafe use of raw pointers with vectors. Modifying a vector's contents via a raw pointer after reallocation can lead to undefined behavior and crashes.  The example showcases the problem and offers a safe solution using standard library functions.

## Bug Description
The original code directly modifies a vector's elements using a raw pointer obtained via `as_mut_ptr()`.  If the vector's capacity is exceeded and needs to reallocate, this raw pointer becomes invalid, resulting in data corruption or a program crash.

## Solution
The solution demonstrates how to avoid this issue by using safe, higher-level methods for vector manipulation.  These methods handle memory management automatically, preventing undefined behavior.