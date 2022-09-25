# Chapter 5

## 5-4 ファイアーウォールの設定

### 5-4-1
#### ファイアウォールを有効にする
```
firewalldサービスの状態を確認
% systemctl status firewalld
```

### 5-4-2
#### ファイアウォールの起動と停止
```
% sudo systemctl start firewalld
% sudo systemctl stop firewalld
```

### 5-4-3

#### firewall-cmd コマンドとゾーンについて
```
ファイアウォールの設定を行う
% firewall-cmd [オプション]
```

#### ネットワークインターフェイスに設定されているゾーンを確認する
```
% firewall-cmd --get-active-zones
```

#### ゾーンのファイアウォール設定を確認する
```
% sudo firewall-cmd --list-all
```

### 5-4-6

#### IPアドレスで拒否する
```
% firewall-cmd --add-source=ネットワークアドレス
```


