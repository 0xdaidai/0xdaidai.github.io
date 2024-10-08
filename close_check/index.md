# bypass_ssl


## wget

```c
echo "check_certificate = off" >> ~/.wgetrc
```

## curl 忽略证书

```bash
echo "-k" > ~/.curlrc
# 因为curl可选参数很多，为了防止命令过长，curl会默认去~/.curlrc下面读取curl的全局参数设置
```

## nodeJS 忽略证书

```bash
# env
NODE_TLS_REJECT_UNAUTHORIZED=0
```

## git 忽略证书

```bash
git config --global http.sslVerify false
```

## python 忽略证书

```bash
1export CURL_CA_BUNDLE=“”
#原理请参考：https://stackoverflow.com/questions/48391750/disable-python-requests-ssl-validation-for-an-imported-module
```

## yum忽略证书

```bash
# /etc/yum.conf
sslverify=false
```

## maven忽略证书

```bash
mvn -Dmaven.wagon.http.ssl.insecure=true -Dmaven.wagon.http.ssl.allowall=true -Dmaven.wagon.http.ssl.ignore.validity.dates=true
```
