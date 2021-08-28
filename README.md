# OptionLib
Implementation of an Option type

This is a simple implementation of an `Option<T>` type, similar to the one in the FSharp.Core libraries, but designed
for use from C# code.

It provides a class to represent an optional object of type `T`. `T` can be any type.

It is different from `System.Nullable<T>` which only works for `struct` types, and it is different from using the C#
nullable syntax extension (where you can put `?` after a class type to indicate that the value might be null).  It
uses properties named `HasValue` and `Value` just like `Nullable<T>`.

The `Option<T>` class has a static method called `Some` which constructs an option with a value, and a static property
called `None` which represents an object that does not have a value.

A version of this class was in **Sunlighter.AsyncQueueLib** but I decided to move it to its own library and NuGet
package, because I am writing other libraries that do not use async queuing, but do use options, and I want to use a
single `Option<T>` type rather than having each of my libraries provide its own.

Maybe one day Microsoft will provide a `System.Option<T>` type, but they might see it as redundant since they already
have `System.Nullable<T>`.
