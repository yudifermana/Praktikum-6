# Praktikum-5

# NAMA : Yudi fermana

# NIM : 312210321

# Kelas : TI.22.A.3

Tugas membuat program sederhana

![ppp](https://user-images.githubusercontent.com/115516653/204179408-d1632219-efff-46f5-a6ec-a197c9ffab0e.jpeg)

Agar dipermudah buat flowchart terlebih dahulu

![pppp](https://user-images.githubusercontent.com/115516653/204179509-ae6eabc3-4e16-4054-9d06-fe879acbaf6f.png)

# Berikut adalah penjelasan dari program nya

- Penggunaan while True

    while True berfungsi untuk mendeteksi jika format yang diinputkan bukan berupa type maka akan muncul error
    
- Saya membuat looping agar program terus berjalan

```python
    while True:
    c = input("\n(L)ihat, (T)ambah, (U)bah, (H)apus, (C)ari, (K)eluar: ")
```

- Penggunaan if c.lower()

    if c.lower() fungsinya apabila user menginputkan denga huruf besar, maka otomatis akan menjadi huruf kecil sehingga kondisi yang digunakan tercapai

- Lalu saya membuat format if untuk memasukkan pilihan, sebagai contoh apabila memilih (t) akan menambah data
```python
    if (c.lower() == 't'):
        print('\nTambah Data Mahasiswa Baru')
        nama= input("Masukkan Nama\t\t: ")
        nim= input("Masukkan NIM\t\t: ")
        nilaiTugas= int(input("Masukkan Nilai Tugas\t: "))
        nilaiUts= int(input("Masukkan Nilai UTS\t: "))
        nilaiUas= int(input("Masukkan Nilai UAS\t: "))
        nilaiAkhir= (0.30 * nilaiTugas) + (0.35 * nilaiUts) + (0.35 * nilaiUas)
        dataMhs[nama]= nim, nilaiTugas, nilaiUts, nilaiUas, nilaiAkhir
        print("\nData Berhasil Ditambahkan!")
```

- Saya juga melakukan percabangan if (elif) untuk melaksanakan pilihan yang lain
- Berikut program untuk mengubah data

```python
    elif (c.lower() == 'u'):
        print('\nMengedit Data Mahasiswa')
        nama = input("Masukkan Nama: ")
        if nama in dataMhs.keys():
            nim= input("Masukkan NIM Baru\t: ")
            nilaiTugas= int(input("Masukkan Nilai Tugas\t: "))
            nilaiUts= int(input("Masukkan Nilai UTS\t: "))
            nilaiUas= int(input("Masukkan Nilai UAS\t: "))
            nilaiAkhir= (0.30 * nilaiTugas) + (0.35 * nilaiUts) + (0.35 * nilaiUas)
            dataMhs[nama] = nim, nilaiTugas, nilaiUts, nilaiUas, nilaiAkhir
            print("\nData Berhasil Di Update!")
        else:
            print("Data tidak ditemukan!")
```            

- Berikut program untuk mencari data
            
```python
    elif (c.lower() == 'c'):
        print('\nCari Data Mahasiswa')
        nama = input("Masukan Nama:  ")
        if nama in dataMhs.keys():
            print("\n                   DAFTAR NILAI MAHASISWA                   ")
            print("==============================================================")
            print("|     Nama     |    NIM    | Tugas |  UTS  |  UAS  |  Akhir |")
            print("==============================================================")
            print("| {0:12s} | {1:9s} | {2:5} | {3:5} | {4:5} | {5:6} |".format(nama, nim, nilaiTugas, nilaiUts, nilaiUas, nilaiAkhir))
            print("==============================================================")
        else:
            print("Datanya {0} Tidak Ada ".format(nama))
```

- Berikut program untuk menghapus data

```python
    elif (c.lower() == 'h'):
        nama = input("Masukkan Nama:  ")
        if nama in dataMhs.keys():
            del dataMhs[nama]
            print("Data Telah dihapus!")
        else:
            print("Data Mahasiswa Tidak Ada".format(nama))
```

- Berikut program untuk melihat data

```python
    elif (c.lower() == 'l'):
        if dataMhs.items():
            print("\n                      DAFTAR NILAI MAHASISWA                    ")
            print("==================================================================")
            print("| No |     Nama     |    NIM    | Tugas |  UTS  |  UAS  |  Akhir |")
            print("==================================================================")
            i = 0
            for x in dataMhs.items():
                i += 1
                print("| {6:2} | {0:12s} | {1:9s} | {2:5} | {3:5} | {4:5} | {5:6} |".format(x[0], x[1][0], x[1][1], x[1][2], x[1][3], x[1][4], i))
            print("==================================================================")
        else:
            print("\n                      DAFTAR NILAI MAHASISWA                    ")
            print("==================================================================")
            print("| No |     Nama     |    NIM    | Tugas |  UTS  |  UAS  |  Akhir |")
            print("==================================================================")
            print("|                          TIDAK ADA DATA!                       |")
            print("==================================================================")
```

- Berikut program untuk keluar dari program

```python
    elif (c.lower() == 'k'):
        print('\n')
        print(21*'=')
        print("Nama\t: yudi fermana\nKelas\t: TI.22.A3\nNIM\t: 312210321")
        print(21*'=')
        break
```

- Dan saya juga menggunakan else yang digunakan apabila salah memasukkan pilihan inputan
```python
    else:
        print("Pilih menu yang tersedia: ")
        
        
  Sekian penjelasan yang saya sampaikan Terima kasih
