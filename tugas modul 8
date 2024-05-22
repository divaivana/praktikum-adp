import os

NAMA_FILE = "Data_keuangan.txt"

def baca_data():
    with open(NAMA_FILE, "r") as file:
        lines = file.readlines()
    transaksi = []
    for line in lines:
        tanggal, keterangan, jumlah, tipe = line.strip().split(",")
        transaksi.append({
            "tanggal": tanggal,
            "keterangan": keterangan,
            "jumlah": jumlah,
            "tipe": tipe
        })
    return transaksi

def tulis_data(transaksi):
    with open(NAMA_FILE, "w") as file:
        for t in transaksi:
            file.write(f"{t['tanggal']},{t['keterangan']},{t['jumlah']},{t['tipe']}\n")

def tambah_transaksi(tanggal, keterangan, jumlah, tipe):
    transaksi = baca_data()
    transaksi.append({
        "tanggal": tanggal,
        "keterangan": keterangan,
        "jumlah": jumlah,
        "tipe": tipe
    })
    tulis_data(transaksi)
    print("Data transaksi telah ditambahkan.")

def hapus_transaksi(tanggal):
    transaksi = baca_data()
    transaksi = [t for t in transaksi if t["tanggal"] != tanggal]
    tulis_data(transaksi)
    print("Data transaksi telah dihapus.")

def tampilkan_transaksi():
    transaksi = baca_data()
    if not transaksi:
        print("Tidak ada data transaksi.")
        return
    print(f"{'Tanggal':<12} {'Keterangan':<30} {'Jumlah':<15} {'Tipe':<15}")
    print("-" * 75)
    for t in transaksi:
        print(f"{t['tanggal']:<12} {t['keterangan']:<30} {t['jumlah']:<15} {t['tipe']:<15}")

while True:
    print("\nMenu:")
    print("1. Tambah Transaksi")
    print("2. Hapus Transaksi")
    print("3. Tampilkan Transaksi")
    print("4. Keluar")
    pilihan = input("Pilih menu (1-4): ")

    if pilihan == '1':
        tanggal = input("Masukkan tanggal transaksi (YYYY-MM-DD): ")
        keterangan = input("Masukkan keterangan transaksi: ")
        jumlah = input("Masukkan jumlah transaksi: ")
        tipe = input("Masukkan tipe transaksi (pemasukan/pengeluaran): ")
        tambah_transaksi(tanggal, keterangan, jumlah, tipe)
    elif pilihan == '2':
        tanggal = input("Masukkan tanggal transaksi yang ingin dihapus (YYYY-MM-DD): ")
        hapus_transaksi(tanggal)
    elif pilihan == '3':
        tampilkan_transaksi()
    elif pilihan == '4':
        break
    else:
        print("Pilihan tidak valid. Silakan coba lagi.")
