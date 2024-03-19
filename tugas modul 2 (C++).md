#include <iostream>
using namespace std;
string a,b,c;
int d,e,f,g,harga,diskon;
int main() {
    cout << "Praktikum ADP Shift 4 Modul 2";
    cout << "\nDiva Ivana";
    cout << "\n2310432036";
    cout << "\n";
    cout << "\nSelamat datang di Bandara Soekarno Hatta";
    cout << "\n============================================================";
    cout << "\nUntuk pembelian tiket mohon isi data diri anda dibawah ini";
    cout << "\nNama anda         : "; cin >> a;
    cout << "Umur anda (tahun) : "; cin >> b;
    cout << "Jenis Kelamin     : "; cin >> c;
    cout << "\n";
    cout << "\n============================================================";
    cout << "\nMohon pilih kota tujuan anda";
    cout << "\n1. Malang";
    cout << "\n2. Yogyakarta";
    cout << "\n3. Pontianak";
    cout << "\n4. Palangkaraya";
    cout << "\nMohon pilih kota tujuan anda (1-4) : "; cin >> d;
    cout << "\n============================================================";
    cout << "\nPilih menu maskapai untuk keberangkatan anda :";
    cout << "\n1. First Class (Rp.5.000.000)"; 
    cout << "\n2. Business Class (RP.4.00.000)"; 
    cout << "\n3. Economy Class (Rp.3.500.000)"; 
    cout << "\n";
    cout << "\nPilih jenis menu maskapai keberangkatan anda : "; cin >> e;
    cout << "Berapa jumlah kursi yang anda pesan : "; cin >> f;
    cout <<"\n";
    cout << "\nStruk pemesanan tiket pesawat :";
    cout << "\n=======================================";
    cout << "\nNama          :"<<a;
    cout << "\nUmur          :"<<b;
    cout << "\nJenis kelamin :"<<c;
    cout << "\n----------------------------------------";
    if (d == 1) {
        cout << "\nKota Tujuan       : Malang";
    } else if (d == 2) {
        cout << "\nKota Tujuan       : Yogyakarta";
    } else if (d == 3) {
        cout << "\nKota Tujuan       : Pontianak";
    } else if (d == 4) { 
        cout << "\nKota Tujuan       : Palangkaraya";
    } else  { 
        cout << "\nTidak ada tujuan diatas";
    }
    if (e == 1) {
        harga = 5000000;
        cout << "\nJenis Maskapai    : First Class";
    } else if (e == 2) {
        harga = 4000000;
        cout << "\nJenis maskapai    : Business Class";
    } else if (e == 3) {
        harga = 3500000;
        cout << "\nJenis maskapai    : Economy Class";
    } else {
        cout << "\nTidak ada menu maskapai";
    }
    if (f > 3) {
        diskon = 0.25*harga;
    } else {
        diskon = 0;
    }
    g = harga*f-diskon;
    cout << "\nJumlah tiket      : "<<f;
    cout << "\nTotal harga tiket : "<<g;
    cout << "\n=================================================================";
    cout << "\nTiket anda berhasil dipesan";
    
    
}
