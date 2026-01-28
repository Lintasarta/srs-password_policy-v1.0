# Functional Requirement

*Tabel 1. Functional Requirement*

| ID       | Keterangan |
|----------|------------|
| PP-SA-01 | Sistem mencatat tanggal terakhir kali pengguna mengganti password. |
| PP-SA-02 | Sistem akan secara otomatis menghitung selisih hari sejak terakhir kali pengguna mengganti kata sandi; bila hari ini sudah memasuki periode tujuh hari terakhir masa hidup password—yaitu mulai hari ke-83 setelah pergantian hingga hari ke-89—maka setiap hari sistem mengirimkan e-mail pengingat kepada pengguna. Dengan demikian, selama rentang waktu tersebut pengguna akan menerima satu pesan per hari yang memberitahukan sisa hari hingga password kedaluwarsa, sehingga ia memiliki kesempatan yang cukup untuk memperbarui kata sandi sebelum aksesnya diblokir pada hari ke-90. |
| PP-SA-03 | Reminder dikirim selama 7 hari berturut-turut (dari hari ke-84 hingga ke-90). |
| PP-SA-04 | Pada saat (Tanggal ganti terakhir + 90 hari), password akan **kadaluarsa** dan pengguna wajib melakukan reset sebelum dapat login kembali. |
| PP-SA-05 | Setelah pengguna berhasil mengubah password (via halaman “Ganti Password”), kirim e-mail konfirmasi berhasil ganti password. |
| PP-SA-06 | Semua e-mail (reminder & konfirmasi) menggunakan template email Layanan Portal Portal Cloudeka. |
