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
  1.

## CIDR
### Subnetting
  1. Menentukan subnet yang ada dalam topologi dan melakukan labelling netmask terhadap masing-masing subnet. Hasilnya ada pada gambar berikut.
      ![cidr_subnet](img/cidr_subnet.jpg)
  2. Dari proses penggabungan yang telah dilakukan, didapatkan sebuah subnet besar yang memiliki NID 192.168.0.0 dengan netmask /16.
  3. Selanjutnya menghitung pembagian IP dengan pohon berdasarkan penggabungan subnet yang telah dilakukan.
      ![cidr_tree](img/cidr_tree.jpg)

### Praktik pada UML
  1.
