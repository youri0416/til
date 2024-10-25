# 問題

メソッドに 3 つの整数 a b c を与えます。  
・「a と b の差が 1」または「a と c の差が 1」であり、かつ「b と c との数値の差が 2 以上」の場合は True  
・それ以外は False  
と出力するメソッドを作りましょう。

出力例：  
close_far(1, 2, 10) → True  
close_far(1, 2, 3) → False  
close_far(4, 1, 3) → True

# 解答

```ruby
def close_far(a, b, c)
  X = (a-b).abs
  Y = (a-c).abs
  Z = (b-c).abs

  if X == 1 && Z >= 2
    puts "True"
  elsif Y == 1 && Z >= 2
    puts "True"
  else
    puts "False"
  end
end
```

### 条件式の省略

```ruby
if (x == 1 && z >= 2) || (y == 1 && z >= 2)
  puts "True"
else
  puts "False"
end
```
