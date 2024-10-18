# slice メソッドの基本

slice メソッドを使うと、文字列や配列の一部を「スライス」（切り取る）ことができます。取り出した部分は新しい文字列や配列として返されます。  
元の配列や文字列から指定された要素を取り出しますが、元の配列や文字列は変更されません。  
slice メソッドは、指定した範囲の要素を新しく返すだけで、元のデータには影響を与えないのがポイントです。

## 文字列での slice の使い方

例 1: 単一の文字を取り出す

```Ruby
str = "こんにちは"
char = str.slice(1)  # インデックスは0から始まります
puts char  # => "ん"
```

例 2: 部分文字列を取り出す（開始位置と長さを指定）

```Ruby
str = "こんにちは"
substring = str.slice(1, 3)  # インデックス1から始まり、3文字を取り出す
puts substring  # => "んにち"
```

例 3: 範囲を指定して取り出す

```Ruby
str = "こんにちは"
substring = str.slice(1..3)  # インデックス1から3までの範囲
puts substring  # => "んにち"
```

例 4: 文字列の末尾から 2 文字を取得する

```ruby
str = "こんにちは"
last_two_chars = str.slice(-2, 2)
puts last_two_chars  # => "ちは"
```

## 配列での slice の使い方

例 1: 単一の要素を取り出す

```Ruby
arr = [10, 20, 30, 40, 50]
element = arr.slice(2)  # インデックス2の要素
puts element  # => 30
```

例 2: 複数の要素を取り出す（開始位置と長さを指定）

```ruby
arr = [10, 20, 30, 40, 50]
sub_array = arr.slice(1, 3)  # インデックス1から始まり、3つの要素を取り出す
puts sub_array.inspect  # => [20, 30, 40]
```

例 3: 範囲を指定して取り出す

```ruby
arr = [10, 20, 30, 40, 50]
sub_array = arr.slice(1..3)  # インデックス1から3までの範囲
puts sub_array.inspect  # => [20, 30, 40]
```

## slice メソッドの別名 []

Ruby では、slice メソッドは[]（ブラケット）でも同じ操作ができます。[]の方がよく使われるため、覚えておくと便利です。

文字列の場合

```ruby
str = "Ruby Programming"
char = str[4]          # インデックス4の文字
substring = str[5, 11] # インデックス5から11文字
range_substr = str[0..3] # インデックス0から3までの文字

puts char         # => " "
puts substring    # => "Programming"
puts range_substr # => "Ruby"
```

配列の場合

```ruby
arr = [100, 200, 300, 400, 500]
element = arr[2]        # インデックス2の要素
sub_array = arr[1, 3]   # インデックス1から3つの要素
range_sub_array = arr[0..2] # インデックス0から2までの要素

puts element        # => 300
puts sub_array.inspect    # => [200, 300, 400]
puts range_sub_array.inspect # => [100, 200, 300]
```

※範囲指定では、..（終点を含む）と...（終点を含まない）があります。
例: 0..3 は 0 から 3 まで、0...3 は 0 から 2 までを指定します。
