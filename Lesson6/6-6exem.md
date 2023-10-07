# 演習問題
- 1.CatalystスイッチのシステムLEDがグリーンに点灯しているときの状態で正しいもの  
A.ブロードキャストストームが発生し、輻輳状態になっている  
B.スイッチに電力は供給されているが、正常に動作していない  
C.スイッチが正常に動作している  
D.ケーブルが接続されていないか、ポートを管理的にシャットダウンしている  
E.STPによってブロックされている状態である

- 2.Catalyst2960シリーズのスイッチを起動したときに「*Would you like to enter the initial configuration dialog? [yes / no]:*」の表示。この時の説明で正しいものを2つ  
A.yesを選択するとセットアップモードが開始される  
B.noを選択すると、スイッチは再起動される  
C.NVRAMにコンフィギュレーションファイルが存在しない  
D.コンフィギュレーションレジスタ値が0x2142になっている  
E.RAMにコンフィギュレーションファイルが存在しない

- 3.スイッチにIPアドレスを設定する理由で正しいものを2つ  
A.スイッチに許可していないコンピュータを接続されないようにするため  
B.リモートからスイッチに管理アクセスするため  
C.SNMPでスイッチの情報収集や監視を行うため  
D.スイッチにVLANを構成し、ブロードキャストドメインを分割するため  
E.レイヤ2スイッチをレイヤ3スイッチとして動作させるため

- 4.CatalystスイッチにIPアドレスを割り当てて管理する時のコマンドを3つ選択  
A.`(config)#no shutdown`  
B.`(config)#vlan 1`  
C.`(config-if)#ip address 192.168.100.64 255.255.255.224`  
D.`(config)#interface fastethernet0/1`  
E.`(config-if)#no shutdown`  
F.`(config)#line vlan 1`  
G.`(config-if)#ip address 192.168.200.97 255.255.255.224`  
H.`(config-if)#ip address 192.168.150.95 255.255.255.224`  
I.`(config)#interface vlan 1`

- 5.スイッチにデフォルトフェートウェイを設定するコマンドを選択
A.`(config)#ip default-gateway 10.1.1.2`  
B.`(config)#interface vlan 1`  
`(config-if)default-gateway 10.1.1.2 255.255.255.0`  
C.`(config)default-gateway 10.1.1.2 255.255.255.0`  
D.`(config)#interface fastethernet0/1`  
`(config-if)ip default-gateway 10.1.1.2`  
E.`(config)ip default-gateway 10.1.1.2 255.255.255.0`

- 6.宛先MACアドレスがffff.ffff.ffff.ffffのフレームを受信した時のスイッチの動作で正しいもの  
A.受信したポートを除く全てのポートからフレームを転送する  
B.全てのポートからフレームを転送する  
C.スイッチはフレームを破棄して送信元へ通知する  
D.MACアドレステーブルを参照し、特定のポートにだけフレームを転送する  
E.送信元アドレスと宛先アドレスをMACアドレステーブルに登録する

- 7.`show mac address-table`コマンドで表示されないものを2つ  
A.VLAN  
B.MACアドレス  
C.タイプ  
D.プロトコル  
E.ポート  
F.IPアドレス

- 8.出力と、フレームをFa0/8で受信したときのSW1の動作として正しいもの  
コマンド:`show mac address-table`  
受信フレーム:0018.738a.51c0(宛先アドレス)、5c00.dd63.e0f4(送信元アドレス)、0x0800(タイプ)、データ、FCS
<br>
A.フレームをFa0 / 9以外の全ポートから転送する  
B.フレームを全ポートから転送する  
C.フレームをFa0 / 8以外の全ポートから転送する  
D.フレームの送信元アドレスをFa0 / 8で登録されているMACアドレスに書き換える  
E.フレームをFa0 / 9からのみ転送する

- 9.スイッチポートを全二重で速度を100Mbpsに固定するためのコマンドを2つ選択  
A.`(config-if)#bandwidth 100`  
B.`(config-if)#full duplex`  
C.`(config-if)#speed 100000`  
D.`(config-if)#speed 100`  
E.`(config-if)#mode full`  
F.`(config-if)#duplex full`

---
回答  
1.LEDがグリーンに点灯している  
C.スイッチが正常に動作している

2.「*Would you like to enter the initial configuration dialog? [yes / no]:*」の説明  
A.yesを選択するとセットアップモードが開始される  
C.NVRAMにコンフィギュレーションファイルが存在しない

3.スイッチにIPアドレスを設定する理由2つ  
B.リモートからスイッチに管理アクセスするため  
C.SNMPでスイッチの情報収集や監視を行うため

4.CatalystスイッチにIPアドレスを割り当てて管理  
I.`(config)#interface vlan 1`:IPアドレスの設定  
G.`(config-if)#ip address 192.168.200.97 255.255.255.224`  
E.`(config-if)#no shutdown`:インターフェイスの有効化

A.`(config)#no shutdown`:コンフィギュレーションモードのため不可  
B.`(config)#vlan 1`:プロンプトが(config-vlan)#に変わる  
サブネットマスクが255.255.255.224の場合(第4オクテットは11100000)、第4オクテットは32ごとにサブネットアドレスが繰り上がる  
C.`(config-if)#ip address 192.168.100.64 255.255.255.224`:サブネットアドレスのため不可  
D.`(config)#interface fastethernet0/1`:レイヤ2スイッチの物理的なスイッチポートにIPアドレスは設定不可  
H.`(config-if)#ip address 192.168.150.95 255.255.255.224`:サブネット192.168.150.64のブロードキャストアドレスのため不可(95 => 01011111)

5.デフォルトゲートウェイを設定する  
A.`(config)#ip default-gateway 10.1.1.2`

6.宛先MACアドレスがffff.ffff.ffff.ffffのフレームを受信した時のスイッチの動作  
A.受信したポートを除く全てのポートからフレームを転送する  

「宛先MACアドレスが未学習のユニキャストフレーム」「ブロードキャストフレーム」「未学習のマルチキャストフレーム」を受信したときにフラッディングを行う(受信したポート以外の全てのポートから転送する処理)。  
C.スイッチはフレームを破棄して送信元へ通知する:これはルータの動作  
E.送信元アドレスと宛先アドレスをMACアドレステーブルに登録する:宛先アドレスは学習しない

7.`show mac address-table`コマンドで表示されないもの  
D.プロトコル  
F.IPアドレス

A.VLAN・B.MACアドレス・C.タイプ・E.ポートは表示される

8.コマンド:`show mac address-table`  
受信フレーム:0018.738a.51c0(宛先アドレス)、5c00.dd63.e0f4(送信元アドレス)、0x0800(タイプ)、データ、FCS  
(0018.738a.51c0:Ports:Fa0 / 9, 5c00.dd63.e0f4:Ports:Fa0 / 8)  
E.フレームをFa0 / 9からのみ転送する:受信フレームの宛先MACアドレスのMACアドレスはMACアドレステーブルに学習されているため
転送処理  
送信元MACアドレスをMACアドレステーブルに学習  
宛先MACアドレステーブルを学習している場合、該当するポートだけにフレームを転送(フィルタリング)  
学習していない場合、受信したポート以外の全てのポートからフレームを転送する(フラッディング)


9.スイッチポートを全二重で速度を100Mbpsに固定する  
D.`(config-if)#speed 100`:2.ポートの速度を100Mbpsに設定  
F.`(config-if)#duplex full`:1.スイッチポートを全二重に設定  
二重モードと速度がデフォルトでautoになっている
