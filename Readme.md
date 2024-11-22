# PENGENALAN GIT DAN GITHUB
|Nama|Divisi|Sub-Divisi|
|----|------|----------|
|Nabila Amalia Maghfira Izani Maula| ELC | Microcontroller|

## Cara Menggunakan Git dan Github
### 1. Unduh dan pasang Git pada PC/Laptop
    https://git-scm.com/downloads
### 2. Buat Akun Github
    https://github.com/join
### 3. Mengatur Git Bash atau Terminal
    git config --global user.name "Masukan username di github"
    git config --global user.email "Masukkan email yang tersambung di github"

### 4. Membuat SSH Keys di GitHub
#### 1) Buka GitHub dan Masuk Ke Settings -> "SSH and GPG keys" -> "New SSH Key"
#### 2) Untuk Membuat Kunci, Buka Git Bash dan Masukkan Perintah Berikut:
     ssh-keygen -t ed25519 -C (masukkan email)
     (>> Kemudian tekan enter 2 kali)
#### 3) Salin SSH key yang Telah Dibuat dengan Perintah Berikut:
     clip < ~/.ssh/id_ed25519.pub
#### 4) setelah clip diatas disalin maka link SSH akan langsung  di keybord dan dimasukkan pada New SSH key di setting Github.
    
## 5. Membuat Repositori
### 1. Buka Laman Github
    https://github.com
    Lakukan Log-in dengan akun yang telah dibuat
### 2. Isikan Nama Repositori yang Diinginkan Lalu Pilih "Public" 
    Lakukan centang pada "Add a README file"
    Setelah Itu Pilih "Create Repository"
### 3. Pilih Menu "Code" Lalu Pilih "SSH" Setelah Itu Salin Link SSH
    Contoh Link : git@github.com:(namapengguna)/(namarepositori).git

## 6. Push File dari Lokal ke Github
### 1. Buat Folder dengan Nama yang Sama dengan Nama Repositori lalu Buka Folder yang telah dibuat
### 2. Buat File Baru untuk Diunggah ke Github
### 3. Klik Kanan pada Mouse Lalu Pilih "Open Git Bash here"
### 4. Lalu Masukkan Command Berikut pada Git Bash
    git init
   	git remote add origin (link SSH yang telah di salin)
   	git branch -M main
    (Untuk memastikan folder lokal sama dengan folder di github maka ketik : git pull origin (branch yang ingin didownload))
### 5. Untuk Mengunggah File pada Folder Lokal, Masukkan Command Berikut pada Git Bash
    git add .
    git commit -m "(deskripsi bebas contohnya first commit)"
    git push origin (branch yang akan ingin diunggah)

## 7. Membuat Branch Baru Menggunakan Git 
### 1. Buka Git Bash pada File yang Terhubung dengan Repositori
### 2. Masukkan Command Berikut Pada Git Bash
    git checkout -B (nama branch yang diinginkan)
### 3. Untuk Pindah Branch Dapat Memasukkan Command Berikut
    git branch -d (nama branch yang ingin dihapus)

## 8. Menghapus Branch Menggunakan Git
### 1. Lakukan Pindah Branch dengan Command Berikut
    git checkout (nama branch yang diinginkan)
### 2. Hapus Branch yang Diinginkan dengan Command Berikut
    git branch -d (nama branch yang ingin dihapus)

## 9. Menggabungkan Brench
### 1. Pindah ke branch yang ingin digabung:
    git checkout (nama branch)
### 2. Gabungkan branch lain ke branch saat ini:
    git merge nama-branch-lain

## 9. Kloning Repositori
### 1. Masuk ke Git Bash pada Folder yang diinginkan
### 2. Masukkan Command Berikut:
    git clone https://github.com/(namapengguna)/(namarepositori).git

## 10. Melihat riwayat Commit
### 1. Masuk ke Git Bash pada Folder yang diinginkan
### 2. Untuk melihat riwayat commit dalam repository:
    git log