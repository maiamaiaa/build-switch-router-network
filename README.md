# build-switch-router-network
Praktikum konfigurasi jaringan dasar menggunakan perangkat Cisco. Meliputi pengaturan router, switch, dan dua PC dengan alamat IPv4 dan IPv6, konfigurasi interface, pengamanan akses, serta verifikasi konektivitas antar perangkat.

<img width="1004" height="277" alt="image" src="https://github.com/user-attachments/assets/d310ee44-9aa7-4829-bc3e-76b447f9b3f6" />
🧩 Hasil Pengujian Jaringan
🔹 Sebelum Dilakukan Konfigurasi

Sebelum dilakukan konfigurasi, semua perangkat belum memiliki alamat IP dan interface masih down.
Akibatnya, komunikasi antar perangkat belum bisa dilakukan.
Hasil ping menunjukkan error:
Request timed out.

🔹 Setelah Dilakukan Konfigurasi
Setelah konfigurasi IP, aktivasi interface, dan routing dilakukan, seluruh perangkat dapat saling berkomunikasi.
<img width="1004" height="277" alt="image" src="https://github.com/user-attachments/assets/a0f4937e-8e91-4ba0-b3f4-b7f944ac55d2" />

✅ Ping PC-A ke PC-B
Reply from 192.168.0.3: bytes=32 time<1ms TTL=128
Berhasil — menandakan koneksi antar jaringan IPv4 sudah berjalan.

✅ Ping PC-A ke Router (R1)
Reply from 192.168.1.1: bytes=32 time<1ms TTL=255
Berhasil — gateway aktif dan dapat diakses dari jaringan lokal.

Kesimpulan 
Sebelum dilakukan konfigurasi, semua perangkat seperti router, switch, dan PC belum memiliki alamat IP dan interface masih dalam keadaan down, sehingga komunikasi antar perangkat tidak dapat dilakukan dan hasil ping menunjukkan Request timed out karena belum ada jalur pengiriman data. Setelah dilakukan konfigurasi alamat IP, aktivasi interface dengan perintah no shutdown, pengaturan gateway pada PC, serta mengaktifkan routing IPv6 dengan ipv6 unicast-routing, semua perangkat dapat saling berkomunikasi. Ping dari PC-A ke PC-B berhasil karena router sudah meneruskan paket antar jaringan berbeda, ping dari switch (S1) ke PC-B juga berhasil karena switch memiliki default gateway menuju router, dan ping dari PC-A ke router berhasil karena keduanya berada di jaringan yang sama. Hal ini menunjukkan bahwa konfigurasi IP dan routing telah dilakukan dengan benar sehingga seluruh perangkat dapat terhubung dengan baik.
