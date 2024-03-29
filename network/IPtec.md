### `IP関連技術1`

`DNSの概要`

- 「www.yahoo.co.jp」のように通信先を特定するものをドメイン名と呼び、ドメイン名を探してくれるサーバをDNSサーバと呼ぶ

- DNSの役割  
コンピュータ上の住所であるIPアドレスを覚えておくのは大変なため、文字での名前(ドメイン名)を覚える様にしている

- ネットワーク層のプロトコルとしてはドメイン名を備えていない。そこでDNSサーバがIPアドレスとドメインの変換を請け負っている

- 上記の操作を名前解決と呼び、各アプリケーションやOSがドメインによるアクセスをしようとしたときに、DNSクライアント(またはOS)がDNSサーバへ依頼する

`名前解決の情報共有`

hostsファイルの場合
- DNSガ出てくる前は、ホスト名とIPアドレスの対応を定義するhostsファイルが使われていた。現在でも会社内や個人等で利用している。Windowsでの配置場所は「C:\Windows\System32\drivers\etc\hosts」

- hostsファイルの場合は1個のファイルを共有して使うため、組織間で情報共有したり情報を総合的に一元管理することは難しい

DNSの場合
- ホストを管理している組織毎にホスト名とIPアドレスの対応関係を管理する

- 組織内で変更すれば、インターネット全体に反映される仕組み

- 初期登録時や上位レベルの変更を除き、他の機関に報告や申請をする必要はない

`ドメイン名の構造`

- 「www.yahoo.co.jp」の場合  
wwwはサーバ(ホスト)名、yahooは組織名、coはセカンドレベルドメイン、jpはトップドメインと呼ぶ

- ドメイン名からIPアドレスに変換することを名前解決と呼び、名前解決の要求を出したクライアントのことをネームリゾルバと呼ぶ

- jpやnet、org等のトップレベルドメインを管理しているのはルートネームサーバ、各ネームサーバが管理する階層(ドメイン)はゾーンと呼ぶ

- 管理組織のドメイン(ゾーン)そのもの(IPアドレスとドメイン名)は上位のDNSサーバに管理してもらう

`DNSの問い合わせ順序`

- 1.リゾルバが設定したキャッシュDNSサーバへ問い合わせを行う

- 2.キャッシュDNSサーバは該当情報を持っていればそれを返す

- 3.該当情報を持っていなければルータサーバへ問い合わせる

- 4.ドメインの木構造を上から順にたどることで、目的の情報があるDNSサーバを見つける

- 目的のゾーン情報を持っているDNSサーバから必要な情報を得て、得た情報をリゾルバ(クライアント、OS、アプリ)に返す

`代表的なゾーンファイルのレコード`

|レコード|内容                   |
|-------|----------------------|
|SOA    |ゾーンの開始・情報       |
|A      |ホスト名に対するIPアドレス|
|NS     |DNSサーバ              |
|CNAME  |ホストの別名に対する正式名|
|MX     |メールサーバ            |
|PTR    |逆引き用                |
