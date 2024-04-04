#include <iostream>
using namespace std;

int main() { 
    cout << "Praktikum ADP Shift 4 Modul 4";
    cout << "\nDiva Ivana";
    cout << "\n2310432036";
    cout << “\n”;
    int countDOR = 0;
    for (int i = 1; i <= 100; ++i) {
        if (i % 3 == 0 || i % 5 == 0) {
            cout << "DOR ";
            countDOR++;
        } else {
            cout << i << " ";
        }
        if (i % 10 == 0) {
            cout << endl;
        }
    }
    cout << "\nTotal DOR yang muncul sebanyak = " << countDOR << endl;
    return 0;
}
