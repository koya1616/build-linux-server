# Chapter 2

## 2-4 ファイルの基本操作コマンドを覚えよう
### 2-4-3
```
 % tree Documents   
Documents
├── bit.png
├── development_secrets.env
├── env
├── keys
│   ├── development.key
│   ├── master.key
│   ├── production.key
│   ├── staging.key
│   └── test.key
└── スクリーンショット 2022-05-07 10.37.49.png
```

```
% mkdir -p ~/作りたいdir/未作成dir/file

「-p」は途中のディレクトリも含めて作成
```

### 2-4-5
```
% rm -i .zcompdump
remove .zcompdump? 
「-i」は削除する前に確認される
```
```
% rm -f .zcompdump
「-f」書き換え権限のないファイルでも確認を行わない
```
```
% rm -r .zcompdump
「-r」がディレクトリを丸ごと削除
```

### 2-4-6
```
% ln -s file1.txt file2.txt
「-s」はシンボリックリンク　を作成
```
```
% ls -il
total 0
 298995 drwx------@  5 user  staff   160  1 17  2022 Applications
 246859 drwx------@ 16 user  staff   512  9  9 22:16 Desktop

「-i」オプションでiノード番号(重複のない番号)を表示
先頭に表示されるのが「iノード番号」
左から３番目はハードリンクの数

・ハードリンク作成
% ln file1.txt file2.txt
```




