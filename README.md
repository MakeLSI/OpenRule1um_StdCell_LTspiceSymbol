# OR1_StdCells
LTspice circuit diagrams for OpenRule1um standard cells

[OpenRule1um standard cells](https://github.com/MakeLSI/OpenRule1um)の
[Glade用ライブラリ](https://github.com/MakeLSI/OpenRule1um/OpenRule1um)
および[KLayoutで使えるgdsライブラリ](https://github.com/MakeLSI/OpenRule1um/StdCell/StdCell_all.gds)
に対応したLTspice版回路図ライブラリです。

## Gladeでのレイアウト検証方法
注意：これには、OR1_StdCells_v1以下の回路図ライブラリつまり
シンボル(*.asy)と回路図(*.asc)の両方を使ってください
1. LTspiceで回路図を描き、ネットリストを作成する
2. Gladeで、Verify->Extract->Run LPEを実行し extracted viewを作る
3. Verify->LVS->Run LVSのフォームで、Schematic Sourceとしてnetlistを指定し、
NetlistはCDL Netlistに、LTspiceで作成したネットリストファイルを指定する
（多分、階層的に回路を作っているので、Hierarchical netlist?をチェックし、Top Cell Nameを指定する）
4. OKをクリックすると、GladeのMessage WindowにLVS結果が表示される

## LTspiceでのシミュレーション方法
（１）[回路図のライブラリを使う方法](https://paper.dropbox.com/doc/LTspice--AiX9r197aR3JVEYTejxB9d7jAg-zvjn13uSb18pSG5uHpzsy)
　OR1_StdCells_v1以下のシンボル(*.asy)と回路図(*.asc)の両方を使ってください
（２）[シンボルのライブラリを使う方法](https://paper.dropbox.com/doc/LTspice--ARCrxoK41rskHCEz1tcoOQXzAg-REFxur8zDV0rh6FPHf5hj)
　OR1_StdCells以下のシンボル(*.asy)を使ってください