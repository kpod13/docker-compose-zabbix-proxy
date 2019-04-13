# docker-compose-zabbix-proxy

This is a docker-compose app with zabbix-proxy.

## Usage

1. Save your psk key to file the key file (by default `zabbix-proxy.psk` or set
different file namy by environment variable `ZBX_TLSPSKFILE`). You can get
more imformation [here](https://www.zabbix.com/documentation/current/en/manual/encryption/using_pre_shared_keys).
2. Start application with params. If you need to use PSK identity name differ
to `zabbix-agent` set it by environment variable `ZBX_TLSPSKIDENTITY`.

```bash
ZBX_SERVER_HOST=monitoring.example.com ZBX_ACTIVESERVERS=monitoring.example.com docker-compose up
```

## Credentials

* [Timur Vasyunin](mailto:timur.vasyunin@icloud.com)