# 問題

1〜100 までの数字をターミナルに出力してください。  
ただし、「3 の倍数」のときは数字の代わりに文字列で Fizz と、「5 の倍数」のときは Buzz、3 と 5 の倍数である「15 の倍数」のときは FizzBuzz と出力してください。

雛形

```ruby
def fizz_buzz
  # ここに処理を書き加えてください
end

fizz_buzz
```

# 解答

```ruby
def fizz_buzz
  num = 1
  while (num <= 100) do
    if num % 15 == 0
      puts "FizzBuzz"
    elsif (num % 3) == 0
      puts "Fizz"
    elsif (num % 5) == 0
      puts "Buzz"
    else
      puts num
    end

    num = num + 1
  end
end

fizz_buzz
```
