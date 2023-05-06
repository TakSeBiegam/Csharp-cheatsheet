# C# CHEATSHEET
This cheatsheet provides a quick reference for common C# syntax and constructs. It is intended for developers who are new to C# or are looking for a quick reference.

This cheatsheet is still a work in progress and may be updated in the future.

Design and inspiration based on <a href="https://github.com/mortennobel/cpp-cheatsheet">mortennobel/cpp-cheatsheet</a>.

**<p align="center">🚧 This repo is still in progress 🚧</p>**

## Preprocessor

```csharp
#region RegionName    // start a region block
// code here
#endregion            // end the region block

#define SYMBOL        // Define a preprocessor symbol
#undef SYMBOL         // Undefine a preprocessor symbol

#if CONDITION         // Start of a conditional block
// code here
#elif CONDITION2      // Optional additional condition
// code here
#else                 // Optional "else" block
// code here
#endif                // End of the conditional block

#line 100 "myfile.cs"                 // control the line number reported by compiler
#error Debugging is not enabled       // Generates a warning during compilation
#warning code needs to be optimized   // Generates an error durin compilation
#pragma warning disable 1234          // Disable warning 1234 for the next line(s)
#pragma warning restore 1234          // Restore warning 1234 for the next line(s)
#pragma warning disable               // Disable all warnings for the next line(s)
#pragma warning restore               // Restore all warnings for the next line(s)
```

## Literals
```csharp
123, 0b1111011, 0x7B        // Integers (decimal, binary, hex)
2147483647, -2147483648     // Integers (32-bit)
123L, 0x7fffffffffffffffL   // Long (64-bit) integers
123.0, 1.23e2              // Double (real) numbers
'a', '\u0061'               // Character (literal, unicode)
'\n', '\\', '\'', '\"'      // Newline, backslash, single quote, double quote
"string\n"                  // Array of characters ending with newline and \0
"hello" "world"             // Concatenated strings
true, false                 // Boolean constants
null                        // Null value (no type)
```

## Declarations
```csharp
int x;                      // Declare x to be an integer (value undefined)
int x = 255;                // Declare and initialize x to 255
short s; long l;            // Usually 16 or 32 bit integer (int may be either)
char c = 'a';               // Usually 16-bit Unicode character
byte b = 255;               // 8-bit unsigned integer
ushort u = 65535;           // 16-bit unsigned integer
uint ui = 4294967295;       // 32-bit unsigned integer
ulong ul = 18446744073709551615; // 64-bit unsigned integer
float f; double d;          // Single or double precision real (never unsigned)
decimal dec = 123.456M;     // Fixed-point decimal with 28-29 significant digits
bool b = true;              // True or false, may also use 1 or 0
int a, b, c;                // Multiple declarations
int[] a = new int[10];      // Array of 10 ints (a[0] through a[9])
int[] a = {0, 1, 2};        // Initialized array (or a[3]={0,1,2}; )
int[,] a = {{1,2}, {4,5}};  // Array of array of ints
string s = "hello";         // String (6 elements including '\0')
var x = 123;                // Type inference: x is an int
var y = "hello";            // Type inference: y is a string
object o = new object();    // Object reference
dynamic d = 123;            // Dynamic type, resolved at runtime
int? nullableInt = null;    // Nullable type, can also be int? or Nullable<int>
ref int r = ref x;          // Ref returns a reference to x
enum Weekend {Sat, Sun};    // Weekend is

```
