# docker-compose-zabbix-proxy

This is a docker-compose app with zabbix-proxy.

## Usage

1. Save your psk key to file the key file (by default `zabbix-proxy.psk` or set
different file name by environment variable `ZBX_TLSPSKFILE`). You can get
more imformation [here](https://www.zabbix.com/documentation/current/manual/encryption/using_pre_shared_keys).

2. Start application with params. If you need to use PSK identity name differ
to `zabbix-agent` set it by environment variable `ZBX_TLSPSKIDENTITY`.


### For the first run

```bash
ZBX_SERVER_HOST=monitoring.example.com ZBX_ACTIVESERVERS=monitoring.example.com ZBX_HOSTNAME=office.example.com ZBX_TLSPSKIDENTITY=office.example.com docker-compose up
```

Check these

* `ZBX_SERVER_HOST` and `ZBX_ACTIVESERVERS` are right names
* `ZBX_HOSTNAME` must be set as the same as a name of your zabbix-proxy name on zabbix-server side (see URI `/zabbix.php?action=proxy.list`)
* `ZBX_TLSPSKIDENTITY` must be the same that was used in PSK generating

## Credentials

* [Timur Vasyunin](mailto:timur.vasyunin@icloud.com)