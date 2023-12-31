# 演習問題
- 1.VLANを構成するメリットを3つ選択  
A.ブロードキャストドメインのサイズを拡張できる  
B.キャンパスネットワークの設計が柔軟にできる  
C.コリジョンドメインの数を増加することができる  
D.スイッチでVLAN間のルーティングが可能になる  
E.ネットワークのセキュリティが強化できる  
F.スイッチの管理が容易になる  
G.ブロードキャストドメインを分割できる

- 2.VLAN2の名前をSalesに変更するために必要なコマンド  
A.`(config)#interface vlan 2`  
B.`(config-if)#vlan name Sales`  
C.`(config)#vlan 2`  
D.`(config-if)#name Sales`  
E.`(config-vlan)#vlan 2 name Sales`  
F.`(config-vlan)#name Sales`

- 3.Catalystスイッチにデフォルトで存在し、削除や変更ができないVLAN IDを選択  
A.VLAN1  
B.VLAN1, 2  
C.VLAN1001 ~ 1005  
D.VLAN1, 1002 ~ 1005  
E.該当なし

- 4.24ポートあるCatalystスイッチに対して4つのVLANを構成。コリジョンドメインとブロードキャストドメインの数(2つ)  
A.コリジョンドメイン:4  
B.ブロードキャストドメイン:1  
C.ブロードキャストドメイン:4  
D.コリジョンドメイン:1  
E.ブロードキャストドメイン:24  
F.コリジョンドメイン:24

- 5.以下に該当する説明と関連用語を選択  
1.アクセスポート 2.トランクポート  
A.VTP  
B.IEEE 802.1Q  
C.1つのVLANフレームのみ転送が可能  
D.一般的にエンドユーザーのPCを接続する  
E.複数のVLANフレームの転送が可能  
F.複数のVLANを構成する2台のスイッチ間を接続する  
G.`show vlan`コマンドのPorts部分に表示される

- 6.ネゴシエーションによって、動的にトランクポートまたはアクセスポートに設定できるプロトコル  
A.VTP  
B.DTP  
C.IEEE 802.1Q  
D.ISL  
E.CDP

- 7.管理者はCatalyst 3560スイッチと他ベンダ製のスイッチ間をトランクポートとして設定する必要がある。この時にCatalystスイッチで必要なコマンドを2つ選択  
A.`(config-if)#switchport mode trunk`  
B.`(config-if)#no switchport nonegotiate`  
C.`(config-if)#switchport mode on`  
D.`(config-if)#switchport mode encapsulation 802.1q`  
E.`(config-if)#switchport trunk enable`  
F.`(config-if)#switchport trunk encapsulation dot1q`  
G.`(config-if)#switchport dynamic auto`

- 8.トランクポートの設定を確認できるコマンドを3つ選択  
A.`show interfaces trunk`  
B.`show interfaces switchport`  
C.`show vlan brief`  
D.`show interfaces vlan`  
E.`show trunk status`  
F.`show interfaces capabilities`

- 9.ホストAとホストB間で通信できない。解決するために必要なデバイスを2つ選択  
VLAN2 --- Switch --- VLAN3  
A.ルータ  
B.ブリッジ  
C.リピータ  
D.レイヤ3スイッチ  
E.ハブ

- 10.Router on a stickの構成でホストAとホストB間で通信するために必要な設定を3つ選択  
ルータ --- Switch(V1, V2) --- VLAN1(172.16.1.1/24), VLAN2(172.16.2.1/24)  
A.ホストAとホストBに異なるデフォルトゲートウェイを設定する  
B.ルータと接続しているスイッチのポートにスタティックVLANを設定する  
C.スイッチにデフォルトゲートウェイを設定する  
D.ルータにルーティングプロトコルを設定する  
E.スイッチと接続しているルータにポートにサブインターフェイスを設定する  
F.ルータと接続しているスイッチのポートにトランクを設定する  
G.ルータとスイッチ間をクロスケーブルで接続する

---
回答  
1.VLANを構成するメリットを3つ  
B.キャンパスネットワークの設計が柔軟にできる  
E.ネットワークのセキュリティが強化できる  
G.ブロードキャストドメインを分割できる

A.ブロードキャストドメインのサイズを拡張できる => 縮小の誤り  
C.コリジョンドメインの数を増加することができる => ポートごとにコリジョンドメインを分割するのはスイッチ  
D.スイッチでVLAN間のルーティングが可能になる => VLANはレイヤ2によってネットワークを分割。スイッチは分割したVLAN同士を相互接続はできない  
F.スイッチの管理が容易になる => 仮想的なグループをつくるため物理的な構成よりも管理は複雑になる  

