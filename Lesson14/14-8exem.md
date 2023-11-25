# 演習問題
- 1.CDPを無効化するコマンドを2つ  
A.`(config)no cdp run`  
B.`(config-if)no cdp run`  
C.`(config)no cdp enable`  
D.`(config-if)no cdp enable`  
E.`(config)cdp disable`  

- 2.出力から、172.16.3.2に対するTelnetセッションの再開方法を選択  
A.disconnect1コマンドを実行する  
B.Ctrl + Shift + 6コマンドを押した後、Xキーを押す  
C.resume1コマンドを実行する  
D.Enterキーを押す  
E.session1コマンドを実行する

- 3.管理者がルータのVTYへアクセスし、debugコマンドを実行したところ何も表示されなかった。この問題を解決するために必要なコマンドを選択  
A.`terminal monitor`  
B.`logging synchronous`  
C.`no debug all`  
D.`show debug`  
E.`show processes`

- 4.管理者がSW2に対してTelnet接続する必要がある。SW2のIPアドレスを調べることができるコマンドを選択  
SW1 --- RT1(コンソール -- PC) --- SW2 --- RT2  
A.`show interfaces`  
B.`show cdp interface`  
C.`show ip interface brief`  
D.`show cdp neighbors`  
E.`show cdp entry *`

- 5.Ciscoルータに内蔵されているメモリの説明に関する用語を分類  
1.ルータが起動するために必要なプログラムが格納されている  
2.ルータが稼働中、動作するために必要な多くの情報を格納している  
3.電源をオフにしても内容が消えないメモリで、ルータの起動時に使用される設定を格納しておく  
4.読み書きされるメモリで、ルータの電源をオフにしても内容は消えない  
A.`runnning-config` B.ブートストラップ C.ROMモニタ D.ROM E.RAM F.`startup-config` G.Cisco IOSソフトウェア H.コンフィギュレーションレジスタ I.ルーティングテーブル J.NVRAM K.Flash L.POST

- 6.ルータの稼働中のコンフィギュレーションモードをサーバへバックアップすることができるコマンド  
A.`copy tftp:startup-config`  
B.`copy startup-config tftp;`  
C.`copy running-config startup-config`  
D.`copy tftp:running-config`  
E.`copy running-config tftp:`

- 7.ルータのコンフィギュレーションモードレジスタに関する説明で正しいものを2つ  
A.デフォルトのコンフィギュレーションレジスタ値は0x2102である  
B.現在のコンフィギュレーションレジスタ値を確認するには`show version`コマンドを使用する  
C.パスワードリカバリでは、コンフィギュレーションレジスタ値を0x2124に変更する必要がある  
D.コンフィギュレーションレジスタ値はフラッシュメモリ内に格納されている  
E.コンフィギュレーションレジスタは12ビットの値であり、16進数で表示される

- 8.あるネットワークで稼働中のルータに`(config)#config-register 0x2142`コマンドを実行した。このルータの再起動したときの状態で正しいものを選択  
A.ROMモニタモードで起動する  
B.Mini IOSで起動する  
C.システムメニューが起動する  
D.セットアップモードで起動する  
E.特に何も変わらず起動する

- 9.`boot system`コマンドでIOSイメージの格納場所として指定可能なものを2つ選択  
A.RAM B.フラッシュメモリ C.HTTPサーバ D.NVRAM E.TFTPサーバ

- 10.新規にCisco IOSイメージをアップグレードする。このとき、ルータ上で確認する事項と、その情報を収集するために使用するコマンドを3つ選択  
A.フラッシュメモリの空き容量を確認する  
B.`show running-config`  
C.`show memory`  
D.ROMの空き容量を確認する  
E.RAMに十分な空き容量があるか確認する  
F.`show processes`  
G.`show version`

- 11.ルータ上をNTPクライアントにするためのコマンド  
A.`(config)#ntp server <ip-address>`  
B.`(config)#ntp client`  
C.`(config)#ntp client enable`  
D.`(config)#ntp server`  
E.`(config)#ntp service enable`

- 12.シスコの第2世代サービス結合型ルータで、現在アクティブなライセンスを確認するためのコマンドを2つ選択  
A.`show version`  
B.`show license`  
C.`show license boot`  
D.`show boot system`  
E.`show license status`

---
回答  
1.CDPを無効化するコマンド2つ

2.172.16.3.2に対するTelnetセッションの再開方法

3.debugコマンドを実行したところ何も表示されない場合の解消方法

4.SW2に対してTelnet接続する必要がある。SW2のIPアドレスを調べることができるコマンド

5.Ciscoルータに内蔵されているメモリの説明

6.ルータの稼働中のコンフィギュレーションモードをサーバへバックアップする

7.ルータのコンフィギュレーションモードレジスタ

8.`(config)#config-register 0x2142`コマンドを実行し、ルータの再起動した

9.`boot system`コマンドでIOSイメージの格納場所を指定可能なものを2つ

10.Cisco IOSイメージをアップグレードするとき、ルータ上で確認する事項と、その情報を収集するために使用するコマンドを3つ

11.ルータ上をNTPクライアントにするためのコマンド

12.シスコの第2世代サービス結合型ルータで、現在アクティブなライセンスを確認するためのコマンドを2つ
