# Ruby 条件分岐

## if ... elsif ... else

 * `false`と`nil`のみ偽。それ以外は真。

```ruby
if x == 16 then
    y = 1
elsif x < 32 then
    y = 2
else 
    y = 3
end
```

## ... if

```ruby
puts 'hogehoge' if a == 'hogehoge'
```

## unless ... else
 * `if`の反対。
 * `elsif`はない。

```ruby
unless x = 16 then
    y = 2
else
    y = 1
end
```
## ...unless

```ruby
puts 'foo' unless a == 'bar'
```

## case ... when

```ruby
case x
when 1 .. 15
    y = 1
when 16
    y = 2
when 17 .. 20
    y = 3
else
    y = 4
end
```
