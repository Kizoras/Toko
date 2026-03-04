# Toko 
Proyek ini dibuat sebagai bagian dari tugas mata pelajaran Basis Data yang bertujuan untuk memahami serta mengimplementasikan konsep JOIN pada sistem manajemen basis data (DBMS).

Materi yang dibahas dalam proyek ini meliputi implementasi perintah JOIN pada SQL, yaitu:
- INNER JOIN
- LEFT JOIN
- RIGHT JOIN

## Database
Database yang digunakan adalah Database Toko.

Database ini dibuat untuk mensimulasikan sistem sederhana pengelolaan pelanggan dan pesanan pada sebuah toko. Struktur database dirancang untuk memahami konsep relasi antar tabel serta penerapan JOIN dalam SQL. Berikut kode join tersebut :

<img width="591" height="150" alt="image" src="https://github.com/user-attachments/assets/f7afb2e7-6a95-40c6-9dc3-8cca387d8fc2" /> 

### Struktur Tabel
1. Tabel Pelanggan :

<img width="606" height="126" alt="image" src="https://github.com/user-attachments/assets/2183e7a1-f073-486d-aebf-76b8e20a1c0b" />

Tabel ini berfungsi untuk menyimpan data pelanggan :
- id_pelanggan → primary key
- nama → nama_pelanggan

Dengan data yang dimasukkan :

<img width="578" height="211" alt="image" src="https://github.com/user-attachments/assets/15f73708-6403-4455-836a-b1960626393b" />

Isi tabel pelanggan :

<img width="591" height="263" alt="image" src="https://github.com/user-attachments/assets/994eeb74-77aa-4cad-9bd3-1c5edf846fc7" />


2. Tabel Pesanan :

<img width="622" height="161" alt="image" src="https://github.com/user-attachments/assets/76491c0a-d4ef-4c71-91a4-227f3ab7ec07" />

Tabel ini menyimpan data pesanan pelanggan :
- id_pesanan → primary key
- id_pelanggan → relasi ke tabel pelanggan
- produk → nama produk yang dipesan

  Dengan data yang dimasukkan :
  
<img width="703" height="198" alt="image" src="https://github.com/user-attachments/assets/be8ae3f1-bed4-4c9e-a387-6de70ba3a856" />

Isi tabel pesanan :

<img width="637" height="282" alt="image" src="https://github.com/user-attachments/assets/43ced0e8-e5ba-46db-aba7-8b80e94d9734" />


## Implementasi JOIN
1. INNER JOIN & Hasil

<img width="1103" height="329" alt="image" src="https://github.com/user-attachments/assets/763e410f-016b-469e-9452-6d0bbb5a69e5" />

Penjelasan :
INNER JOIN hanya menampilkan data yang memiliki kecocokan di kedua tabel.
Pelanggan Sari tidak muncul karena tidak memiliki pesanan.

2. LEFT JOIN & Hasil :

<img width="1091" height="360" alt="image" src="https://github.com/user-attachments/assets/589d6a23-ccc5-4545-95cc-fb425603fe1e" />

Penjelasan :
LEFT JOIN menampilkan semua data dari tabel kiri (pelanggan).
Karena Sari tidak memiliki pesanan, maka kolom produk bernilai NULL.

3. RIGHT JOIN & Hasil :

<img width="1093" height="331" alt="image" src="https://github.com/user-attachments/assets/311aa237-e999-466d-9365-2be093dfc978" />

Penjelasan :
RIGHT JOIN menampilkan semua data dari tabel kanan (pesanan).
Karena semua pesanan memiliki pasangan pelanggan, hasilnya sama seperti INNER JOIN.

### Kesimpulan
Dari tugas yang sudah dikerjakan, bisa disimpulkan bahwa perintah JOIN pada SQL berfungsi untuk menggabungkan data dari beberapa tabel yang saling berelasi, yang dimana INNER JOIN menampilkan data yang memiliki kecocokan di kedua tabel, LEFT JOIN menampilkan seluruh data dari tabel kiri meskipun tidak memiliki pasangan di tabel kanan, dan RIGHT JOIN menampilkan seluruh data dari tabel kanan meskipun tidak memiliki pasangan di tabel kiri, sehingga pemahaman JOIN sangat penting dalam pengelolaan database relasional.
