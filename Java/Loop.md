# Java ループ

## for文

```java
for (int ix = 0; ix < 10; ++ix) {
    x = y * ix;
}
```

## 拡張for文

```java
for (String name : list) {
    System.out.println(name);
}
```

## while文

```java
while (y > 5) {
    --y;
    if (cancelled()) {
        break;
    }
    if (skip()) {
        continue;
    }
}
```

## do ... while文

```java
do {
    x /= 10;
} while (x > 1);
```
