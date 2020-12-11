# Jarkom_Modul4_Lapres_A02
Lapres Jarkom Modul 4 A02

## VLSM
### Subnetting
  1. Melakukan subnetting pada topologi yang diberikan. Sehingga terbentuklah 13 subnet di dalam topologi seperti pada gambar berikut.
      ![vlsm_subnet](img/vlsm_subnet.png)
  2. Menentukan jumlah alamat IP yang dibutuhkan oleh tiap subnet dan lmelakukan labelling netmask berdasarkan jumlah IP yang dibutuhkan.
      | Subnet      | Jumlah IP   | Netmask |
      | ----------- |         ---:| ------- |
      | A1          | 721         | /22     |
      | A2          | 252         | /24     |
      | A3          | 13          | /28     |
      | A4          | 502         | /23     |
      | A5          | 521         | /22     |
      | A6          | 2           | /30     |
      | A7          | 2           | /30     |
      | A8          | 2           | /30     |
      | A9          | 701         | /22     |
      | A10         | 2           | /30     |
      | A11         | 2021        | /21     |
      | A12         | 101         | /25     |
      | A13         | 1001        | /22     |
      | Total       | 5841        | /19     |
      
      Berdasarkan total IP dan netmask yang dibutuhkan, maka dapat menggunakan netmask /19 untuk memberikan pengalamatan IP pada subnet.
  3.  Subnet besar yang dibentuk memiliki NID 192.168.0.0 dengan netmask /19. Selanjutnya menghitung pembagian IP berdasarkan NID dan netmask tersebut menggunakan pohon seperti gambar berikut.
      ![vlsm_tree](img/vlsm_tree.jpg)

