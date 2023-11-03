# Regex Tutorial: Matching a Hex Value

## Introduction
Welcome to the Regex Tutorial on matching a Hex Value! In this tutorial, we'll explore the components of the regular expression `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/` and understand how it validates hex color codes.

## Summary
The regex is designed to validate hex color values, accounting for both the standard 6-digit hex codes and shorter 3-digit hex codes. It allows an optional '#' at the beginning and then checks for either a 6-digit hex code or a 3-digit hex code.

## Table of Contents
1. [Optional '#' - `#?`](#optional)
2. [Hex Code (6 digits) - `([a-f0-9]{6})`](#hex6)
3. [Hex Code (3 digits) - `([a-f0-9]{3})`](#hex3)

## 1. Optional '#' - `#?`<a name="optional"></a>
The first component, `#?`, makes the '#' at the beginning of a hex color code optional. This allows for both `#RRGGBB` and `RRGGBB` formats.

```javascript
/^#?/
```
Examples
-#1a2b3c (valid)
-3d4e5f (valid)
-invalidColor (invalid)

## 2. Hex Code (6 digits) - `([a-f0-9]{6})`<a name="hex6"></a>
The second part, `([a-f0-9]{6})`, matches a 6-digit hex color code. It consists of characters 'a' to 'f' and digits 0 to 9.

```javascript
/([a-f0-9]{6})/
```
Examples:

-#1a2b3c (valid)
-#3d4e5f (valid)
-#invalid (invalid)

## 3. Hex Code (3 digits) - `([a-f0-9]{3})`<a name="hex3"></a>
The third part, `([a-f0-9]{3})`, matches a 3-digit hex color code. It also consists of characters 'a' to 'f' and digits 0 to 9.

```javascript
/([a-f0-9]{3})/
```
Examples:

-#abc (valid)
-#123 (valid)
-#xyz (invalid)


## About the Author
This tutorial was written by [moe-j22](https://github.com/moe-j22).

---
