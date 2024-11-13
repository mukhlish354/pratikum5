## Program Input Nilai
```python
def hitung_nilai_akhir(nilai_tugas_values, nilai_uts_values, nilai_uas_values ):
    nilai_akhir = (nilai_tugas_values * 0.30) + (nilai_uts_values *0.35) + (nilai_uas_values *0.35)
    return round(nilai_akhir, 2)  # Membulatkan hasil ke dua tempat desimal

# Hasil untuk menyimpan data
nama = []
nim = []
nilai_tugas = []
nilai_uts = []
nilai_uas = []
nilai_akhir_values = []

while True:
    # input data mahasiswa 
    nama_values = input ("Nama: ")
    nim_values = input ("NIM: ")
    try:
        nilai_tugas_values = float(input("Nilai Tugas: "))
        nilai_uts_values = float(input("Nilai UTS: "))
        nilai_uas_values = float(input("Nilai UAS: "))
    except ValueError:
        print("Masukkan nilai dengan format yang benar (angka). Coba lagi.")
        continue

    #Hitung nilai akhir
    nilai_akhir = hitung_nilai_akhir(nilai_tugas_values, nilai_uts_values, nilai_uas_values)

    # Simpan data 
    nama.append(nama_values)
    nim.append(nim_values)
    nilai_tugas.append(nilai_tugas_values)
    nilai_uts.append(nilai_uts_values)
    nilai_uas.append(nilai_uas_values)
    nilai_akhir_values.append(nilai_akhir)

    # Tanya apakah ingin menambah data lagi 
    tambah_data = input("Apakah anda ingin menambah data lagi? (y/t): ")
    if tambah_data == 't':
        break

# Output daftar mahasiswa
print("\nDaftar Mahasiswa: ")
print(f"{'Nama':<20} | {'NIM':<10} | {'Tugas':<10} | {'UTS':<10} | {'UAS':<10} | {'Nilai Akhir':<10}")
print("=" *80)

# Menampilkan semua data yang sudah dimasukkan 
for i in range(len(nama)):
    print(f"{nama[i]:<20} {nim[i]:<13} {nilai_tugas[i]:<11} {nilai_uts[i]:<13} {nilai_uas[i]:<13} {nilai_akhir_values[i]:<10}")
```
## Hasil 
```
Nama: Aziz
NIM: 312410080
Nilai Tugas: 100
Nilai UTS: 95
Nilai UAS: 85
Apakah anda ingin menambah data lagi? (y/t): t

Daftar Mahasiswa:
Nama                 | NIM        | Tugas      | UTS        | UAS        | Nilai Akhir     
================================================================================
Aziz                 312410080     100.0       95.0          85.0          93.0
```
# Penjelasan Program
1. Fungsi hitung_nilai_akhir()
- Fungsi ini bertugas untuk menghitung nilai akhir mahasiswa berdasarkan kontribusi masing-masing nilai:
   - Nilai Tugas memiliki bobot 30%.
   - Nilai UTS memiliki bobot 35%.
    - Nilai UAS memiliki bobot 35%.
- Hasil perhitungan nilai akhir kemudian dibulatkan hingga dua angka desimal menggunakan round(nilai_akhir, 2).
2. List untuk Menyimpan 
- Ini adalah list (daftar) yang akan digunakan untuk menyimpan data mahasiswa. Setiap list ini akan menyimpan data terkait dengan mahasiswa:
  - nama: Daftar nama mahasiswa.
  - nim: Daftar NIM mahasiswa.
  - nilai_tugas: Daftar nilai tugas mahasiswa.
  - nilai_uts: Daftar nilai UTS mahasiswa.
  - nilai_uas: Daftar nilai UAS mahasiswa.
  - nilai_akhir_values: Daftar nilai akhir mahasiswa setelah dihitung.
3. Input Data Mahasiswa (Looping dengan while True)
  - Program ini menggunakan loop while True, yang berarti program akan terus meminta input data mahasiswa hingga pengguna memutuskan untuk berhenti.
  - Pengguna diminta untuk menginput Nama, NIM, Nilai Tugas, Nilai UTS, dan Nilai UAS.
  - Validasi Input: Dengan menggunakan try-except, jika nilai yang dimasukkan untuk Nilai Tugas, Nilai UTS, atau Nilai UAS bukan angka (misalnya teks), program akan menampilkan pesan kesalahan dan meminta input 
    ulang.
4. Perhitungan Nilai Akhir
  - Fungsi hitung_nilai_akhir() dipanggil dengan parameter yang diinput oleh pengguna untuk menghitung nilai akhir mahasiswa.    
5. Menyimpan Data
  - Data yang dimasukkan (nama, NIM, nilai tugas, UTS, UAS, dan nilai akhir) disimpan ke dalam list yang telah dideklarasikan sebelumnya.
  - Setiap data mahasiswa ditambahkan ke dalam list dengan menggunakan metode.append().

## Flowchart




   
