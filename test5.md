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

---
21.2つの異なるルーティングプロトコルから同じ宛先ネットワークへ2つ以上の異なるルートが存在する場合、ルータは次のどの属性を使用して最適パスを選択するか。  
B.アドミニストレーティブディスタンス

A.ホップ数  
C.メトリック  
D.デュアル アルゴリズム

---
22.ルータが2つの異なるネイバー(EIGRPネイバーとOSPFネイバー)から、同じルートを学習した時、ルーティングテーブルにインストールされるそのルート情報のAD値はどれか。  
C.90 => EIGRPのAD値

A.10  
B.20 => EBGPのAD値  
D.110 => OSPFのAD値

---
23.EIGRPを有効化しているルータが2つの異なるパスから同じルートを学習した時、ルータは最適なパスを選択するためにどのパラメータを使用するか。  
D.メトリック

A.ホップ数  
B.コスト値  
C.アドミニストレーティブディスタンス

---
24.スタティックルートとダイナミックルートに関する正しい説明は次のどれか。  
A.スタティックルートはネットワーク管理者によって手動で作成されるのに対して、ダイナミックルートはルーティングプロトコルによって自動的に学習され調整される。

---
25.ディスタンスベクタ型のダイナミックルーティングプロトコルは次のどれか(2つ選択)  
C.EIGRP  
D.RIP

A.OSPF B.IS-IS => リンクステート型  
E.BGP => EGPルーティングプロトコル

---
26.ルーティングテーブルを表示した時、どの情報を知ることができるか(2つ選択)  
B.AD値が動的または手動でコンフィグ設定されたかどうか  
D.あて先ルートが追加されてからの経過時間

A.ルーティングプロトコルの自律システム番号  
C.どのネイバー関係が確立したかどうか

---
27.リンクステート型のダイナミックルーティングプロトコルは次のどれか(2つ選択)  
A.OSPF  
B.IS-IS

C.EIGRP  
D.RIP  
E.BGP

---
28.ルータが複数のルーティングプロトコルを介して172.16.1.0 / 24のルート情報を学習した時、次のどのルートがルーティングテーブルにインストールされるか。  
D.最も小さなAD値を持つルート

A.プレフィックス長が最も短く一致するルート  
B.最も小さいコスト値を持つルート  
C.最も大きなネクストホップのIPアドレスを持つルート

---
29.管理者がフローティングスタティックルートを設定する理由は次のどれか(2つ選択)  
B.ダイナミックルーティングが失敗した時、代替のスタティックルートを有効にするため  
D.プライマリパスがダウンした時に、トラフィックをセカンダリパスへ自動的に切り替えてルーティングさせるため

A.スタティックルートによる負荷分散を実現するため  
C.パケットの送信元IPに基づいて負荷分散を実現するため

---
30.デフォルトルートの正しい説明は次のどれか。  
A.ルーティングテーブル上に宛先ネットワークが存在しない場合に使用されるルート

B.ダイナミックルーティングが失敗した場合にのみ使用されるルート  
C.スタティックルーティングが失敗した場合にのみ使用されるルート  
D.ルータの内部でデフォルトで設定されているルート

---
31.エンジニアがOSPFネイバーをDR(指定ルータ)としてコンフィグ設定した場合、そのDR(指定ルータ)が適切なモードであると確認できるステータスは次のどの状態か。  
D.Full

A.Init  
B.Exchange  
C.2-way

---
32.OSPFを実行する2つのルータはシリアルインタフェースで接続されている。カプセル化がPPPである場合、`show ip ospf interface`で表示されるネットワークタイプはどれか。  
C.point-to-point

A.broadcast  
B.nonbroadcast  
D.point-to-multipoint

---
33.OSPFを実行する2つのルータは、GigabitEthernetインタフェースで接続されている。このインターフェースは次のどのタイプのOSPFネットワークに属しているか。  
A.broadcast

B.nonbroadcast  
C.point-to-point  
D.point-to-multipoint

---
34.`show ip ospf interface`コマンドにより表示される情報は次のどれか。  
C.OSPF関連のインターフェース情報を表示

A.OSPFネイバー情報をインターフェースごとに表示  
B.OSPFネイバー情報をインターフェースタイプごとに表示  
D.OSPFルーティングプロセスに関する一般情報を表示

