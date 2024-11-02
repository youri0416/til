# 問題

任意の数字が配列の中の何番目に格納されているかを確認できるプログラムを実装します。  
以下の配列から任意の数字を探して何番目に含まれているかという結果を返す search メソッドを、each_with_index を用いて作成しましょう。

```ruby
input = [3, 5, 9 ,12, 15, 21, 29, 35, 42, 51, 62, 78, 81, 87, 92, 93]
```

雛形

```ruby
def search(target_num, input)
  # 処理を記述
end

input = [3, 5, 9 ,12, 15, 21, 29, 35, 42, 51, 62, 78, 81, 87, 92, 93]
# 呼び出し例
search(11, input)
```

出力例  
search(5, input) → 2 番目にあります  
search(12, input) → 4 番目にあります  
search(7, input) → その数は含まれていません

# 解答

```ruby
def search(target_num, input)
  input.each_with_index do |num, index|
    if num == target_num
      puts "#{index + 1}番目にあります"
      return
    end
  end
  puts "その数は含まれていません"
end

input = [3, 5, 9 ,12, 15, 21, 29, 35, 42, 51, 62, 78, 81, 87, 92, 93]
# 呼び出し例
search(11, input)
```
