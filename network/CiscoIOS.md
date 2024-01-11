URL:https://network00.net/category/ciscoios/

# Cisco IOS

---
### `IOS入門`

- モード変更のコマンド</br>
<img width="600" alt="" src="./images/モード変更.png"></br>
ユーザモード:統計情報を表示。ルータの基本的な状態の確認が可能  
特権モード:ルータの設定を表示。詳細な状態の確認やファイルの移動等が行える  
グローバルコンフィギュレーションモード:ルータに全体的な設定・変更を苦悪ことができる  
項目別の設定モード:項目別に詳細な設定・変更を行うことができる(インターフェイス設定モード、ルータ設定モード等)

- パスワードの設定  
Enable password  
`Router(config)#enable secret xxx`
ユーザモードパスワード(コンソール)  
`Router(config)#line console 0`  
`Router(config-line)#password xxxx`  
`Router(config-line)#login`  
ユーザモードパスワード(Telnet)  
`Router(config)#line vty 0 4`  
`Router(config-line)#password xxxx`  
`Router(config-line)#login`  
パスワードの設定確認  
`Router#show running-config`  
(表示されるパスワードを無効にしたい場合は以下のコマンドを実行)  
`Router(config)#service password-encryption`  
ユーザ名を用いたローカル認証  
`Router(config)#line console 0`  
`Router(config-line)#username yyyy password xxxx`  
(コンソールでこの認証を有効にする場合)  
`Router(config)#line console 0` => 遠隔接続の場合は`Router(config)#line vty 0 4`  
`Router(config-line)#login local`

- その他の基本的なコマンド  
ルータのホスト名を設定  
`Router(config)#hostname xxxx`  
設定の表示と保存  
`Router#show running-config`  
`Router#copy running-config startup-config`  
保存した設定の削除、ルータの再起動  
`Router#write erase`  
`Router#reload` => 組み合わせることで工場出荷状態へ戻すことが可能

---
### `インターフェイスの設定`

- インターフェイスの設定  
インターフェイス設定モード  
`(config)#interface [type] [port]`  
IPアドレスの設定  
`(config-if)#ip address [ip-address] [subnet-mask]`  
インターフェイスの有効化  
`(config-if)#no shutdown`

- 設定例の構成

<img width="600" alt="" src="./images/インターフェイス設定例.png">

- ルータ:R1のインターフェイス設定  
`R1(config)#interface fastethernet 0/0` => インターフェイス設定  
`R1(config-if)#ip address 192.168.10.1 255.255.255.0` => IPアドレスの設定  
`R1(config-if)#no shutdown` => インターフェイスの有効化</br></br>
`R1(config-if)#interface serial 0/0`  
`R1(config-if)#ip address 192.168.20.1 255.255.255.0`  
`R1(config-if)#no shutdown`</br></br>
`R1(config-if)#interface serial 0/1`  
`R1(config-if)#ip address 192.168.30.1 255.255.255.0`  
`R1(config-if)#no shutdown`

- ルータ:R2のインターフェイス設定  
`R2(config)#interface fastethernet 0/0`  
`R2(config-if)#ip address 192.168.40.1 255.255.255.0`  
`R2(config-if)#no shutdown`</br></br>
`R2(config-if)#interface serial 0/0`  
`R2(config-if)#ip address 192.168.20.2 255.255.255.0`  
`R2(config-if)#no shutdown`

- ルータ:R3のインターフェイス設定  
`R3(config)#interface fastethernet 0/0`  
`R2(config-if)#ip address 192.168.50.1 255.255.255.0`  
`R2(config-if)#no shutdown`</br></br>
`R2(config-if)#interface serial 0/0`  
`R2(config-if)#ip address 192.168.30.2 255.255.255.0`  
`R2(config-if)#no shutdown`

- インターフェイス状態の確認

<img width="500" alt="" src="./images/インターフェイスの状態.png">

`#show ip interface brief` => インターフェイスの要約情報を表示。Statusは物理層の状態、Protocolはレイヤ2(データリンク層)の状態を判断できる  
`#show ip interface` => インターフェイスに対して適用したアクセスリストを確認する

---
### `スタティックルート`
ルータでは、経路制御を行っており、宛先IPアドレスに対して最適な経路をルーティングテーブルから探してネクストホップアドレスを決めている。

