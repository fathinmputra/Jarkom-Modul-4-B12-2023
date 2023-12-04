# Praktikum Jaringan Komputer
# Modul 4
### Kelompok B12
### Anggota :
|            Nama           |     NRP    |
| ------                    | ------     |
| Darvin Exaudi Simanjuntak | 5025211172 |
| Fathin Muhashibi Putra    | 5025211229 |

**Soal :** [link](https://docs.google.com/document/d/1PFDIgt5fC4PMmUaDKxw9ZEgwzpzgFv0xvo3K7PRkj10/edit)

# Topologi
<img width="822" alt="topologi fix" src="https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/103252800/038518ab-3bf3-4c41-9e99-efa4c08cef92">

Penentuan Subnet :

![topologi subnet](https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/103252800/7646a47d-aa1c-4578-abdb-e7abd3d1db21)

## METODE VLSM
**Langkah 1** - Menentukan jumlah alamat IP yang dibutuhkan oleh tiap subnet dan melakukan labelling netmask berdasarkan jumlah IP yang dibutuhkan.

<img width="500" alt="image" src="https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/103252800/2fbf8f15-61f3-4cba-bcb0-a886ce7660c7">

Berdasarkan total IP dan netmask yang dibutuhkan, maka kita dapat menggunakan netmask /19 untuk memberikan pengalamatan IP pada subnet.

Kemudian, subnet diurutkan berdasarkan jumlah netmask : 

<img width="378" alt="image" src="https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/103252800/5ae63e45-fdc0-4e20-8d36-c0d2428344eb">


**Langkah 2** - Subnet besar yang dibentuk memiliki NID 192.184.0.0 dengan netmask /19. Kemudian menghitung pembagian IP berdasarkan NID dan netmask menggunakan pohon (tree).

<img width="500" alt="image" src="https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/103252800/8d3c8570-90ed-4a46-a51d-f54e1d8561c2">

**Langkah 3** - Melakukan subnetting dengan menggunakan pohon (tree)  tersebut untuk pembagian IP sesuai dengan kebutuhan masing-masing subnet yang ada.

<img width="500" alt="image" src="https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/103252800/af8350fc-1609-4877-a7dc-e7bc7fb1976d">

Berdasarkan Tree tersebut akan mendapat pembagian IP sebagai berikut.

<img width="500" alt="image" src="https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/103252800/355c4890-8240-4a19-9b6d-ff0e68f191d7">

### Konfigurasi Cisco Packet Tracer :

Kita perlu melakukan **__IP Configuration__** pada router, client, dan server terlebih dahulu, sebagai berikut :

**Router :**
- Pilih Router yang akan dikonfigurasi dengan cara "Klik" pada router tersebut. **Contoh: Router Aura**

<img width="411" alt="image" src="https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/103252800/1b796d77-ea74-4959-abaf-f2cfaf1d2390">

- Pada menu "Config" terdapat "Interface" untuk mengatur IP Configuration Router yang terdiri dari IPv4Address dan Subnet Mask.

<img width="526" alt="image" src="https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/103252800/bbc15b8e-3ecf-4cd4-be33-35032b48c796">

- Kemudian, isi IPv4Address dan Subnet Mask pada masing-masing interface yang terhubung berdasarkan hasil perhitungan subnet metode VLSM yang sudah didapatkan sebelumnya.

<img width="526" alt="image" src="https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/103252800/445f27db-3a27-4b94-a87f-f8e18ff76dba">

<img width="527" alt="image" src="https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/103252800/4afdb8db-2cad-45a5-bad8-cdc1fb052d00">

<img width="528" alt="image" src="https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/103252800/f86032b0-8593-4cfd-9d3a-2b2556112f51">

- Lakukan, langkah-langkah **Konfigurasi IP** di atas pada **seluruh Router** yang ada.

**Client atau Server :**
- Pilih Client atau Server yang akan dikonfigurasi dengan cara "Klik" pada Client atau Server tersebut. **Contoh: CLient LakeKorridor**

<img width="198" alt="image" src="https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/103252800/7af66ee0-cf9d-4b8a-98ca-b5f740a7f535">

- Pada menu "Desktop" pilih "IP Configuration" untuk mengatur IP Configuration Client atau server yang terdiri dari IPv4Address, Subnet Mask, dan Default Gateway.

<img width="526" alt="image" src="https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/103252800/0cef296c-dff7-4e09-a8ce-e84774487e13">

- Kemudian, isi IPv4Address, Subnet Mask, dan Default Gateway berdasarkan hasil perhitungan subnet metode VLSM yang sudah didapatkan sebelumnya.
<img width="527" alt="image" src="https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/103252800/73d86d7d-adc3-4c22-87ba-434b1fb527ba">

- Lakukan, langkah-langkah **Konfigurasi IP** di atas pada **seluruh Client dan Server** yang ada.

### Static Routing :

Kita perlu melakukan **routing** pada **seluruh Router**. Langkah-langkah melakukan routing, sebagai berikut :
- Pilih Router yang akan diberi route dengan cara "Klik" pada router tersebut. **Contoh: Router Frieren**
  
<img width="455" alt="image" src="https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/103252800/0199b4cc-16bb-40db-b9ca-b30df8b8b49e">

- Pada menu "Config", terdapat "Routing", kemudian klik "Static" untuk menambahkan route pada Router yang terdiri dari Network, Mask, dan Next Hop. Isi satu persatu route, kemudian klik "Add" hingga seluruh route dari router tersebut ditambahkan.
  
<img width="525" alt="image" src="https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/103252800/e43608f6-ace4-4bb3-bb4d-9a4589832eac">

- Lakukan, langkah-langkah **Routing** di atas pada **seluruh Router** yang ada.
  
- List Route dari setiap Router, sebagai berikut :
  
**Route List:**
**Aura**
Kanan:
- Ke A10 lewat Denken:
  - Network 192.184.22.0
  - Mask 255.255.255.0
  - Next Hop 192.184.24.130

Kiri:
- Ke A6 lewat Frieren:
  - Network 192.184.24.120
  - Mask 255.255.255.252
  - Next Hop 192.184.24.126
- Ke A7 lewat Frieren:
  - Network 192.184.24.64
  - Mask 255.255.255.224
  - Next Hop 192.184.24.126
- Ke A3 lewat Frieren:
  - Network 192.184.24.116
  - Mask 255.255.255.252
  - Next Hop 192.184.24.126
- Ke A4 lewat Frieren:
  - Network 192.184.24.96
  - Mask 255.255.255.248
  - Next Hop 192.184.24.126
- Ke A5 lewat Frieren:
  - Network 192.184.8.0
  - Mask 255.255.252.0
  - Next Hop 192.184.24.126
- Ke A2 lewat Frieren:
  - Network 192.184.24.112
  - Mask 255.255.255.252
  - Next Hop 192.184.24.126
- Ke A1 lewat Frieren:
  - Network 192.184.0.0
  - Mask 255.255.248.0
  - Next Hop 192.184.24.126

Bawah:
- Ke A12 lewat Eisen:
  - Network 192.184.24.104
  - Mask 255.255.255.248
  - Next Hop 192.184.24.134
- Ke A13 lewat Eisen:
  - Network 192.184.24.136
  - Mask 255.255.255.252
  - Next Hop 192.184.24.134
- Ke A14 lewat Eisen:
  - Network 192.184.24.140
  - Mask 255.255.255.252
  - Next Hop 192.184.24.134
- Ke A15 lewat Eisen:
  - Network 192.184.12.0
  - Mask 255.255.252.0
  - Next Hop 192.184.24.134
- Ke A16 lewat Eisen:
  - Network 192.184.23.0
  - Mask 255.255.255.0
  - Next Hop 192.184.24.134
- Ke A17 lewat Eisen:
  - Network 192.184.24.144
  - Mask 255.255.255.252
  - Next Hop 192.184.24.134
- Ke A18 lewat Eisen:
  - Network 192.184.20.0
  - Mask 255.255.254.0
  - Next Hop 192.184.24.134
- Ke A19 lewat Eisen:
  - Network 192.184.24.148
  - Mask 255.255.255.252
  - Next Hop 192.184.24.134
- Ke A20 lewat Eisen:
  - Network 192.184.24.0
  - Mask 255.255.255.192
  - Next Hop 192.184.24.134
- Ke A21 lewat Eisen:
  - Network 192.184.16.0
  - Mask 255.255.252.0
  - Next Hop 192.184.24.134

**Denken**
- Balik ke Aura:
    - Network 0.0.0.0
    - Netmask 0.0.0.0
    - Next Hop 192.184.24.129
      
**Frieren**
- Ke A5 lewat Flamme:
  - Network 192.184.8.0
  - Mask 255.255.252.0
  - Next Hop 192.184.24.122
- Ke A2 lewat Flamme:
  - Network 192.184.24.112
  - Mask 255.255.255.252
  - Next Hop 192.184.24.122
- Ke A1 lewat Flamme:
  - Network 192.184.0.0
  - Mask 255.255.248.0
  - Next Hop 192.184.24.122
- Ke A3 lewat Flamme:
  - Network 192.184.24.116
  - Mask 255.255.255.252
  - Next Hop 192.184.24.122
- Ke A4 lewat Flamme:
  - Network 192.184.24.96
  - Mask 255.255.255.248
  - Next Hop 192.184.24.122
- Balik ke Aura:
  - Network 0.0.0.0
  - Mask 0.0.0.0
  - Next Hop 192.184.24.125


**Flamme**
- Ke A1 Lewat Fern:
  - Network 192.184.0.0
  - Mask 255.255.248.0
  - Next Hop 192.184.24.114
- Ke A4 Lewat Himmel:
  - Network 192.184.24.96
  - Mask 255.255.255.248
  - Next Hop 192.184.24.118
- Balik ke Frieren:
  - Network 0.0.0.0
  - Mask 0.0.0.0
  - Next Hop 192.184.24.121

**Fern**
- Balik ke Flamme:
  - Network 0.0.0.0
  - Mask 0.0.0.0
  - Next Hop 192.184.24.113

**Himmel**
- Balik ke Flamme:
  - Network 0.0.0.0
  - mask 0.0.0.0
  - Next Hop 192.184.24.117


**Eisen**
- Ke A15 lewat Lugner
  - Network 192.184.12.0
  - Mask 255.255.252.0
  - Next Hop 192.184.24.142
- Ke A16 lewat Lugner
  - Network 192.184.23.0
  - Mask 255.255.255.0
  - Next Hop 192.184.24.142
- Ke A18 lewat Linie
  - Network 192.184.20.0
  - Mask 255.255.254.0
  - Next Hop 192.184.24.146
- Ke A19 lewat Linie
  - Network 192.184.24.148
  - Mask 255.255.255.252
  - Next Hop 192.184.24.146
- Ke A20 lewat Linie
  - Network 192.184.24.0
  - Mask 255.255.255.192
  - Next Hop 192.184.24.146
- Ke A21 lewat Linie
  - Network 192.184.16.0
  - Mask 255.255.252.0
  - Next Hop 192.184.24.146
- Balik ke Aura
  - Network 0.0.0.0
  - Mask 0.0.0.0
  - Next Hop 192.184.24.133


**Lugner**
- Balik ke Eisen:
  - Network 0.0.0.0
  - Mask 0.0.0.0
  - Next Hop 192.184.24.141

**Linie**
- Ke A20 lewat Lawine:
  - Network 192.184.24.0
  - Mask 255.255.255.192
  - Next Hop 192.184.24.150
- Ke A21 lewat Lawine:
  - Network 192.184.16.0
  - Mask 255.255.252.0
  - Next Hop 192.184.24.150
- Balik ke Eisen:
  - Network 0.0.0.0
  - Mask 0.0.0.0
  - Next Hop 192.184.24.145

**Lawine**
- Ke A21 lewat Heiter:
  - Network 192.184.16.0
  - Mask 255.255.252.0
  - Next Hop 192.184.24.2
- Balik Ke Linie:
  - Network 0.0.0.0
  - Mask 0.0.0.0
  - Next Hop 192.184.24.149

**Heiter**
- Balik ke Lawine:
  - Network 0.0.0.0
  - Mask 0.0.0.0
  - Next Hop 192.184.24.1




## METODE CIDR
### Topologi GNS3
![image](https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/133391111/e272ed4f-82fc-4896-97e1-e40a3787df92)

- Pada topologi GNS ini, ditambahkan switch diantara router. Sesuai dengan perintah yang ada di modul 4 :

![image](https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/133391111/798bd316-500e-48fa-8cd4-0b33bcd57b70)

### Penggabungan Subnet

Berikut adalah penggabungan subnetnya :

- **Penggabungan Pertama**

![image](https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/133391111/57b8f35a-adfd-4687-8031-7a31fc8c6b72)
![image](https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/133391111/86f5db40-2702-4748-8813-471435838728)

- **Penggabungan Kedua**

![image](https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/133391111/c6125006-7b5c-48eb-85e6-7717a316eabb)
![image](https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/133391111/6031781a-7480-4d2c-9d22-4888ff853851)

- **Penggabungan Ketiga**

![image](https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/133391111/82637f6f-bee3-4512-bbb3-26e9b68e762c)
![image](https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/133391111/c556fa8f-e965-4c6c-b8ed-862de3748516)

- **Penggabungan Keempat**

![image](https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/133391111/5c95e593-b538-44a8-87e5-f486a2153c5b)
![image](https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/133391111/86df01c6-8fb4-4762-b397-ab53690416a0)

- **Penggabungan Kelima**

![image](https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/133391111/ee1b2b32-d34a-491a-bf37-8acf3fa54a50)
![image](https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/133391111/c6f7d5ff-71aa-4f9b-88ff-b0bd2d187588)

- **Penggabungan Keenam**

![image](https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/133391111/969144de-b725-4b92-aa9c-13f984fa2462)
![image](https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/133391111/0886a4ff-3bd2-480f-b4b6-216170c67da4)

- **Penggabungan Ketujuh**

![image](https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/133391111/fda63dfc-525c-450b-b3da-e90fa4c9c3ad)
![image](https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/133391111/bbbb7fc9-ff27-475c-9cde-226e5b9b8fd3)

- **Penggabungan Kedelapan**

![image](https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/133391111/00e67386-1c53-4bd3-a31b-2b9fcb1b2ee2)
![image](https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/133391111/ae9dbb5f-0c04-4c89-b041-b4413664d46a)

### Tree CIDR
Setelah menggabungkan subnetnya, dapat dihitung untuk pembagian IP nya menggunakan tree. Berikut pembagiannya menggunakan tree :

![image](https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/133391111/bc65449a-39b6-45b0-b05e-faedf6aa94c9)

### Pembagian IP
Berikut adalah pembagian IP sesuai dengan tree sebelumnya :

![image](https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/133391111/cd4eded5-7d94-4264-b75e-df2dbc955c70)

### Configuration Network
Setelah mendapatkan hasil pembagian IP, kita dapat memasukkan pembagian IP tersebut ke dalam konfigurasi di `GNS3`.

Berikut adalah konfigurasi `router, client, dan server` pada `GNS3` menggunakan pembagian IP `CIDR` :

**ROUTER :**

- Aura
```
auto eth0
iface eth0 inet dhcp

# kanan
auto eth1
iface eth1 inet static
	address 192.185.0.1
	netmask 255.255.255.252

# bawah
auto eth2
iface eth2 inet static
	address 192.184.64.1
	netmask 255.255.255.252

# kiri
auto eth3
iface eth3 inet static
	address 192.186.128.1
	netmask 255.255.255.252
```

- Denken
```
# 0/0 - kiri
auto eth0
iface eth0 inet static
	address 192.185.0.2
	netmask 255.255.255.252

# 0/1 - kanan
auto eth1
iface eth1 inet static
	address 192.185.1.1
	netmask 255.255.255.0
```

- Frieren
```
# kanan
auto eth0
iface eth0 inet static
	address 192.186.128.2
	netmask 255.255.255.252

# atas
auto eth1
iface eth1 inet static
	address 192.186.64.1
	netmask 255.255.255.224

# kiri
auto eth2
iface eth2 inet static
	address 192.186.32.1
	netmask 255.255.255.252
```

- Flamme
```
# kanan
auto eth0
iface eth0 inet static
	address 192.186.32.2
	netmask 255.255.255.252

# atas
auto eth1
iface eth1 inet static
	address 192.186.24.1
	netmask 255.255.255.252

# kiri
auto eth2
iface eth2 inet static
	address 192.186.4.1
	netmask 255.255.252.0

# bawah
auto eth3
iface eth3 inet static
	address 192.186.0.1
	netmask 255.255.255.252
```

- Fern
```
# bawah
auto eth0
iface eth0 inet static
	address 192.186.24.2
	netmask 255.255.255.252

# kiri
auto eth1
iface eth1 inet static
	address 192.186.16.1
	netmask 255.255.248.0
```

- Himmel
```
# atas
auto eth0
iface eth0 inet static
	address 192.186.0.2
	netmask 255.255.255.252

# bawah
auto eth1
iface eth1 inet static
	address 192.186.0.9
	netmask 255.255.255.248
```

- Eisen
```
# atas
auto eth0
iface eth0 inet static
	address 192.184.64.2
	netmask 255.255.255.252

# kanan atas
auto eth1
iface eth1 inet static
	address 192.184.16.1
	netmask 255.255.255.252

# kiri
auto eth2
iface eth2 inet static
	address 192.184.32.1
	netmask 255.255.255.248

# bawah
auto eth3
iface eth3 inet static
	address 192.184.160.1
	netmask 255.255.255.252

# kanan
auto eth4
iface eth4 inet static
	address 192.184.8.1
	netmask 255.255.255.252
```

- Lugner
```
# kiri
auto eth0
iface eth0 inet static
	address 192.184.8.2
	netmask 255.255.255.252

# kanan
auto eth1
iface eth1 inet static
	address 192.184.0.1
	netmask 255.255.252.0

# kanan bawah
auto eth2
iface eth2 inet static
	address 192.184.4.1
	netmask 255.255.255.0
```

- Linie
```
# atas
auto eth0
iface eth0 inet static
	address 192.184.160.2
	netmask 255.255.255.252

# bawah
auto eth1
iface eth1 inet static
	address 192.184.144.1
	netmask 255.255.254.0

# kiri
auto eth2
iface eth2 inet static
	address 192.184.136.1
	netmask 255.255.255.252
```

- Lawine
```
# kanan
auto eth0
iface eth0 inet static
	address 192.184.136.2
	netmask 255.255.255.252

# kiri
auto eth1
iface eth1 inet static
	address 192.184.128.1
	netmask 255.255.255.192
```

- Heiter
```
# atas
auto eth0
iface eth0 inet static
	address 192.184.128.2
	netmask 255.255.255.192

# kiri
auto eth1
iface eth1 inet static
	address 192.184.132.1
	netmask 255.255.252.0
```

**CLIENT :** 

- RoyalCapital 
```
auto eth0
iface eth0 inet static
	address 192.185.1.2
	netmask 255.255.255.0
        	gateway 192.185.1.1
```

- WillieRegion
```
auto eth0
iface eth0 inet static
	address 192.185.1.3
	netmask 255.255.255.0
        	gateway 192.185.1.1
```

- LakeKorridor
```
auto eth0
iface eth0 inet static
	address 192.186.64.2
	netmask 255.255.255.224
        	gateway 192.185.64.1
```

- LaubHills
```
auto eth0
iface eth0 inet static
	address 192.186.16.2
	netmask 255.255.248.0
       	gateway 192.186.16.1
```

- AppetitRegion
```
auto eth0
iface eth0 inet static
	address 192.186.16.3
	netmask 255.255.248.0
        	gateway 192.186.16.1
```

- RohrRoad
```
auto eth0
iface eth0 inet static
	address 192.186.4.2
	netmask 255.255.252.0
        	gateway 192.186.4.1
```

- SchwerMountains
```
auto eth0
iface eth0 inet static
	address 192.186.0.10
	netmask 255.255.255.248
        gateway 192.186.0.9
```

- TurkRegion 
```
auto eth0
iface eth0 inet static
	address 192.184.0.2
	netmask 255.255.252.0
        	gateway 192.184.0.1
```

- GrobeForest
```
auto eth0
iface eth0 inet static
	address 192.184.4.2
	netmask 255.255.255.0
        	gateway 192.184.4.1
```

- GranzChannel
```
auto eth0
iface eth0 inet static
	address 192.184.144.2
	netmask 255.255.254.0
        	gateway 192.184.144.1
```

- BredtRegion
```
auto eth0
iface eth0 inet static
	address 192.184.128.2
	netmask 255.255.255.192
        	gateway 192.184.128.1
```

- RiegelCanyon
```
auto eth0
iface eth0 inet static
	address 192.184.132.3
	netmask 255.255.252.0
        	gateway 192.184.132.1
```

**SERVER :** 

- Stark 
```
auto eth0
iface eth0 inet static
	address 192.184.16.2
	netmask 255.255.255.252
        	gateway 192.184.16.1
```

- Richter 
```
auto eth0
iface eth0 inet static
	address 192.184.32.2
	netmask 255.255.255.248
        	gateway 192.184.32.1
```

- Revolte 
```
auto eth0
iface eth0 inet static
	address 192.184.32.3
	netmask 255.255.255.248
        	gateway 192.184.32.1
```

- Sein
```
auto eth0
iface eth0 inet static
	address 192.184.132.2
	netmask 255.255.252.0
        	gateway 192.184.132.1
```

### Routing
Supaya semua subnet dapat saling terhubung, maka diperlukan routing. Berikut adalah perintah routing pada masing masing router GNS :

- Aura
```
route add -net 192.185.1.0 netmask 255.255.255.0 gw 192.185.0.2 
route add -net 192.186.32.0 netmask 255.255.255.252 gw 192.186.128.2
route add -net 192.186.64.0 netmask 255.255.255.224 gw 192.186.128.2
route add -net 192.186.0.0 netmask 255.255.255.252 gw 192.186.128.2
route add -net 192.186.0.8 netmask 255.255.255.248 gw 192.186.128.2
route add -net 192.186.4.0 netmask 255.255.252.0 gw 192.186.128.2
route add -net 192.186.24.0 netmask 255.255.255.252 gw 192.186.128.2
route add -net 192.186.16.0 netmask 255.255.248.0 gw 192.186.128.2
route add -net 192.184.32.0 netmask 255.255.255.248 gw 192.184.64.2
route add -net 192.184.16.0 netmask 255.255.255.252 gw 192.184.64.2
route add -net 192.184.8.0 netmask 255.255.255.252 gw 192.184.64.2
route add -net 192.184.0.0 netmask 255.255.252.0 gw 192.184.64.2
route add -net 192.184.4.0 netmask 255.255.255.0 gw 192.184.64.2
route add -net 192.184.160.0 netmask 255.255.255.252 gw 192.184.64.2
route add -net 192.184.144.0 netmask 255.255.254.0 gw 192.184.64.2
route add -net 192.184.136.0 netmask 255.255.255.252 gw 192.184.64.2
route add -net 192.184.128.0 netmask 255.255.255.192 gw 192.184.64.2
route add -net 192.184.132.0 netmask 255.255.252.0 gw 192.184.64.2
```

- Denken
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.185.0.1
```

- Frieren
```
route add -net 192.186.4.0 netmask 255.255.252.0 gw 192.186.32.2
route add -net 192.186.24.0 netmask 255.255.255.252 gw 192.186.32.2
route add -net 192.186.16.0 netmask 255.255.248.0 gw 192.186.32.2
route add -net 192.186.0.0 netmask 255.255.255.252 gw 192.186.32.2
route add -net 192.186.0.8 netmask 255.255.255.248 gw 192.186.32.2
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.186.128.1
```

- Flamme
```
route add -net 192.186.16.0 netmask 255.255.248.0 gw 192.186.24.2
route add -net 192.186.0.8 netmask 255.255.255.248 gw 192.186.0.1
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.186.32.1
```

- Fern
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.186.24.1
```

- Himmel
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.186.0.1
```

- Eisen
```
route add -net 192.184.0.0 netmask 255.255.252.0 gw 192.184.8.2
route add -net 192.184.4.0 netmask 255.255.255.0 gw 192.184.8.2
route add -net 192.184.144.0 netmask 255.255.254.0 gw 192.184.160.2
route add -net 192.184.136.0 netmask 255.255.255.252 gw 192.184.160.2
route add -net 192.184.128.0 netmask 255.255.255.192 gw 192.184.160.2
route add -net 192.184.132.0 netmask 255.255.252.0 gw 192.184.160.2
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.184.64.1
```

- Lugner
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.184.8.1
```

- Linie
```
route add -net 192.184.128.0 netmask 255.255.255.192 gw 192.184.136.2
route add -net 192.184.132.0 netmask 255.255.252.0 gw 192.184.136.2
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.184.160.1
```

- Lawine
```
route add -net 192.184.132.0 netmask 255.255.252.0 gw 192.184.128.2
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.184.136.1
```

- Heiter
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.184.128.1
```

> Pada setiap router di GNS3, terdapat file `script.sh` yang berisi command-command routing di atas sehingga tinggal bash filenya untuk melakukan routing.

### Hasil Testing

Berikut adalah beberapa testing yang dilakukan :

- Ping LaubHills dari GranzChannel

![image](https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/133391111/a241d2bd-662a-4917-9bf0-eb5c97d7f088)

- Ping RiegelCanyon dari RoyalCapital

![image](https://github.com/fathinmputra/Jarkom-Modul-4-B12-2023/assets/133391111/ca8db38b-3674-40e3-b21e-7e77a798c57e)
