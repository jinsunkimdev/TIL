# Mapオブジェクト?
## ES2015(ES6)から導入された、Map オブジェクトはキーと値のペアを保持し、キーが最初に挿入された順序を覚えています。キーや値には任意の値 (オブジェクトとプリミティブ値)を使用することができます。
```javascript
// オブジェクト
	const obj = {
		Jinsun : 'Kim'
	}
	console.log(obj.Jinsun) // Kim  
```
```javascript
// Mapオブジェクト
	const map = new Map()
	console.log(map.size) // 0
	map.set('Jinsun', 'Kim')
	map.set('Jinsun2', 'Kim2')
	console.log(map.size) // 2

	map.delete('Jinsun2')
	console.log(map.size) // 1

	console.log(map.get('Jinsun')) // Kim

	map.clear()
	console.log(map.size) // 0
```
最初にMapをせい生成(と初期化)すること！

Mapへの値の追加は map.set(キー, 値) で、
値を取り出すのは map.get(キー) 

## Map VS オブジェクト
### Mapの方がもっと便利
### 1. キーの存在確認が簡単
has(key)で、そのキーがmapオブジェクトに存在するかどうかを確認できます。
```javascript
const map = new Map([["key1", 1000]]);
console.log(map.has("key1"));   // true
console.log(map.has("key2"));   // false
```

### 2. キーにどんな値でも設定することができる
Mapに値をセットする際のキーにはあらゆるオブジェクトが使えます。

 このときのマップが特定のキーをすでに持っているか、つまり挿入と上書きの判定は基本的に===演算子と同じです。
```javascript
const map = new Map();
map.set(NaN, "value");
// NaNは===で比較した場合は常にfalse
console.log(NaN === NaN); // => false
// MapはNaN同士を比較できる
console.log(map.has(NaN)); // => true
console.log(map.get(NaN)); // => "value"
```

### 3. forEach が簡単に使える
```javascript
const map = new Map([["key1", "value1"], ["key2", "value2"]]);
const results = [];
map.forEach((value, key) => {
    results.push(`${key}:${value}`);
});
console.log(results); // => ["key1:value1","key2:value2"]
```

### for...of が使える
```javascript
	const map = new Map()
	map.set("key1", "dog")
	map.set("key2", "cat")
	map.set("key3", "bird")

	for(const entry of map){
		console.log(entry)
	}
	/* 
	Array ["key1", "dog"]
	Array ["key2", "cat"]
	Array ["key3", "bird"] 
	 */
	const objectArr = ['a', 'b', 'c']
	for (const [index, element] of objectArr.entries())
  	console.log(index, element);
	/* 0 "a"
	   1 "b"
	   2 "c" */
```
entriesメソッドでマップイテレータを確認することができる。