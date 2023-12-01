# 演習問題
- 1.RIPv2の説明で正しいものを4つ  
A.トポロジに変更があった場合、即時にアップデートを送信する  
B.Helloパケットを使用して隣接ルータとネイバー関係を確立後にアップデートを送信する  
C.トポロジに変更がない場合、アップデートを送信しない  
D.自動経路集約はデフォルトで有効化されている  
E.クラスレスルーティングプロトコルであり、手動経路集約のみ可能である  
F.トポロジに変更がない場合でも定期的にアップデートを送信する  
G.メトリックはコストを使用する  
H.認証機能をサポートしている

- 2.出力から正しい説明を3つ(出力割愛)  
A.アップデートを送信してから18秒経過している  
B.networkコマンドは1行だけ実行している  
C.no auto-summaryコマンドは実行していない  
D.1つのインターフェイスでRIPv2が動作している  
E.経路情報が無効だと判断した時、180秒後に経路が削除される  
F.Router1のネクストホップルータのIPアドレスは172.16.101.1である  
G.maximum-pathsコマンドを実行している

- 3.無限カウントを防ぐためのRIPの最大値  
A.15 B.12 C.20 D.16 E.30

- 4.RIPのデフォルトのタイマー値が正しいもの  
A.Sending updates every 60 seconds, next due in 18 seconds  
Invalid after 180 seconds, hold down 180, flushed after 220  
B.Sending updates every 30 seconds, next due in 18 seconds  
Invalid after 160 seconds, hold down 160, flushed after 240  
C.Sending updates every 30 seconds, next due in 18 seconds  
Invalid after 180 seconds, hold down 180, flushed after 240  
D.Sending updates every 30 seconds, next due in 18 seconds  
Invalid after 120 seconds, hold down 120, flushed after 220  
E.Sending updates every 30 seconds, next due in 18 seconds  
Invalid after 180 seconds, hold down 240, flushed after 180

- 5.ルーティングプロトコルのHelloメッセージが送信できない原因で考えられるもの  
A.ネイバー関係を確立していない  
B.カプセル化タイプの不一致  
C.アドミニストレーティブディスタンス値の不一致  
D.インターフェイスにpassive-interfaceを設定している  
E.インターフェイスに誤ったbandwidth値を設定している

- 6.出力から、全てのアクティブなインターフェイス上でRIPv2を有効化するためのコマンドを5つ選択(出力割愛)  
A.`(config)#ip router rip`  
B.`(config-router)#network 10.0.0.0`  
C.`(config-router)#network 172.31.20.0`  
D.`(config-router)#network 192.168.7.0`  
E.`(config-router)#network 172.31.0.0`  
F.`(config)#router rip`  
G.`(config-router)#network 192.168.0.0`  
H.`(config-router)#version 2`  
I.`(config-router)#no auto-summary`  
J.`(config-router)#network 192.168.13.0`

- 7.前問をの出力を参照し、Fa0 / 1インターフェイスからRIPのアップデートの送信を抑制するコマンド  
A.`(config)#interface fa0/1`  
`(config-if)#passive-interface`  
B.`(config)#interface fa0/1`  
`(config-if)#ip rip update passive`  
C.`(config)#router rip`  
`(config-router)#ip passive-interface fa0/1`  
D.`(config)#interface fa0/1`  
`(config-if)#no ip rip update`  
E.`(config)#router rip`  
`(config-router)#passive-interface fa0/1`

- 8.RIPv2の自動経路集約を無効化するためのコマンド  
A.`(config-router)#auto-summary disable`  
B.`(config-router)#no auto-summary run`  
C.`(config-router)#auto-summary`  
D.`(config-router)#no auto-summary`  
E.自動経路集約は無効化できない

- 9.RIPのアップデートでデフォルトルートを配布するためのコマンド  
A.`(config-if)#ip rip default-route originate`  
B.`(config-router)#default-information originate`  
C.`(config-router)#default-route originate`  
D.`(config-if)#ip rip default-information originate`  
E.`(config-router)#rip update default-route originate`

