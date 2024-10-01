# include?メソッド
配列や文字列、ハッシュなどに特定の要素や値が含まれているかどうかを確認するために使います。  

### 配列での使用例 
```Ruby
fruits = ["apple", "banana", "cherry"]

if fruits.include?("banana")
  puts "The array includes 'banana'."
else
  puts "The array does not include 'banana'."
end
```
結果: The array includes 'banana'.  

### 文字列での使用例
```Ruby
sentence = "The quick brown fox jumps over the lazy dog."

if sentence.include?("fox")
  puts "The sentence includes 'fox'."
else
  puts "The sentence does not include 'fox'."
end
```
結果: The sentence includes 'fox'.  

### ハッシュでの使用例
```Ruby
person = { name: "John", age: 30, city: "New York" }

if person.include?(:age)
  puts "The hash includes the key :age."
else
  puts "The hash does not include the key :age."
end
```
結果: The hash includes the key :age.  

### 応用例
```Ruby
nested_array = [["apple", "banana"], ["cherry", "date"]]

if nested_array.flatten.include?("cherry")
  puts "The nested array includes 'cherry'."
else
  puts "The nested array does not include 'cherry'."
end
```
結果: The nested array includes 'cherry'.  
ここでは、先に flatten メソッドを使用して多次元配列を一つの配列に変換し、その後に include? メソッドで要素が含まれているかを確認しています。

# flattenメソッド
配列を一次元にするために使用されます。特に、ネストされた配列（多次元配列）を平坦化して単一の配列にするのに便利です。  
### ベーシックな例
```Ruby
nested_array = [1, [2, 3], [4, [5, 6]]]

flattened_array = nested_array.flatten

puts flattened_array.inspect
```
結果: [1, 2, 3, 4, 5, 6]  

### ネストの深さを指定
```Ruby
nested_array = [1, [2, [3, [4, 5]]]]

flattened_array_1_level = nested_array.flatten(1)
flattened_array_2_levels = nested_array.flatten(2)

puts flattened_array_1_level.inspect
puts flattened_array_2_levels.inspect
```
結果:  
flattened_array_1_level は [1, 2, [3, [4, 5]]]  
flattened_array_2_levels は [1, 2, 3, [4, 5]]  
ここでは、flatten(1) を使って1レベルだけ平坦化し、flatten(2) を使って2レベルまで平坦化しています。  

### 空の配列やネストのない配列の場合
空の配列やネストのない配列に対して flatten を使うと、単に元の配列が返されます。  
```Ruby
empty_array = []
simple_array = [1, 2, 3, 4]

flattened_empty_array = empty_array.flatten
flattened_simple_array = simple_array.flatten

puts flattened_empty_array.inspect
puts flattened_simple_array.inspect
```
結果:  
flattened_empty_array は []  
flattened_simple_array は [1, 2, 3, 4]  

### 元の配列は変更しない
flatten メソッドは元の配列を変更せず、新しい配列を返します。元の配列を変更したい場合は flatten! メソッドを使います。

# flatten!メソッド
```Ruby
nested_array = [1, [2, 3], [4, [5, 6]]]

nested_array.flatten! # これで元の配列が変更されます

puts nested_array.inspect
```
結果: [1, 2, 3, 4, 5, 6]


