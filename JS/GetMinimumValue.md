# 最小値を取得
## Math.min()
```javascript
	let minValue = Math.min(...arr)
```
### MathオブジェクトのMinメソッドの数値は配列の場合はNaN(Not-A-Number) を返す。
### なので引数にスプレッド構文で配列を指定することで、配列の値をすべて渡し、最小値・最大値の値を取得することができる。
## Math.min.apply()
```javascript
	let minValue = Math.min(null, arr)
```
### apply()は、thisを指定する客体、処理を実行するメソッド。関数に配列として値をまとめて渡すことができるため、ループ文を省略することができる。

### → 最小値を取得する際に基準とする変数の初期化
  ```javascript
	let min = Number.MAX_SAFE_INTEGER
  ```
