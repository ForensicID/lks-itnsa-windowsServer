# 📝 Windows Server Configuration - LKS ITNSA

Note konfigurasi untuk modul Windows Server.

---

## 🚀 Urutan Eksekusi (Step-by-Step)

Key step by step:

1.  **Change Hostname & IP**
    * Lakukan di awal sebelum install role apapun.
2.  **AD and DNS (SERVICE1)**
    * Install Active Directory Domain Services & DNS.
    * Promote menjadi Domain Controller.
3.  **Join Domain (SERVICE2)**
    * Arahkan DNS Client SERVICE2 ke IP SERVICE1.
    * Join ke domain yang baru dibuat.
4.  **Configure AD**
    * Manajemen User, Group, dan OU.
    * *(Detail: Lihat folder `AD` dan file `GPO.txt`)*
5.  **RDS (Remote Desktop Services)**
    * Konfigurasi layanan remote desktop.
    * *(Detail: Lihat file `RDP.txt`)*
6.  **ADCS (Active Directory Certificate Services)**
    * Konfigurasi Certificate Authority (CA).
    * *(Detail: Lihat folder `CA`)*
7.  **IIS SERVICE1 (SSL)**
    * Setup Web Server (IIS) dan binding sertifikat SSL dari CA.
    * *(Detail: Lihat file `WP-IIS.txt`)*

---

## 📂 Daftar File Referensi

* `AD/` - Konfigurasi Active Directory Join & Users
* `CA/` - Konfigurasi Certificate Authority
* `DNS.txt` - Catatan setup DNS
* `GPO.txt` - Konfigurasi Group Policy Object
* `WP-IIS.txt` - Konfigurasi Web Server & WordPress
* `RDP.txt` - Konfigurasi Remote Desktop
* `SysPrep.txt` - Catatan untuk cloning/sysprep

---

> **Catatan:** Pastikan firewall dikonfigurasi dengan benar agar antar-service bisa saling berkomunikasi.
