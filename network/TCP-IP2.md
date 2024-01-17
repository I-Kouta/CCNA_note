### `TCP / IP基礎2`

TCP / IP(OSI参照)モデルの各階層

`インターネット層(ネットワーク層)`  
IPアドレスを用いて宛先までパケットを送付する。レイヤ3以上で働く全てのパソコンやルータの機器は、必ずその機能を実装しなければならない

- 第3層に位置し、データリンク(ネットワークインターフェイス)層とトランスポート層の橋渡しをする

- 主となるプロトコルはIP

- PDUはパケット

- インターネット(ネットワーク)層として利用される機器は**ルータ**や**L3スイッチ**がある

代表的なプロトコルは下記の3つ

- ネットワーク上に存在する全ての機器には固有の住所のようなものが割り振られている。これをIPアドレスという

- ICMP:*Internet Control Message Protocol*の略。通信が届いているかどうかを確認するためのプロトコル

- ARP:*Address Resolution Protocol*の略。パケットのIPアドレスから物理的なアドレス(MACアドレス)を取得するプロトコル

`トランスポート層`  
主な役割は機器間で同じアプリケーション(プログラム)同士での通信を可能とすること。PC内部では複数のプログラムが同時に動作しているため、通信がどのプログラム宛なのかを識別する必要がある。識別にはポート番号と呼ばれる識別子が使われる

- 第4層に位置し、アプリケーション(セッション)層とネットワーク層の橋渡しをする

- PDUはセグメント

- ポート番号とアプリケーション層を関連づける

- データを分割する、分割されたデータを組み直す

トランスポート層の代表的なプロトコルは下記の2つ

- TCPの場合、コネクション型で信頼性のある通信を確立する。両端のホスト間でデータの到達性を保証する

- UDPの場合、コネクションレス型で信頼性のないぶん、速度重視。パケット数が少ない通信やブロードキャストやマルチキャストの通信、ビデオや音声などのマルチメディア通信に適している

`アプリケーション層`  
TCP / IPモデルでは、OSI参照モデルのセッション層やプレゼンテーション層、アプリケーション層は全てアプリケーションプログラムの中で実現させると考えられている。通信を伴うアプリケーションの多くはクライアント / サーバモデルで作られており、アプリケーションを開発する際に、サーバ型とクライアント側に要求を満たす仕組みを作る必要がある

- トランスポート層以下の階層はアプリケーションからの独立性は高い  

- アプリケーション層(セッション層以上)のプロトコルはアプリケーションから独立性は低い(アプリケーションの機能に応じて作られている)

- 各アプリケーション毎にプロトコルが存在する(2010年ごろから現在では様々なアプリケーションがhttp, httpsを使用している)