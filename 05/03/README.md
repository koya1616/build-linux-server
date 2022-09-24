# Chapter 5

## 5-3 ネットワークの基本コマンド

```
% ip [オプション]　オブジェクト　[サブコマンド]
ネットワークインターフェイスの設定や確認をする
```
```
% ping [オプション] [ホスト名もしくはIPアドレス]
接続先のホストにアクセスできるかどうかを調べる

% ping google.com
PING google.com (172.217.174.110): 56 data bytes
64 bytes from 172.217.174.110: icmp_seq=0 ttl=116 time=359.822 ms
```
```
% traceroute [オプション]　ホスト名もしくはIPアドレス
指定したホストまでの経路を調べる

% traceroute google.co.jp
traceroute to google.co.jp (172.217.174.99), 64 hops max, 52 byte packets
 1  10.195.0.254 (10.195.0.254)  308.226 ms  167.739 ms  269.542 ms
```
```
% host [オプション] ホスト名もしくはIPアドレス
DNSサーバーに問い合わせを行う

% host google.co.jp
google.co.jp has address 172.217.174.99
google.co.jp has IPv6 address 2404:6800:4004:810::2003
google.co.jp mail is handled by 0 smtp.google.com.
```
```
% dig [@DNSサーバー]　ホスト名もしくはIPアドレス
DNSサーバーに問い合わせを行う(hostコマンドより詳細に)

% dig google.co.jp

; <<>> DiG 9.10.6 <<>> google.co.jp
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 46752
;; flags: qr rd ra; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 4096
;; QUESTION SECTION:
;google.co.jp.			IN	A

;; ANSWER SECTION:
google.co.jp.		152	IN	A	172.217.174.99

;; Query time: 88 msec
;; SERVER: 10.7.161.1#53(10.7.161.1)
;; WHEN: Sat Sep 24 18:13:52 JST 2022
;; MSG SIZE  rcvd: 57

```






