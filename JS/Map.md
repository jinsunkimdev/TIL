# Mapオブジェクト?
## ES2015(ES6)から導入された、キーと値の組み合わせを保持することができるオブジェクト。
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
var map = new Map([["key1", 1000]]);
console.log(map.has("key1"));   // true
console.log(map.has("key2"));   // false
```
### 2. forEach が簡単に使える
```javascript
const map = new Map([["key1", "value1"], ["key2", "value2"]]);
const results = [];
map.forEach((value, key) => {
    results.push(`${key}:${value}`);
});
console.log(results); // => ["key1:value1","key2:value2"]
```

### 3. キーにどんな値でも設定することができる