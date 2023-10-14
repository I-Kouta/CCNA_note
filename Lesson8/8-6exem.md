# 演習問題
- 1.パケットを受信したときのルータの動作として正しいもの  
A.宛先IPアドレスとルーティングテーブルを参照する  
B.レイヤ3ヘッダを書き換えて転送する  
C.送信元IPアドレスとルーティングテーブルを参照する  
D.宛先MACアドレスとMACアドレステーブルを検索する  
E.レイヤ2ヘッダを書き換えて転送する

- 2.ルーティングテーブルを表示するためのコマンド  
A.`show routing-table`  
B.`show io router`  
C.`show ip routing`  
D.`show ip route`  
E.`show protocols`

- 3.経路集約の利点を2つ  
A.ルーティングテーブルのサイズを拡張し、同時に複数のパケットを処理することができる  
B.ルーティングプロトコルの設定を簡素化できる  
C.ルーティングテーブルのサイズを縮小し、ルータの負荷を軽減できる  
D.VLSMのアドレス設計が可能になるため、効率的にIPアドレスの割り当てができる  
E.リンク障害が発生したときに影響が及ぶ範囲を制限することができる

- 4.メトリックの説明で正しいものを2つ  
A.メトリックが最大の経路情報をルーティングテーブルに学習する  
B.RIPとOSPFは同じメトリックを使用する  
C.複数のルーティングプロトコルで同じ宛先ネットワークの経路情報を受信した場合に最適経路を選択するための優先度  
D.ルーティングプロトコルが同じ宛先ネットワークの経路情報を複数受信した場合に最適経路を選択するための値  
E.EIGRPは複合メトリックを使用するルーティングプロトコルである

- 5.適切なルータでデフォルトルートを正しく設定しているコマンド  
(Fa0 / 0, 192.168.1.1 / 24)R1(S0 / 0, 1.1.1.2 / 24)---(S0 / 1, 1.1.1.1 / 24)ISP  
A.`R1(config)#ip route 0.0.0.0.0.0.0.0 s0/0`  
B.`ISP(config)#ip route 0.0.0.0.0.0.0.0 1.1.1.2`  
C.`ISP(config)#ip default-route 1.1.1.2`  
D.`R1(config)#ip route 0.0.0.0 255.255.255.255 1.1.1.1`  
E.`R1(config)#default route 0.0.0.0.0.0.0.0 s0/0`  

- 6.2台のルータ間で使用されるルーティングプロトコルを選択  
R1(AS65000)---ISP(AS65100)  
A.EIGRP  
B.RIPv2P  
C.OSRF  
D.IS-IS  
E.BGP

- 7.デフォルトのアドミニストレーティブディスタンス値が最小のプロトコル  
A.OSRF  
B.IBGP  
C.RIP  
D.IS-IS  
E.EIGRP

- 8.プライマリ回線がダウンした場合にだけ使用できるスタティックルートの実装を選択  
A.フローティングスタティックルート  
B.スタティックデフォルトルート  
C.アドミニストレーティブルート  
D.フレームリレールート  
E.ダイナミックルート