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
A.`running-config` B.ブートストラップ C.ROMモニタ D.ROM E.RAM F.`startup-config` G.Cisco IOSソフトウェア H.コンフィギュレーションレジスタ I.ルーティングテーブル J.NVRAM K.Flash L.POST

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

- 11.ルータをNTPクライアントにするためのコマンド  
A.`(config)#ntp server <ip-address>`  
B.`(config)#ntp client`  
C.`(config)#ntp client enable`  
D.`(config)#ntp master`  
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
A.`(config)no cdp run` => デバイス全体でCDPを無効化  
D.`(config-if)no cdp enable` => 特定インターフェイスのみCDPを無効化

B.`(config-if)no cdp run` => モードが誤り  
C.`(config)no cdp enable` => モードが誤り  
E.`(config)cdp disable`

CDPはデフォルトで有効になっている。

2.172.16.3.2に対するTelnetセッションの再開方法  
C.resume1コマンドを実行する

A.disconnect1コマンドを実行する => クライアントが中断しているセッションを切断することができる  
B.Ctrl + Shift + 6コマンドを押した後、Xキーを押す => TelnetやSSHを中断することができる  
D.Enterキーを押す => 直前のセッションが再開される(*が表示される)  
E.session1コマンドを実行する => 不正

クライアントは`show session`コマンドで中断中のセッション情報を確認できる。

3.debugコマンドを実行したところ何も表示されない場合の解消方法  
A.`terminal monitor` => ログメッセージやデバッグを表示する

B.`logging synchronous` => コマンド入力の途中でメッセージが割り込まれたときにコマンドを再表示する  
C.`no debug all` => 全てのデバッグ機能を無効にする  
D.`show debug` => どのデバッグ機能が有効になっているか確認する  
E.`show processes` => CPU使用率やプロセスに関する情報を表示する

特権EXECモードからコマンドを実行する必要がある。

4.SW2に対してTelnet接続する必要がある。SW2のIPアドレスを調べることができるコマンド  
SW1 --- RT1(コンソール -- PC) --- SW2 --- RT2  
E.`show cdp entry *`

A.`show interfaces` => 自身のインターフェイス情報を表示  
B.`show cdp interface` => CDPが有効なインターフェイスの情報を表示するコマンド  
C.`show ip interface brief` => 自身のインターフェイスの要約情報を表示  
D.`show cdp neighbors` => detailが不足。要約情報にはIPアドレスは含まれない

隣接デバイスにIPアドレスが割り当てられている場合、CDPで取得した情報にはIPアドレスも含まれている。ただし、詳細情報でないといけない。`show cdp neighbors detail`でも可能。

5.Ciscoルータに内蔵されているメモリの説明  
1.ルータが起動するために必要なプログラムが格納されている  
=> B.ブートストラップ, C.ROMモニタ, D.ROM L.POST  
2.ルータが稼働中、動作するために必要な多くの情報を格納している  
=>A.`running-config`, E.RAM, I.ルーティングテーブル  
3.電源をオフにしても内容が消えないメモリで、ルータの起動時に使用される設定を格納しておく  
=>F.`startup-config`, H.コンフィギュレーションレジスタ, J.NVRAM  
4.読み書きされるメモリで、ルータの電源をオフにしても内容は消えない
=> G.Cisco IOSソフトウェア, K.Flash

ROM、フラッシュメモリ、NVRAM、RAMの４つのメモリが内蔵されている。  
ROM:読み込み専用のメモリで、ルータの電源をオフにしても内容が消えない。  
フラッシュメモリ:自由に読み書き可能で、ルータの電源をオフにしても内容は消えない。  
RAN:読み書き可能だが、ルータの電源をオフにすると内容が消えてしまう。  
NVRAM:不揮発性ランダムアクセスメモリ。電源を切っても内容が消えない。

6.ルータの稼働中のコンフィギュレーションモードをサーバへバックアップする  
E.`copy running-config tftp:`

A.`copy tftp:startup-config` => startup-configは稼働中ではない  
B.`copy startup-config tftp;` => startup-configは稼働中ではない  
C.`copy running-config startup-config` => 稼働中の設定をNVRAMに保存する  
D.`copy tftp:running-config` => 順番が反対

特権EXECモードからcopyコマンドで「コピー元 コピー先」の順で指定する。

7.ルータのコンフィギュレーションモードレジスタ  
A.デフォルトのコンフィギュレーションレジスタ値は0x2102である  
B.現在のコンフィギュレーションレジスタ値を確認するには`show version`コマンドを使用する

C.パスワードリカバリでは、コンフィギュレーションレジスタ値を0x2124に変更する必要がある => 0x2142に変更する必要がある。これでルータのNVRAMのstartup-configを無視して起動するため、パスワードなしで特権EXECモードに遷移することができる  
D.コンフィギュレーションレジスタ値はフラッシュメモリ内に格納されている => NVRAM内  
E.コンフィギュレーションレジスタは12ビットの値であり、16進数で表示される => 16ビットの値

8.`(config)#config-register 0x2142`コマンドを実行し、ルータの再起動した  
D.セットアップモードで起動する

0x2142で起動する(3桁目が4)とNVRAMの設定を無視するためstartup-configをロードせずにスタートアップモードで起動する。

9.`boot system`コマンドでIOSイメージの格納場所を指定可能なものを2つ  
B.フラッシュメモリ  
E.TFTPサーバ

IOSの検索順序:フラッシュッメモリ => TFTPサーバ => ROM

10.Cisco IOSイメージをアップグレードするとき、ルータ上で確認する事項と、その情報を収集するために使用するコマンドを3つ  
A.フラッシュメモリの空き容量を確認する => `show flash:`コマンドで確認できる  
E.RAMに十分な空き容量があるか確認する  
G.`show version` => フラッシュメモリとRAMのサイズを確認できる

通常はIOSイメージファイルは圧縮されているため、ファイルを展開してRAMにロードしてIOSが実行される。

11.ルータをNTPクライアントにするためのコマンド  
A.`(config)#ntp server <ip-address>`  

D.`(config)#ntp master` => ルータをNTPサーバとして設定するコマンド  

グローバルコンフィギュレーションモードからコマンドを使用する。

12.シスコの第2世代サービス結合型ルータで、現在アクティブなライセンスを確認するためのコマンドを2つ  
A.`show version`  
B.`show license` => Cisco IOSソフトウェアライセンスに関する情報を確認
