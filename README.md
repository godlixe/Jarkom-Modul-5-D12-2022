# Jarkom-Modul-5-D12-2022
Repository laporan resmi praktikum Jaringan Komputer 2022
Praktikum Jaringan Komputer Modul 5 (Firewall) 2022.

## Anggota Kelompok:

| Nama                           | NRP        | Nomor Yang dikerjakan |
| ------------------------------ | ---------- | --------------------- |
| Hafizh Mufid Darussalam        | 5025201093 | 5-7               |
| Januar Evan Zuriel Banjarnahor | 5025201210 | 1 (Setting Proxy Client dan Server config)		      |
| Alexander 			 | 5025201247 | A-D                 |

## Topologi
![](https://github.com/godlixe/Jarkom-Modul-5-D12-2022/blob/main/SS%20Modul%205/Modul5.png?raw=true)

## VLSM Tree
![](https://github.com/godlixe/Jarkom-Modul-5-D12-2022/blob/main/SS%20Modul%205/Modul5_Tree.png?raw=true)

## Tabel Subnetting
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

## Tabel IP Node
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