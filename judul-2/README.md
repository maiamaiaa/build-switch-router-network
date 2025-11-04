# build-switch-router-network
Youtube Link : https://youtu.be/IdQRE3cnS_c

🧩 Hasil Pengujian Jaringan

🔹 Sebelum Dilakukan Konfigurasi

![WhatsApp Image 2025-11-04 at 01 42 30_85ea7aae](https://github.com/user-attachments/assets/7c962c48-552c-4783-89d5-c763f29ba89b)

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
