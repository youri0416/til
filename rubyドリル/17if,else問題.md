# 問題

以下の要件を満たす parrot_trouble メソッドを実装しましょう。

最近、あなたはオウムを飼いはじめました。しかし、近隣から「夜にオウムの鳴き声がうるさい」と苦情がくるようになりました。あなたはこれをシステムで解決しようと考え、次のようなプログラムの要件を考えました。

第一引数にオウムが鳴く場合は true を指定し、鳴かない false を指定する
第二引数には時間を指定する（ただし、「分」は考えないものとする）
20 時から翌朝 7 時までの間にオウムが鳴いた場合は「NG」と出力する（20 時と 7 時は含まれない）
上記以外の場合は「OK」と出力する

```Ruby
def parrot_trouble(talking, hour)
  # ここに条件式を実装する
end

# 呼び出し例
parrot_trouble(true, 6)
```

出力例  
parrot_trouble(true, 6) → NG  
parrot_trouble(true, 7) → OK  
parrot_trouble(false, 6) → OK  
parrot_trouble(false, 7) → OK

# 解答

```Ruby
def parrot_trouble(talking, hour)
  if talking && (hour < 7 || hour > 20)
    puts "NG"
  else
    puts "OK"
  end
end

prrot_trouble(true, 6)
```

## Java

```java
public class ParrotTrouble {
    public static void parrotTrouble(boolean talking, int hour) {
    // talking: オウムが話しているかどうかを表す boolean 型引数。
    // hour: 時間（0〜23の範囲）を表す int 型引数。
        if (talking && (hour < 7 || hour > 20)) {
            // 条件を満たす場合、"NG" を出力
            System.out.println("NG");
        } else {
            // 条件を満たさない場合、"OK" を出力
            System.out.println("OK");
        }
    }

    public static void main(String[] args) {
        // 呼び出し例
        parrotTrouble(true, 6);  // 出力: NG
        parrotTrouble(true, 8);  // 出力: OK
        parrotTrouble(false, 6); // 出力: OK
    }
}

```
