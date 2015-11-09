# Table

A representing a mapping of keys of a type `K` to values of a type `V` or indexed array of values, or with object-like access. It is typically created with a hash literal:

## As maps

```lua
{["a"] = 2, ["b"] = 3} # Map[String, Int)]
```

Usage

```ruby
def two = map{"a"} # 2
```

## As arrays
```lua
{"a", "b"} # Array[String]
```

Usage

```ruby
def a = array{0} # a
```

## As objects

```coffeescript
{key1: 'a', key2: 'b'} # Type[String]
```

Usage

```ruby
def a = object.key1 # a
```