# Chapter 4

## 4-3 ディスクの管理とLVM
```
Dmesg displays the contents of the system message buffer.
This command needs to be run as root.
$ sudo dmesg
```
```
現在オープンされているファイルを表示
% lsof
```
```
fdiskコマンドはパーティション作成

mkfsコマンドはXFSファイルシステムでフォーマットする
```

#### LVM(Logical Volume Manager)による仮想パーティション
```
PV(Physical Volume)を作成する
% pvcreate
```
```
作成したPVを既存のVG(Volume Group)へ追加する
% vgextend VG PG
```
```
LV(Logical Volume)を拡張する
% lvextend -L size LV
```
