# Java or C# プログラマが React + Typescript で心を折られないために事前に知っておいたほうが良いこと

## Structural Subtyping(構造的部分型)(TypeScript) と Nominal Subtyping(公称的部分型)(Java等) 違いを理解する

[ TypeScript: 異なる2つの型システム「公称型」と「構造的部分型」 ]( https://qiita.com/suin/items/52cf80021361168f6b0e )

Java ( Nominal Subtyping ) では以下の型は別の型だが、Structural Subtyping 目線では同じとみなされる。

```java

interface Foo {
  String foo(int a);
}

interface Bar {
  String bar(int a);
}

```

Foo foo = new Bar{ ..(略).. } 
- Nominal Subtyping    -> 代入できない。 
- Structural Subtyping -> 代入できる。引数と戻り値の型が同じなので、同じ型とみなされる



## 名前を捨てろ

## 公式チュートリアルが罠