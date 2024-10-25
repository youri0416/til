# abs メソッド

数値の絶対値を返すために使うメソッドです。  
絶対値とは、数値の正負を無視したその数の大きさのことです。  
例えば、-5 の絶対値は 5、3 の絶対値もそのまま 3 です。

Ruby では、.abs メソッドを使うことで簡単に絶対値を求めることができます。  
書き方はとてもシンプルで、数値の後ろに.abs を付けるだけです。

### 例

```ruby
number = -10
puts number.abs  # 結果: 10
```

.abs は数値がマイナスでもプラスにして返してくれます。  
プラスの数値の場合、そのままの値が返されます。

### 例

```ruby
positive_number = 7
negative_number = -7

puts positive_number.abs  # 結果: 7
puts negative_number.abs  # 結果: 7

```

### 計算式に対して使う例 ①

```ruby
result = (5 - 10).abs
puts result  # 結果: 5

```

### 計算式に対して使う例 ②

```ruby
result = (3 * -4 + 2 - 10).abs
puts result  # 結果: 20

```

ポイント  
1 計算式全体を丸括弧()で囲む。  
2 .abs を計算式の外側に付けると、計算結果の絶対値が取得できる。
