# Generics

You can make a class generic based on one or more type variables. For example:

```ruby
class MyBox
  def value : T
  
  def new(value : T)
    @value = value
  end
end
```

Then you instantiate it like this:

```ruby
new MyBox[Int](1)

box = new MyBox[String]("hello")
box.value.length #=> 5
```

The above now works, because `MyBox` is now not a single type, but a family of types identified with a `T` type: `MyBox[Int]` is a different type than `MyBox[String]`, and their `@value` variable is not shared.

## Type variables inference

Type restrictions in a generic type's constructor are free variables when type arguments were not specified, and then are used to infer them. For example:

```ruby
new MyBox(1)       # MyBox[Int]
new MyBox("hello") # MyBox[String]
```

In the above code we didn't have to specify the type arguments of `MyBox`, the compiler inferred them.
In this way generic types are less tedious to work with.

## Generic types inheritance

Generic classes and structs can be inherited. When inheriting you can specify an instance of the generic type, or delegate type variables:

```ruby
class Parent[T]
end

class IntChild < Parent[Int32]
end

class GenericChild[T] < Parent[T]
end
```
