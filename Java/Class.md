# Java クラス・インタフェース

## フィールドのアクセス制御

|アクセス指定子|意味                                                  |
|:-------------|:-----------------------------------------------------|
|`private`     |このクラス（内部クラス含む）からアクセス可能          |
|(なし)        |`private` + 同じパッケージの他のクラスからアクセス可能|
|`protected`   |(なし) + 派生クラスからアクセス可能                   |
|`public`      |すべてのクラスからアクセス可能                        |


## クラス

 * ファイル名は＜publicクラスの名前＞.javaにする。
 * パッケージとファイルの存在するディレクトリは一致する必要がある。

```java
package com.hironytic.mycodes.java;

/**
 * クラスの例
 */
public class Example {
    /** フィールド */
    private int foo;

    /** static フィールド */
    private static int hoge = 10;
    private static String name;

    /** 定数を定義するときはこんな感じに */
    public static final float PI = 3.14f;

    // staticイニシャライザ
    static {
        name = "Taro";
    }
    
    /**
     * コンストラクタ
     */
    public Example() {
        this(0);
    }
    
    /**
     * 引数を伴ったコンストラクタ
     * @param foo 引数
     */
    public BaseClass(int foo) {
        this.foo = foo;
    }
    
    /**
     * メソッドの例
     * @param v0 値0
     * @param v1 値1
     * @return 計算結果
     */
    public int calc(int v0, int v1) {
        int result = v0 + v1 + foo;
        return result;
    }
}
```

## インタフェース

```java
package com.hironytic.mycodes.java;

/**
 * インタフェースの例
 */
public interface Computable {
    
    /**
     * メソッド
     * @return 結果
     */
    public int compute();
}
```

## クラスの継承

```java
import com.hironytinc.mycodes.java.Base;

public class Derived extends Base {
    ...
}
```

## インタフェースの実装

```java
import com.hironytinc.mycodes.java.SomeInterface;
import com.hironytinc.mycodes.java.AnotherInterface;

public class Concrete implements SomeInterface, AnotherInterface {
    ...
}
```
