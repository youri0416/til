# 問題

正の整数を入力します。その整数が、  
10 の倍数（10,20,30...）からの差が 2 以内であるときは True  
それ以外は False  
と出力するメソッドを作りましょう。

出力例：  
near_ten(12)→True  
near_ten(17)→False  
near_ten(19)→True

# 解答

```ruby
def near_ten(num)
  quotient = num % 10
  if quotient <=2 || quotient >=8
    puts "True"
  else
    puts "False"
  end
end
```
