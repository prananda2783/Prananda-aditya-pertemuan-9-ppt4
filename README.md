## Program Data Mahasiswa
<hr>

Pada pertemuan-9 ini saya dari kelas TI.A.1 diberikan tugas oleh Dosen untuk menginput data kedalam list.
Beserta
[flowchart](fc/flowerchat-dikonversi.pdf) dan contoh tugas yang di berikan pada pertemuan-9 <br>

![P-4](ss/ss%20ppt%204.jpg)

<hr>


### Berikut inputannya :
<hr>
''' python
nilai = []
ulang = True

while ulang
    nama = input ("Masukan nama:")
    nim = input ("masukan NIM:")
    tugas = INT(input("masukan nilai tugas:"))
    uts = int(input("masukan nilai UTS:"))
    uas = int(input("Masukkan Nilai UAS: "))
    akhir = (tugas * 30/100) + (uts * 35/100) + (uas * 35/100)

    nilai.append([nama, nim, tugas, uts, uas, int(akhir)])
    if (input("Tambah data (y/t)?") == 't'):
        ulang = False

print("\n                      Daftar Nilai Mahasiswa")
print("==================================================================")
print("|No. |     Nama     |    NIM    | Tugas |  UTS  |  UAS  |  Akhir |")
print("==================================================================")
i = 0
for item in nilai:
    i += 1
    print("| {no:2d} | {nama:12s} | {nim:9s} | {tugas:5d} | {uts:5d} | {uas:5d} | {akhir:6.2f} |"
          .format(no=i, nama=item[0], nim=item[1], tugas=item[2], uts=item[3], uas=item[4], akhir=item[5]))
print("==================================================================")
```
#### Penjelasan:
1.) Pertama kita membuat variable list kosong.
''''Python
nilai = []
ulang = True
''''
>Variable ulang = True digunakan untuk mengontrol perulangan

2.) Lalu kita membuat kondisi perulangan dan statement yang akan dijalankan ketika perulangan terjadi.
```` python
while ulang:
    nama = input("Masukkan Nama: ")
    nim = input("Masukkan NIM: ")
    tugas = int(input("Masukkan Nilai Tugas: "))
    uts = int(input("Masukkan Nilai UTS: "))
    uas = int(input("Masukkan Nilai UTS: "))
    akhir = (tugas * 30/100) + (uts * 35/100) + (uas * 35/100)

    nilai.append([nama, nim, tugas, uts, uas, int(akhir)])
````
 >Dari statement diatas, kita akan diminta untuk menginput nama, nim, nilai tugas, nilai uts, dan nilai uas, lalu system akan menjumlahkan nilai-nilai tersebut dan menghasilkan nilai akhir.
Setelah menginput berbagai data atau item, inputan item tersebut akan masuk ke dalam list 'nilai'

3.) Setelah membuat perulangan, kita membuat statement untuk menghentikan atau keluar dari perulangan yang terjadi.
```` python
    if (input("Tambah data (y/t)?") == 't'):
        ulang = False
````
>Untuk keluar dari perulangan kita hanya perlu menginputkan *t* apabila diminta pada saat program dijalankan.
*t* akan membuat variable ulang = True menjadi ulang = False yang mana akan menghentikan perulangan yang terjadi.

4.) Terakhir kita akan mencetak hasil dari program yang telah dibuat.
```` python
print("\n                      Daftar Nilai Mahasiswa")
print("==================================================================")
print("|No. |     Nama     |    NIM    | Tugas |  UTS  |  UAS  |  Akhir |")
print("==================================================================")
i = 0
for item in nilai:
    i += 1
    print("| {no:2d} | {nama:12s} | {nim:9s} | {tugas:5d} | {uts:5d} | {uas:5d} | {akhir:6.2f} |"
          .format(no=i, nama=item[0], nim=item[1], tugas=item[2], uts=item[3], uas=item[4], akhir=item[5]))
print("==================================================================")
````
Berikut hasil dari program data mahasiswa 
![HASIL](ss/nilai%20ppt4.jpg)
