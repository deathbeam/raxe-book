# Regex

Regular expressions are represented by the regex literal:

```ruby
def foo_or_bar = ~/foo|bar/
def heeello    = ~/h(e+)llo/
def integer    = ~/\d+/
```

A regular expression literal is character by `~/` and ended by `/` character.

It can be followed by these modifiers:

* i: ignore case (PCRE_CASELESS)
* m: multiline (PCRE_MULTILINE)
* x: extended (PCRE_EXTENDED)

For example

```crystal
r = /foo/imx
```

Slashes must be escaped:

```crystal
slash = /\//
```

An alternative syntax is provided:

```crystal
r = %r(regex with slash: /)
```
