# 演習問題
- 1.エンドユーザへIPv6アドレスを割り当てるエンティティ  
A.RIR B.IANA C.IEEE D.IETF E.ISP

- 2.IPv6の特徴で正しいものを2つ選択  
A.アドレス空間が48ビットから128ビットへ拡張された  
B.Mobile IPとIPsecが標準搭載されている  
C.ヘッダ構造を複雑化し、より高度なルーティングが可能になった  
D.DHCPサーバが用意しなくてもIPv6アドレスの自動割り当てができる  
E.ブロードキャストとマルチキャストによって効率的な通信を行う

- 3.グループ内の最も近いノードと通信するためのIPv6アドレス  
A.ユニキャストアドレス  
B.マルチキャストアドレス  
C.グループ指定アドレス  
D.ループバックアドレス  
E.エニーキャストアドレス

- 4.IPv6アドレスの説明で正しいものを2つ選択  
A.ユニキャストアドレスの後半64ビットはインターフェイスIDである  
B.IPv6アドレスの1つのフィールドは8ビットである  
C.IPv6のループバックアドレスは::1のみである  
D.特定リンクのみで有効なアドレススコープはユニークローカルである  
E.1つのインターフェイスにつき、グローバルユニキャストアドレスを1つだけ割り当てることができる

- 5.EUI-64フォーマットのインターフェイスIDの説明で正しいものを2つ選択  
A.MACアドレスを基に生成される  
B.デフォルトゲートウェイを基に生成される  
C.真ん中に16ビットのFFFEを挿入する  
D.U / Lビットに1をセットする  
E.先頭に16ビットのFFFFを挿入する

- 6.IPv6のリンクローカルユニキャストアドレス  
A.FE08::1234:D0FF:FEDD:34AC  
B.FF80::5678:D0FF:FEDD:34AC  
C.EF80::1234:D0FF:FEDD:34AC  
D.FE80::5678:D0FF:FEDD:34AC  
E.EF08::1234:D0FF:FEDD:34AC

- 7.以下の説明に該当するIPv6マルチキャストアドレスを選択  
1.同一リンク上の全RIPngルータ宛  
2.同一リンク上の全ノード宛  
3.同一リンク上の全ルータ宛  
A.FF02::9 B.FF02::2 C.FF02::5 D.FF02::1

- 8.IPv6ルーティングを有効にするためのコマンド  
A.`(config)ipv6 enable`  
B.`(config)ipv6 unicast-routing`  
C.`(config)ipv6 routing`  
D.`(config)ipv6 unicast routing`  
E.`(config)ipv6 routing enable`

---
回答  
1.エンドユーザへIPv6アドレスを割り当てる  
E.ISP

A.RIR B.IANA C.IEEE D.IETF

2.IPv6の特徴を2つ  
B.Mobile IPとIPsecが標準搭載されている  
D.DHCPサーバが用意しなくてもIPv6アドレスの自動割り当てができる

A.アドレス空間が48ビットから128ビットへ拡張された => 32ビットから  
C.ヘッダ構造を複雑化し、より高度なルーティングが可能になった => 簡素化された  
E.ブロードキャストとマルチキャストによって効率的な通信を行う => ブロードキャストは廃止された

3.グループ内の最も近いノードと通信するIPv6アドレス  
E.エニーキャストアドレス => 複数のノードに対して同じIPv6グローバルユニキャストアドレスを割り当てる。そのアドレスがエニーキャストアドレスとなって、同じエニーキャストアドレスを持つノードのグループの中で、最も近いノードとの通信を可能にする。

4.IPv6アドレスの説明で正しいもの2つ  
A.ユニキャストアドレスの後半64ビットはインターフェイスIDである => 前半64ビットはプレフィックス  
C.IPv6のループバックアドレスは::1のみである

B.IPv6アドレスの1つのフィールドは8ビットである => 16ビットずつ:で区切って8フィールドを16進数表記する  
D.特定リンクのみで有効なアドレススコープはユニークローカルである => リンクローカル  
E.1つのインターフェイスにつき、グローバルユニキャストアドレスを1つだけ割り当てることができる => 複数割り当てることが可能

5.EUI-64フォーマットのインターフェイスIDの説明で正しい説明2つ  
A.MACアドレスを基に生成される => MACアドレスを24ビットずつに分割する  
C.真ん中に16ビットのFFFEを挿入する

D.U / Lビットに1をセットする => 反転させるが正しい

6.IPv6のリンクローカルユニキャストアドレス  
D.FE80::5678:D0FF:FEDD:34AC => 先頭10ビットが「1111 1110 10」で始まる(FE80::/10)

A.FE08::1234:D0FF:FEDD:34AC  
B.FF80::5678:D0FF:FEDD:34AC  
C.EF80::1234:D0FF:FEDD:34AC  
E.EF08::1234:D0FF:FEDD:34AC

7.IPv6マルチキャストアドレスを選択  
1.同一リンク上の全RIPngルータ宛 => A.FF02::9  
2.同一リンク上の全ノード宛 => D.FF02::1  
3.同一リンク上の全ルータ宛 => B.FF02::2

C.FF02::5 => これは同一リンク上の全OSPFルータ

8.IPv6ルーティングを有効にするコマンド  
B.`(config)ipv6 unicast-routing`
