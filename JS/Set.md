# Setオブジェクト？
## ES2015(ES6)から導入された、重複した値がないことを保証したコレクション。
### → 値が一意であることが保証されている
### → 順序を持たず、インデックスでアクセスできない
```javascript
	// Setの作成
	let set = new Set()
```
Iteratorオブジェクトなので初期値として渡すことができる。

+ size

+ add 

+ delete(value) 

+ clear() 

+ has(value)

### for...of, forEach
Setへの追加順に要素を取り出る。
MapをSetに、SetをMapに交換しやすい。
```javascript
	// for...of
	let set = new Set()
	set.add("dog")
	set.add("cat")
	set.add("fish")

	for(let value of set)
	{
		console.log(value)
	}
	// dog
	// cat
	// fish
	set.forEach(v => console.log(v))
	// dog
	// cat
	// fish
```