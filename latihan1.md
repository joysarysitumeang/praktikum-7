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
