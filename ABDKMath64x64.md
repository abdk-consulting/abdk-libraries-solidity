ABDK Math 64.64
===============

Library of mathematical functions operating with signed 64.64-bit fixed point numbers.

Copyright (c) 2019, [ABDK Consulting](https://abdk.consulting/)

All rights reserved.

Signed 64.64 Fixed Point Numbers
--------------------------------

Signed 64.64-bit fixed point number is basically a simple fraction whose
numerator is a signed 128-bit integer and denominator is 2^64.  As long as
denominator is always the same, there is no need to store it, thus in Solidity
signed 64.64-bit fixed point numbers are represented by int128 type holding only
the numerator.

Signed 64.64-bit fixed point numbers combine wide rage and decent precision with
good performance, and should be a good fit for most applications that need to deal
with real numbers.

Simple Arithmetic
-----------------

Here is the list of simple arithmetic functions provided by the library.

    function add (int128 x, int128 y) internal pure returns (int128)

Add one signed 64.64 fixed point number to another and return result as signed
64.64 fixed point number.

    function sub (int128 x, int128 y) internal pure returns (int128)

Subtract one signed 64.64 fixed point number from another and return result as
signed 64.64 fixed point number.

    function mul (int128 x, int128 y) internal pure returns (int128)

Multiply one signed 64.64 fixed point number by another and return result as
signed 64.64 fixed point number.

    function muli (int128 x, int256 y) internal pure returns (int256)

Multiply signed 64.64 fixed point number by signed 256-bit integer number and
return result as signed 256-bit integer number.

    function mulu (int128 x, uint256 y) internal pure returns (uint256)

Multiply signed 64.64 fixed point number by unsigned 256-bit integer number and
return result as unsigned 256-bit integer number.

    function div (int128 x, int128 y) internal pure returns (int128)

Divide one signed 64.64 fixed point number by another and return result as
signed 64.64 fixed point number.

    function divi (int256 x, int256 y) internal pure returns (int128)

Divide one signed 256-bit integer number by another and return result as signed
64.64 fixed point number.

    function divu (uint256 x, uint256 y) internal pure returns (int128)

Divide one unsigned 256-bit integer number by another and return result as
signed 64.64 fixed point number.

    function neg (int128 x) internal pure returns (int128)

Calculate opposite for signed 64.64 fixed point number, i.e. `-x`, and return
result as signed 64.64 fixed point number.

    function abs (int128 x) internal pure returns (int128)

Calculate absolute value of signed 64.64 fixed point number and return result as
signed 64.64 fixed point number.

    function inv (int128 x) internal pure returns (int128)

Calculate reciprocal for signed 64.64 fixed point number, i.e. `1/x`, and
return result as signed 64.64 fixed point number.

Average
-------

Here are average functions.

    function avg (int128 x, int128 y) internal pure returns (int128)

Calculate arithmetic average of two signed 64.64 fixed point numbers and return
result as signed 64.64 fixed point number.

    function gavg (int128 x, int128 y) internal pure returns (int128)

Calculate geometric average of two signed 64.64 fixed point numbers and return
result as signed 64.64 fixed point number.

Power and Root
--------------

Here are power and root functions.

    function pow (int128 x, uint256 y) internal pure returns (int128)

Raise signed 64.64 fixed point number to non-negative integer power and return
result as signed 64.64 fixed point number.

    function sqrt (int128 x) internal pure returns (int128)

Calculate square root of signed 64.64 fixed point number and return result as
signed 64.64 fixed point number.

Exponent and Logarithm
----------------------

Here are exponent and logarithm functions.

    function log_2 (int128 x) internal pure returns (int128)

Calculate binary logarithm of signed 64.64 fixed point number and return
result as signed 64.64 fixed point number.

    function ln (int128 x) internal pure returns (int128)

Calculate natural logarithm of signed 64.64 fixed point number and return
result as signed 64.64 fixed point number.

    function exp_2 (int128 x) internal pure returns (int128)

Calculate binary exponent of signed 64.64 fixed point number, i.e. `2^x` and
return result as signed 64.64 fixed point number.

    function exp (int128 x) internal pure returns (int128)

Calculate natural exponent of signed 64.64 fixed point number, i.e. `e^x` and
return result as signed 64.64 fixed point number.

Conversions
-----------

Here are conversion functions.

    function fromInt (int256 x) internal pure returns (int128)

Convert signed 256-bit integer number into signed 64.64-bit fixed point number.

    function toInt (int128 x) internal pure returns (int64)

Convert signed 64.64-bit fixed point number into signed 64-bit integer number.

    function fromUInt (uint256 x) internal pure returns (int128)

Convert unsigned 256-bit integer number into signed 64.64-bit fixed point
number.

    function toUInt (int128 x) internal pure returns (uint64)

Convert signed 64.64-bit fixed point number into unsigned 64-bit integer
number.

    function from128x128 (int256 x) internal pure returns (int128)

Convert signed 128.128-bit fixed point number into signed 64.64-bit fixed point
number.

    function to128x128 (int128 x) internal pure returns (int256)

Convert signed 64.64-bit fixed point number into signed 128.128-bit fixed point
number.
