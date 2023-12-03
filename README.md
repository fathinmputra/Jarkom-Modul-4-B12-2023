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
- Kanan:
  - Ke A10 lewat Denken:
    - Network 192.184.22.0
    - Mask 255.255.255.0
    - Next Hop 192.184.24.130

- Kiri:
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

- Bawah:
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




## METODE VLSM
