ABDK Math 64.64
===============

Library of mathematical functions operating with signed 64.64-bit fixed point
numbers.

Copyright (c) 2019, [ABDK Consulting](https://abdk.consulting/)

All rights reserved.

Signed 64.64 Fixed Point Numbers
--------------------------------

Signed 64.64-bit fixed point number is basically a simple fraction whose
numerator is a signed 128-bit integer and denominator is 2^64.  As long as
denominator is always the same, there is no need to store it, thus in Solidity
signed 64.64-bit fixed point numbers are represented by int128 type holding only
the numerator.

Signed 64.64-bit fixed point numbers combine wide range and decent precision
with good performance, and should be a good fit for most applications that need
to deal with real numbers.

Simple Arithmetic
-----------------

Here is the list of simple arithmetic functions provided by the library.

    function add (int128 x, int128 y) internal pure returns (int128)

Add one signed 64.64 fixed point number to another and return the result as a
signed 64.64 fixed point number.

    function sub (int128 x, int128 y) internal pure returns (int128)

Subtract one signed 64.64 fixed point number from another and return the result
as a signed 64.64 fixed point number.

    function mul (int128 x, int128 y) internal pure returns (int128)

Multiply one signed 64.64 fixed point number by another and return the result as
a signed 64.64 fixed point number.

    function muli (int128 x, int256 y) internal pure returns (int256)

Multiply a signed 64.64 fixed point number by a signed 256-bit integer number
and return the result as a signed 256-bit integer number.

    function mulu (int128 x, uint256 y) internal pure returns (uint256)

Multiply a signed 64.64 fixed point number by an unsigned 256-bit integer number
and return the result as an unsigned 256-bit integer number.

    function div (int128 x, int128 y) internal pure returns (int128)

Divide one signed 64.64 fixed point number by another and return the result as
a signed 64.64 fixed point number.

    function divi (int256 x, int256 y) internal pure returns (int128)

Divide one signed 256-bit integer number by another and return the result as a
signed 64.64 fixed point number.

    function divu (uint256 x, uint256 y) internal pure returns (int128)

Divide one unsigned 256-bit integer number by another and return the result as
a signed 64.64 fixed point number.

    function neg (int128 x) internal pure returns (int128)

Calculate the opposite for a signed 64.64 fixed point number, i.e. `-x`, and
return the result as a signed 64.64 fixed point number.

    function abs (int128 x) internal pure returns (int128)

Calculate absolute value of a signed 64.64 fixed point number and return the
result as a signed 64.64 fixed point number.

    function inv (int128 x) internal pure returns (int128)

Calculate the reciprocal for a signed 64.64 fixed point number, i.e. `1/x`, and
return the result as a signed 64.64 fixed point number.

Average Values
--------------

Here are average value functions.

    function avg (int128 x, int128 y) internal pure returns (int128)

Calculate the arithmetic average of two signed 64.64 fixed point numbers and
return the result as a signed 64.64 fixed point number.

    function gavg (int128 x, int128 y) internal pure returns (int128)

Calculate the geometric average of two signed 64.64 fixed point numbers and
return the result as a signed 64.64 fixed point number.

Power and Root
--------------

Here are power and root functions.

    function pow (int128 x, uint256 y) internal pure returns (int128)

Raise a signed 64.64 fixed point number to a non-negative integer power and
return the result as a signed 64.64 fixed point number.

    function sqrt (int128 x) internal pure returns (int128)

Calculate the square root of a signed 64.64 fixed point number and return the
result as a signed 64.64 fixed point number.

Exponentiation and Logarithm
----------------------------

Here are exponential and logarithm functions.

    function log_2 (int128 x) internal pure returns (int128)

Calculate the binary logarithm of a signed 64.64 fixed point number and return
the result as a signed 64.64 fixed point number.

    function ln (int128 x) internal pure returns (int128)

Calculate the natural logarithm of a signed 64.64 fixed point number and return
the result as a signed 64.64 fixed point number.

    function exp_2 (int128 x) internal pure returns (int128)

Raise 2 to the power of a signed 64.64 fixed point number, i.e. calculate
`2^x`, and return the result as a signed 64.64 fixed point number.

    function exp (int128 x) internal pure returns (int128)

Exponentiate a signed 64.64 fixed point number, i.e. calculate `e^x`, and
return the result as a signed 64.64 fixed point number.

Conversions
-----------

Here are conversion functions.

    function fromInt (int256 x) internal pure returns (int128)

Convert a signed 256 bit integer number into a signed 64.64 bit fixed point
number.

    function toInt (int128 x) internal pure returns (int64)

Convert a signed 64.64 bit fixed point number into a signed 64 bit integer
number.

    function fromUInt (uint256 x) internal pure returns (int128)

Convert an unsigned 256 bit integer number into a signed 64.64 bit fixed point
number.

    function toUInt (int128 x) internal pure returns (uint64)

Convert a signed 64.64 bit fixed point number into a unsigned 64 bit integer
number.

    function from128x128 (int256 x) internal pure returns (int128)

Convert a signed 128.128 bit fixed point number into a signed 64.64 bit fixed
point number.

    function to128x128 (int128 x) internal pure returns (int256)

Convert a signed 64.64 bit fixed point number into a signed 128.128 bit fixed
point number.
