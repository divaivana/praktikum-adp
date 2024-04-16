print("TUGAS MODUL 5 SHIFT 4")
print("NAMA  : DIVA IVANA")
print("NIM   : 2310432036")
print("==============================")

def input_array():
    while True:
        try:
            array = list(map(int, input("Masukkan array (bilangan bulat 0-9 dipisahkan oleh spasi): ").split()))
            if all(0 <= num <= 9 for num in array):
                return array
            else:
                print("Mohon masukkan bilangan bulat antara 0 sampai 9 saja.")
        except ValueError:
            print("Mohon masukkan bilangan bulat saja.")

def main():
    print("Masukkan array pertama:")
    array_a = input_array()
    
    print("Masukkan array kedua:")
    array_b = input_array()
    
    unique_a = list(set(array_a) - set(array_b))
    unique_b = list(set(array_b) - set(array_a))
    common = list(set(array_a) & set(array_b))
    
    print("Elemen yang hanya berada di array pertama:", unique_a)
    print("Elemen yang hanya berada di array kedua:", unique_b)
    print("Elemen yang berada di kedua array:", common)

if __name__ == "__main__":
    main()
