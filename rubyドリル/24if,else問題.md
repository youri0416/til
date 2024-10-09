# 問題

EC サイトのポイント付与サービスを考えます。  
購入金額が 999 円以下の場合、3%のポイント  
購入金額が 1000 円以上の場合、5%のポイント  
このように付与されるポイントを出力するメソッドを作りましょう。

ただし誕生日の場合はポイントが 5 倍になります。  
誕生日の場合は true, 誕生日でない場合は false で表します。  
また、小数点以下をすべてのポイント計算が終わったあとに切り捨てましょう。

呼び出し方：  
calculate_points(amount, is_birthday)

出力例：  
calculate_points(500, false) → ポイントは 15 点です  
calculate_points(2000, false) → ポイントは 100 点です  
calculate_points(3000, true) → ポイントは 750 点です

# 解答

```ruby

def calculate_points(amount, is_birthday)
  if amount <= 999
    point = amount * 0.03
  else
    point = amount * 0.05
  end
  if is_birthday
    point = point * 5
  end
  puts "ポイントは#{point.floor}点です"
end

```
