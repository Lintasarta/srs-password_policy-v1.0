# Product Overview

Modul **Password Policy** pada Portal Cloudeka adalah komponen yang terintegrasi penuh dengan layanan autentikasi dan manajemen akun. Fungsinya untuk:

- **Memantau siklus hidup password** setiap pengguna dengan melacak kapan terakhir kali password diubah.
- **Mengirim pemberitahuan** (reminder) secara otomatis sebelum password kadaluarsa, sehingga pengguna punya cukup waktu untuk mengganti.
- **Memaksa reset password** saat sudah melewati masa aktif agar tidak ada akun yang terus-menerus menggunakan password usang.
- **Mengonfirmasi** kepada pengguna bahwa penggantian password telah sukses melalui email.

Secara teknis, modul ini memanfaatkan scheduler (cron job atau Kubernetes CronJob) untuk menjalankan cek harian, engine template HTML untuk merender email, dan SMTP server untuk pengiriman. Semua aktivitas—mulai dari perhitungan umur password hingga logging status email—dicatat dalam sistem logging terpusat untuk audit dan keperluan troubleshooting.
