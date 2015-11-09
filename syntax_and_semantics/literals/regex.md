# Regex

Regular expressions are represented by the regex literal:

```ruby
def foo_or_bar = ~/foo|bar/
def heeello    = ~/h(e+)llo/
def integer    = ~/\d+/
```

A regular expression literal is character by `~/` and ended by `/` character.

It can be followed by these modifiers:

* i: case insensitive matching
* g: global replace or split, see below
* m: multiline matching, ^ and $ represent the beginning and end of a line
* s: the dot . will also match newlines (Neko, C++, PHP, Flash and Java targets only)
* u: use UTF-8 matching (Neko and C++ targets only)

For example

```ruby
def r = ~/foo/img
```

Slashes must be escaped:

```ruby
def slash = ~/\//
```
