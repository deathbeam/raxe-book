# String

A String represents an immutable sequence of UTF-8 characters.

A String is typically created with a string literal, enclosing UTF-8 characters in double quotes:

```ruby
"hello world"
```

A backslash can be used to denote some characters inside the string:

```ruby
"\"" # double quote
"\\" # backslash
"\e" # escape
"\f" # form feed
"\n" # newline
"\r" # carriage return
"\t" # tab
"\v" # vertical tab
```

A string can span multiple lines with triple quote (`###`) syntax:

```ruby
"""hello
      world" # same as "hello\n      world"""
```

Note that in the above example trailing and leading spaces, as well as newlines,
end up in the resulting string. To avoid this, you can split a string into multiple lines
by joining multiple literals with a plus:

```ruby
"hello " +
"world, " +
"no newlines" # same as "hello world, no newlines"
```

## Interpolation

To create a String with embedded expressions, you can use string interpolation:

```ruby
def a = 1
def b = 2
def r = "sum = #{a + b}" # "sum = 3"
```
