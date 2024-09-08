# Windows-Server-2019
Windows Server 2019

Konfigurasi Awal Server
- Login ke Server: Masuk ke server menggunakan akun administrator.
Setel Nama Server:
- Buka Server Manager.
- Pilih Local Server di panel sebelah kiri.
- Klik Computer Name
- Pilih Change untuk mengubah nama server jika diperlukan.
- Sesuaikan value pada computer name
- klik OK
- ada kotak dialog untuk melakukan restart maka klik ok untuk menerapkan perubahan nama.

![image](https://github.com/user-attachments/assets/b3e4d34b-ff83-417b-827b-f5a4acead094)

![image](https://github.com/user-attachments/assets/1c4c93f1-d358-4ec0-9bcd-1ae815639f6e)


Menginstal Active Directory Domain Services (AD DS)
Buka Server Manager:

- Pilih Manage > Add Roles and Features.
- Centang Skip this page by default, next

![image](https://github.com/user-attachments/assets/d676b49f-150c-4710-a481-fdec265e5010)

- Ikuti wizard hingga ke bagian Server Roles.
- Centang Active Directory Domain Services
- Klik Add Features dan ikuti wizard untuk menyelesaikan pemasangan.

![image](https://github.com/user-attachments/assets/33e656a5-04f0-49bb-81fc-ac97defacfc5)


- Ikuti wizard hingga ke bagian Confirmation.
- centang Restart the destinations server automaticallt if required
- akan muncul dialog dan Klik Yes untuk konfirmasi
- Klik install

![image](https://github.com/user-attachments/assets/eb2380ea-ca5d-4f53-8276-2fb906c4cef3)


- 
Promosikan Server sebagai Domain Controller:

Setelah AD DS terpasang, buka Server Manager.
Klik pada Notification Flag (ikon segitiga kuning) dan pilih Promote this server to a domain controller.
Pilih Add a new forest jika ini adalah domain pertama yang Anda buat, dan masukkan nama domain yang diinginkan.
Ikuti wizard untuk mengonfigurasi opsi domain, DSRM password (Directory Services Restore Mode), dan DNS.
Setelah konfigurasi selesai, server akan di-restart.
