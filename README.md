# Windows Server 2019

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

Setelah restart, server Anda akan siap digunakan sebagai **Domain Controller**.
