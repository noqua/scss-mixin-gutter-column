# scss-mixin-gutter-column

レスポンシブ対応。カラム数とカラム間marginを自由に設定するMixin。

# 使い方/Usage

Mixinをインクルードしてください。

```
@import 'mixin-gutter-column';
```


包括要素内で```col()```mixinをインクルードし、カラム数やカラム要素のclass名などを指定します。

```
/*
@include col(
	number of column, // *required ex) 3
	gutter margin, // *required ex) 30px
	class name, // ex) '.child'
	display type(flex/float/grid), // ex) flex
	is list(true/false) // ex) false
) {
	other styles
}
*/

@include col(
	カラム数,	 // *必須 例) 3
	カラム間margin幅, // *必須 例) 30px
	カラムのセレクタ, // 例) '.child'
	CSSのタイプ(flex/float/grid), // 例) flex
	リストか否か(true/false) // 例) false
) {
	その他のスタイル
}
```

カラム数

## 使い方例/Sample

- 包括要素 : ```.container```
- カラム数 : 4
- カラム間margin幅 : 30px
- カラムのセレクタ : ```.child```
- CSSのタイプ : flexbox
- リストか否か : false

### HTML

```
<div class="container">
	<div class="child">.child</div>
	<div class="child">.child</div>
	<div class="child">.child</div>
	<div class="child">.child</div>
	<div class="child">.child</div>
	<div class="child">.child</div>
</div><!-- /.container -->
```

### SCSS

```
.container {
	@include col(4, 30px, '.child', flex, false);
}
```

<img src="https://github.com/noqua/scss-mixin-gutter-column/blob/image/image/sample-1.png" alt="sample" title="sample" width="609">

※上下marginはmixinには含まれませんので、必要に応じて個別で設定してください。<br>

その他の使い方例は```index.html```でご確認ください。
