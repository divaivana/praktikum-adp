import os

NAMA_FILE = "Data_belanja.txt"

def baca_data():
    with open(NAMA_FILE, "r") as file:
        lines = file.readlines()
    belanja = []
    for line in lines:
        nama_barang, jumlah, harga, total = line.strip().split(",")
        belanja.append({
            "nama_barang": nama_barang,
            "jumlah": jumlah,
            "harga": harga,
            "total": total
        })
    return belanja

def tulis_data(belanja):
    with open(NAMA_FILE, "w") as file:
        for b in belanja:
            file.write(f"{b['nama_barang']},{b['jumlah']},{b['harga']},{b['total']}\n")

def tambah_belanja(nama_barang, jumlah, harga):
    belanja = baca_data()
    total = jumlah * harga
    belanja.append({
        "nama_barang": nama_barang,
        "jumlah": jumlah,
        "harga": harga,
        "total": total
    })
    tulis_data(belanja)
    print("Data belanja telah ditambahkan.")

def tampilkan_belanja():
    belanja = baca_data()
    if not belanja:
        print("Tidak ada data belanja.")
        return
    print(f"{'Nama Barang':<20} {'Jumlah':<15} {'Harga':<15} {'Total':<15}")
    print("-" * 70)
    for b in belanja:
        print(f"{b['nama_barang']:<20} {b['jumlah']:<15} {b['harga']:<15} {b['total']:<15}")

while True:
    print("\nMenu:")
    print("1. Tambah Belanja")
    print("2. Tampilkan Belanja")
    print("3. Keluar")
    pilihan = input("Pilih menu (1-3): ")

    if pilihan == '1':
        nama_barang = input("Masukkan nama barang: ")
        jumlah = input("Masukkan jumlah barang: ")
        harga = input("Masukkan harga barang: ")
        tambah_belanja(nama_barang, jumlah, harga)
    elif pilihan == '2':
        tampilkan_belanja()
    elif pilihan == '3':
        break
    else:
        print("Pilihan tidak valid. Silakan coba lagi.")