- スタティックルートの設定コマンド  
`(config)#ip route [network] [subnet-mask] [interface] [next_hop] [AD] [permanent]`  
network:宛先ネットワーク  
mask:サブネットマスク  
interface:次のルータへ送出する際のインターフェイス  
next_hop:宛先ネットワークへ転送するための次のルータのアドレス  
AD:スタティックルートの場合は1  
permanent:状態に無関係でルーティングテーブルに保持される

- スタティックルートの設定例

<img width="500" alt="" src="./images/スタティックルート.png">

・ルータ:R1のスタティックルートの設定  
`R1(config)#ip route 192.168.40.0 255.255.255.0 Serial0/0 192.168.20.2` => それぞれの方向に向いているインターフェイスを記述する  
`R1(config)#ip route 192.168.50.0 255.255.255.0 Serial0/1 192.168.30.2`

・ルータ:R2のスタティックルートの設定  
`R2(config)#ip route 192.168.10.0 255.255.255.0 Serial0/0 192.168.20.1`  
`R2(config)#ip route 192.168.30.0 255.255.255.0 Serial0/0 192.168.20.1`  
`R2(config)#ip route 192.168.50.0 255.255.255.0 Serial0/0 192.168.20.1`

・ルータ:R3のスタティックルートの設定  
`R2(config)#ip route 192.168.10.0 255.255.255.0 Serial0/0 192.168.30.1`  
`R2(config)#ip route 192.168.20.0 255.255.255.0 Serial0/0 192.168.30.1`  
`R2(config)#ip route 192.168.40.0 255.255.255.0 Serial0/0 192.168.30.1`

- ルーティングテーブルの見方

ルータ:R3のルーティングテーブル  
`R3#show ip route` => ルーティングテーブルの表示

C 192.168.50.0 is directly connected, FastEthernet0/0  
S 192.168.40.0 [1/0] via 192.168.30.1  
C 192.168.30.0 is directly connected, Serial0/0  
S 192.168.20.0 [1/0] via 192.168.30.1  
S 192.168.10.0 [1/0] via 192.168.30.1

via 192.168.30.1 => ネクストホップアドレス  
[1/0] => アドミニストレーティブディスタンス値  
Cは直接接続されたネットワーク、SはRIPルート

- デフォルトルートの設定

ルーティングテーブルに存在しないネットワークを宛先とするパケットを、次のホップのルータへ送信するために使用する。  
デフォルトルートの設定:  
`R3(config)#ip route 0.0.0.0 0.0.0.0 [next-hop]`

---
### `VLAN`

- VLANの種類  
スタティックVLAN  
ポートベースVLANと呼ばれる方式。手動でポートごとにVLANを定義する  
ダイナミックVLAN
VLANの割り当てを自動的に決定する。MAC(アドレス)ベースVLAN、プロトコルベースVLANなどの方式が該当する。

- VLANの識別  
アクセスリンク:1つのVLANだけに属しており、PC等の機器を接続するリンクに適用する。  
トランクリンク:複数のVLANに属しており、スイッチ間を接続するリンクに適用する。  
ISL(*Inter-Switch Link*):シスコ独自のトラッキングプロトコル  
IEEE802.1Q:IEEE標準のトラッキングプロトコル

<img width="500" alt="" src="./images/VLAN識別.png">

- VLANの設定コマンド  
VLANの作成  
`(config)#vlan [vlan-id]`  
`(config-vlan)name [vlan-name]` (名前設定は必須ではない)  
インターフェイスへの適用  
`(config-if)#switchport mode access`  
`(config-if)#switchport access vlan [vlan-id]`  
トランクリンクの設定  
`(config-if)#switchport trunk encapsulation [dot1q | isl]`  
`(config-if)#switchport mode trunk`  

- VLANの設定例

<img width="500" alt="" src="./images/VLAN設定.png">

