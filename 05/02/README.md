# Chapter 5

## 5-2 ローカルネットワークでのホスト名の解決

### 5-2-1

#### /etc/hostsファイルにホスト名とIPアドレスを登録する
```
/etc/hosts

##
# Host Database
#
# localhost is used to configure the loopback interface
# when the system is booting.  Do not change this entry.
##
127.0.0.1	localhost
255.255.255.255	broadcasthost
::1             localhost
# Added by Docker Desktop
# To allow the same kube context to work on the host and the container:
127.0.0.1 kubernetes.docker.internal
# End of section

「::1」はIPv6用のループバックアドレス
```

### 5-2-2

#### マルチキャストDNS
```
マルチキャストDNSはローカルネットワーク上の機器を自動認識・設定するための仕組み
```

#### ファイアウォールの設定
```
% sudo firewall-cmd --add-service=mdns --zone=public --permanent
success

% sudo firewall-cmd --reload
success
```

#### クライアントの設定
```
以下でマルチキャストDNSが利用できる
  epelリポジトリを利用でいるようにする
  % sudo dnf -y install epel-release

  nss-mdnsパッケージをインストールする
  % sudo dnf -y install nss-mdns
  
Macや、Windows 10、UbuntuではデフォルトでマルチキャストDNSが動作しているため、
お互いに「ホスト名.local」でアクセスできる
```

### 5-2-3

#### ローカルにDNSサーバーを立てる
```
/etc/hostsの設定をそのままDNSデータベースとして利用できる「dnsmasq」パッケージをインストール
% sudo dnf install -y dnsmasq

仮想環境用のサービス「libvirtd」が起動していたら停止させる
% systemctl(launchctl) disable --now libvirtd
```

#### DNSサーバにアクセスする
```
dig ホスト名　＠DNSサーバ
```
