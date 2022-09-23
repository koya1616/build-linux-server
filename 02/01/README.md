# Chapter 2

## 2-1 ターミナルでコマンドを入力する
### 2-1-1 ターミナルについて
    
・ターミナルの先頭部分
```
[ユーザー名@ホスト名　　ディレクトリ名]$
```

・[~]はホームディレクトリを表す
### 2-1-2
・dateコマンド入力
```
user@host ~ % date
2022年 9月23日 金曜日 10時14分32秒 JST
```
「JST」は日本時間。協定世界時 (UTC)もある。

・uname
```
user@host ~ % uname
Darwin
```
システム情報を表示するuname
```
user@host ~ % uname -p
arm
```
「-p」オプションはCPUの種類
```
% uname -p -n
aoyamakuyanoAir arm

```
「-n」オプションはネットワーク内のホスト名を表示
