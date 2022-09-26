# Chapter 6

## 6-1 Windowsのファイルサーバー

#### Samba専用のユーザーを登録する
```
% pdbedit -a ユーザー名

ユーザー一覧
% sudo pdbedit -L
```
```
smb.confのエラーチェックを行う
% testparm
```
