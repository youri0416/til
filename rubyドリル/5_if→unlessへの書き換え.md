# 問題

次の if 文を unless というメソッドを用いて書き換えてください。

```ruby
if a + b > 0
  puts "計算結果は0より大きいです"
end
```

# 解答

```ruby
unless a + b <= 0
  puts "計算結果は0より大きいです"
end
```
