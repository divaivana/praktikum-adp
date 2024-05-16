def hitung_glbb(n):
    data_glbb = []
    for i in range(n):
        kecepatan_awal = float(input(f"Masukkan kecepatan awal untuk data ke-{i+1}: "))
        percepatan = float(input(f"Masukkan percepatan untuk data ke-{i+1}: "))
        waktu = float(input(f"Masukkan waktu untuk data ke-{i+1}: "))
        
        kecepatan_akhir = kecepatan_awal + (percepatan * waktu)
        jarak = kecepatan_awal * waktu + 0.5 * percepatan * waktu ** 2
        
        data_glbb.append([kecepatan_awal, percepatan, waktu, kecepatan_akhir, jarak])
    
    print("\n-------------------------------------------------------------------------")
    print("| No | Kecepatan Awal | Percepatan | Waktu | Kecepatan Akhir | Jarak    |")
    print("-------------------------------------------------------------------------")
    
    for i in range(n):
        data = data_glbb[i]
        print(f"| {i+1:^2} | {data[0]:^14.2f} | {data[1]:^10.2f} | {data[2]:^5.2f} | {data[3]:^15.2f} | {data[4]:^6.2f} |")
    
    print("-------------------------------------------------------------------------")

jumlah_data = int(input("Masukkan jumlah data GLBB: "))
hitung_glbb(jumlah_data)
