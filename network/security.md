### `セキュリティ1`
### `セキュリティ2`
(割愛アリ)

`セキュリティの重要性`

- TCP / IPでは、昔はセキュリティを重視ていなかったが、インターネットが普及した現在では悪意を持った利用者等が多数存在するようになったため、セキュリティが重視されるようになった

- セキュリティとは害からの保護。一般には保安のことで、犯罪や事故などを防止するための警備や予防措置全般を指す。さらに、害が発生してしまってからの回復処置を検討・計画しておくこともセキュリティの一部と言える

- セキュリティの中でもIT技術者が主に行うのは、情報セキュリティやサイバーセキュリティ

- 情報セキュリティやサイバーセキュリティは大枠では同じ様な意味。情報セキュリティは置き忘れ等の自己管理の部分や物理的な部分を含むが、サイバーセキュリティはネットワーク経由での犯行に対するセキュリティという意味合いが強い

サイバー攻撃の例

- 被害の例  
・機密情報を盗まれる  
・ホームページやファイルの内容が改竄される  
・攻撃の踏み台にされる  
・サーバやシステムが攻撃されてサービス提供が不能になる

- 被害者と加害者  
・個人、組織、企業いずれに対しても行われる  
・金銭目的も愉快犯なものもある  
・首謀者が直接行うのではなく、他者に依頼して犯行が行われることもある

- 手口の具体例  
・(ランサムウェア)システムやファイルを人質にして金銭を要求する  
・(標的型攻撃)特定の特定の組織内の機密情報を狙う攻撃  
・(マルウェア)不正かつ有害に動作させる意図で作成された悪意のあるソフトウェアや悪質なコードの総称。コンピュータウイルスやワームなどが含まれる

### `主なセキュリティ機能`

ファイアウォールの役割や機能

|機能 / 役割|説明|
|----------|---|
|パケットフィルタリング|IPアドレスやポート番号を判別し通信を通すか決める|
|アプリケーションゲートウェイ|代理で外部ネットワークに接続する。ユーザやアプリケーション毎のアクセス制御も行う|
|ネットワークアドレス変換|NAT, NAPTを行う|
|DMZ|インターネットに公開するサーバを配置する。LAN内なのに外部からアクセスできる場所|

ファイアウォールのアクセス制御の例

|場所 / 方向|制限内容|
|----------|------|
|外部 => DMZ|サーバに対してアクセス可|
|DMZ => 社内|一部許可、ほぼアクセスできない|
|社内 => DMZ|管理者のみアクセスできるように制限|
|外部 => 社内|ほぼアクセスできない|
|社内 => 外部|ほぼ自由にアクセスアクセス可|

ファイアウォールにあって、ルータにない機能

|機能|説明|
|---|----|
|ユーザ認証|ユーザ名で通信を通すか判別|
|ログ収集|通過したログを記録する|
|コンテンツフィルタリング|添付ファイルなどを認識して許可されたものだけ通す|

`暗号化技術の基礎`

暗号化技術の階層分類

|階層|暗号化技術|
|---|---------|
|アプリケーション|SSH, SSL-Telnet, PET等の遠隔ログインなど|
|セッション, トランスポート|SSL / TLS, SOCKS V5の暗号化|
|ネットワーク|IPsec|
|データリンク|イーサネット・WANの暗号化装置など, PPTP(PPP)|

`セキュリティのためのプロトコル`

IPsecとVPN
- VPN(*Virtual Private Network*)は、仮想的に拠点間を専用線で接続したのと同等に扱えるネットワーク。つまり、仮想的なプライベートネットワーク接続

- インターネット(広帯域で安価な光回線等含む)などの公衆網を利用する場合でも、安全に企業の拠点間通信を実現できる

- 安全確保のために拠点間では通信は暗号化されている。それを実現するためにIPsec等の今度なセキュリティを実現させられる

|使用技術|分類|説明|
|------|----|---|
|IPsec-VPN|インターネットVPN|セキュリティプロトコルにIPsecを使用|
|SSL-VPN|インターネットVPN|セキュリティプロトコルにSSLを使用|
|MPLS-VPN|MPLS-VPN|通信事業者のプライベートIP網内|