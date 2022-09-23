# Chapter 4

## 4-5 ジョブとプロセスの管理
### 4-5-1
```
コマンド    <- フォアグランドジョブ
コマンド &  <-　　バックグラウンドジョブ

[Ctrl] + [Z]で一時停止
```
```
bgコマンドはフォアグランドジョブをバックグランドジョブにする
```
```
jobsはジョブの一覧を表示
```
```
fgはフォアグランドジョブにする
```

### 4-5-2
#### 実行中のプロセス
```
% ps -e
  PID TTY           TIME CMD
 1306 ttys000    0:00.02 login -pf user
 1308 ttys000    0:00.57 -zsh
 
「-e」オプションはシステム全体のプロセスを表示

PID：  一意の番号で、　プロセスID
TTY：  プロセスが実行されたターミナルの名前
TIME： CPU消費時間

TTYが「？」になっているときは端末に依存しないプロセス
```

#### プロセスの親子関係を表示する
```
% pstree
-+= 00001 root /sbin/launchd
 |--= 00295 root /usr/libexec/logd
 |--= 00296 root /usr/libexec/UserEventAgent (System)
 |--= 00298 root /System/Library/PrivateFrameworks/Uninstall.framework/Resources/uninstalld
 |--= 00299 root /System/Library/Frameworks/CoreServices.framework/Versions/A/Frameworks/FSEvents.framework/Versions/A/Support/fseventsd
 |--= 00300 root /System/Library/PrivateFrameworks/MediaRemote.framework/Support/mediaremoted
 |-+= 00302 root /usr/sbin/systemstats --daemon
 | \--- 00936 root /usr/sbin/systemstats --logger-helper /private/var/db/systemstats
```

### 4-5-3

#### プロセスにシグナルをおくる
```
kill [-シグナル]　プロセスID
kill [-シグナル]　ジョブ番号
```

#### ジョブやプロセスを強制終了
```
% kill -SIGKILL 1198
```

#### シグナル一覧を表示
```
kill -l
```

#### プロセス名でシグナルを送る
```
ps -e | grep プロセス名
```


