print ("Tugas Modul 3 Shift 4")
print ("Nama : Diva ivana")
print ("Nim : 2310432036")

nomor = int(input("Masukkan Nomor Huruf pada Piramida (<26) = "))
tot = 1

for i in range(1, nomor+1):
    for j in range(1, nomor-i+1):
        print("  ", end="")
    
    huruf = 'A'
    
    for k in range(i):
        print(huruf, end=" ")
        huruf = chr(ord(huruf) + 1)
    
    huruf = chr(ord(huruf) - 2)
    
    for k in range(i-1):
        print(huruf, end=" ")
        huruf = chr(ord(huruf) - 1)
    
    tot += 2
    
    print()
