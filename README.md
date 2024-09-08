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


- klik close

![image](https://github.com/user-attachments/assets/c7a9aaaf-09c0-4fc2-9aac-d3acd591ce7f)


Promosikan Server sebagai Domain Controller:
- Setelah AD DS terpasang, buka Server Manager.
- Klik pada Notification Flag (ikon segitiga kuning) dan pilih Promote this server to a domain controller.

![image](https://github.com/user-attachments/assets/b0d9d9e6-e206-4103-9320-3b18df16ab51)


- Pilih Add a new forest jika ini adalah domain pertama yang Anda buat,
- dan masukkan nama domain yang diinginkan, next.

![image](https://github.com/user-attachments/assets/7c84714d-25dc-4a21-a111-ed0f132cfc54)


- Ikuti wizard untuk mengonfigurasi opsi domain, isikan DSRM password (Directory Services Restore Mode), next

![image](https://github.com/user-attachments/assets/dfcbe2f7-6791-4b11-9f46-5ba39f2473ef)


- Ikuti wizard hingga ke bagian Prerequisites Check, klik Install. 

![image](https://github.com/user-attachments/assets/6d5dcb5e-3b73-4112-98d9-b722750aeefe)

- Setelah Installasi selesai akan auto restart



- 
- sd
- asd
Setelah konfigurasi selesai, server akan di-restart.
