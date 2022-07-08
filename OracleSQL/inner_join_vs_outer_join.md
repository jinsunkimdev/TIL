# Inner Join VS Outer Join
## Inner Join(内部結合)?
### Inner Joinは二つのテーブルの間の共通性に焦点を当てている。

 二つ以上の（または複数の）テーブル間で条件を満たすデータを抽出すること。

 数学のベン図で表現すると交集合。

 ## Outer Join(会部結合)?
 ### Outer Joinは内部結合の逆。

 指定したテーブルを他のテーブルに結合すること。

 外部結合は三つのタイプがある。

<ol>
<li>Left Outer Join (or Left Join)</li>
<li>Right Outer Join (or Right Join)</li>
<li>Full Outer Join (or Full Join)</li>
</ol>

一部のデータは共有され、他のデータは共有されないため、このプロセスでnullが生成されることがある。

### Left Outer Join(左外部結合)

左側のテーブルを基準とするのが「左外部結合」（LEFT OUTER JOIN）

### Right Outer Join(右外部結合)

右側のテーブルを基準とするのが「右外部結合」（RIGHT OUTER JOIN）

### Full Outer Join(完全外部結合)

完全外部結合（FULL OUTER JOIN）は、両方のテーブルを基準とし、それぞれに一致しないレコードも抽出結果に含めます。