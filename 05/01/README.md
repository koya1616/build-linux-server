# Chapter 5

## 5-1 ネットワークの基本設定

### 5-1-1
#### NetworkManager
```
CentOSでは、ネットワークの管理をNetworkManagerというサービスが担っている。
```

### 5-1-3
#### ターミナルのTUI（Text User Interface）による設定
```
% sudo nmtui
```

### 5-1-4
#### nmcliコマンドによる設定
```
ネットワークデバイスの一覧を表示するにはdeviceサブコマンドを示す
% nmcli device
```

#### インターフェイスの設定状況
```
% nmcli device show デバイス名
```

#### nmcliの実行例
```
指定したネットワークインターフェイスにIPアドレスを割り当てる書式
% nmcli connection modify "コネクション名" ipv4.address IPアドレス/サブネットマスクビット数

ex.1 「有線接続１」のIPアドレスを固定の「192.168.3.30」に設定する
% sudo nmcli connection modify "有線接続1" ipv4.address 192.168.3.30/24

ex.2 IPアドレスを自動で割り当てる
% sudo nmcli c modify "有線接続1" ipv4.address auto

ex.3 DNSサーバーを「192.168.3.1」に設定
% sudo nmcli connection modify "有線接続1" ipv4.dns 192.168.3.1

ex.4 デフォルトゲートウェイを「192.168.3.1」に設定
% sudo nmcli connection modify "有線接続1" ipv4.gateway 192.168.3.1
```

#### 設定を反映させる
```
% sudo nmcli connection down "有線接続1"
% sudo nmcli connection up "有線接続1"
```
