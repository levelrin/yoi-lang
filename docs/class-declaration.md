# Class Declaration

You need to create a file with `.yoi-class` extension to define a class.

Note that the file name will be the name of class.
For example, a file name `user.yoi-class` defines a class `user`.

Only lower-cased English letters, integers, and hyphens (-) are allowed for a class name.

A hyphen (-) will be used as a space in the class name.
For example, `http-client.yoi-class` will define a class `http client`.

## File Content

The content consists of the following:
1. description
2. constructor
3. default
4. predefined

The `description` is the place where you document the class.

The `constructor` is the place where you define instance variables (fields).
The values of those fields will be determined during the object initialization, like in Java.

The `default` is similar to the `constructor`, except the dependencies might not be injected via constructor.
If that's the case, the default values will be used.

The `predefined` is the place where you define fields without dependency injection via constructor.

Please see the following for an example.

```yoi
== description ==

Description of the class.

== constructor ==

name (string)

== default ==

profile picture (photo)
  path: "pic/default.png"

== predefined ==

uuid, generate value
-> id (string)

```

As you can see, there are two ways to assign values:
1. Object initialization shown in `default`.
2. Method call shown in `predefined`.

Note that the method call won't occur until that field is used.
In other words, the value will be assigned on demand.
The method call will occur only once, and the value will be kept.

Unlike typical programming languages, you are not allowed to declare methods in the class file.
Instead, methods are defined through separate files.
