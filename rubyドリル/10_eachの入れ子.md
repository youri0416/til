# 問題

以下のように、果物の名前と値段が入った配列があります。  
この配列を用いて、果物の名前とそれぞれの合計額が出力される  
コードを記述してください。

```ruby
fruits_price = [["apple", [200, 250, 220]], ["orange", [100, 120, 80]], ["melon", [1200, 1500]]]

（出力）
appleの合計金額は670円です
orangeの合計金額は300円です
melonの合計金額は2700円です
```

# 解答

```ruby
fruits_price = [["apple", [200, 250, 220]], ["orange", [100, 120, 80]], ["melon", [1200, 1500]]]

fruits_price.each do |fruit|
  sum = 0
  fruit[1].each do |price|
    sum += price
  end
  puts "#{fruit[0]}の合計金額は#{sum}円です"
end
```

## 解説

fruits_price のリストにアクセスする際の添字は、以下のようになります。

```ruby
fruits_price[0]     -> ["apple", [200, 250, 220]]
fruits_price[1]     -> ["orange", [100, 120, 80]]
fruits_price[2]     -> ["melon", [1200, 1500]]
```

各果物の価格にアクセスする場合、内側のリストも添字で指定します。

```ruby
fruits_price[0][1][0]  -> 200  (appleの最初の価格)
fruits_price[0][1][1]  -> 250  (appleの2番目の価格)
fruits_price[0][1][2]  -> 220  (appleの3番目の価格)

fruits_price[1][1][0]  -> 100  (orangeの最初の価格)
fruits_price[1][1][1]  -> 120  (orangeの2番目の価格)
fruits_price[1][1][2]  -> 80   (orangeの3番目の価格)

fruits_price[2][1][0]  -> 1200 (melonの最初の価格)
fruits_price[2][1][1]  -> 1500 (melonの2番目の価格)

```

### each ループ

```ruby
fruits_price.each do |fruit|
```

・each は、リストの中の要素を順番に取り出して処理するためのループです。  
・|fruit| の部分は、リストの要素が 1 つずつ fruit という名前で取り出されることを示しています。  
1 回目のループ: fruit = ["apple", [200, 250, 220]]  
2 回目のループ: fruit = ["orange", [100, 120, 80]]  
3 回目のループ: fruit = ["melon", [1200, 1500]]

### 各価格を sum に加算する

```ruby
fruit[1].each do |price|
  sum += price
end
```

```ruby
sum = 0
[200, 250, 220].each do |price|
  sum += price
end
```

fruit[1] は、その果物の価格のリストです。例えば、1 回目のループでは fruit[1] は [200, 250, 220] です。  
この fruit[1].each の部分で、価格リスト [200, 250, 220] の中の数字（価格）を 1 つずつ取り出して price に代入します。  
sum += price は sum = sum + price の省略形で、price の値を sum に足しています。

#### 例：

1 回目のループ（apple の場合）では次のように合計が計算されます。

sum に 200 を足して、sum は 200 になる。  
次に 250 を足して、sum は 450 になる。  
最後に 220 を足して、sum は 670 になる。

### 結果を表示する

```ruby
puts "#{fruit[0]}の合計金額は#{sum}円です"
```

```ruby
appleの合計金額は670円です
orangeの合計金額は300円です
melonの合計金額は2700円です
```
