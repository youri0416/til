# 問題

以下の要件を満たす in1to10 メソッドを実装しましょう。

・第一引数の num が 1 以上かつ 10 以下の範囲であれば True を出力すること  
・第二引数の outside_mode が True の場合は、第一引数 num が条件範囲外でも True を出力すること  
・それ以外は False を出力すること

雛形

```ruby
def in1to10(num, outside_mode)
  # ここに条件式を記述する
end

# 呼び出し例
in1to10(5,false)
in1to10(11,false)
in1to10(11,true)
```

出力例  
in1to10(5,false) →True  
in1to10(11,false) →False  
in1to10(11,true) →True

# 解答

```ruby
def in1to10(num, outside_mode)
  if (num >=1 && num <= 10) || outside_mode
    puts "True"
  else
    puts "False"
  end
end

# 呼び出し例
in1to10(5,false)
in1to10(11,false)
in1to10(11,true)
```

# Java

```java
public class Main {
// クラスの定義です。Javaのプログラムは「クラス」という単位で構成されます。
// Mainはクラスの名前です。ファイル名もMain.javaと一致させます。
    public static void in1to10(int num, boolean outsideMode) {
    // メソッドの定義です。メソッドは、特定の処理をまとめて実行するための単位です。
    // publicは他のクラスからもアクセスできるようにする公開の設定です。
    // staticは、このメソッドがインスタンス（オブジェクト）を作らずに使えることを示しています。
    // voidは、このメソッドが値を返さないことを意味します。
    // in1to10はメソッドの名前です。
    //(int num, boolean outsideMode) はこのメソッドが受け取る引数（パラメータ）です。num は整数（int）で、outsideModeは真偽値（boolean）です。

        if ((num >= 1 && num <= 10) || outsideMode) {
            System.out.println("True");
            // 画面に "True" と表示する命令です。
            // System.out.println は、コンソールに出力するためのメソッドです。

        } else {
            System.out.println("False");
        }
    }

    public static void main(String[] args) {
    // Javaプログラムの開始地点を示す特別なメソッドです。
    // mainメソッドは、Javaプログラムを実行するときに最初に呼び出されます。
    // String は文字列型（テキストデータ）を表す型です。
    // [] は「配列」を表す記号で、複数の String をまとめて扱うことができます。
    // String[] は、「複数の文字列を格納できる配列」という意味になります。例えば、{"hello", "world"} など、複数の文字列が入ったリストのようなものです。
    // args は配列の名前です。この名前は自由に付けられますが、慣習的に args がよく使われます。
    // args の内容は、プログラムをコマンドラインで実行したときに渡された引数（値）が格納されます。
        in1to10(5, false);   // True
        // in1to10メソッドを呼び出して、num に 5、outsideMode に false を渡します。
        in1to10(11, false);  // False
        in1to10(11, true);   // True
    }
}
```