---
35.ルーティングプロトコルのOSPFとして正しく説明されているのはどれか(3つ選択)  
A.VLSMをサポートしている  
C.ネットワークの不安定性をネットワークの1つのエリアに限定できる時がある  
E.ルーティングアップデートを広範囲に制御できる

B.RIPv2よりもコンフィグレーションがシンプルである  
D.ネットワーク上のルーティングのオーバヘッドを増加させる

---
36.OSPFの`router-id`コマンドでルータを設定したが、そのIPアドレスはまだ物理interfaceを反映している時、影響を最小限に抑える方法で問題を修正するための方法はどれか。  
A.OSPFプロセスを再起動する

B.OSPFを実行しているルータを再起動する  
C.ルータを設定保存する  
D.loopbackインターフェースのIPアドレスを指定する

---
37.OSPFネイバーの隣接関係を確立することに妨げる可能性がある状況はどれか(2つ選択)  
D.隣接するOSPFルータの両方ともが同じルータIDを使用している。

B.隣接するOSPFルータのHelloタイマーとDeadタイマーがミスマッチしている  
A.隣接するOSPFルータのプロセスIDがミスマッチしている  
C.マルチキャストアドレス224.0.0.10のトラフィックをACLでブロックしている

---
38.OSPFのリンクステートの集合体を表示するためのコマンドは次のどれか。  
C.`show ip ospf database`

A.`show ip ospf neighbor`  
B.`show ip route`  
D.`show ip link neighbor`

---
39.OSPFのHelloプロトコルの役割を説明しているのは次のどれか(2つ選択)  
A.OSPFネイバー関係を維持している  
C.OSPFネイバーを動的に発見している

B.OSPFネイバー探索にネットワーク全体にブロードキャストパケットを送出する  
D.OSPF以外のルーティングプロトコルとの隣接関係を維持している

---
40.OSPFv2の動作を有効にするために、アクティブなインターフェースで構成する必要な2つの最小のパラメータは次のどれか(2つ選択)  
B.OSPFエリア  
C.OSPFプロセスID

A.IPv6アドレス  
D.OSPF MD5の認証キー

---
41.標準ACL、拡張ACLの最も効率的な適用場所は次のどれか(2つ選択)  
A.標準ACL：宛先ネットワークに近いルーティング機器のインターフェース  
D.拡張ACL：送信元ネットワークに近いルーティング機器のインターフェース

B.標準ACL：送信元ネットワークに近いルーティング機器のインターフェース  
C.拡張ACL：宛先ネットワークに近いルーティング機器のインターフェース

---
42.interfaceに適用されているACLを確認するためのコマンドは次のどれか。  
B.`show ip interface`

---
43.CiscoルータをDHCPクライアントにするためのコマンドは次のどれか。  
B.`(config-if)# ip address dhcp`

---
44.GigabitEthernet0/1がDHCP経由で設定されていることを示すコマンドはどれか。  
C.`show ip interface GigabitEthernet 0/1`

A.`show ip dhcp pool` => DHCPプールの表示  
D.`show cdp neighbor` => CDPの情報

---
45.DHCPの役割を正しく説明しているのは次のどれか(2つ選択)  
A.DHCPサーバはクライアントIPアドレスを動的にリースする  
D.DHCPサーバはIPアドレスのプールから特定のIPアドレスを除外する機能を持つ

B.DHCPクライアントは、DHCPで割り当て可能なプール情報を維持する  
C.DHCPサーバはクライアントからの更新を要求することなくIPアドレスを割り当てる

---
46.CiscoルータをDHCPサーバに設定して、そのDHCPサーバ上で割り当てられているアドレスを確認するためのコマンドは次のどれか。  
C.`show ip dhcp binding`

A.`show ip dhcp pool`  
B.`show ip dhcp conflict`  
D.`show ip interface`

---
47.次のどのタイプのIPアドレスが、NATデバイスのパブリックIPアドレス(グローバルIPアドレス)であるか。  
B.inside global

A.inside local  
C.outside local  
D.outside global

---
48.NATのコンフィグ設定でどのキーワードにより、1つの外部IPアドレスを複数のホストに使用することができるか。  
C.overload

A.pool  
B.dynamic  
D.nat

---
49.NAT overloadの性質について正しい説明は次のどれか。  
A.内部IPアドレスに対して、1対多の関連性を適用する

