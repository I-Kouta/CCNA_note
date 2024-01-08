URL:https://network00.net/category/ciscoios/

# IOS入門

### `インターフェイスの設定`

- インターフェイス設定モード  
`(config)#interface [type] [port]`

- IPアドレスの設定  
`(config-if)#ip address [ip-address] [subnet-mask]`

- インターフェイスの有効化  
`(config-if)#no shutdown`

### `設定例の構成`

<img width="700" alt="" src="./images/インターフェイス設定例.png">

### `ルータ:R1のインターフェイス設定`
`R1(config)#interface fastethernet 0/0` => インターフェイス設定  
`R1(config-if)#ip address 192.168.10.1 255.255.255.0` => IPアドレスの設定  
`R1(config-if)#no shutdown` => インターフェイスの有効化

`R1(config-if)#interface serial 0/0`  
`R1(config-if)#ip address 192.168.20.1 255.255.255.0`  
`R1(config-if)#no shutdown`

`R1(config-if)#interface serial 0/1`  
`R1(config-if)#ip address 192.168.30.1 255.255.255.0`  
`R1(config-if)#no shutdown`

### `ルータ:R2のインターフェイス設定`

### `ルータ:R3のインターフェイス設定`

### `インターフェイス状態の確認`