・VLANの作成、スイッチ:SW1, SW2, SW3  
SW1:`(config)#vlan 10`  
SW1:`(config-vlan)#name GROUP10`
SW2:`(config)#vlan 20`  
SW2:`(config-vlan)#name GROUP20`</br></br>
・インターフェイスへの適用、スイッチ:SW1, SW2  
`SW1(config)#interface fastethernet0/0`  
`SW1(config-if)#switchport mode access`  
`SW1(config-if)#switchport access vlan 10`  
`SW1(config)#interface fastethernet0/1`  
`SW1(config-if)#switchport mode access`  
`SW1(config-if)#switchport access vlan 20`</br></br>
・トランクリンクの設定  
スイッチ:SW1, SW2  
`SW1(config)#interface fastethernet0/23`  
`SW1(config-if)#switchport trunk encapsulation dot1q` ※デフォルトのため省略可  
`SW1(config-if)#switchport mode trunk`  
スイッチ:SW3  
`SW3(config)#interface fastethernet0/0-1`  
`SW1(config-range)#switchport trunk encapsulation dot1q` ※デフォルトのため省略可  
`SW1(config-if)#switchport mode trunk`

- VLANの確認

<img width="500" alt="" src="./images/VLAN確認.png">

`show vlan brief`:スイッチに存在する全てのVLANに関する情報を表示。briefで概要情報のみ表示

<img width="500" alt="" src="./images/トランクリンク確認.png">

`show interface trunk`:トランクポートの設定や状態を表示

- ルータによるVLAN間ルーティング  
ルータのインターフェイス数よりも多くのVLANは使用できない。その場合は1つの物理インターフェイスだけでVLAN間ルーティングを可能にする方法がある(*router-on-a-stick*)。

<img width="500" alt="" src="./images/VLAN間ルーティング.png">

・ルータの設定  
`R1(config)#interface gigabitEthernet0/0.1` => インターフェイスの設定  
`R1(config-subif)#encapsulation dot1Q 10`  
`R1(config-subif)#ip address 192.168.10.1 255.255.255.0`</br></br>
`R1(config)#interface gigabitEthernet0/0.2`
`R1(config-subif)#encapsulation dot1Q 20`  
`R1(config-subif)#ip address 192.168.20.1 255.255.255.0`

・スイッチ:SW3の設定  
`SW3(config)#interface gigabitEthernet3/3`  
`SW3(config-subif)#switchport trunk encapsulation dot1q` => トランクリンクの設定  
`SW3(config-subif)#switchport mode trunk`

---
### `ルーティング(RIP)`

・*Router Information Protocol*の略  
・中小規模のネットワーク向け  
・コンバージェンス(収束)に時間がかかる  
・ホップをメトリックとして使用  
・ディスタンベクター型のルーティングプロトコル

- RIPルーティングの設定例

<img width="500" alt="" src="./images/RIPルーティング.png">

・ルータ:R1のRIPルーティングの設定  
`R1(config)#router rip` => RIPプロセスの有効化  
`R1(config-router)#network 192.168.10.0` => RIPを有効にするインターフェイスの指定  
`R1(config-router)#network 192.168.20.0`  
`R1(config-router)#network 192.168.30.0`  
`R1(config-router)#passive-interface fastethernet0/0` => パッシブインターフェイスの設定(ルーティングアップデートの抑制)</br></br>
・ルータ:R2のRIPルーティングの設定  
`R2(config)#router rip`  
`R2(config-router)#network 192.168.20.0`  
`R2(config-router)#network 192.168.40.0`  
`R2(config-router)#passive-interface fastethernet0/0`</br></br>
・ルータ:R3のRIPルーティングの設定  
`R2(config)#router rip`  
`R2(config-router)#network 192.168.30.0`  
`R2(config-router)#network 192.168.50.0`  
`R2(config-router)#passive-interface fastethernet0/0`</br></br>
`(config-router)#auto-summary` => 自動集約を有効(デフォルトで有効)

- RIPルーティングの確認  
`show ip route` => ルーティングテーブルの確認  
`show ip protocols` => ルーティングプロトコルの確認。各種タイマ、RIPのバージョン、有効な設定したネットワークなどを確認できる  
`debug ip rip` => ルーティングプロトコルの確認(デバッグ)

### `ワイルドカードマスクとアクセスリスト`

- ワイルドカードマスク  
・192.168.10.0 / 26をチェック対象にした場合  
=> 192.168.10.0 0.0.0.63</br></br>
・192.168.10.1を指定したい場合  
=> host 192.168.10.1</br></br>
・全てのIPアドレスを指定  
0.0.0.0 255.255.255.255(省略でany)</br></br>
・192.168.0.0 / 24 ~ 192.168.3.0 / 24の4つを指定  
=> 192.168.0.0 0.0.3.255(22ビット目まで共通のため)
