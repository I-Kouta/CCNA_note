# 演習問題
- 1.RT1の管理者は以下の設定でログアウトした。再びRT1にアクセスしてユーザEXECモードから特権モードに移行する際に必要となるパスワード  
`RT1(config)#enable password Cisco`  
`RT1(config)#enable secret Sanfran`  
`RT1(config)#line vty 0 4`  
`RT1(config-line)#password CCNA`  
A.CCNA  
B.Cisco  
C.Sanfran  
D.Cisco, Sanfran  
E.Cisco, CCNA  
F.CCNA, Sanfran

- 2.出力から正しい説明を4つ  
A.RT1にパスワード入力なしでリモートログインすることができる  
B.`show startup-config`コマンドを実行した出力結果  
C.RT1にTelnetまたはSSHでリモートログインできる  
D.コンソールポートを使用してログインする際に、ユーザ名とパスワードを要求される  
E.バナーメッセージの設定によってセキュリティが強化されている  
F.`show running-config`コマンドを実行した出力結果  
G.RT1に同時に最大4台のPCからTelnet接続できる  
H.Fa0インターフェイスは管理的に有効化されている  
I.ユーザEXECモードから特権EXECモードへ移行する時、パスワードは「\$1$d8nC…」を入力する必要がある

- 3.`service password-encryption`コマンドを実行したときの説明で正しいもの  
A.`running-config`にある全てのパスワードが暗号化されている  
B.新規で設定するパスワードは暗号化されない  
C.line consoleとline vtyに設定されたパスワードのみ暗号化される  
D.セキュリティを強化するため、デフォルトで有効化されている  
E.`no service password-encryption`を実行すると、暗号化されたパスワードはプレーンテキストに復元される

- 4.管理者がスイッチにポートセキュリティを設定する目的  
A.許可していないホストからスイッチに対してTelnetアクセスされるのを防ぐため  
B.スイッチポートを許可していないホストによって無効化されるのを防ぐため  
C.許可していないホストがLANへアクセスするのを防ぐため  
D.許可していない宛先MACアドレスへの通信を防ぐため  
E.スイッチの管理インターフェイスに対する不正なアクセスを防ぐため

- 5.ポートセキュリティを設定したスイッチポートに対して、受信フレームの送信元MACアドレスを動的に`running-config`に保存するためのコマンド  
A.`switchport port-security mac-address static`  
B.`switchport port-security mac-address dynamic`  
C.`switchport port-security violation protect`  
D.`switchport port-security source-address protect`  
E.`switchport port-security mad-address sticky`

---
回答  
1.再びRT1にアクセスしてユーザEXECモードから特権モードに移行する際に必要となるパスワード  
`RT1(config)#enable password Cisco` => これは上書きされる  
`RT1(config)#enable secret Sanfran`  
`RT1(config)#line vty 0 4`  
`RT1(config-line)#password CCNA` => TelnetでVTYへリモートログインする際に入力する必要がある  
C.Sanfran

2.出力から正しい説明を4つ  
A.RT1にパスワード入力なしでリモートログインすることができる => VTYのline設定の「no login」  
D.コンソールポートを使用してログインする際に、ユーザ名とパスワードを要求される => コンソールポートのline設定に「login local」とあれば、`username`コマンドで設定されたユーザ名とパスワードが必要  
F.`show running-config`コマンドを実行した出力結果 => Current configuration  
H.Fa0インターフェイスは管理的に有効化されている => 無効であれば`shutdown`が表示されている

B.`show startup-config`コマンドを実行した出力結果 => `running-config`  
C.RT1にTelnetまたはSSHでリモートログインできる =>  telnetのみ  
E.バナーメッセージの設定によってセキュリティが強化されている => welcomeは非推奨。強化はされていない  
G.RT1に同時に最大4台のPCからTelnet接続できる => 0 ~ 4の5台  
I.ユーザEXECモードから特権EXECモードへ移行する時、パスワードは「\$1$d8nC…」を入力する必要がある => これは暗号化された結果(`enable secret`コマンド)

3.`service password-encryption`コマンドを実行したときの説明で正しいもの  
A.`running-config`にある全てのパスワードが暗号化されている

既に設定されたパスワード、これから設定するパスワードのどちらも全て暗号化される。デフォルトでは有効になっておらず、noコマンドを実行してもプレーンテキストは復元されず、新たに設定したパスワードは暗号化されなくなる。

4.管理者がスイッチにポートセキュリティを設定する目的  
C.許可していないホストがLANへアクセスするのを防ぐため

許可したMACアドレスからのフレームを転送し、それ以外のMACアドレスからのフレームをブロックしてLANへのアクセスを防ぐことができる。  
D.許可していない宛先MACアドレスへの通信を防ぐため => フレームの宛先MACアドレスは感知しない

5.ポートセキュリティを設定したスイッチポートに対して、受信フレームの送信元MACアドレスを動的に`running-config`に保存するためのコマンド  
E.`switchport port-security mac-address sticky` => スティッキーラーニングを有効にする

C.`switchport port-security violation protect` => セキュリティ違反が発生した時の違反モードをprotectに変更する
