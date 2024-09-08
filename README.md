# Windows Server 2019

## Daftar Isi
1. [Konfigurasi Awal Server](#konfigurasi-awal-server)
   - [1. Login ke Server](#1-login-ke-server)
   - [2. Setel Nama Server](#2-setel-nama-server)
2. [Menginstal Active Directory Domain Services (AD DS)](#menginstal-active-directory-domain-services-ad-ds)
   - [1. Buka Server Manager](#1-buka-server-manager)
   - [2. Pilih Peran (Server Roles)](#2-pilih-peran-server-roles)
   - [3. Konfirmasi Instalasi](#3-konfirmasi-instalasi)
   - [4. Selesai Instalasi](#4-selesai-instalasi)
3. [Promosikan Server Sebagai Domain Controller](#promosikan-server-sebagai-domain-controller)
   - [1. Buka Server Manager](#1-buka-server-manager-1)
   - [2. Tambahkan Forest Baru](#2-tambahkan-forest-baru)
   - [3. Konfigurasi Domain](#3-konfigurasi-domain)
   - [4. Selesaikan Instalasi](#4-selesaikan-instalasi)
   - [5. Restart Server](#5-restart-server)
4. [Menguji dan Berinteraksi dengan Server LDAP Secara Manual](#menguji-dan-berinteraksi-dengan-server-ldap-secara-manual)
   - [1. Buka ldp.exe](#1-buka-ldpexe)
   - [2. Koneksi ke Server LDAP](#2-koneksi-ke-server-ldap)

---

## Konfigurasi Awal Server

### 1. Login ke Server
- Masuk ke server menggunakan akun **administrator**.

### 2. Setel Nama Server
- Buka **Server Manager**.
- Pilih **Local Server** di panel sebelah kiri.
- Klik **Computer Name**.
- Pilih **Change** untuk mengubah nama server jika diperlukan.
- Sesuaikan nama pada **Computer Name**.
- Klik **OK**.
- Muncul kotak dialog untuk melakukan restart, klik **OK** untuk menerapkan perubahan nama.

![Server Manager](https://github.com/user-attachments/assets/b3e4d34b-ff83-417b-827b-f5a4acead094)

![Restart Computer](https://github.com/user-attachments/assets/1c4c93f1-d358-4ec0-9bcd-1ae815639f6e)

---

## Menginstal Active Directory Domain Services (AD DS)

### 1. Buka Server Manager
- Pilih **Manage** > **Add Roles and Features**.
- Centang **Skip this page by default**, lalu klik **Next**.

![Add Roles and Features](https://github.com/user-attachments/assets/d676b49f-150c-4710-a481-fdec265e5010)

### 2. Pilih Peran (Server Roles)
- Ikuti wizard hingga ke bagian **Server Roles**.
- Centang **Active Directory Domain Services**.
- Klik **Add Features** dan ikuti wizard untuk menyelesaikan pemasangan.

![Active Directory Domain Services](https://github.com/user-attachments/assets/33e656a5-04f0-49bb-81fc-ac97defacfc5)

### 3. Konfirmasi Instalasi
- Ikuti wizard hingga ke bagian **Confirmation**.
- Centang **Restart the destination server automatically if required**.
- Akan muncul dialog konfirmasi, klik **Yes**.
- Klik **Install** untuk memulai proses instalasi.

![Confirmation](https://github.com/user-attachments/assets/eb2380ea-ca5d-4f53-8276-2fb906c4cef3)

### 4. Selesai Instalasi
- Setelah instalasi selesai, klik **Close**.

![Close Wizard](https://github.com/user-attachments/assets/c7a9aaaf-09c0-4fc2-9aac-d3acd591ce7f)

---

## Promosikan Server Sebagai Domain Controller

### 1. Buka Server Manager
- Setelah AD DS terpasang, buka **Server Manager**.
- Klik pada **Notification Flag** (ikon segitiga kuning) dan pilih **Promote this server to a domain controller**.

![Promote to Domain Controller](https://github.com/user-attachments/assets/b0d9d9e6-e206-4103-9320-3b18df16ab51)

### 2. Tambahkan Forest Baru
- Pilih **Add a new forest** jika ini adalah domain pertama yang Anda buat.
- Masukkan nama domain yang diinginkan, kemudian klik **Next**.

![Add a New Forest](https://github.com/user-attachments/assets/7c84714d-25dc-4a21-a111-ed0f132cfc54)

### 3. Konfigurasi Domain
- Ikuti wizard untuk mengonfigurasi opsi domain.
- Isikan password untuk **DSRM (Directory Services Restore Mode)**, lalu klik **Next**.

![Configure Domain](https://github.com/user-attachments/assets/dfcbe2f7-6791-4b11-9f46-5ba39f2473ef)

### 4. Selesaikan Instalasi
- Ikuti wizard hingga ke bagian **Prerequisites Check**, lalu klik **Install**.

![Prerequisites Check](https://github.com/user-attachments/assets/6d5dcb5e-3b73-4112-98d9-b722750aeefe)

### 5. Restart Server
- Setelah instalasi selesai, server akan otomatis restart.

---

## Menguji dan Berinteraksi dengan Server LDAP Secara Manual

### 1. Buka ldp.exe
- Buka Command Prompt: Tekan `Win + R`, ketik `cmd`, dan tekan `Enter`.
- Jalankan ldp.exe: Ketik `ldp` dan tekan `Enter`. Ini akan membuka jendela ldp.exe.

### 2. Koneksi ke Server LDAP
- Koneksi: Pilih **Connection** di menu, kemudian pilih **Connect**.
  - Masukkan Detail Server:
    - **Server**: Masukkan nama host atau alamat IP server LDAP (misalnya, `172.10.10.10` atau `SERVERWIN-001.addsSecLab.id`).
    - **Port**: Masukkan port yang digunakan oleh server LDAP. Port default untuk LDAP adalah `389`. Jika menggunakan LDAPS (LDAP Secure), port defaultnya adalah `636`.
  - Klik **OK**: Klik tombol **OK** untuk menghubungkan ke server LDAP. Jika koneksi berhasil, Anda akan melihat pesan status di jendela output.


cara mengaktifkan schema Active Directory 
buka cmd ketikan: regsvr32 schmmgmt.dll

![image](https://github.com/user-attachments/assets/17c41d72-2f6f-45e8-a70a-24fa8f8327a3)

menambahkan attribute pada active directory
buka cmd ketikan mmc
pilih file > klik Add/Remove snap-in
akan muncul pop up 
pilih Active Directory Schema > add > OK
berikut adalah before after setelah penambahan attribute employeeID
pastikan melakukan restart services AD setelah melakukan perubahan attribute

![image](https://github.com/user-attachments/assets/9b072b37-4160-4f2f-9ff7-997d9e1ffa10)







