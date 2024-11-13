# 問題

以下の要件を満たす police_trouble メソッドを実装しましょう。

あなたは警官です。a と b 二人の容疑者の取り調べをしています。このとき、次のルールで証言の真偽判定を行います。  
※問題文で登場した a と b 二人の容疑者は、今回実装する police_trouble メソッドの引数として取り扱っていきます。

・第一引数 a と第二引数 b どちらの証言も真(true)であれば、True を出力すること  
・第一引数 a と第二引数 b どちらの証言も偽(false)であれば、True を出力すること  
・第一引数 a と第二引数 b で証言の真偽が一致しない場合であれば、False を出力すること

雛形

```ruby
def police_trouble(a, b)
  # ここに条件式を記述する
end

# 呼び出し例
police_trouble(true, true)
police_trouble(false, false)
police_trouble(true, false)
```

出力例  
police_trouble(true, true) → True  
police_trouble(false, false) → True  
police_trouble(true, false) → False

# 解答

```ruby
def police_trouble(a, b)
  if (a  && b) || (!a && !b)
    puts "True"
  else
    puts "False"
  end
end

# 呼び出し例
police_trouble(true, true)
police_trouble(false, false)
police_trouble(true, false)
```
