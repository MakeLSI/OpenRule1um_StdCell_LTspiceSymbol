# OR1_StdCells
LTspice circuit diagrams for OpenRule1um standard cells

[OpenRule1um standard cells](https://github.com/MakeLSI/OpenRule1um)の
[Glade用ライブラリ](https://github.com/MakeLSI/OpenRule1um/OpenRule1um)
に対応したLTspice版回路図ライブラリです。

## Gladeでのレイアウト検証方法

1. LTspiceで回路図を描き、ネットリストを作成する
2. Gladeで、Verify->Extract->Run LPEを実行し extracted viewを作る
3. Verify->LVS->Run LVSのフォームで、Schematic Sourceとしてnetlistを指定し、
NetlistはCDL Netlistに、LTspiceで作成したネットリストファイルを指定する
（多分、階層的に回路を作っているので、Hierarchical netlist?をチェックし、Top Cell Nameを指定する）
4. OKをクリックすると、GladeのMessage WindowにLVS結果が表示される