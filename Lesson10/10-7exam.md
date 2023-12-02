# 演習問題
- 1.アクセスリストの説明で不適切なもの  
A.アクセスリストによって、ルータから発信されるパケットを制御することはできない  
B.アクセスリストによって、パケットのフィルタリングを行うことができる  
C.アクセスリストの番号によって、指定できる条件が決められている  
D.アクセスリストはトラフィックの分離を行うことができる  
E.アクセスリストによって、ルータへのウイルス侵入を防止できる

- 2.インバウンドのアクセスリストが処理されるタイミングとして正しいもの  
A.パケットをインターフェイスで受信したとき  
B.パケットをインターフェイスから送信するとき  
C.パケットを受信してルーティングテーブルを参照したあと  
D.パケットを受信してARP処理を行ったあと  
E.パケットを受信してインターフェイスから送信したあと

- 3.ワイルドカードマスクの説明で正しいものを2つ  
A.特定のホストを指定するとき、ワイルドカードマスクは全て0を指定する  
B.特定のホストを指定するとき、ワイルドカードマスクは全て1を指定する  
C.任意の指定をするとき、ワイルドカードマスクは全て0を指定する  
D.任意の指定をするとき、ワイルドカードマスクは全て1を指定する  
E.任意のプロトコルを指定するとき、ワイルドカードマスクを使用する

- 4.標準ACLの説明で正しいものを2つ選択  
A.ワイルドカードマスクは省略できない  
B.条件に送信元IPアドレスを含めることはできない  
C.ワイルドカードマスクを省略すると0.0.0.0が適用される  
D.条件に特定のプロトコルを指定することができる  
E.条件に宛先IPアドレスを含めることはできない

- 5.アクセスリストのステートメントと同じ意味をもつものを2つ  
`access-list 10 permit 172.16.1.1`  
A.`access-list 10 permit host 172.16.1.1`  
B.`access-list 10 permit ip 172.16.1.1`  
C.`access-list 10 permit 172.16.1.1 0.0.0.0`  
D.`access-list 10 permit 172.16.1.1 255.255.255.255`  
E.`access-list 10 permit any`

- 6.アクセスリストの適用場所の説明で正しいものを2つ  
A.標準アクセスリストの場合、宛先近くに配置する  
B.拡張アクセスリストの場合、宛先近くに配置する  
C.標準アクセスリストの場合、送信元近くに配置する  
D.拡張アクセスリストの場合、送信元近くに配置する  
E.標準アクセスリストの場合、送信元、宛先のどちらにも配置できる  

- 7.アクセスリストの条件で、特定のサブネット「172.16.20.0 / 24」を指定するためのワイルドカードマスク  
A.255.255.255.0  
B.255.255.0.0  
C.0.0.255.255  
D.0.0.0.255  
E.0.0.31.255  

- 8.ルータを通過するパケットのフィルタリングを設定したい。ルータのFa0 / 1インターフェイスでパケットを着信したとき、ACL10と照合させるためのコマンド  
A.`(config)#interface fa0/1`  
`(config-if)#ip access-list 10 out`  
B.`(config)#interface fa0/1`  
`(config-if)#ip access-list 10 in`  
C.`(config)#interface fa0/1`  
`(config-if)#ip access-group 10 out`  
D.`(config)#interface fa0/1`  
`(config-if)#access-group 10 in`  
E.`(config)#interface fa0/1`  
`(config-if)#ip access-group 10 in`

- 9.ルータのインターフェイスに適用したアクセスリストの方向を確認できるコマンド  
A.`show interfaces`  
B.`show ip interface`  
C.`show access-lists`  
D.`show ip route`  
E.`show interface access-lists`

- 10.ACLの条件に一致したパケット数を消去するためのコマンド  
A.`(config)#no access-list <acl-number>`  
B.`#clear access-list counters`  
C.`(config-if)#no ip access-group <acl-number>`  
D.`#delete access-list counters`  
E.`(config)#no access-list counters`

---
回答  
1.アクセスリストの説明の誤り  
E.アクセスリストによって、ルータへのウイルス侵入を防止できる  

正しいもの  
A.アクセスリストによって、**ルータから発信される**パケットを制御することはできない  
B.アクセスリストによって、パケットのフィルタリングを行うことができる  
C.アクセスリストの番号によって、指定できる条件が決められている  
D.アクセスリストはトラフィックの分離を行うことができる

2.インバウンドのアクセスリストが処理されるタイミング  
A.パケットをインターフェイスで受信したとき

パケットを受信してACLと照合し、許可で一致した場合、ルーティングテーブルを参照して発進インターフェイスを決定

3.ワイルドカードマスクの説明(2つ)  
A.特定のホストを指定するとき、ワイルドカードマスクは全て0を指定する  
D.任意の指定をするとき、ワイルドカードマスクは全て1を指定する

IPアドレスのどの部分をチェックするかと指定する。0を指定すると対応するビットをチェックし、1を指定すると無視する

4.標準ACLの説明  
C.ワイルドカードマスクを省略すると0.0.0.0が適用される  
E.条件に宛先IPアドレスを含めることはできない => 送信元IPアドレスだけを指定できる

5.`access-list 10 permit 172.16.1.1`と同じ意味をもつものを2つ  
A.`access-list 10 permit host 172.16.1.1` => 172.16.1.1 0.0.0.0と同じ意味  
C.`access-list 10 permit 172.16.1.1 0.0.0.0` => 0.0.0.0が省略されている  

E.`access-list 10 permit any` => 全てのパケットを許可する

6.アクセスリストの適用場所  
A.標準アクセスリストの場合、宛先近くに配置する  
D.拡張アクセスリストの場合、送信元近くに配置する

標準アクセスリストはパケットの送信元アドレスをチェックする。そのため送信元近くに配置をすると意図しないコンピュータにもアクセスが出来なくなる可能性がある

7.172.16.20.0 / 24を指定するワイルドカードマスク  
D.0.0.0.255

8.ルータのFa0 / 1インターフェイスでパケットを着信したとき、ACL10と照合させる  
E.`(config)#interface fa0/1`  
`(config-if)#ip access-group 10 in`

9.アクセスリストの方向を確認できる  
B.`show ip interface`

A.`show interfaces`:インターフェイスの詳細情報を表示  
C.`show access-lists`:全てのACL(ステートメント)を表示  
D.`show ip route`:ルーティングテーブルを表示

10.ACLの条件に一致したパケットを消去する  
B.`#clear access-list counters`

A.`(config)#no access-list <acl-number>`:アクセスリストを削除  