# Chapter 3

## 3-5 シェルの環境設定
```
エイリアスの設定
% alias エイリアス名="コマンド"
```
```
シェルの変数の一覧を表示する
% set
```
```
環境変数の一覧を表示する
% printenv
```
```
カレンダー表示
% cal
```
```
現在の環境に設定を反映する
% source
Shell builtin commands are commands that can be executed within the running shell's process.
Note that, in the case of csh(1) builtin commands, the command is executed in a subshell if it occurs as any component of a pipeline except the last.
```
```
 % type ls
ls is /bin/ls

「type」は組み込みコマンドかどうか見る
```
