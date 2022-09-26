# Chapter 5

## 5-5 SELinux(Security-Enhanced Linux)

### 5-5-2

#### SELinuxの主な機能
- TE(Type Enforcement): プロセスにアクセスを許可する権限を与える機能
- RBAC(Role-based access control): ユーザーごとに権限を設定する
- MCS(Multi Category security): アクセス分離機能

#### TEについて
```
許可するセキュリティポリシーの設定例
allow httpd_t httpd_sys_content_t:file { read getattr };
```

#### SELinuxの動作モード
```
SELinuxのモードを表示する
% getenforce
```
```
SELinuxのモードを変更する
% setenforce　モード
```
```
ブーリアン値を設定する
% getsebool　ブーリアン値
```
```
ブーリアン値を表示する
% setsebool　ブーリアン値 値(onもしくはoff)
```
