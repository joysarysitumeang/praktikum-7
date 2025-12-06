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

    else:
        print("Pilihan tidak valid!")
## hasil

<img width="1918" height="1078" alt="Screenshot 2025-12-06 192232" src="https://github.com/user-attachments/assets/0a76d13c-b7d6-47eb-a6ee-06ceda8a90b8" />
<img width="1917" height="477" alt="Screenshot 2025-12-06 192253" src="https://github.com/user-attachments/assets/90bc0b3b-727d-4748-b795-81f002f8747a" />
<img width="1919" height="407" alt="Screenshot 2025-12-06 192313" src="https://github.com/user-attachments/assets/33d8bcd1-b22f-4bd5-b0fe-941f20227dff" />
<img width="1918" height="1074" alt="Screenshot 2025-12-06 192419" src="https://github.com/user-attachments/assets/74d65112-6aca-4943-88a2-456f34b2f28d" />