B.内部IPアドレスに対して、1対1の関連性を適用する  
C.内部IPアドレスに対して、多対多の関連性を適用する  
D.WAN側に接続するGigabitEthernetインターフェースに対してのみ適用できる

---
50.以下のCiscoルータ上のコンフィグ設定によって有効になる機能は次のどれか。  
`(config)#ip nat pool CISCO 192.168.1.0 192.168.1.10 255.255.255.0`  
D.ダイナミックNATアドレスプール

A.スタティックNAT  
B.PAT  
C.DHCPプール

---
51.ネットワークの3階層ネットワークに該当する3つの層は次のどれか(3つ選択)  
B.アクセス層  
D.ディストリビューション層  
F.コア層

---
52.3階層ネットワークトポロジーのおける正しい説明は次のどれか(2つ選択)  
B.ディストリビューション層では、レイヤ2とレイヤ3処理を行う  
D.コア層は、一方に障害が発生しても継続的に通信維持できるよう設計する

A.アクセス層では、ルーティングを実行する => デストリビューション層  
C.コア層は、エンドデバイスの接続を行う => アクセス層

---
53.CDPが有効なCiscoデバイスが相互接続されている時、隣接デバイスのインターフェースのIPアドレスが設定されていない時、どのような状態になるか。  
B.CDPは正常に動作するが、そのネイバーからのIPアドレス情報は認識しない

A.CDPは、そのネイバーの別のインターフェースのIPアドレスを使用して認識する  
C.CDPは正常に動作するが、そのネイバーからの全ての情報を認識しない  
D.CDPは無効となり、そのネイバーからの全ての情報を認識しない

---
54.ネットワーク管理者がCDPを有効化する利点や理由は次のどれか(2つ選択)  
A.レイヤ3接続が正常に動作しない時、デバイス間のレイヤ2接続を確認できること => **シスコ独自のレイヤ2プロトコル**  
C.デバイスにTelnet接続するために、隣接デバイスのIPアドレスを確認できること

B.2つのデバイスを相互接続するケーブルタイプを確認できること  
D.隣接デバイスのVLAN情報を確認できること

---
55.Cisco IOSでグローバルにLLDPを有効化するためのコマンドはどれか。  
A.`Cisco(config)# lldp run`

---
56.次のどのコマンドを使用することで、LLDPの任意のインターフェースで初期化するための遅延時間を秒単位で指定することができるか。  
C.lldp reinit

---
57.LLDPの初期化遅延を3秒に設定するためのコマンドは次のどれか。  
B.`Cisco(config)# lldp reinit 3`

---
58.PoEにおける受電デバイスと給電デバイスの正しい組合わせは次のどれか。  
B.PSE（給電デバイス：PoEスイッチ）  
C.PD（受電デバイス：IP電話、無線アクセスポイント）

---
59.PoEのIEEE 802.3af power classification override機能が有効になっている時、Catalystのスイッチポートで実行されるアクションは次のどれか。  
A.監視対象のスイッチポートが電力の最大管理値を超えると、ポートはシャットダウンされErrdisable状態となる。

---
60.Catalystのスイッチポートに着信するフレームが、フレームチェックシーケンスに失敗する時、次のどのインターフェースカウンターが増加するか(2つ選択)  
A.CRC  
B.input errors

---
61.Catalystでデフォルトで作成されているVLANのVLAN IDは次のどれか(2つ選択)
B.1  
E.1005  
=> 標準ACLは1 ~ 99, 1300 ~ 1999、拡張ACLは100 ~ 199, 2000 ~ 2699

---
62.フレームのフラッディングが発生した時の正しい動作は次のどれか。  
D.フレームは、元のポートを除き同じVLAN内のスイッチ上の全てのポートに送信される

---
63.CDPにより収集できる情報は次のどれか(2つ選択)  
A.ネイティブVLAN  
C.VTPドメイン名

---
64.スイッチネットワークでVTPを使用するメリットは次のどれか(2つ選択)  
B.スイッチネットワーク全体でVLANの一貫性を維持する  
D.スイッチネットワーク全体にVLAN情報を自動的に伝播できる

---
65.次の音声VLANの設定をした時、Cisco IP Phoneを接続している時の動作はどれか。  
`interface GigabitEthernet0/1`  
`switchport voice vlan 3`  
A.IP電話はVLAN3でデータを送受信、IP電話に接続されたPCはVLAN1でデータを送受信