### Praktik pada CPT
  1. Membuat topologi di CPT.
      ![topologi_cpt](img/topologi_cpt.png)
  2. Mengatur IP untuk masing-masing interface yang ada di setiap device sesuai dengan pembagian subnet pada pohon VLSM.
      - IP pada interface SURABAYA
          - mengarah ke CLOUD
              
              ![sby_cloud](img/sby_int_cloud.png)
          - mengarah ke MOJOKERTO
              
              ![sby_mojo](img/sby_int_mojo.png)
          - mengarah ke BATU (A7)
              
              ![sby_batu](img/sby_int_a7.png)
          - mengarah ke PASURUAN (A8)
              
              ![sby_pasuruan](img/sby_int_a8.png)
          - mengarah ke SAMPANG (A13)
              
              ![sby_sampang](img/sby_int_a13.png)
      - IP pada interface PASURUAN
          - mengarah ke SURABAYA (A8)
              
              ![pas_sby](img/pas_int_a8.png)
          - mengarah ke SIDOARJO (A9)
              
              ![pas_mojo](img/pas_int_a9.png)
          - mengarah ke PROBOLONGGO (A10)
              
              ![pas_pro](img/pas_int_a10.png)        
      - IP pada interface PROBOLINGGO
          - mengarah ke PASURUAN (A10)
              
              ![pro_pas](img/prob_int_a10.png)
          - mengarah ke BANYUWANGI (A11)
              
              ![pro_bny](img/prob_int_a11.png)
          - mengarah ke BONDOWOSO (A12)
              
              ![pro_bds](img/prob_int_a12.png)
      - IP pada interface MADIUN
          - mengarah ke BOJONEGORO (A3)
              
              ![mdn_bjn](img/mdn_int_a3.png)
          - mengarah ke BATU (A4)
              
              ![mdn_mojo](img/mdn_int_a4.png)
      - IP pada interface BATU
          - mengarah ke MADIUN (A4)
              
              ![batu_mdn](img/batu_int_a4.png)
          - mengarah ke NGANJUK (A5)
              
              ![batu_ngj](img/batu_int_a5.png)
          - mengarah ke KEDIRI (A6)
              
              ![batu_kdr](img/batu_int_a6.png)
          - mengarah ke SURABAYA (A7)
              
              ![batu_sby](img/batu_int_a7.png)
      - IP pada interface KEDIRI
          - mengarah ke MALANG
              
              ![kdr_mlg](img/kdr_int_mlg.png)
          - mengarah ke BATU (A6)
              
              ![kdr_batu](img/kdr_int_a9.png)
          - mengarah ke BLITAR (A2)
              
              ![kdr_blt](img/kdr_int_a2.png)
      - IP pada interface BLITAR
          - mengarah ke TULUNGAGUNG (A1)
              
              ![blt_tlg](img/blt_int_a1.png)
          - mengarah ke LUMAJANG (A2)
              
              ![blt_lmj](img/blt_int_a2.png)
      - IP pada interface SAMPANG
          
          ![client_sampang](img/cpt_sampang.png)
      - IP pada interface SIDOARJO
          
          ![client_sampang](img/cpt_sidoarjo.png)
      - IP pada interface BANYUWANGI
          
          ![client_sampang](img/cpt_banyuwangi.png)
      - IP pada interface JEMBER
          
          ![client_sampang](img/cpt_jember.png)
      - IP pada interface BONDOWOSO
          
          ![client_sampang](img/cpt_bondowoso.png)
      - IP pada interface JOMBANG
          
          ![client_sampang](img/cpt_jombang.png)
      - IP pada interface BOJONEGORO
          
          ![client_sampang](img/cpt_bojonegoro.png)
      - IP pada interface NGANJUK
          
          ![client_sampang](img/cpt_nganjuk.png)
      - IP pada interface TULUNGAGUNG
          
          ![client_sampang](img/cpt_tulungagung.png)
      - IP pada interface LUMAJANG
          
          ![client_sampang](img/cpt_lmj.png)
      - IP pada interface MOJOKERTO
          
          ![client_sampang](img/cpt_mojo.png)
      - IP pada interface MALANG
          
          ![client_sampang](img/cpt_malang.png)
  3. Melakukan routing pada setiap Router.
      - SURABAYA
          1. Routing ke A1
              - Network: 192.168.4.0
              - Mask: 255.255.252.0
              - Next Hop: 192.168.0.6
          2. Routing ke A2
              - Network: 192.168.1.0
              - Mask: 255.255.255.0
              - Next Hop: 192.168.0.6
          3. Routing ke A3
              - Network: 192.168.0.16
              - Mask: 255.255.255.240
              - Next Hop: 192.168.0.6
          4. Routing ke A4
              - Network: 192.168.2.0
              - Mask: 255.255.254.0
              - Next Hop: 192.168.0.6
          5. Routing ke A5
              - Network: 192.168.8.0
              - Mask: 255.255.252.0
              - Next Hop: 192.168.0.6
          6. Routing ke A6
              - Network: 192.168.0.0
              - Mask: 255.255.255.252
              - Next Hop: 192.168.0.6
          7. Routing ke A9
              - Network: 192.168.12.0
              - Mask: 255.255.252.0
              - Next Hop: 192.168.0.10
          8. Routing ke A10
              - Network: 192.168.0.12
              - Mask: 255.255.255.252
              - Next Hop: 192.168.0.10
          6. Routing ke A11
              - Network: 192.168.0.128
              - Mask: 255.255.255.128
              - Next Hop: 192.168.0.10
          8. Routing ke MALANG
              - Network: 10.151.73.24
              - Mask: 255.255.255.252
              - Next Hop: 192.168.0.6
      - PASURUAN
          1. Default Routing
              - Network: 0.0.0.0
              - Mask: 0.0.0.0
              - Next Hop: 192.168.0.9
          2. Routing ke A11
              - Network: 192.168.24.0
              - Mask: 255.255.248.0
              - Next Hop: 192.168.0.14
          3. Routing ke A12
              - Network: 192.168.0.128
              - Mask: 255.255.255.128
              - Next Hop: 192.168.0.14
      - PROBOLINGGO
          1. Default Routing
              - Network: 0.0.0.0
              - Mask: 0.0.0.0
              - Next Hop: 192.168.0.13
      - MADIUN
          1. Default Routing
              - Network: 0.0.0.0
              - Mask: 0.0.0.0
              - Next Hop: 192.168.2.1
      - BATU
          1. Default Routing
              - Network: 0.0.0.0
              - Mask: 0.0.0.0
              - Next Hop: 192.168.0.5
          2. Routing ke A1
              - Network: 192.168.4.0
              - Mask: 255.255.252.0
              - Next Hop: 192.168.0.2
          3. Routing ke A2
              - Network: 192.168.1.0
              - Mask: 255.255.255.0
              - Next Hop: 192.168.0.2
          4. Routing ke A3
              - Network: 192.168.0.16
              - Mask: 255.255.255.240
              - Next Hop: 192.168.2.2
          5. Routing ke MALANG
              - Network: 10.151.73.24
              - Mask: 255.255.255.252
              - Next Hop: 192.168.0.2
      - KEDIRI
          1. Default Routing
              - Network: 0.0.0.0
              - Mask: 0.0.0.0
              - Next Hop: 192.168.0.1
          2. Routing ke A1
              - Network: 192.168.4.0
              - Mask: 255.255.252.0
              - Next Hop: 192.168.1.2
      - BLITAR
          1. Default Routing
              - Network: 0.0.0.0
              - Mask: 0.0.0.0
              - Next Hop: 192.168.1.1
## CIDR
### Subnetting
  1. Menentukan subnet yang ada dalam topologi dan melakukan labelling netmask terhadap masing-masing subnet. Hasilnya ada pada gambar berikut.
      ![cidr_subnet](img/cidr_subnet.jpg)
  2. Dari proses penggabungan yang telah dilakukan, didapatkan sebuah subnet besar yang memiliki NID 192.168.0.0 dengan netmask /16.
  3. Selanjutnya menghitung pembagian IP dengan pohon berdasarkan penggabungan subnet yang telah dilakukan.
      ![cidr_tree](img/cidr_tree.jpg)

