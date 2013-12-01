# Java 例外

## 一般的な事項

 * 例外は`Throwable`を継承。
 * `Throwable` … 直接使うことはないと思うけど (checked)
    * `Exception` … 回復可能なエラー用 (checked)
        * `RuntimeException` (unchecked)
    * `Error` … 回復不可能なエラー用 (unchecked)
 * checkedな例外はメソッドのthrowsに書く必要がある。

## throw

```java
if (error) {
    throw new HogehogeException("error has occured!");
}
```

## try ... catch ... finally

```java
try {
    doSomething();
} catch (HogehogeException ex) {
    logException(ex);
} catch (FooException ex) {
    logFooException(ex);
} finally {
    resources.close();
}
```
