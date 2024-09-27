# 配列での index メソッド

### 例 1: 単純な配列の要素検索

```ruby
fruits = ["apple", "banana", "cherry", "date"]
result = fruits.index("banana")

# => 1
```

ここでは、配列 fruits の中で"banana"が最初に現れる位置を探しています。インデックスは 0 から始まるので、"banana"の位置は 1 です。

### 例 2: 要素が存在しない場合

```ruby
fruits = ["apple", "banana", "cherry", "date"]
result = fruits.index("grape")

# => nil
```

"grape"は配列に存在しないため、結果は nil となります。

# 文字列での index メソッド

### 例 3: 単純な文字列検索

```ruby
text = "Hello, world!"
result = text.index("world")

# => 7
```

ここでは、文字列 text の中で"world"が最初に現れる位置を探しています。H、e、l、l、o、,、スペース（空白）に続いて"world"が始まるため、その位置は 7 です。

### 例 4: 文字が存在しない場合

```ruby
text = "Hello, world!"
result = text.index("planet")

# => nil
```

"planet"は文字列に存在しないため、結果は nil となります。