---
回答  
1.RIPv2で正しいもの4つ  
A.トポロジに変更があった場合、即時にアップデートを送信する => トリガードアップデート  
D.自動経路集約はデフォルトで有効化されている  
F.トポロジに変更がない場合でも定期的にアップデートを送信する  
H.認証機能をサポートしている => シンプルパスワード認証とMD5認証をサポート

B.Helloパケットを使用して隣接ルータとネイバー関係を確立後にアップデートを送信する => これはリンクステート型  
E.クラスレスルーティングプロトコルであり、手動経路集約のみ可能である => 自動でも可能  
G.メトリックはコストを使用する => メトリックはホップ数

2.正しい説明を3つ  
B.networkコマンドは1行だけ実行している  
C.no auto-summaryコマンドは実行していない  
F.Router1のネクストホップルータのIPアドレスは172.16.101.1である

A.アップデートを送信してから18秒経過している => next due in 18 secondsは次のアップデートまで18s  
D.1つのインターフェイスでRIPv2が動作している => 有効なインターフェイス名とバージョンは複数ある  
E.経路情報が無効だと判断した時、180秒後に経路が削除される => 無効と認識されてから60s(240 - 180)経過で経路情報は削除される  
G.maximum-pathsコマンドを実行している => ロードバランシング(負荷分散)はデフォルトの4のまま

3.無限カウントを防ぐためのRIPの最大値  
D.16 => アクセス可能なホップカウントの最大値は15

4.RIPのデフォルトのタイマー値  
C.Sending updates every 30 seconds, next due in 18 seconds  
Invalid after 180 seconds, hold down 180, flushed after 240

Sendingが30s、Invalidが180s、Hold downが180s、Flushed afterが240s

5.ルーティングプロトコルのHelloメッセージが送信できない原因  
D.インターフェイスにpassive-interfaceを設定している

OSRFやEIGRP(ディスタンスベクター型のルーティングプロトコル)では、Helloパケットも送信されない。RIPはディスタンスベクター型であり、Helloパケットは使用しない  

6.全てのアクティブなインターフェイス上でRIPv2を有効化するコマンド5つ  
B.`(config-router)#network 10.0.0.0`  
E.`(config-router)#network 172.31.0.0`  
F.`(config)#router rip` => 1.RIPプロセスの有効化のためルータコンフィギュレーションモードに移行する  
H.`(config-router)#version 2` => 2.RIPバージョン2の有効化  
J.`(config-router)#network 192.168.13.0`  

クラスフルなネットワークアドレス(ホスト部が0)である必要がある。  
C.`(config-router)#network 172.31.20.0` => 20が不適切  
D.`(config-router)#network 192.168.7.0` => 管理的に無効になっている(クラスフルネットワークアドレスにはなっている)  
G.`(config-router)#network 192.168.0.0` => ホスト部は24ビット  
I.`(config-router)#no auto-summary`  
アドレスクラス:  
クラスA:先頭が**0**でネットワーク部は8ビット(1 ~ 126)  
クラスB:先頭は**10**でネットワーク部は16ビット(128 ~ 191)  
クラスC:先頭は**110**でネットワーク部は28ビット(192 ~ 223)  
クラスD:先頭は**1110**で同一ネットワークでのみ送信されルータで転送されない(224 ~ 239)

7.RIPのアップデートの送信を抑制するコマンド  
E.`(config)#router rip`:ルータコンフィギュレーションモードに移行  
`(config-router)#passive-interface fa0/1`:先頭にipはつかない

8.自動経路集約を無効化するコマンド  
D.`(config-router)#no auto-summary`

C.`(config-router)#auto-summary`:自動経路集約を有効化する

9.RIPのアップデートでデフォルトルートを配布する  
B.`(config-router)#default-information originate`
