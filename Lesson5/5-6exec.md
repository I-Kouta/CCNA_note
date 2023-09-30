# 演習問題
- 1.ルータのコンソールポートを使用して管理アクセスをするときの説明として正しくないものを2つ  
A.ルータとPCには同じサブネットのIPアドレスを設定しておく必要がある  
B.ターミナルソフトのシリアルポート設定でボーレートを14,400にする必要がある  
C.ロールオーバーを使用する必要がある  
D.ルータが工場出荷時であってもアクセスが可能である  
E.PCのシリアルポートとルータのコンソールポートを接続する必要がある

- 2.IOSのモードに関する説明に該当するプロンプトを選択  
1.ルーティングプロトコルの設定を行う  
2.設定した全ての情報を見ることができる  
3.デバイス全体に関わる設定を行う  
4.一部の情報のみ表示でき、pingやtelnetを実行できる  
5.コンソールやVTYを行う  
</br>
A.`#`  
B.`(config-line)#`  
C.`(config-router)#`  
D.`(config)#`  
E.`>`

- 3.特権EXECモードへ移行することができるコマンドを3つ選択  
A.`Router#exec`  
B.`Router(config)#exit`  
C.`Router#enable`  
D.`Router#configure terminal`  
E.`Router>enable`  
F.`Router#disable`  
G.`Router>exec`  
H.`Router(config-if)#exit`  
I.`Router(config-if)#end`

- 4.特権EXECモードへ移行するためのコマンドを実行しても「e」で始めることしか覚えていない。このときの対象方法  
A.?キーを押す  
B.eと入力した後に続けてTabキーを押す  
C.eと入力したあとに続けて?キーを押す  
D.showと入力した後にスペースを入れて?キーを押す  
E.IOSのコマンドは省略形があるのでeだけ入力して実行する  

- 5.少し前に実行したコマンドを表示する方法を2つ  
A.`show terminal`コマンドを実行する  
B.↑キーを押す  
C.?キーを押す  
D.Ctrl + Pキーを押す  
E.Tabキーを押す

- 6.pingコマンドが実行可能なモード  
A.ユーザEXECモードのみ  
B.特権EXECモードのみ  
C.グローバルコンフィギュレーションのみ  
D.特権EXECモードとグローバルコンフィギュレーション  
E.ユーザEXECモードと特権EXECモード  

- 7.コマンドを実行して「% Incomplete command」というメッセージが表示されたときの原因  
A.入力した文字が不足しているため、コマンドを特定できなかった  
B.入力したコマンドの一部に誤りがある  
C.コマンドを実行するモードが誤っている  
D.コマンドが不完全である  
E.存在しないコマンドである

- 8.拡張pingの説明として正しいものを2つ  
A.特権EXECモードでのみ実行できる  
B.パケットの数やタイムアウト時間を指定できるが、プロトコルは指定できない  
C.ping\<ip address>コマンドで実行する  
D.ICMPエコーパケットの送信元IPアドレスを変更することができる  
E.拡張pingが成功した場合、*(アスタリスク)が表示される

- 9.ある管理者はルータのホスト名を変更した。ルータを再起動したときに変更した内容が自動的に反映されるようにするためのコマンド  
A.`#copy startup-config running-config`  
B.`#copy running-config startup-config`  
C.`#copy startup-config`  
D.`#copy running-config`  
E.設定は自動的にコンフィギュレーションファイルへ反映されるためコマンドは不要

- 10.ルータを再起動したときに自動的に読み込まれる設定を確認するコマンド  
A.`show nvram:`  
B.`show running-config`  
C.`show flash:`  
D.`show startup-config`  
E.`show reload-config`

- 11.Catalyst Switchを工場出荷時の状態を戻すために必要なコマンドを3つ
A.`#reload`  
B.`#exit`  
C.`#erase flash:vlan.dat`  
D.`#delete startup-config`  
E.`#delete vlan.dat`  
F.`#erase startup-config`  
G.`#erase running-config`  
H.`#system reload`

- 12.管理者は新しく購入したルータに基本設定を行い、再起動しても現在の設定と同じにするために次のコマンドを実行した。このときの説明として正しいもの  
`RT1#copy startup-config running-config`  
`%% Non-volatile configuration memory invalid or not present`  
A.現在の設定はNVRAMへ保存された  
B.コピー元とコピー先の指定が誤っている  
C.コマンドを実行するモードが誤っている  
D.NVRAMにrunning-configが存在していない  
E.コマンドの構文が間違っている

---
回答  
1  
A.ルータとPCには同じサブネットのIPアドレスを設定しておく必要がある  
B.ターミナルソフトのシリアルポート設定でボーレートを14,400にする必要がある  

2  
1.ルーティングプロトコルの設定 => C.`(config-router)#`  
2.設定した全ての情報を見る => A.`#`  
3.デバイス全体に関わる設定 => D.`(config)#`  
4.一部の情報のみ表示でき、pingやtelnetを実行 => E.`>`  
5.コンソールやVTYを行う => B.`(config-line)#`

3.特権EXECモードへ移行するコマンド  
B.`Router(config)#exit`  
E.`Router>enable`  
I.`Router(config-if)#end`

A.`Router#exec`:execというコマンドは存在しない  
C.`Router#enable`#だと不可。ユーザEXECモード(>)からenableコマンドを実行することが可能(B)  
D.`Router#configure terminal`:特権EXECモードからグローバルコンフィギュレーションモードへの移行  
F.`Router#disable`:特権EXECモードからユーザEXECモードへ移行  
G.`Router>exec`:execというコマンドは存在しない  
H.`Router(config-if)#exit`:インターフェイスコンフィギュレーションモードからグローバルコンフィギュレーションモードに戻る

4  
C.eと入力したあとに続けて?キーを押す  
これでeから始まるコマンドのリストが表示される

5.少し前に実行したコマンドを実行する  
B.↑キーを押す  
D.Ctrl + Pキーを押す

6.pingコマンドを実行する  
E.ユーザEXECモードと特権EXECモード

7.「% Incomplete command」というメッセージが表示されたときの原因  
D.コマンドが不完全である

8  
A.特権EXECモードでのみ実行できる  
D.ICMPエコーパケットの送信元IPアドレスを変更することができる  

C.ping\<ip address>コマンドで実行する:IPアドレス・ホスト名の入力をせずに実行する必要がある  
E.拡張pingが成功した場合、*(アスタリスク)が表示される:成功した場合の表示は「!」

9.はルータのホスト名を変更し、ルータを再起動したときに変更した内容が自動的に反映されるコマンド  
B.`#copy running-config startup-config`  

10.ルータを再起動したときに自動的に読み込まれる設定を確認するコマンド  
D.`show startup-config`

11.Catalyst Switchを工場出荷時の状態を戻すために必要なコマンドを3つ  
A.`#reload`:2.システムの再起動  
E.`#delete vlan.dat` :3.vlan.datの削除(または`delete flash:vlan.dat`)  
F.`#erase startup-config`:1.startup-configの削除  

B.`#exit`:管理アクセスをログアウト  
C.`#erase flash:vlan.dat`:eraseではなくdeleteなら可  
D.`#delete startup-config`:deleteではなくeraseなら可  
G.`#erase running-config`:現在の設定情報なのでeraseやdeleteで削除できない  
H.`#system reload`:存在しない

12  
`RT1#copy startup-config running-config`  
`%% Non-volatile configuration memory invalid or not present`  
B.コピー元とコピー先の指定が誤っている=> コピー元、コピー先の順で指定する  
