# Jarkom-Modul-5-D12-2022
Repository laporan resmi praktikum Jaringan Komputer 2022
Praktikum Jaringan Komputer Modul 5 (Firewall) 2022.

## Anggota Kelompok:

| Nama                           | NRP        | Nomor Yang dikerjakan |
| ------------------------------ | ---------- | --------------------- |
| Hafizh Mufid Darussalam        | 5025201093 | 5-7               |
| Januar Evan Zuriel Banjarnahor | 5025201210 | 1-6		      |
| Alexander 			 | 5025201247 | A-D                 |

## A. Topologi
![](https://github.com/godlixe/Jarkom-Modul-5-D12-2022/blob/main/SS%20Modul%205/Modul5.png?raw=true)

## B. Subnetting
### VLSM Tree
![](https://github.com/godlixe/Jarkom-Modul-5-D12-2022/blob/main/SS%20Modul%205/Modul5_Tree.png?raw=true)

### Tabel Subnetting
| Subnet | Jumlah IP | Length | IP          | Subnet Mask     |
| ------ | --------- | ------ | ----------- | --------------- |
| A1     | 3         | /29    | 10.21.7.128 | 255.255.255.248 |
| A2     | 2         | /30    | 10.21.7.144 | 255.255.255.252 |
| A3     | 63        | /25    | 10.21.7.0   | 255.255.255.128 |
| A4     | 701       | /22    | 10.21.0.0   | 255.255.252.0   |
| A5     | 2         | /30    | 10.21.7.148 | 255.255.255.252 |
| A6     | 256       | /23    | 10.21.4.0   | 255.255.254.0   |
| A7     | 201       | /24    | 10.21.6.0   | 255.255.255.0   |
| A8     | 3         | /29    | 10.21.7.136 | 255.255.255.248 |
| Total  | 1231      | /21    |             |                 |

### Tabel IP Node
| Subnet | Node            | IP          | Subnet Mask     |
| ------ | --------------- | ----------- | --------------- |
| A1     | Westalis (eth1) | 10.21.7.129 | 255.255.255.248 |
| A1     | Eden            | 10.21.7.130 | 255.255.255.248 |
| A1     | Wise            | 10.21.7.131 | 255.255.255.248 |
| A2     | Westalis (eth0) | 10.21.7.145 | 255.255.255.252 |
| A2     | Strix (eth1)    | 10.21.7.146 | 255.255.255.252 |
| A3     | Westalis (eth2) | 10.21.7.1   | 255.255.255.128 |
| A3     | Forger          | 10.21.7.2   | 255.255.255.128 |
| A4     | Westalis (eth3) | 10.21.0.1   | 255.255.252.0   |
| A4     | Desmond         | 10.21.0.2   | 255.255.252.0   |
| A5     | Strix (eth2)    | 10.21.7.149 | 255.255.255.252 |
| A5     | Ostania (eth0)  | 10.21.7.150 | 255.255.255.252 |
| A6     | Ostania (eth1)  | 10.21.4.1   | 255.255.254.0   |
| A6     | Blackbell       | 10.21.4.2   | 255.255.254.0   |
| A7     | Ostania (eth2)  | 10.21.6.1   | 255.255.255.0   |
| A7     | Briar           | 10.21.6.2   | 255.255.255.0   |
| A8     | Ostania (eth3)  | 10.21.7.137 | 255.255.255.248 |
| A8     | Garden          | 10.21.7.138 | 255.255.255.248 |
| A8     | SSS             | 10.21.7.139 | 255.255.255.248 |

### Konfigurasi Node

- Eden
```
auto eth0
iface eth0 inet static
address 10.21.7.130
netmask 255.255.255.248
gateway 10.21.7.129
```

- Wise
```
auto eth0
iface eth0 inet static
address 10.21.7.131
netmask 255.255.255.248
gateway 10.21.7.129
```

- Garden
```
auto eth0
iface eth0 inet static
address 10.21.7.138
netmask 255.255.255.248
gateway 10.21.7.137
```

- SSS
```
auto eth0
iface eth0 inet static
address 10.21.7.139
netmask 255.255.255.248
gateway 10.21.7.137
```

- Strix
```
auto eth0
iface eth0 inet dhcp

auto eth1
iface eth1 inet static
address 10.21.7.146
netmask 255.255.255.252

auto eth2
iface eth2 inet static
address 10.21.7.149
netmask 255.255.255.252
```

- Westalis
```
auto eth0
iface eth0 inet static
address 10.21.7.145
netmask 255.255.255.252
gateway 10.21.7.146

auto eth1
iface eth1 inet static
address 10.21.7.129
netmask 255.255.255.248

auto eth2
iface eth2 inet static
address 10.21.7.1
netmask 255.255.255.128

auto eth3
iface eth3 inet static
address 10.21.0.1
netmask 255.255.252.0
```

- Ostania
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
address 10.21.7.150
netmask 255.255.255.252
gateway 10.21.7.149

auto eth1
iface eth1 inet static
address 10.21.4.1
netmask 255.255.254.0

auto eth2
iface eth2 inet static
address 10.21.6.1
netmask 255.255.255.0

auto eth3
iface eth3 inet static
address 10.21.7.137
netmask 255.255.255.248
```

- Desmond
```
#auto eth0
#iface eth0 inet static
#address 10.21.0.2
#netmask 255.255.252.0
#gateway 10.21.0.1

auto lo
iface lo inet loopback

auto eth0
iface eth0 inet dhcp
```

- Briar
```
#auto eth0
#iface eth0 inet static
#address 10.21.6.2
#netmask 255.255.255.0
#gateway 10.21.6.1

auto lo
iface lo inet loopback

auto eth0
iface eth0 inet dhcp
```

- Blackbell
```
#auto eth0
#iface eth0 inet static
#address 10.21.4.2
#netmask 255.255.254.0
#gateway 10.21.4.1

auto lo
iface lo inet loopback

auto eth0
iface eth0 inet dhcp
```

- Forger
```
#auto eth0
#face eth0 inet static
#address 10.21.7.2
#netmask 255.255.255.128
#gateway 10.21.7.1

auto lo
iface lo inet loopback

auto eth0
iface eth0 inet dhcp
```

### C. Routing
![](https://github.com/godlixe/Jarkom-Modul-5-D12-2022/blob/main/SS%20Modul%205/routing.png?raw=true)

### D. DHCP Server & Relay

- Konfigurasi DHCP Server pada WISE

![](https://github.com/godlixe/Jarkom-Modul-5-D12-2022/blob/main/SS%20Modul%205/dhcp-server-1.png?raw=true)
![](https://github.com/godlixe/Jarkom-Modul-5-D12-2022/blob/main/SS%20Modul%205/dhcp-server-2.png?raw=true)
![](https://github.com/godlixe/Jarkom-Modul-5-D12-2022/blob/main/SS%20Modul%205/dhcp-server-3.png?raw=true)

- Konfigurasi DHCP Relay pada Westalis & Ostania

![](https://github.com/godlixe/Jarkom-Modul-5-D12-2022/blob/main/SS%20Modul%205/dhcp-relay-1.png?raw=true)

## E. Firewall
1. Agar topologi yang kalian buat dapat mengakses keluar, kalian diminta untuk mengkonfigurasi Strix menggunakan iptables, tetapi Loid tidak ingin menggunakan MASQUERADE.
  
  Lakukan pada router Strix :
  ```
  my_eth0_ip=$(/sbin/ifconfig eth0 | grep 'inet addr:' | cut -d: -f2 | awk '{ print $1 }')
  iptables -t nat -A POSTROUTING -o eth0 -j SNAT --to-source "$my_eth0_ip" -s 10.21.0.0/21
  ```
  `my_eth0_ip` digunakan untuk mengambil ip dari interface eth0 dari `Strix` karena IP eth0 didapatkan dengan DHCP. Kemudian lakukan POSTROUTING Firewall tabel nat untuk mengubah source address dari luar menjadi address Strix
  
  Pengetesan :
  Silahkan coba `apt-get update` pada setiap routing

2. Kalian diminta untuk melakukan drop semua TCP dan UDP dari luar Topologi kalian pada server yang merupakan DHCP Server demi menjaga keamanan.

  Lakukan script ini pada Strix :
  ```
  iptables -A FORWARD -d 10.21.7.131 -p tcp -i eth0 -j DROP
  iptables -A FORWARD -d 10.21.7.131 -p udp -i eth0 -j DROP
  ```
