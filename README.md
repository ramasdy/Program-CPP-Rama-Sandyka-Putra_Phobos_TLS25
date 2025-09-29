#include <iostream>
using namespace std;

int main() {
    int times[] = {80, 135, 150, 212};
    int durasi[] = {20, 3, 80};   // hijau, kuning, merah
    string warna[] = {"Hijau", "Kuning", "Merah"};

    int cycle = 103;      // total lama siklus
    int offset = 24;      // geser sesuai kondisi awal

    for (int t : times) {
        int pos = (t + offset) % cycle;
        int idx = (pos < durasi[0]) ? 0 :
                  (pos < durasi[0] + durasi[1]) ? 1 : 2;
        cout << "Detik " << t << " -> " << warna[idx] << endl;
    }
    return 0;
}
