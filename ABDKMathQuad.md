ABDK Math Quad
==============

Library of mathematical functions operating with IEEE 754 quadruple precision
(128 bit) floating point numbers.

Copyright (c) 2019, [ABDK Consulting](https://abdk.consulting/)

All rights reserved.

IEEE 754 Quadruple Precision Floating Point Numbers
---------------------------------------------------

IEEE 754 standard specifies quadruple precision floating point numbers to have:

* sign bit: 1 bit,
* exponent: 15 bits,
* significand precision: 113 bits (112 explicitly stored).

This gives from 33 to 36 significant decimal digits precision.

The minimum strictly positive (subnormal) value is `2^−16494 ≈ 10^−4965`
and has a precision of only one bit.  The minimum positive normal value is
`2^−16382 ≈ 3.3621 × 10^−4932` and has a precision of 113 bits, i.e.
`±2^−16494` as well.  The maximum representable value is
`2^16384 − 2^16271 ≈ 1.1897 × 10^4932`.

The following special values are supported:

* `NaN` (not a number),
* `+Infinity`,
* `-Infinity`.

The format has two zero values: `0` (positive zero) and `-0` (negative zero).

Comparison
----------

Here is the list of comparison functions provided by the library.

    function isNaN (bytes16 x) internal pure returns (bool)

Test whether given quadruple precision floating point number is NaN (not a
number).

    function isInfinity (bytes16 x) internal pure returns (bool)

Test whether given quadruple precision floating point number is infinity, either
positive or negative.

    function sign (bytes16 x) internal pure returns (int8)

Get the sign of a quadruple precision floating point number, i.e. `-1` if
argument is negative, `0` if argument is zero, i.e. `0` or `-0`, and `1` if
argument is positive.

    function cmp (bytes16 x, bytes16 y) internal pure returns (int8)

Compare two quadruple precision floating point numbers, and return `-1` if
`x < y`, `0` if `x = y`, and `1` is `x > y`.  Basically, this function
returns `sign (x - y)`.

    function eq (bytes16 x, bytes16 y) internal pure returns (bool)

Test whether two quadruple precision floating point numbers are equal.

Simple Arithmetic
-----------------

Simple arithmetic functions.

    function add (bytes16 x, bytes16 y) internal pure returns (bytes16)

Add one quadruple precision floating point number to another and return the
result as a quadruple precision floating point number.

    function sub (bytes16 x, bytes16 y) internal pure returns (bytes16)

Subtract one quadruple precision floating point number from another and
return the result as a quadruple precision floating point number.

    function mul (bytes16 x, bytes16 y) internal pure returns (bytes16)

Multiply one quadruple precision floating point number by another and return the
result as a quadruple precision floating point number.

    function div (bytes16 x, bytes16 y) internal pure returns (bytes16)

Divide one quadruple precision floating point number by another and return the
result as a quadruple precision floating point number.

    function neg (bytes16 x) internal pure returns (bytes16)

Calculate the opposite for a quadruple precision floating point number, i.e.
`-x`, and return the result as a quadruple precision floating point number.

    function abs (bytes16 x) internal pure returns (bytes16)

Calculate absolute value of a quadruple precision floating point number and
return the result as a quadruple precision floating point number.

Root, Logarithm, and Exponentiation
-----------------------------------

Root, logarithm, and exponentiation functions.

    function sqrt (bytes16 x) internal pure returns (bytes16)

Calculate the square root of a quadruple precision floating point number and
return the result as a quadruple precision floating point number.

    function log_2 (bytes16 x) internal pure returns (bytes16)

Calculate the binary logarithm of a quadruple precision floating point number
and return the result as a quadruple precision floating point number.

    function ln (bytes16 x) internal pure returns (bytes16)

Calculate the natural logarithm of a quadruple precision floating point number
and return the result as a quadruple precision floating point number.

    function pow_2 (bytes16 x) internal pure returns (bytes16)

Raise 2 to the power of a quadruple precision floating point number, i.e.
calculate `2^x`,  and return the result as a quadruple precision floating
point number.

    function exp (bytes16 x) internal pure returns (bytes16)

Exponentiate a quadruple precision floating point number, i.e. calculate
`e^x`,  and return the result as a quadruple precision floating point number.

Conversions
-----------

Here are conversion functions.

    function fromInt (int256 x) internal pure returns (bytes16)

Convert a signed 256 bit integer number into a quadruple precision floating
point number.

    function toInt (bytes16 x) internal pure returns (int256)

Convert a quadruple precision floating point number into a signed 256 bit
integer number.

    function fromUInt (uint256 x) internal pure returns (bytes16)

Convert an unsigned 256 bit integer number into a quadruple precision floating
point number.

    function toUInt (bytes16 x) internal pure returns (uint256)

Convert a quadruple precision floating point number into an unsigned 256 bit
integer number.

    function from128x128 (int256 x) internal pure returns (bytes16)

Convert a signed 128.128 bit fixed point number into a quadruple precision
floating point number.

    function to128x128 (bytes16 x) internal pure returns (int256)

Convert a quadruple precision floating point number into a signed 128.128 bit
fixed point number.

    function from64x64 (int128 x) internal pure returns (bytes16)

Convert a signed 64.64 bit fixed point number into a quadruple precision
floating point number.

    function to64x64 (bytes16 x) internal pure returns (int128)

Convert a quadruple precision floating point number into a signed 64.64 bit
fixed point number.

    function fromOctuple (bytes32 x) internal pure returns (bytes16)

Convert an octuple precision floating point number into a quadruple precision
floating point number.

    function toOctuple (bytes16 x) internal pure returns (bytes32)

Convert a quadruple precision floating point number into an octuple precision
floating point number.

    function fromDouble (bytes8 x) internal pure returns (bytes16)

Convert a double precision floating point number into a quadruple precision
floating point number.

    function toDouble (bytes16 x) internal pure returns (bytes8)

Convert a quadruple precision floating point number into a double precision
floating point number.