2.VLAN2の名前をSalesに変更する  
C.`(config)#vlan 2`  
F.`(config-vlan)#name Sales`

3.Catalystスイッチにデフォルトで存在し、削除や変更ができないVLAN ID  
D.VLAN1, 1002 ~ 1005

CatalystスイッチでサポートされるVLAN ID(VLAN番号)の範囲は0 ~ 4095だが、実際に使用できる範囲はIOSの種類とVTPの動作モードによって異なる。デフォルトのVLANは削除したり名前を変更したりできない

4.24ポートあるCatalystスイッチに対して4つのVLANを構成  
C.ブロードキャストドメイン:4  
F.コリジョンドメイン:24

スイッチポート数はコリジョンドメイン数、VLAN数はブロードキャストドメイン数と一致する  
コリジョンドメイン:コリジョンによって影響を及ぼす範囲のこと。スイッチ、ルータはポートごとに分割でき、リピータやハブでは分割できない  
ブロードキャストドメイン:ネットワーク上の全ノードを対象にして、データを送るために予約されている特別なアドレス。IPアドレスであれば255.255.255.255

5  
1.アクセスポート:  
C.1つのVLANフレームのみ転送が可能  
D.一般的にエンドユーザーのPCを接続する:クライアントPCやサーバを接続する  
G.`show vlan`コマンドのPorts部分に表示される

2.トランクポート:  
A.VTP:トランクポートで動作する  
B.IEEE 802.1Q:トランクプロトコルはISLも該当する  
E.複数のVLANフレームの転送が可能  
F.複数のVLANを構成する2台のスイッチ間を接続する:スイッチやルータと接続するポート

6.ネゴシエーションによって、動的にトランクポートまたはアクセスポートに設定できるプロトコル  
B.DTP

A.VTP:ドメイン内でVLAN情報を共有・同期するためのプロトコル  
C.IEEE 802.1Q:IEEE標準のトランクプロトコル  
D.ISL:シスコ独自のトランクプロトコル  
E.CDP:隣接するCiscoデバイスの情報を収集できるプロトコル

7.Catalyst 3560スイッチと他ベンダ製のスイッチ間をトランクポートとして設定する時にCatalystスイッチで必要なコマンド  
A.`(config-if)#switchport mode trunk`:トランクポートの設定  
F.`(config-if)#switchport trunk encapsulation dot1q`:トランクプロトコルの設定

8.トランクポートの設定を確認できるコマンドを3つ  
A.`show interfaces trunk`  
B.`show interfaces switchport`  
C.`show vlan brief`:Ports部分にインターフェイス名が表示されなければトランクポートとして動作している

D.`show interfaces vlan`:VLAN管理インターフェイスの情報表示  
E.`show trunk status`:存在しない  
F.`show interfaces capabilities`:スイッチでサポートしている機能(トランクプロトコルなど)を確認する

9.ホストAとホストB間で通信できない。解決するために必要なデバイス  
VLAN2 --- Switch --- VLAN3  
A.ルータ  
D.レイヤ3スイッチ

VLAN2とVLAN3によって、２つのブロードキャストドメインが構成されている。異なるVLANに所属するホスト間の通信にはルーティングデバイス(ルータかレイヤ3スイッチ)が必要。

10.Router on a stickの構成でホストAとホストB間で通信するために必要な設定を3つ  
ルータ --- Switch(V1, V2) --- VLAN1(172.16.1.1/24), VLAN2(172.16.2.1/24)  
A.ホストAとホストBに異なるデフォルトゲートウェイを設定する:ホストは自身が所属するVLANのサブインターフェイスに設定されたIPアドレスをデフォルトゲートウェイに割り当てる  
E.スイッチと接続しているルータにポートにサブインターフェイスを設定する  
F.ルータと接続しているスイッチのポートにトランクを設定する

B.ルータと接続しているスイッチのポートにスタティックVLANを設定する  
C.スイッチにデフォルトゲートウェイを設定する:IPアドレスを設定不要  
D.ルータにルーティングプロトコルを設定する:ルータに直接接続されたサブネット間のルーティングの場合は不要  
G.ルータとスイッチ間をクロスケーブルで接続する:ルータとスイッチ間の接続にはストレートケーブルが適切