---
66.STPはどのようにしてレイヤー2のループを防止しているか。  
B.ポートブロッキング

---
67.`spanning-tree portfast`コマンドの主な効果は次のどれか。  
A.PCを接続した時やスイッチを再起動した時、即座にポートをフォワーディングにする  

---
68.特定のインターフェースをスパニングツリープロトコルでの優先転送インターフェースとして構成するために変更できる値は次のどれか。  
C.ポートプライオリティ

---
69.`show spanning-tree vlan`コマンドで「Spanning tree enabled protocol rstp」と表示された時、このスイッチでのスパニングツリーのモードは次のどれか。  
B.スパニングツリーのモードは、Rapid PVST+である

---
70.スイッチで最上位BPDU(最良のBPDU)を受信するとポートはどのタイプになるか。  
C.ルートポート

---
71.ネゴシエーションプロトコルを使用することなく、2つのスイッチ間でEtherChannelを構成するためには、次のどのモードを使用する必要があるか。  
C.on

---
72.EtherChannelの技術についての正しい説明は次のどれか(2つ選択)  
A.FastEthernetまたはGigabitEthernetインターフェースを単一の EtherChannel に束ねることで帯域幅を拡大する  
B.EtherChannel内のリンクの1つに障害が発生しても冗長性を維持できる。

---
73.オープンスタンダードプロトコル(LACP)でレイヤ3EtherChannelを確立するためのスイッチでの必要なコンフィグはどれか(2つ選択)  
A.`interface GigabitEthernet0/1`  
`channel-group 5 mode active`  
D.`interface port-channel 5`
`no switchport`
`ip address 192.168.0.1 255.255.255.0`

---
74.アクティブにネゴシエートするEtherChanelを構成するために使用するコンフィグ設定は次のどれか(2つ選択)  
B.`channel-group 5 mode desirable`  
D.`channel-group 5 mode active`

---
75.EtherChannelを構成する時、LACPデバイスが検出された場合にのみ、LACPを有効にするモードは次のどれか。  
C.passive

---
76.送信元と宛先IPアドレスに基づいたEtherChannel内でのトラフィックを負荷分散を実現するためのコマンドは次のどれか。  
B.`(config)# port-channel load-balance src-dst-ip`  

---
77.EtherChannelを構成するインターフェースにおいて、プロトコルのモードまで確認するコマンドはどれか。  
C.`show etherchannel detail`  

---
78.Cisco独自のプロトコルでEtherChannelを構成するモードは次のどれか(2つ選択)  
C.desirable  
D.auto

---
79.LACPとPagPを使用せずにEtherChannelを構成するモードは次のどれか  
B.on

---
80.対向スイッチとのEtherChannelの構成に失敗した場合、次のどれが原因であるか。  
C.対向スイッチの物理ポートの「speed/duplex、VLAN番号」が一致していない

---
81.HSRPグループを構成する2つの要件は次のどれか(2つ選択)  
C.1つのアクティブルータ  
D.1つ以上のスタンバイルータ

---
82.HSRPグループ内のルータの優先度を確認するためのコマンドはどれか。  
D.`show standby`

---
83.ルータを再起動した後、高いプライオリティのHSRPルータがHSRPのプライマリルータになることを保証するためには、次のどのコンフィグ設定が必要となるか。  
B.`standby 5 preemp`

---
84.VRRPで使用される仮想MACアドレスは次のどのMACアドレスか。  
D.0000.5E00.0111

---
85.HSRPにおける予測できる動作は次のどれか(2つ選択)  
A.2台のルータは、LAN上のデバイスのデフォルトゲートウェイとして使用する仮想IPアドレスを共有する。  
B.2台のルータは、一方をアクティブルータに、もう一方をスタンバイルータになるようにネゴシエートする。

---
86.大都市圏の複数の支社をWANで相互接続する必要があり、通信要件として、WANで伝送される音声、ビデオ、データなど大容量トラフィックが高速通信できること、既存LANネットワークをスムーズに統合できることである。最適なWAN接続方式は次のどれか。  
D.Ethernet WAN（広域イーサネット）

---
87.CiscoデバイスをNTPサーバとして構成するために必要なコマンドは次のどれか。  
B.`ntp master`

