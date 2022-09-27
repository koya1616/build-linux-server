# Chapter 7

## 7-1 Apacheの概要
- [Apache httpd](https://weblabo.oscasierra.net/apache-macos-usage/)

#### 現在ロードされているすべての静的および動的モジュールの一覧
```
% httpd -M
AH00557: httpd: apr_sockaddr_info_get() failed for aoyamakuyanoAir
AH00558: httpd: Could not reliably determine the server's fully qualified domain name, using 127.0.0.1. Set the 'ServerName' directive globally to suppress this message
Loaded Modules:
 core_module (static)
 so_module (static)
 http_module (static)
 mpm_prefork_module (shared)
 authn_file_module (shared)
 authn_core_module (shared)
 authz_host_module (shared)
 authz_groupfile_module (shared)
 authz_user_module (shared)
 authz_core_module (shared)
 access_compat_module (shared)
 auth_basic_module (shared)
 reqtimeout_module (shared)
 filter_module (shared)
 mime_module (shared)
 log_config_module (shared)
 env_module (shared)
 headers_module (shared)
 setenvif_module (shared)
 version_module (shared)
 slotmem_shm_module (shared)
 unixd_module (shared)
 status_module (shared)
 autoindex_module (shared)
 negotiation_module (shared)
 dir_module (shared)
 alias_module (shared)
 hfs_apple_module (shared)
```

#### Webサーバの起動
```
% sudo systemctl enable --now httpd
```








