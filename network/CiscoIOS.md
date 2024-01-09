URL:https://network00.net/category/ciscoios/

# Cisco IOS

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
