print("Tugas Modul 6 Shift 4")
print("Nama : Diva Ivana")
print("Nim : 2310432036")
print("-----------------------------------------------------")

print("Tabel Harga dan Stok Barang")
n = int(input("Masukkan jumlah barang: "))

barang = []
for i in range(n):
    nama = input(f"Nama barang ke-{i+1}: ")
    harga = int(input(f"Harga barang {nama}: "))
    stok = int(input(f"Stok barang {nama}: "))
    barang.append([nama, harga, stok])

print("\n-----------------------------------------------------------")
print("|    Nama    |    Harga   |    Stok    |    Total     |")
print("-----------------------------------------------------------")
total_keuntungan = 0
for data in barang:
    total_barang = data[1] * data[2]
    total_keuntungan += total_barang
    print(f"| {data[0]:^10} | {data[1]:^10} | {data[2]:^10} | {total_barang:^12} |")
print("-----------------------------------------------------------")

keuntungan_per_barang = [[data[0], data[1] * data[2]] for data in barang]

keuntungan_tertinggi = keuntungan_per_barang[0]
keuntungan_terendah = keuntungan_per_barang[0]
for barang_keuntungan in keuntungan_per_barang:
    if barang_keuntungan[1] > keuntungan_tertinggi[1]:
        keuntungan_tertinggi = barang_keuntungan
    if barang_keuntungan[1] < keuntungan_terendah[1]:
        keuntungan_terendah = barang_keuntungan

print(f"\nNama barang dengan keuntungan tertinggi: {keuntungan_tertinggi[0]}, Total: {keuntungan_tertinggi[1]}")
print(f"Nama barang dengan keuntungan terendah: {keuntungan_terendah[0]}, Total: {keuntungan_terendah[1]}")
print(f"Total keuntungan: {total_keuntungan}")
