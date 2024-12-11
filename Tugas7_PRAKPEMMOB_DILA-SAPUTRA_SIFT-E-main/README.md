Nama: Mochamad Azizan
NIM: H1D022046
Shift baru: E
Shift lama: B
Screenshoot bukti
![image](https://github.com/user-attachments/assets/edadef27-efef-45a0-8eea-3a948c437ea0)
![image](https://github.com/user-attachments/assets/e531e4af-6541-4237-82c5-0e33169296a9)
![image](https://github.com/user-attachments/assets/26013957-29d2-4819-977c-fd1869f1470d)


Penjelasan source code
Baik, saya akan menjelaskan cara kerja login secara sederhana tanpa source code:

Cara Kerja Login:

1. Tahap Input:
- User memasukkan username dan password pada form login
- Aplikasi melakukan validasi awal untuk memastikan input tidak kosong
- Jika input kosong, tampilkan pesan error

2. Tahap Pengiriman Data:
- Data username dan password dikirim ke server (API)
- Pengiriman menggunakan metode HTTP POST
- Data diformat dalam bentuk JSON

3. Tahap Pemrosesan di Server:
- Server menerima data login
- Password di-hash menggunakan MD5 untuk keamanan
- Server melakukan pengecekan ke database
- Jika data cocok, server membuat token unik
- Server mengirim response berisi status login, token, dan username

4. Tahap Penanganan Response:
- Aplikasi menerima response dari server
- Jika login berhasil:
  * Token dan username disimpan di penyimpanan lokal
  * Status autentikasi diperbarui
  * User diarahkan ke halaman home
- Jika login gagal:
  * Tampilkan pesan error yang sesuai
  * User tetap di halaman login

5. Tahap Penyimpanan Session:
- Token dan username disimpan di storage lokal (Preferences)
- Data ini digunakan untuk:
  * Mengecek status login user
  * Mempertahankan session
  * Mengakses halaman yang membutuhkan autentikasi

6. Pengamanan:
- Password di-hash sebelum disimpan
- Menggunakan token untuk verifikasi
- Ada guard untuk mengamankan routing
- Validasi input untuk mencegah data kosong
- Penanganan CORS di sisi server

7. Fitur Tambahan:
- Auto login jika session masih aktif
- Notifikasi untuk berbagai status login
- Redirect otomatis sesuai status autentikasi
- Logout untuk mengakhiri session

