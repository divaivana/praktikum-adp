print("Praktikum ADP Shift 4 Modul 2")
print("Diva Ivana")
print("2310432035")
print("Selamat datang di Bandara Soekarno Hatta")
a = str(input("Nama anda   :"))
b = str(input("Umur        :"))
c = str(input("Jenis kelamin :"))
print()
print("===========================================================")
print()
print("Mohon pilih kota tujuan anda")
print("1.Malang")
print("2.Yogyakarta")
print("3.Pontianak")
print("4.Palangkaraya")
print()
d = int(input("Mohon pilih kota tujuan anda (1-4) : "))
print()
print("==========================================================")
print("Pilih menu maskapai untuk keberangkatan anda")
print("1.First Class (Rp.5.000.000)")
print("2.Business Class (Rp.4.000.000)")
print("3.Economy Class (Rp.3.500.000)")
print()
e = int(input("Pilih menu maskapai keberangkatan anda :"))
f = int(input("Berapa jumlah kursi yang anda pesan    :"))
print()
print("Struk pemesanan tiket pesawat : ")
print("===============================================")
print()
print("Nama          :",a)
print("Umur          :",b)
print("Jenis kelamin :",c)
print("-----------------------------------------------")
if (d == 1) :
    print("Kota tujuan : Malang")
elif (d == 2) :
    print("Kota tujuan : Yogyakarta")
elif (d == 3) :
    print("Kota tujuan : Pontianak")
elif (d == 4) :
    print("Kota tujuan : Palangkaraya")
else :
    print("Tidak ada kota tujuan diatas")
    
if (e == 1) :
    harga = 5000000
    print("Jenis maskapai : First Class")
elif (e== 2) :
    harga = 4000000
    print("Jenis maskapai : Business Class")
elif (e == 3) :
    harga = 3500000
    print("Jenis maskapai : Economy Class")
else :
    print ("Tidak ada menu maskapai diatas")
    
if (f > 3) :
    diskon = 0.25*harga
else :
    diskon = 0
    
g = harga*f-diskon
print("Jumlah tiket      :",f)
print("Total harga tiket :",g)
print("Tiket anda berhasil dipesan")