A.`ntp server` => NTPサーバと時刻同期する

---
88.`show ntp status`コマンドの出力から判断できる情報は次のどれか(2つ選択)  
A.クロックが同期されているかどうか  
D.クロックが同期されているピアのIPアドレス

---
89.IP SLAがUDPジッタを測定するためには、次のどの機能またはプロトコルが必要か。  
A.NTP

---
90.QoSのWREDによって実行される2つのアクションは次のどれか(2つ選択)  
B.優先度の高いパケットがドロップする前に、優先度の低いパケットをドロップさせる  
D.キューが満杯になることを防ぐことにより、輻輳を緩和できる

---
91.次のどのアクションのセットが、多要素認証の要件を満たしているか。  
A.ユーザはユーザ名をパスワードを入力して、スマホの認証アプリで通知をクリック。

---
92.サイト間VPNの通信を行う際、ユーザデータの転送を行うプロトコルは次のどれか。  
D.IPsec

---
93.ハブアンドスポーク構成でフルメッシュトポロジーを確立するVPNの種類はどれか。  
B.Dynamic Multipoint VPN

---
94.以下のコンフィグ設定を行った時、スイッチの動作にどのような影響がでるか。  
`(config)# ip arp inspection vlan 10`  
`(config)# interface GigabitEthernet0/1`  
`(config-if)# switchport mode access`  
`(config-if)# switchport access vlan 10`  
D.GigabitEthernet0/1のインターフェースの状態がuntrust(信頼できない)になる

---
95.以下のコンフィグ設定を行った時、スイッチの動作にどのような影響がでるか。  
`(config)# ip arp inspection vlan 10`  
`(config)# interface GigabitEthernet0/1`  
`(config-if)# switchport mode access`  
`(config-if)# switchport access vlan 10`  
A.GigabitEthernet0/1に着信してくるトラフィックのうち、無効なMAC/IPアドレスの関連付けテーブル(バインディングテーブル)持つ全てのARPトラフィックを破棄する

---
96.以下のコンフィグでネットワーク全体で正常に通信できている時、GigabitEthernet0/1のインターフェースに次のどのタイプのネットワーク機器を接続する必要があるか。  
`(config)# ip arp inspection vlan 10`  
`(config)# interface GigabitEthernet0/1`  
`(config-if)# ip arp inspection trust`  
D.ルータ

---
97.DHCPスヌーピングを有効にするコマンドは次のどれか。  
D.`(config)# ip dhcp snooping`

---
98.`aaa new-model`コマンドを1行設定することで、どのような効果が得られるか。  
B.そのデバイス上でAAAがサービスが有効になる

---
99.AAAの「認証」と「認可」の主な違いは次のどれか。  
B.認証はネットワークシステムにアクセスしようとしているユーザーの識別と検証を行い、認可はユーザが実行できるタスクを制御する

---
100.RADIUSとTACACS+の違いは何か。  
A.TACACS+は「認証」「認可」のサービスが分離しているのに対して、RADIUSでは、「認証」「認可」のサービスが統合されている

---
101.異なるセグメント上の端末と通信できるが、インターネット上ではルーティングされず、組織内ネットワークでのみ有効なアドレスのタイプは次のどれか。  
B.ユニークローカル

---
102.インターフェースでIPv6を構成する場合、どのIPv6マルチキャストグループが自動的に参加するか(2つ選択)  
A.FF02::1 => 同一リンク上の全ノード(リンクローカル)のマルチキャストアドレス  
B.FF02::2 => 同一リンク上の全ルータ(リンクローカル)のマルチキャストアドレス  
=> どちらも予約済みのIPv6マルチキャストアドレス

---
103.IPv6パケットをグループアドレス宛てに送信するIPv6アドレスのブロックはどれか。  
D.FF00::/8

---
104.インターフェースの指定されたIPv6プレフィックスとMACアドレスから、自動的にIPv6アドレスを生成するコマンドは次のどれか。  
A.ipv6 address autoconfig => ステートレスアドレス自動設定の有効化

---
105.IPv6の通信方式は次のどれか(2つ選択)  
B.anycast  
C.multicast

