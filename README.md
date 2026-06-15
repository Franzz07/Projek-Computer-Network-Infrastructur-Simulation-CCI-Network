# Mid Exam Network Division - Central Computer Improvement (CCI) 🌐

[cite_start]Repositori ini berisi project simulasi jaringan Cisco Packet Tracer yang disusun untuk memenuhi tugas Ujian Tengah Semester (Mid Exam) Divisi Network di Central Computer Improvement (CCI) Telkom University[cite: 1, 2, 3, 4, 7].

## 👥 Anggota Kelompok B
* [cite_start]**Fx Farrel Azalea Immanuel** (103032500025) [cite: 6]
* [cite_start]**Naoki Ilham Aufaa Nugroho** (101012500016) [cite: 6]
* [cite_start]**Abdul Jabbar Hawali Al Dzahabi** (103032400108) [cite: 6]
* [cite_start]**Raiyan Abizar** (102022530074) [cite: 6]

## 📝 Deskripsi Project
[cite_start]Project ini mensimulasikan infrastruktur jaringan berskala menengah dengan membagi jaringan ke dalam beberapa divisi menggunakan arsitektur **VLAN**[cite: 13, 26, 59]. [cite_start]Jaringan ini dikelola oleh 3 Router utama dan 5 Switch, serta mengimplementasikan **Inter-VLAN Routing**, distribusi IP otomatis via **DHCP**, dan **Static Routing** antar router[cite: 242, 298, 461, 563].

## ✨ Fitur Utama & Konfigurasi
1. **VLAN (Virtual Local Area Network)**
   Jaringan diisolasi menjadi beberapa segmen berikut untuk keamanan dan efisiensi manajemen:
   * [cite_start]**VLAN 20 (HRD):** `192.168.11.0/28` [cite: 86, 105]
   * [cite_start]**VLAN 30 (Finance):** `192.168.12.0/28` [cite: 93, 101]
   * [cite_start]**VLAN 40 (Office):** `192.168.13.0/25` [cite: 59, 103]
   * [cite_start]**VLAN 50 (Logistic):** `192.168.14.0/28` [cite: 158, 161, 168]
   * [cite_start]**VLAN 60 (Cafetaria):** `192.168.15.0/25` [cite: 124, 130]
   * [cite_start]**VLAN 70 (Developer):** `192.168.16.0/27` [cite: 13, 36]
   * [cite_start]**VLAN 80 (Lobby):** `192.168.17.0/25` [cite: 141, 142, 170]
   * [cite_start]**VLAN 90 (Server):** `192.168.18.0/29` [cite: 26, 38]

2. **Inter-VLAN Routing (Router-on-a-Stick)**
   [cite_start]Menggunakan sub-interface pada Router dengan enkapsulasi `dot1Q` agar antar VLAN dapat saling berkomunikasi[cite: 202, 206, 228, 231].

3. **DHCP Server**
   Konfigurasi DHCP Pool pada router untuk memberikan alokasi IP Address secara otomatis kepada *end-devices* di area publik atau area dengan mobilitas tinggi:
   * [cite_start]`DHCP_OFFICE` (VLAN 40) [cite: 242]
   * [cite_start]`DHCP_CAFE` (VLAN 60) [cite: 286]
   * [cite_start]`DHCP_LOBBY` (VLAN 80) [cite: 292]

4. **Static Routing**
   [cite_start]Penentuan jalur routing secara manual (Static Route) untuk menghubungkan ketiga Router (R1, R2, R3) sehingga seluruh subnet yang berbeda dapat saling melakukan ping[cite: 299, 300, 302, 303, 305, 306].

## 🚀 Cara Menjalankan Simulasi
1. Pastikan kamu sudah menginstal aplikasi **Cisco Packet Tracer**.
2. Clone repositori ini:
   ```bash
   git clone [https://github.com/username-kamu/mid-exam-cci-network.git](https://github.com/username-kamu/mid-exam-cci-network.git)
