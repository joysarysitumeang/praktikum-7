
## praktikum-7
```
## program sederhana menampilkan daftar nilai mahasiswa

```python
class Mahasiswa:
    def __init__(self):
        self.data = []

    def tambah(self, nama, nilai):
        self.data.append({"nama": nama, "nilai": nilai})
        print(f"Data '{nama}' berhasil ditambahkan.")

    def tampilkan(self):
        if not self.data:
            print("Tidak ada data mahasiswa.")
        else:
            print("\nDaftar Nilai Mahasiswa:")
            for mhs in self.data:
                print(f"Nama: {mhs['nama']}, Nilai: {mhs['nilai']}")

    def hapus(self, nama):
        for mhs in self.data:
            if mhs["nama"].lower() == nama.lower():
                self.data.remove(mhs)
                print(f"Data '{nama}' berhasil dihapus.")
                return
        print(f"Data dengan nama '{nama}' tidak ditemukan.")

    def ubah(self, nama, nilai_baru):
        for mhs in self.data:
            if mhs["nama"].lower() == nama.lower():
                mhs["nilai"] = nilai_baru
                print(f"Data '{nama}' berhasil diubah.")
                return
        print(f"Data dengan nama '{nama}' tidak ditemukan.")


# Program Utama (Opsional)
m = Mahasiswa()

while True:
    print("\n=== MENU ===")
    print("1. Tambah Data")
    print("2. Tampilkan Data")
    print("3. Hapus Data")
    print("4. Ubah Data")
    print("5. Keluar")

    pilihan = input("Pilih menu: ")

    if pilihan == "1":
        nama = input("Masukkan nama: ")
        nilai = input("Masukkan nilai: ")
        m.tambah(nama, nilai)

    elif pilihan == "2":
        m.tampilkan()

    elif pilihan == "3":
        nama = input("Nama yang ingin dihapus: ")
        m.hapus(nama)

    elif pilihan == "4":
        nama = input("Nama yang ingin diubah: ")
        nilai_baru = input("Nilai baru: ")
        m.ubah(nama, nilai_baru)

    elif pilihan == "5":
        print("Program selesai.")
        break
```
## penjelasan

PENJELASAN PROGRAM

Program ini dibuat untuk mengelola daftar nilai mahasiswa menggunakan konsep OOP (Object-Oriented Programming) pada bahasa pemrograman Python. Program memiliki satu class utama bernama Mahasiswa, yang bertugas mengatur seluruh proses penambahan, penampilan, penghapusan, dan pengubahan data mahasiswa

1. Class Mahasiswa

Class ini berfungsi sebagai tempat penyimpanan data dan menyediakan method untuk mengelola data mahasiswa.

Atribut:

data
Tipe: list
Digunakan untuk menyimpan seluruh data mahasiswa. Data disimpan dalam bentuk dictionary.
2. Penjelasan Method

a. tambah(nama, nilai)

Digunakan untuk menambahkan data baru ke dalam list.
Ketika method ini dipanggil, sistem akan membuat sebuah dictionary berisi nama dan nilai, lalu menambahkannya ke list data.

Fungsi:

Menambah mahasiswa baru

Menyimpan nilai mahasiswa

b. tampilkan()

Digunakan untuk menampilkan seluruh data mahasiswa yang tersimpan.

Jika list kosong, program akan menampilkan pesan bahwa data tidak tersedia.
Jika ada data, program akan mencetak daftar nama dan nilai mahasiswa satu per satu.

Fungsi:

Melihat seluruh data mahasiswa

c. hapus(nama)

Method ini berfungsi untuk menghapus data mahasiswa berdasarkan nama yang dicari.

Program akan mencari data dengan nama yang cocok (case-insensitive).
Jika ditemukan, data akan dihapus.
Jika tidak ditemukan, program akan memberi pesan bahwa data tidak ada.

Fungsi:

Menghapus data mahasiswa tertentu

d. ubah(nama, nilai_baru)

Fungsinya untuk mengubah nilai mahasiswa berdasarkan nama.

Program akan mencari mahasiswa dengan nama tertentu, lalu mengganti nilai lamanya menjadi nilai baru.

Fungsi:

Mengubah nilai mahasiswa

Memperbarui data yang salah atau ingin diganti

## diagram class
```

+--------------------------------------------------+
|                   Mahasiswa                      |
+--------------------------------------------------+
| - data: list                                     |
+--------------------------------------------------+
| + tambah(nama: string, nilai: int) : void        |
| + tampilkan() : void                             |
| + hapus(nama: string) : void                     |
| + ubah(nama: string, nilai_baru: int) : void     |
+--------------------------------------------------+

```
## penjelasan

Penjelasan singkat:

data → menyimpan list mahasiswa dalam bentuk dictionary {"nama": ..., "nilai": ...}

tambah() → menambahkan data mahasiswa

tampilkan() → menampilkan seluruh data

hapus() → menghapus data berdasarkan nama

ubah() → mengubah nilai berdasarkan nama

## flowchart
```

                 +----------------------+
                 |      Mulai Program   |
                 +----------+-----------+
                            |
                    +-------v--------+
                    |  Tampilkan     |
                    |     Menu       |
                    +-------+--------+
                            |
                     +------v-----+
                     | Input User |
                     +------+-----+
                            |
          ---------------------------------------------------
          |                    |                  |         |
     +----v----+         +-----v-----+      +-----v-----+  +-----v-----+
     | Tambah  |         | Tampilkan |      |   Hapus   |  |   Ubah    |
     +----+----+         +-----+-----+      +-----+-----+  +-----+-----+
          |                    |                  |             |
          +---------+----------+------------------+-------------+
                            |
                    +-------v-------+
                    | Keluar? (5)   |
                    +-------+-------+
                            |
                       +----v----+
                       | Selesai |
                       +---------+
```
## HASIL
<img width="1918" height="1078" alt="Screenshot 2025-12-06 192232" src="https://github.com/user-attachments/assets/8dd37f48-c75f-4fb4-973c-fdad5477969d" />
<img width="1917" height="477" alt="Screenshot 2025-12-06 192253" src="https://github.com/user-attachments/assets/500001a7-96b3-465a-8273-dccb88f31f4b" />
<img width="1919" height="407" alt="Screenshot 2025-12-06 192313" src="https://github.com/user-attachments/assets/cf882482-f5b3-437c-b13d-9cc12e56e740" />
<img width="1918" height="1074" alt="Screenshot 2025-12-06 192419" src="https://github.com/user-attachments/assets/75ff1011-f962-46a8-9a78-62ba93427d0d" />






