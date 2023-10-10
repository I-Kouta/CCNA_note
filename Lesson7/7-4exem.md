# 演習問題
- 1.セットアップモードの説明で正しくないものを2つ  
A.ルータを初期化した状態で起動すると、セットアップモードが起動する  
B.ルータを起動した後でセットアップモードをやり直すことはできない  
C.ルータのコンフィギュレーションレジスタが0x2102のとき、NVRAMの設定を無視してセットアップモードで起動する  
D.NVRAMにstartup-configを一度も保存しないで再起動すると、セットアップモードが起動する  
E.ルータを再起動したときに「*Would you like to enter the initial configuration dialog? [yes / no]:*」が表示された場合、コンフィギュレーションレジスタ値は0x2142の可能性がある

- 2.Ciscoルータのインターフェイスステータスの説明として正しいものを選択  
A.「*administratively down, line protocol is down*」は、リンクに何らかの障害が発生したことを示す  
B.FastEthernet0インターフェイスでshutdownコマンドを実行すると、ステータスは「*FastEthernet0 is down, line protocol is down*」と表示される  
C.「*FastEthernet0 is up, line protocol is down*」と表示されるとき、物理層は正常であるがネットワーク層に問題があることを示している  
D.FastEthernet0インターフェイスでno shutdownコマンドを実行し、ステータスが「*FastEthernet0 is down, line protocol is down*」と表示されるとき、ケーブルが接続されていない可能性がある  
E.「*FastEthernet0 is up, line protocol is up*」と表示されるとき、対向デバイスに対するpingは成功する

- 3.ルータのFa0インターフェイスにIPアドレスを設定して通信するためのコマンド  
PCのIP address:192.168.1.200 / 26, Gateway:192.168.1.254  
A.`(config)#interface fastethernet 0`  
`(config-if)#ip address 192.168.1.200 255.255.255.128`  
`(config-if)#no shutdown`  
B.`(config)#interface fastethernet 0`  
`(config-if)#ip address 192.168.1.254 255.255.255.224`  
`(config-if)#no shutdown`  
C.`(config)#interface fastethernet 0`  
`(config-if)#ip address 192.168.1.254 255.255.255.192`  
`(config-if)#shutdown`  
D.`(config)#interface fastethernet 0`  
`(config-if)#ip address 192.168.1.201 255.255.255.224`  
`(config-if)#no shutdown`  
E.`(config)#interface fastethernet 0`  
`(config-if)#ip address 192.168.1.254 255.255.255.192`  
`(config-if)#no shutdown`

- 4.`show version`コマンドで確認できないものを選択  
A.DRAMの容量  
B.インターフェイスの種類と数  
C.稼働中のIOSの格納場所とファイル名  
D.コンフィギュレーションレジスタ量  
E.CPU使用率  
F.システムを起動したときの状況

- 5.出力結果から正しいもの(結果割愛)  
A.`show interfaces fastethernet1`コマンドの出力結果である  
B.サブネットマスクには255.255.252.0を設定している  
C.ネットワークアドレスは172.16.80.0 / 21  
D.二重モードと速度は自動的に選択される  
E.ブロードキャストアドレスは172.16.80.255  
F.帯域幅は110Mbpsである  
G.インターフェイス説明文は設定されていない  
H.コリジョンが発生したのでインターフェイスがレイヤ1でダウンしている  
I.インターフェイスは管理的にダウンになっている

---
回答  
1.セットアップモードの説明で正しくないもの  
B.ルータを起動した後でセットアップモードをやり直すことはできない  
C.ルータのコンフィギュレーションレジスタが0x2102のとき、NVRAMの設定を無視してセットアップモードで起動する => 0x2102はデフォルト値。0x2142で起動した場合、セットアップモードを開始するかの確認メッセージが表示される  

2.Ciscoルータのインターフェイスステータス  
D.FastEthernet0インターフェイスでno shutdownコマンドを実行し、ステータスが「*FastEthernet0 is down, line protocol is down*」と表示されるとき、ケーブルが接続されていない可能性がある

A.「*administratively down, line protocol is down*」 => 管理的に無効化されている  
C.「*FastEthernet0 is up, line protocol is down*」と表示されるとき、物理層は正常であるがネットワーク層に問題があることを示している => 物理層は正常、データリンク層が正常に動作していない  
E.「*FastEthernet0 is up, line protocol is up*」と表示されるとき、対向デバイスに対するpingは成功する => ネットワーク層以上の通信は接続性を確認してみないと分からない

3.ルータのFa0インターフェイスにIPアドレスを設定して通信するためのコマンド  
E.`(config)#interface fastethernet 0`:インターフェイスの設定モードへ移行  
`(config-if)#ip address 192.168.1.254 255.255.255.192`:IPアドレスの設定  
`(config-if)#no shutdown`:インターフェイスを有効にする

4.`show version`コマンドで確認できないもの  
E.CPU使用率 => `show processes`コマンドを使用する

5.出力結果から正しいもの  
C.ネットワークアドレスは172.16.80.0 / 21  
D.二重モードと速度は自動的に選択される:`Auto-duplex, Auto Speed`  
G.インターフェイス説明文は設定されていない:設定されていればDescription:~という記載がある

B.サブネットマスクには255.255.252.0を設定している => /21なので255.255.248.0  
E.ブロードキャストアドレスは172.16.80.255 => ネットワークアドレスより、172.16.87.255 / 21  
F.帯域幅は110Mbpsである => BW 100000 Kbit / secなので100Mbps  
H.コリジョンが発生したのでインターフェイスがレイヤ1でダウンしている => 統計情報に0 collisionsとある  
I.インターフェイスは管理的にダウンになっている => *administratively down*という記載はない
