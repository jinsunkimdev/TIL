# Binary Searchアルゴリズム
## Sorted Array の中央値を探す(Middle)。
## Start, End の値と比較して、ターゲットが、右にあれば、Startを中央値に、そうでなければ、Endを中央値に、ずばりの値であれば、それを返却。
```javascript
let numList = undefined

const binarySearch = (num, startIndex, endIndex) => {
	if(endIndex < startIndex) return false
	if(endIndex === startIndex) return num === numList[startIndex]

	// Get Middle
	const pivotIndex = Math.floor((endIndex + startIndex) / 2)
	if(num === numList[pivotIndex]) return true
	else if(num > numList[pivotIndex])
		return binarySearch(num, pivotIndex + 1, endIndex)
	else if(num < numList[pivotIndex])
		return binarySearch(num, startIndex, pivotIndex - 1)
}
```
### <ul>
### <li>最初のIndexをLeft, 最後のIndex をRightとして、中央値を　Pivotとする</li>

### <li>Pivotの値がターゲットなら、Pivotのポインタを返却</li>

### <li>Pivotの値がターゲットより大きいなら、Right = pivot - 1</li>

### <li>Pivotの値がターゲットより小さいなら、Left = pivot + 1</li>

### <li>LeftとRightの大小関係が入れ替わったら、Left のインデックスの値がターゲットの値</li>

### <li>Recursionでタゲットの値を見つけるまで繰り返す。</li>
### </ul>