---
106.IPv6エニーキャストアドレスの特徴は次のどれか(3つ選択)  
B.one-to-nearest（1対最も近い）通信モデル  
D.エニーキャストのグループ内の複数のデバイスに同じIPv6アドレス  
E.送信デバイスに最も近いグループインターフェースへパケットを送信

---
107.IPv6ユニキャストアドレッシングの特性の正しい説明は次のどれか(2つ選択)  
A.グローバルユニキャストアドレスは「2000::/3」で始まるアドレス  
C.ループバックアドレスは1つだけであり、そのアドレスは「::1」

---
108.CiscoルータでIPv6ユニキャストルーティングを有効にするコマンドはどれか。  
D.`(config)#ipv6 unicast-routing`

---
109.IPv6 ACLがルータに設定されているかどうか確認するためのコマンドはどれか。  
C.`show ipv6 access-list`

---
110.IPv4ネットワーク上でIPv6トラフィックをルーティングできる手法はどれか。  
C.6to4トンネリング

---
111.IEEE802.11b/g ワイヤレスインフラの展開で、次のどの設計要素が最も重要か  
D.物理的に近接しているアクセスポイントに重複しないチャネルを割り当てる

---
112.PSK(事前共有鍵)モードのWPA2では、どのタイプの無線の暗号化が使用されるか。  
D.AES 256bit

---
113.5GHzの周波数帯域を使用している無線LAN規格は次のどれか(2つ選択)  
A.IEEE802.11a  
D.IEEE802.11ac

---
114.Cisco Wireless LAN Controllerを導入するメリットは次のどれか。  
A.各アクセスポイントに対して個別に設定する必要がなくなる

---
115.Cisco WLCへの接続が失われた後も無線クライアントに引き続きサービスを提供する統合アクセスポイントのモードは次のどれか。  
C.flexconnect

---
116.Cisco WLCの設定で、Voice over WLANの導入を設定する時にGUI上の設定画面で選択されるQoSプロファイルは次のどれか。  
D.Platinum

---
117.WLCのどの機能を有効にすると、特定のネットワークから管理アクセスが制限されるか。  
B.CPU ACL

---
118.Cisco WLCで管理できる無線アクセスポイントのモードは次のどれか。  
B.lightweight

---
119.Cisco WLCのGUI画面で新しい「WLAN」を設定する時に入力する必要がある値となる「項目」は次のどれか(2つ選択)  
A.SSID  
C.Profile Name

---
120.Cisco WLCでWPA2-PSKを使用してWLANを構成する場合、WLCのGUI画面ではどの2つのフォーマットを選択できるか(2つ選択)  
B.ASCII  
D.HEX（hexadecimal）

---
121.ネットワーク自動化のメリットは次のどれか(2つ選択)  
C.運用コストの削減  
D.信頼性の高い結果を伴う迅速な設定変更

---
122.サウスバウンドAPIは次のどれか(2つ選択)  
B.OpenFlow  
C.NETCONF

---
123.Spine-and-Leafアーキテクチャでは、追加のアクセスポートが必要な場合、どのようにしてネットワークの拡張性を可能にするか。  
C.リーフスイッチは、全てのスパインスイッチにフルメッシュで接続して追加できる

---
124.REST APIでサポートされているエンコード方式は次のどれか(2つ選択)  
C.XML  
D.JSON

---
125.企業はクラウドサービスの導入を検討している。企業側(クラウドの利用者側)で、仮想マシンに独自にOSをインストールできるクラウドサービスは次のどれか。  
C.IaaS(Infrastructure as a Service)

---
126.従来のネットワークとコントローラーベースのネットワークの正しい説明はどれか。  
A.コントローラーベースのネットワークのみが、コントロールプレーンとデータプレーンを分離している

---
127.コントローラーベースのアーキテクチャで、エッジデバイスと相互作用するために使用されるAPIは次のどれか。  
B.southbound API

---
128.構成管理ツールのChefで使用する言語、ポート番号の正しい組合わせはどれか。  
A.コード記述言語：Ruby TCPポート番号：10002

---
129.構成管理ツールのPuppetで使用する言語、ポート番号の正しい組合わせはどれか。  
D.コード記述言語：独自言語 TCPポート番号：8140

---
130.構成管理ツールのAnsibleで使用する言語、通信に使用するプロトコルの正しい組合わせはどれか。  
D.コード記述言語：YAML 通信に使用するプロトコル：SSH
