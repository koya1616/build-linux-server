# Chapter 8

## 8-2 SSHの活用

scpコマンドによるファイルコピー
```
% scp [オプション] コピー元のパス　コピー先のパス
パスは[ユーザー名＠ホスト名：パス]

-r オプション: ディレクトリを丸ごとコピー 
-p オプション:　　タイムスタンプやパーミッションなどの属性を保持
```

#### sftpを使用してFTPのように接続する
```
SSHによるファイル転送を行う
% sftp ユーザー名＠ホスト名
```

#### ダウンロードツールwget
- [wget](https://linuxize.com/post/wget-command-examples/)
