# 演習問題
- 1.ルータのインターフェイスにIPアドレスを動的に割り当てるコマンド  
A.`(config)#ip dhcp enable`  
B.`(config-if)#ip address dhcp`  
C.`(config)#ip dhcp address`  
D.`(config-if)#ip address dynamic`  
E.`(config-if)#ip dhcp client`

- 2.DHCPの動作として正しいもの  
A.DISCOVERメッセージは、DHCPサーバがDHCPクライアントを検出するために送信する  
B.DHCPサーバはDISCOVERメッセージを受信するとACKで応答する  
C.DISCOVERメッセージはブロードキャストで送信される  
D.DHCPクライアントは、最初にREQUESTメッセージを送信してIPアドレスを要求する  
E.DHCPクライアントにIPアドレスが自動的に割り当てられるまでに3回メッセージをやり取りする

- 3.DHCPクライアントに通知するデフォルトゲートウェイを設定するためのコマンド  
A.`(dhcp-config)#default-router <ip-address>`  
B.`(config)#ip default-gateway <ip-address>`  
C.`(config-dhcp)#ip default-gateway <ip-address>`  
D.`(config-dhcp)#ip ip gateway <ip-address>`  
E.`(config)#ip ip dhcp excluded-address <ip-address>`

- 4.Windows PCでIPアドレスを自動的に割り当てる設定をしている時、DHCPで取得したIPアドレスなどの設定情報を確認するコマンド  
A.`ipconfig /release`  
B.`show ip dhcp pool`  
C.`show ip dhcp binding`  
D.`show ip dhcp conflict`  
E.`ipconfig /all`

- 5.ルータに`ip helper-address <server-address>`コマンドを設定したときの説明で正しいもの  
A.DHCPクライアントからの要求に対してルータが応答を返す  
B.DHCPパケットを受信したルータは、指定したIPアドレスへ中継する  
C.ルータがDHCPクライアントに対してDHCPサーバのIPアドレスを通知する  
D.ルータのインターフェイスにIPアドレスを自動的に割り当てる  
E.ルータはDHCPサーバとして動作する

- 6.NATの利点で正しいものを2つ  
A.内部ローカルアドレスとプライベートアドレスを変換できる  
B.内部ネットワークと外部ネットワークを分けることで企業ネットワークを安全にインターネットに接続できる  
C.内部ネットワークで使用しているアドレスを隠蔽し、セキュリティを向上する  
D.IPアドレスの不足の問題を解決する  
E.ルータのルーティングテーブルのサイズを小さくし、メモリの消費を抑えることができる

- 7.ポート番号を使用して複数のIPアドレスを1つのグローバルアドレスに変換する方式  
A.ダイナミックNAT  
B.スタティックNAT  
C.多重NAT  
D.グローバルNAT  
E.オーバーローディング

- 8.NATテーブルを参照するコマンド  
A.`show ip nat statistics`  
B.`show ip nat translations`  
C.`show nat translations`  
D.`show nat route nat`  
E.`show nat table`

- 9.ルータに設定したスタティックルートNATのコマンド  
出力内容:  
`RT1#show ip nat translation`  
Inside global:100.150.200.1 Inside local:192.168.1.1  
A.`ip nat inside source static 192.168.1.1 100.150.200.1`  
B.`ip nat pool static 192.168.1.1 100.150.200.1`  
C.`ip nat outside source static 192.168.1.1 100.150.200.1`  
D.`ip nat static pool 192.168.1.1 100.150.200.1`  
E.`ip nat inside source static 100.150.200.1 192.168.1.1`

- 10.PATを有効にするときのキーワードで正しいもの  
A.pat  
B.multiplex  
C.overload  
D.stack  
E.overloading

- 11.NATのIPアドレスを変換の様子を確認するコマンド  
A.`debug nat`  
B.`debug ip nat`  
C.`show nat`  
D.`debug ip nat translations`  
E.`show ip nat`

---
回答  
1.ルータのインターフェイスにIPアドレスを動的に割り当てるコマンド  
B.`(config-if)#ip address dhcp`

2.DHCPの動作で正しいもの  
C.DISCOVERメッセージはブロードキャストで送信される  
因みに、DISCOVERやREQUESTはブロードキャストなので通常はルータは転送しない

A.DISCOVERメッセージは、DHCPサーバがDHCPクライアントを検出するために送信する => クライアントからサーバへのメッセージ  
B.DHCPサーバはDISCOVERメッセージを受信するとACKで応答する => 応答はOFFER、ACKはREQUESTの受信に対する応答  
D.DHCPクライアントは、最初にREQUESTメッセージを送信してIPアドレスを要求する => DISCOVERでサーバを検出する  
E.DHCPクライアントにIPアドレスが自動的に割り当てられるまでに3回メッセージをやり取りする => 4つのメッセージを交換する

3.DHCPクライアントに通知するデフォルトゲートウェイを設定するためのコマンド  
A.`(dhcp-config)#default-router <ip-address>`

4.DHCPで取得したIPアドレスなどの設定情報を確認する  
E.`ipconfig /all`

5.ルータに`ip helper-address <server-address>`コマンドを設定  
B.DHCPパケットを受信したルータは、指定したIPアドレスへ中継する => UDPポート番号に基づいて、ブロードキャストのパケットをユニキャストにして中継する

6.NATの利点(2つ)  
C.内部ネットワークで使用しているアドレスを隠蔽し、セキュリティを向上する  
D.IPアドレスの不足の問題を解決する  
プライベートIPアドレスとグローバルIPアドレスを相互変換し、IPアドレスの不足を解決する

A.内部ローカルアドレスとプライベートアドレスを変換できる => 通常は内部ローカルアドレスにはプライベートアドレスを使用しているためNATによる変換は行わない

7.ポート番号を使用して複数のIPアドレスを1つのグローバルアドレスに変換する方式  
E.オーバーローディング => ポート番号を利用して複数のノードで1つのグローバルアドレスを共有して変換する

A.ダイナミックNAT:変換されるアドレス範囲をプールに登録し、その範囲のいずれかに変換される  
B.スタティックNAT:予め手動で設定したアドレスに1対1で変換する

8.NATテーブルを参照する  
B.`show ip nat translations`

A.`show ip nat statistics` => 統計情報を表示、テーブル情報は出ない

9.ルータに設定したスタティックルートNATのコマンド  
出力内容:  
`RT1#show ip nat translation`  
Inside global:100.150.200.1 Inside local:192.168.1.1  
A.`ip nat inside source static 192.168.1.1 100.150.200.1` => 内部ローカルアドレス、内部グローバルアドレスの順が正しい

E.`ip nat inside source static 100.150.200.1 192.168.1.1` => 順番逆

10.PATを有効にする  
C.overload => 複数のプライベートアドレスに対して1つのグローバルIPアドレスを共有してアドレスを変換する

11.NATのIPアドレスを変換の様子を確認する  
B.`debug ip nat` => 特権EXECモードから行う
