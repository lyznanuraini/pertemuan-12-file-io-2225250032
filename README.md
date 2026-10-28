# Pertemuan 12 File I/O dan Error Handling

## Identitas
- **Nama:** Lyzna Nuraini
- **NIM:** 2225250032
- **Kelas:** 3E

## Tujuan
Membaca, memvalidasi, mengolah, dan menulis data file dengan Python[cite: 13].

## Format File Input
NIM, nilai[cite: 13]

## Cara Menjalankan
```bash
python3 tugas/rekap_nilai_file.py
```[cite: 13]

## Error yang Ditangani
- `FileNotFoundError`[cite: 13]
- `ValueError`[cite: 13]

## Test Case
| Kondisi | Kondisi Input | Hasil yang Diharapkan | Status |
| :--- | :--- | :--- | :--- |
| **Normal** | Semua baris valid | Semua record diproses dan rekap benar.[cite: 12] | Berhasil |
| **File hilang** | `nilai.txt` tidak tersedia | Pesan file tidak ditemukan; program tidak crash.[cite: 12] | Berhasil |
| **Nilai invalid** | A004,abc | Baris invalid dilewati/dilaporkan; record lain tetap diproses.[cite: 12] | Berhasil |
| **Baris kosong** | Ada baris kosong | Baris kosong dilewati.[cite: 12] | Berhasil |
| **Batas lulus** | Nilai 60 | Dihitung sebagai lulus.[cite: 12] | Berhasil |

## Refleksi
Error yang sering diantisipasi adalah `ValueError` ketika data numerik pada file input berisi teks atau format yang salah. Dengan menerapkan blok `try-except` spesifik di setiap baris, program dapat melewati data yang tidak valid dengan aman tanpa menghentikan proses rekapitulasi data valid lainnya.
