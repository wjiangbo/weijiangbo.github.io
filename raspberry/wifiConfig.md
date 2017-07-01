## raspebrry wifi 配置

1. 修改 /etc/wpa_supplicant/wpa_supplicant.conf

添加 wifi 信息 
```
network{
    ssid="SSID"
    psk="pasword"
}
```
2. 修改 /etc/network/interfaces
 ```
 auto wlan0
 iface wlan0 inet dhcp
    pre-up wpa_supplicant -Dwext -i wlan0 -c /ect/wpa_supplicant/wpa_supplicant.conf -B
```