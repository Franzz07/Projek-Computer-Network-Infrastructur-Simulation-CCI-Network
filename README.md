# Enterprise Network Simulation with Inter-VLAN and Static Routing 🌐

Repositori ini berisi project simulasi infrastruktur jaringan berskala menengah yang dibangun menggunakan Cisco Packet Tracer. Project ini dikembangkan sebagai bagian dari kegiatan Divisi Network di Central Computer Improvement (CCI) Telkom University.


## 📝 Deskripsi Project
Project ini mensimulasikan infrastruktur jaringan perusahaan dengan membagi jaringan ke dalam beberapa divisi menggunakan arsitektur **VLAN**. Jaringan ini dikelola oleh 3 Router utama dan 5 Switch, serta mengimplementasikan **Inter-VLAN Routing**, distribusi IP otomatis via **DHCP Server**, dan **Static Routing** untuk menghubungkan router antar gedung/area.

## Fitur Utama & Konfigurasi
1. **VLAN (Virtual Local Area Network)**
   Jaringan diisolasi menjadi beberapa segmen berikut untuk keamanan dan efisiensi manajemen:
   * **VLAN 20 (HRD):** `192.168.11.0/28`
   * **VLAN 30 (Finance):** `192.168.12.0/28`
   * **VLAN 40 (Office):** `192.168.13.0/25`
   * **VLAN 50 (Logistic):** `192.168.14.0/28`
   * **VLAN 60 (Cafetaria):** `192.168.15.0/25`
   * **VLAN 70 (Developer):** `192.168.16.0/27`
   * **VLAN 80 (Lobby):** `192.168.17.0/25`
   * **VLAN 90 (Server):** `192.168.18.0/29`

2. **Inter-VLAN Routing (Router-on-a-Stick)**
   Menggunakan sub-interface pada Router dengan enkapsulasi `dot1Q` agar antar VLAN yang berbeda segmen dapat saling berkomunikasi.

3. **DHCP Server**
   Konfigurasi DHCP Pool pada router untuk memberikan alokasi IP Address secara otomatis kepada *end-devices* di area publik atau area dengan mobilitas tinggi:
   * `DHCP_OFFICE` (VLAN 40)
   * `DHCP_CAFE` (VLAN 60)
   * `DHCP_LOBBY` (VLAN 80)

4. **Static Routing**
   Penentuan jalur routing secara manual (Static Route) untuk menghubungkan ketiga Router (R1, R2, R3) sehingga seluruh subnet yang berada di bawah router yang berbeda dapat saling terhubung.
