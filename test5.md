URL:https://www.infraexpert.com/blog/category/ccnaexam01/

---
1.OSI参照モデルの目的について、正しく解説している説明文は次のどれか(2つ選択)  
A.それぞれのレイヤで発生するネットワークの通信機能を定義している。  
B.ネットワーク全体をどのようにデータが移動していくのか理解を促進している。

C.階層化アプローチにより、信頼性の高いデータ配信を保証している。  
D.データの単位をレイヤ2ではパケット、レイヤ3ではフレームと定義している。

---
2.2つのエンドポイント間のコネクション確立で、TCPとUDPとではどのように異なるか。  
A.TCPは3ウェイハンドシェイクを使用し、UDPはメッセージ配送を保証しない。

---
3.トラフィック着信をホストに通知するためのEthernet Frameの構成要素はどれか。  
B.プリアンブル

A.FCS  
C.Typeフィールド  
D.Dataフィールド

---
4.IPv4プライベートアドレス空間を使用する最も適した理由は次のどれか(2つ選択)  
B.グローバルIPアドレスを節約するため  
D.企業内通信を可能にするため

A.アプリケーションとの通信を確立するため  
C.NATを導入するため

---
5.TCPとUDPとでは「信頼性」と「通信タイプ」に関して正しい説明はどれか。  
A.TCPは信頼性がありコネクション型プロトコルであるが、UDPは信頼性がないコネクションレス型プロトコルである。

---
6.SNMPエージェントが実行する機能として正しい説明はどれか。  
D.SNMPマネージャからの要求に応じて、MIB変数に関する情報を送信する。

A.ネットワークデバイスがRadius認証する際に仲介する役割を担う。  
B.ネットワーク上でLayer3デバイスの動作を管理する。  
C.障害が発生した場合にそのイベント情報を各デバイスから要求する。  

---
7.FTPとTFTPに関する正しい説明は次のどれか(2つ選択)  
A.FTPはTCPプロトコル上で動作して、ポート番号に20と21を使用する。  
D.TFTPはUDPプロトコル上で動作して、ポート番号に69を使用する。

---
8.コネクション型通信を行うプロトコルは次のどれか(3つ選択)  
B.SMTP  
D.FTP  
E.SSH

A.SNMP  
C.VoIP  
F.TFTP

---
9.光ファイバーケーブルについて正しく説明されているのは次のどれか(2つ選択)  
A.光は、光ファイバーケーブルのコアを透過する  
B.コア(glass core)は、クラッドに包まれている

C.BNCコネクタが光ファイバーの接続に使用される  
D.RJ45コネクタが光ファイバーの接続に使用される

---
10.宛先MACアドレスが不明なフレームをレイヤ2スイッチが受信した時、レイヤ2スイッチがデフォルトで行う動作は次のどれか。  
C.Layer2スイッチは受信したポートを除く全てのポートにフレームをフラッディングする。

A.Layer2スイッチは受信したフレームを全てのポートにフラッディングする。
B.Layer2スイッチは受信したフレームを全てドロップする。  
D.Layer2スイッチは宛先MACアドレスを学習するためCPUへパケットコピーを送信する。

---
11.CiscoルータやCatalystスイッチ上でパスワードがプレーンテキストとしてコンフィグに保存されないようにするコマンドは次のどれか。  
B.`service password-encryption`

A.`enable password`  
C.`enable secret`  
D.`username cisco password encrypt`

---
12.CDP(*Cisco Discovery Protocol*)の役割を正しい説明は次のどれか。  
D.上記の全て。 => 隣接するデバイスの情報を知ることができるシスコ独自のレイヤ2プロトコル

A.接続されているCiscoデバイスのIPアドレスを確認することができる。  
B.接続されているCiscoデバイスのハードウェアプラットフォームを確認できる。  
C.Catalystスイッチがそのポートに接続されているデバイスを検出できる。  

---
13.CDP(*Cisco Discovery Protocol*)に関する正しい説明は次のどれか。  
B.Cisco独自のプロトコルである。

A.ネットワーク層で動作するプロトコルである。  
C.物理層とデータリンク層の2つの層で動作するプロトコル。  
D.ルータ、ファイアウォール、スイッチなど全てのデバイスからの情報を検出できる。

---
14.Ciscoルータ上でSSHのRSAキーを生成するには、どのコンフィグレーションが必要か。  
C.DNSドメイン名を割り当てるコンフィグ設定

A.VTYアクセスのコンフィグ設定  
B.ユーザ名とパスワードのコンフィグ設定  
D.SSHのバージョンのコンフィグ設定

---
15.VTYアクセスでSSHに加えてTelnetをサポートするためのコマンドは次のどれか。  
C.`(config-line)#transport input telnet ssh`

A.`(config-line)#transport input telnet`  
B.`(config-line)#transport input ssh`  
D.`(config-line)#transport input level 15`

---
16.Cisco IOSでSSHが正常に動作するために満たす必要があるのは次のどれか(2つ選択)  
A.Ciscoルータ上で「ip domain-name」コマンドを設定する必要がある。  
B.CiscoルータはK9（crypto）IOSイメージを実行している必要がある。

C.Ciscoルータ上でIPルーティングを実行している必要がある。  
D.Ciscoルータ上でtelnetを無効化する必要がある。

---
17.Cisco IOSイメージファイルが保存されている場所は次のどれか。  
D.フラッシュメモリ

A.NVRAM  
B.RAM  
C.DRAM  

---
18.Ciscoルータの設定を初期化するためのコマンドは次のどれか。  
C.`#erase startup-config`

A.`#write terminal`  
B.`#erase running-config`  
D.`(config)#erase startup-config`

---
19.Ciscoルータへのリモート接続する際に通信プロトコルを暗号化できるのは次のどれか。  
D.SSH

A.HTTP  
B.SNMP  
C.telnet

---
20.Telnet / SSH接続で自動的なログアウトを無効化するコマンドは次のどれか。  
C.`(config-line)#exec-timeout 0 0`

A.`(config)#exec-timeout 0 0`  
B.`(config)#timeout exec disable`  
D.`(config-line)#timeout exec disable`
