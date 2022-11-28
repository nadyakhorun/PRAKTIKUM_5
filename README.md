#PRAKTIKUM_5

NAMA    : NADYA KHAIRUNNISA

NIM     : 312210133

KELAS   : TI.22.A1

## DAFTAR ISI <br>
| No | Description | Link |
|-----|------|-----|
|1|Latihan|[Click Here](#latihan)|
|2|Praktikum_5|[Click Here](#praktikum_5)|
|3|Flowchart Praktikum_5|[Click Here](#flowchart-praktikum_5)|

## Latihan

Buat Dictionary daftar kontak

Nama sebagai key, dan nomor sebagai value
- Tampilkan kontaknya Ari
- Tambah kontak baru dengan nama Riko, nomor 087654544
- Ubah kontak Dina dengan nomor baru 088999776
- Tampilkan semua Nama
- Tampilkan semua Nomor
- Tampilkan daftar Nama dan nomornya
- Hapus kontak Dina
## Langkah-langkah :

1. Buat program terlebih dahulu seperti gambar di bawah ini
![TUGAS PRAKTIKUM 5 (8)](https://user-images.githubusercontent.com/115801823/204231879-59898201-eb94-4b1a-a991-fde37d245be8.PNG)
![TUGAS PRAKTIKUM 5 (9)](https://user-images.githubusercontent.com/115801823/204232096-0e76da03-ad7f-420e-9e8c-f3283f425236.PNG)

      daftarKontak = {"Nama":"Nomer Telpon"}
      kontak       = {'Ari':'081267888', 'Dina' : '087677776'}

      #print
      print(30*"═")
      print("    Nama    |  Nomor Telepon  ") #prinr daftarkontak
      print(30*"-")
      print("   # Ari    | ", kontak['Ari']) #print kontak Ari
      print("   # Dina   | ", kontak['Dina']) #print kontak Dina
      print(30*"═")

      #Tampilkan kontaknya Ari
      print("Tampilkan kontaknya Ari")
      print("    Ari     | ", kontak['Ari']) #print kontak Ari
      print(30*"═")
      #Tambah kontak baru dengan nama Riko, nomor 087654544
      print("Tambah kontak baru dengan nama Riko, nomor 087654544")
      kontak['Riko'] = '087654544'
      print("    Riko    | ", kontak['Riko'])
      print(30*"═")

      #Ubah kontak Dina dengan nomor baru 088999776
      print("Ubah kontak Dina dengan nomor baru 088999776")
      kontak['Dina'] = '088999776'
      print("    Dina    | ", kontak['Dina'])
      print(30*"═")

      #Tampilkan semua Nama
      print("Tampilkan semua Nama")
      print(kontak.keys())
      print(30*"═")

      #Tampilkan semua Nomor
      print("Tampilkan semua Nomor")
      print(kontak.values())
      print(30*"═")

      #Tampilkan daftar Nama dan nomornya
      print("Tampilkan daftar Nama dan nomornya")
      print(kontak.items())
      print(30*"═")

      #MengHapus kontak Dina
      print("Hapus kontak Dina")
      kontak.pop('Dina')
      print(kontak.items())
      print(30*"═")
2. Hasil RUN
![TUGAS PRAKTIKUM 5 (6)](https://user-images.githubusercontent.com/115801823/204232489-2d4899a8-3a5b-4dd0-8a8a-7befc25704a3.PNG)
![TUGAS PRAKTIKUM 5 (7)](https://user-images.githubusercontent.com/115801823/204232528-3423bb9d-a381-4acc-84cc-dd14ee00bd67.PNG)

## Praktikum 5

Buat program sederhana yang akan menampilkan daftar nilai mahasiswa, dengan ketentuan :

- Program dibuat dengan menggunakan Dictionary
- Tampilkan menu pilihan : (Tambah Data, Ubah Data, Hapus Data, Tampilkan Data, Cari Data)
- Nilai Akhir diambil dari perhitungan 3 komponen nilai (tugas : 30%, UTS : 35%, UAS : 35%)
- Buat flowchart dan penjelasan programnya pada README.md.
- Commit dan push repository ke github.
## Langkah-langkah :

1. Buat programnya terlebih dahulu seperti gambar di bawah ini
![TUGAS PRAKTIKUM 5 (3)](https://user-images.githubusercontent.com/115801823/204233109-43a65c4b-3565-40d5-91cf-046ad5623461.PNG)
![TUGAS PRAKTIKUM 5 (4)](https://user-images.githubusercontent.com/115801823/204233171-fb409986-9447-4741-af35-45107af53307.PNG)
![TUGAS PRAKTIKUM 5 (5)](https://user-images.githubusercontent.com/115801823/204233235-c14f09a9-e863-4af7-9061-2db630f8028b.PNG)

        print("====================================")
        print("======>  Program Input Nilai  <======")
        print("====================================")
        data = {}
        while True:
            print("")
            m = input("===>> (L)ihat, (T)ambah, (U)bah, (H)apus, (C)ari, (K)eluar : <=== ")
            print("================================================================")
            print("| NO |  Nama     |   Nim    |  Tugas  |  UTS  |  UAS  |   Akir |")
            print("================================================================")
            print(">>>>>>>>>>>>>>>>>>>>>>>> TIDAK ADA DATA <<<<<<<<<<<<<<<<<<<<<<<<")
            if m.lower() == 'k':
                break

            elif m.lower() == 'l':
                print("----- DAFTAR NILAI -----")
                print("==================================================================================")
                print("| NO |   NAMA     |   NIM        |  TUGAS   |   UTS     |   UAS      |  AKHIR    |")
                print("==================================================================================")
                i = 0
                for x in data.items():
                    i += 1
                    print("|  1 |{0:9}   |{1:9}     |{2:9} |{3:9}  |{4:9}   |{5:9}  |" .format(x[0], x[1][0],
                                                                                               x[1][1], x[1][2], x[1][3],
                                                                                               x[1][4], i))

                else:
                    print("====================>>>>>>>>>>>>> Tidak Ada Data <<<<<<<<<<<<<====================")

            elif m.lower() == 't':
                print("--------------- Tambah Data ---------------")
                nama = input("Nama                  : ")
                nim = input("Nim                   : ")
                tugas = float(input("Masukan Nilai Tugas   : "))
                uts = float(input("Masukan Nilai UTS     : "))
                uas = float(input("Masukan Nilai UAS     : "))
                akhir = (int(tugas) * .30) + (int(uts) * .35) + (int(uas) * .35)
                data[nama] = nim, tugas, uts, uas, akhir

            elif m.lower() == 'u':
                print("----- Ubah Data Mahasiswa -----")
                nama = input("Nama  : ")
                if nama in data.keys():
                    nim = input("Nim : ")
                    tugas = float(input("masukan nilai tugas : "))
                    uts = float(input("masukan nilai Uts : "))
                    uas = float(input("masukan nilai uas : "))
                    akhir = (int(tugas) * .30) + (int(uts) * .35) + (int(uas) * .35)
                    data[nama] = nim, tugas, uts, uas, akhir

                else:
                    print("Tidak Ada data")

            elif m.lower() == 'h':
                print("Hapus Data Mahasiswa")
                nama = input("nama : ")
                if nama in data.keys():
                    print("Datanya", nama, "adalah {0}".format(data[nama]))
                else:
                    print("Tidaak Ada Data")

            else:
                print("Pilih menu yang tersedia")
