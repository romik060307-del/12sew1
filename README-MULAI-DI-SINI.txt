OHLI TUNEL / OHLI SOCIAL — FREE SERVER PACK v3.0.0

PAKET INI MENYEDERHANAKAN PEMASANGAN SERVER DI ORACLE CLOUD ALWAYS FREE.

APA YANG SUDAH DISIAPKAN?
- Installer satu perintah untuk Ubuntu 22.04/24.04/26.04.
- Node.js 24 LTS dan systemd untuk restart otomatis.
- PostgreSQL lokal (hanya lokal, tidak dibuka ke internet).
- DuckDNS untuk subdomain gratis dan pembaruan IP otomatis.
- Caddy untuk HTTPS otomatis dan reverse proxy (termasuk WebSocket).
- Folder upload persisten, pemeriksaan kesehatan, dan backup lokal terjadwal.
- Halaman status OHLI sementara agar hostname/HTTPS bisa diuji sebelum backend sosial dipasang.
- Skrip deploy backend dari ZIP.

CARA PALING SINGKAT:
1. Buat VM Ubuntu yang bertanda Always Free di Oracle Cloud. Gunakan ARM A1 hingga maksimum 2 OCPU/12 GB RAM jika tersedia, dan pasang public IPv4.
2. Buat nama DuckDNS gratis, misalnya ohli-social.duckdns.org. Simpan token DuckDNS.
3. Upload folder server/ ke VM, lalu jalankan:
   sudo bash install-one-click.sh
4. Installer akan meminta subdomain dan token DuckDNS, lalu menyiapkan server. Setelah selesai, buka alamat HTTPS yang ditampilkan.

PENTING BANGET:
- File yang tersedia dalam percakapan ini adalah source aplikasi OHLI TUNEL Android, BUKAN source backend OHLI Social. Karena itu paket ini tidak dapat mengaktifkan login, feed, chat, komentar, upload sosial, atau fitur OHLI Social yang belum ada source-nya.
- Installer menyiapkan hosting dan halaman status sementara. Untuk menjalankan OHLI Social yang asli, deploy ZIP backend melalui:
  sudo bash deploy-backend.sh /path/ke/ohli-social-backend.zip
  ZIP backend Node.js harus berisi package.json dengan scripts.start yang benar.
- Jangan mengirim token DuckDNS, password database, atau file /etc/ohli/ohli.env ke siapa pun.
- Server gratis bukan jaminan uptime 100%. Oracle Always Free dapat mengalami kehabisan kapasitas saat pembuatan, maintenance, gangguan jaringan, dan reclamation instance idle. Selalu simpan backup di luar VM.
- Jangan membuat resource yang tidak bertanda Always Free dan jangan upgrade ke Pay As You Go jika target biaya Rp0.
- APK OHLI TUNEL Android di folder optional-android-source bersifat opsional untuk tunnel dari HP. Untuk hosting VPS, APK tidak harus terus hidup dan tidak diperlukan sebagai server utama.

BACA: docs/KEJUJURAN-DAN-BATASAN.txt
