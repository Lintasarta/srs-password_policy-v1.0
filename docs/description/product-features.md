# Product Features

Berikut fitur produk yang tersedia diantaranya sebagai berikut:

- **Password Expiration Enforcement**  
  Sistem otomatis menandai password sebagai kedaluwarsa setelah 90 hari sejak terakhir kali diubah.

- **Automated Reminder Emails**  
  Mulai 7 hari sebelum masa berlaku habis, pengguna menerima email pengingat sekali per hari (hari ke-83 hingga ke-89). Subjek dan isi email dapat menampilkan sisa hari hingga kadaluarsa.

- **Forced Password Reset**  
  Pada hari ke-90, pengguna yang belum mengganti password akan diblokir aksesnya hingga melakukan reset lewat halaman Ganti Password.

- **Confirmation Notification**  
  Segera setelah password berhasil diperbarui, sistem mengirim email konfirmasi dengan detail waktu perubahan dan instruksi jika bukan pemilik akun yang melakukan.

- **Standardized Email Templates**  
  Semua email (reminder & konfirmasi) menggunakan template HTML standar Portal Cloudeka, sehingga tampilan konsisten dan mudah dipelihara.

- **Robust Scheduling & Retry Logic**  
  Penjadwalan diatur lewat cron job/Kubernetes CronJob harian pada pukul 00:00. Pengiriman email yang gagal otomatis dicoba ulang hingga 3× dengan mekanisme exponential back-off.

- **Logging & Monitoring**  
  Setiap pengiriman email dicatat (user ID, timestamp, status success/failure) dalam sistem logging dan dapat dipantau oleh tim operasi. Mendukung integrasi ke dashboard monitoring untuk metrik deliverability dan error rate.
