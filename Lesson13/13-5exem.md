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

2.出力から正しい説明を4つ

3.`service password-encryption`コマンドを実行したときの説明で正しいもの

4.管理者がスイッチにポートセキュリティを設定する目的

5.ポートセキュリティを設定したスイッチポートに対して、受信フレームの送信元MACアドレスを動的に`running-config`に保存するためのコマンド