### Praktik pada UML
  1. Membuat topologi di UML. Penomoran switch pada topologi adalah sebagai berikut.
      ![switch](img/switch.png)
      ![topologi_uml1](img/topologi1.png)
      ![topologi_uml2](img/topologi2.png)
  2. Mengatur IP untuk masing-masing interface yang ada di setiap device sesuai dengan pembagian subnet pada pohon CIDR.
      - IP pada interface SURABAYA
          
          ![int_sby1](img/surabaya1.png)
          ![int_sby2](img/surabaya2.png)
          
          Keterangan:
          - eth0: Mengarah ke CLOUD
          - eth1: Mengarah ke MOJOKERTO
          - eth2: Mengarah ke BATU (A6)
          - eth3: Mengarah ke PASURUAN (A2)
          - eth4: Mengarah ke SAMPANG (A1)
      - IP pada interface PASURUAN
          
          ![int_pas](img/pasuruan.png)
          
          Keterangan:
          - eth0: Mengarah ke SURABAYA (A2)
          - eth1: Mengarah ke SIDOARJO (A7)
          - eth2: Mengarah ke PROBOLINGGO (A3)
      - IP pada interface PROBOLINGGO
          
          ![int_prob](img/probolinggo.png)
          
          Keterangan:
          - eth0: Mengarah ke PASURUAN (A3)
          - eth1: Mengarah ke BANYUWANGI (A8)
          - eth2: Mengarah ke BONDOWOSO (A4)
      - IP pada interface MADIUN
          
          ![int_mdn](img/madiun.png)
          
          Keterangan:
          - eth0: Mengarah ke A5
          - eth1: Mengarah ke BOJONEGORO (A9)
      - IP pada interface BATU
          
          ![int_batu](img/batu.png)
          
          Keterangan:

      - IP pada interface KEDIRI
          
          ![int_kediri](img/kediri.png)
          
          Keterangan:
          - eth0: Mengarah ke BATU (A11)
          - eth1: Mengarah ke MALANG
          - eth2: Mengarah ke A13
      - IP pada interface BLITAR
          
          ![int_blt](img/blitar.png)
          
          Keterangan:
          - eth0: Mengarah ke A13
          - eth1: Mengarah ke TULUNGAGUNG (A12)
      - IP pada interface SAMPANG
          
          ![int_smp](img/sampang.png)
          
          Keterangan:
          - eth0: Mengarah ke SURABAYA (A1)
      - IP pada interface SIDOARJO
          
          ![int_sda](img/sidoarjo.png)
          
          Keterangan:
          - eth0: Mengarah ke PASUEUAN (A7)
      - IP pada interface BANYUWANGI
          
          ![int_byw](img/banyuwangi.png)
          
          Keterangan:
          - eth0: Mengarah ke PROBOLINGGO (A8)
      - IP pada interface JEMBER
          
          ![int_jbr](img/jember.png)
          
          Keterangan:
          - eth0: Mengarah ke PROBOLINGGO (A8)
      - IP pada interface BONDOWOSO
          
          ![int_bds](img/bondowoso.png)
          
          Keterangan:
          - eth0: Mengarah ke PROBOLINGGO (A4)
      - IP pada interface JOMBANG
          
          ![int_jbg](img/jombang.png)
          
          Keterangan:
          - eth0: Mengarah ke A5
      - IP pada interface BOJONEGORO
          
          ![int_bjn](img/bojonegoro.png)
          
          Keterangan:
          - eth0: Mengarah ke MADIUN (A9)
      - IP pada interface NGANJUK
          
          ![int_ngj](img/nganjuk.png)
          
          Keterangan:
          - eth0: Mengarah ke BATU (A10)
      - IP pada interface TULUNGAGUNG
          
          ![int_tlg](img/tulungagung.png)
          
          Keterangan:
          - eth0: Mengarah ke BLITAR (A12)
      - IP pada interface LUMAJANG
          
          ![int_lmj](img/lumajang.png)
          
          Keterangan:
          - eth0: Mengarah ke A13
      - IP pada interface MOJOKERTO
          
          ![int_mjk](img/mojokerto.png)
          
          Keterangan:
          - eth0: Mengarah ke SURABAYA
      - IP pada interface MALANG
          
          ![int_mlg](img/malang.png)
          
          Keterangan:
          - eth0: Mengarah ke KEDIRI
  3. Melakukan routing dengan membuat file route.sh pada setiap Router.
      - SURABAYA
          
          ![sby_route](img/surabayaroute.png)
          
          Keterangan:
          - routing pertama adalah routing ke D1
          - routing kedua adalah routing ke D2
          - routing ketiga adalah routing ke MALANG
      - PASURUAN
          
          ![pas_route](img/pasuruanroute.png)
          
          Keterangan:
          - routing ke B2
      - BATU
          
          ![batu_route](img/baturoute.png)
          
          Keterangan:
          - routing pertama adalah routing ke B1
          - routing kedua adalah routing ke A9
          - routing ketiga adalah routing ke MALANG
      - KEDIRI
          
          ![kdr_route](img/kediriroute.png)
          
          Keterangan:
          - routing ke A12
