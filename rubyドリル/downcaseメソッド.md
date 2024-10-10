# downcase メソッド

.downcase は、文字列内のすべての大文字を対応する小文字に変換します。  
小文字はそのまま変わりません。小文字の部分には影響を与えず、大文字だけを小文字にします。  
このメソッドは、入力されたデータを一貫した形式で扱いたいときに使うことがよくあります。  
たとえば、ユーザーが入力したメールアドレスや名前を小文字で統一したい場合に便利です。

### 基本的な使い方

```ruby
str = "HELLO World"
puts str.downcase  # => "hello world"
```

str.downcase は、文字列 "HELLO World" の大文字をすべて小文字に変換します。  
結果は "hello world" です。

### 例 1: 全部大文字の文字列を小文字に変換

```ruby
str = "RUBY IS FUN"
puts str.downcase  # => "ruby is fun"
```

### 例 2: すでに小文字の文字列

```ruby
str = "ruby"
puts str.downcase  # => "ruby"
```

### 例 3: 大文字と小文字が混在した文字列

```ruby
str = "Hello Ruby"
puts str.downcase  # => "hello ruby"
```
